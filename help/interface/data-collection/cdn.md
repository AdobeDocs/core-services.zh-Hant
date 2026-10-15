---
title: 透過CDN路由資料收集
description: 瞭解如何設定內容傳遞網路(CDN)，以轉送資料收集請求至Adobe而不會影響資料品質。
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '1421'
ht-degree: 0%
---
# 透過CDN路由資料收集

有些組織會透過其內容傳遞網路(CDN)路由資料收集請求，而非直接傳送至Adobe。 常見原因包括Web應用程式防火牆(WAF)保護、要求所有網站流量都必須通過CDN的公司政策，以及檢查傳送至Adobe的流量的功能。 CDN會接收貴組織擁有的主機名稱要求，然後轉送至Adobe資料收集主機名稱（稱為來源）。

>[!IMPORTANT]
>
>Adobe無法檢閱或驗證您的CDN設定。 貴組織和CDN提供者需負責正確設定CDN。 如需設定CDN的協助，請聯絡您的CDN提供者。 未正確設定的CDN可能會導致資料遺失。

## 選擇來源型別 {#origin-type}

| | 第三方來源（建議） | 第一方來源 |
| --- | --- | --- |
| **原始主機名稱** | `data.adobedc.net`的租使用者ID子網域，例如`example.data.adobedc.net` | 您的第一方主機名稱，例如`data.example.com` |
| Adobe伺服器上的&#x200B;**憑證** | Adobe的憑證(`*.data.adobedc.net`) | [客戶管理的憑證](customer-managed-cert.md) |
| **憑證續約** | 不需要任何專案 | 您的組織會更新憑證，並在每次到期前提供憑證給Adobe |
| **區域鎖定的[RDC](rdc.md)** | 不支援 | 支援 |
| **何時使用** | 所有CDN實作，除非您的組織需要第一方來源 | 您的安全性原則需要直接控制來源憑證，或是您的組織需要區域鎖定的RDC型別 |

>[!NOTE]
>
>[Adobe管理的憑證方案](adobe-managed-cert.md)不支援CDN實作。 Adobe無法驗證網域擁有權或續約指向您CDN之主機名稱的憑證。 使用第三方來源或具有[客戶管理的憑證](customer-managed-cert.md)的第一方來源。

## 所有CDN實作的需求 {#requirements}

Adobe資料收集程式庫（例如AppMeasurement和Web SDK）包含Adobe在每個請求中所需的一切。 設定您的CDN以轉送這些要求至Adobe，而不變更它們。

>[!IMPORTANT]
>
>切勿變更端點或決定資料去向的任何專案，包括報表套裝ID (AppMeasurement)或資料串流ID (Web SDK)。 變更這些值會導致資料遺失。

您的CDN設定必須：

* 轉送要求方法、URL路徑、查詢字串和內文，不做變更。
* 保留`Host`標頭不變。
* Adobe Cookie設定的網域維持不變。
* 保留本指南的[Cookie區段](cookies/overview.md)中列出的所有Cookie。
* 新增包含訪客IP位址的`X-Forwarded-For`標頭。 Adobe會使用此標題來定位地理位置。 若不使用地理位置資訊，地理位置資料會反映CDN伺服器的位置，而非訪客。
* 將Adobe的回應傳回瀏覽器，而不做變更。

您的CDN設定可以：

* 移除Adobe未使用的Cookie，例如網站上其他系統的Cookie。 不相關的Cookie會為每一個請求增加額外負荷。
* 使用WAF、機器人篩選或個人資料移除服務，只要這些服務不會變更上述任何專案。 將服務套用至生產流量之前，請先使用開發報表套裝或資料流測試這些服務。 過於激進的篩選可能會移除足夠的資料，導致報表無法使用。

您的CDN設定不得：

* 快取資料收集要求或回應。 每個請求都必須送達Adobe。
* 指向不存在的原始主機名稱。
* 接受過期的憑證，或從來源釘選特定憑證。 Adobe不支援提供過期的憑證，並可隨時移除這些憑證。

## 使用第三方來源設定CDN {#third-party-origin}

第三方來源使用Adobe自己的憑證，因此您的組織不需要在Adobe伺服器上維護憑證。

1. 尋找您組織的租使用者ID。 請參閱[尋找您的租使用者ID](collection-domain.md#tenant-id)。
1. 在您的CDN設定中，將原始主機名稱設定為`data.adobedc.net`的租使用者ID子網域。 例如 `example.data.adobedc.net`。
1. 啟用來源的伺服器名稱指示(SNI)。 將SNI主機名稱設定為原始主機名稱（例如`example.data.adobedc.net`），而非您網站的主機名稱。
1. 設定您的CDN以符合上述所有CDN實作](#requirements)的[需求。
1. 如果您的實作傳送資料以進行變更的主機名稱，[請更新您的實作](collection-domain.md#update-implementation)。 如果您保留相同的主機名稱，實作上就不需要變更。

>[!WARNING]
>
>請勿將來源設定為Adobe提供做為CNAME目標的主機名稱，例如`hiodsibxvip01.data.adobedc.net`。 該主機名稱會繫結至您的第一方憑證，且在移除憑證時可能會停止運作。

協力廠商來源一律使用預設的[RDC型別](rdc.md)，因此資料可在任何Adobe資料收集位置收集。

## 使用第一方來源設定CDN {#first-party-origin}

只有在貴組織需要第一方來源時，才使用它。 常見原因包括：

* 您的安全性原則需要直接控制原始憑證。 例如，您的組織必須能夠透過自己的憑證授權單位撤銷憑證。
* 您的組織需要區域鎖定的[RDC型別](rdc.md)。

1. 請連絡Adobe客戶服務，為您的第一方主機名稱（例如`data.example.com`）設定[客戶管理的憑證](customer-managed-cert.md)。 如果您的組織需要地區鎖定RDC型別，請在請求中指定。
1. 在您的CDN設定中，將原始主機名稱設定為您的第一方主機名稱。
1. 啟用來源的伺服器名稱指示(SNI)。 將SNI主機名稱設定為您的第一方主機名稱，並設定您的CDN以預期您的第一方憑證來自來源。
1. 設定您的CDN以符合上述所有CDN實作](#requirements)的[需求。
1. 如果您的實作傳送資料以進行變更的主機名稱，[請更新您的實作](collection-domain.md#update-implementation)。 如果您保留相同的主機名稱，實作上就不需要變更。

>[!IMPORTANT]
>
>貴組織有責任續約客戶管理的憑證，並在憑證過期前提供給Adobe客戶服務。 如果Adobe伺服器上的憑證過期，您的CDN可以在不通知您的情況下拒絕連線並捨棄資料。 請參閱[更新您的憑證](customer-managed-cert.md#renewals)。

## 將現有的第一方實作移至CDN {#migrate}

如果您的組織目前使用Adobe託管的憑證將資料直接傳送至第一方主機名稱，請使用下列步驟移至CDN：

1. 識別所有將Adobe產品中的資料傳送至第一方主機名稱的每個實作。 其他產品（例如Adobe Target或Adobe Journey Optimizer）可能會使用相同的主機名稱，而單一憑證可涵蓋許多主機名稱。
1. 選擇[原始型別](#origin-type)。 如果您選擇第一方來源，請聯絡Adobe客戶服務，在憑證過期之前將憑證轉換為[客戶管理的憑證](customer-managed-cert.md)。
1. 設定您的CDN。 請保留現有的主機名稱，這樣您就不需要更新實作。
1. 在憑證過期之前，請將主機名稱指向您的CDN，並切換所有實施以使用它。
1. [檢查您的資料](#check)。
1. 如果您選擇第三方來源，請聯絡Adobe客戶服務，將您的第一方憑證標示為移除。

一旦您的主機名稱指向您的CDN，Adobe就無法更新您的第一方憑證。 如果任何實作在憑證過期時仍舊仰賴憑證，則該實作的資料會遺失。 聯絡Adobe客戶服務可讓您的組織控制何時移除憑證。

## 檢查您的資料 {#check}

Adobe無法驗證您的CDN設定。 在您透過CDN路由資料收集後，請比較變更前後的資料：

* 資料持續以一般數量抵達預期的報表套裝、資料串流或資料集。
* 地理位置報表會顯示訪客的位置，而非CDN伺服器所在的小城市。
* 不重複訪客計數不會意外增加。
* 在瀏覽器的開發人員工具中，成功對主機名稱提出資料收集請求，且Adobe Cookie設定在與之前相同的網域上。

## 常見設定錯誤

已知下列問題會導致資料品質問題或資料遺失。 此清單並非詳盡無遺。

| 症狀 | 可能的原因 |
| --- | --- |
| 資料停止抵達報表套裝或資料流 | CDN會變更請求URL，或原始主機名稱不存在 |
| 憑證過期後資料停止送達 | CDN需要來自來源的第一方憑證，而該憑證已過期 |
| 地理位置資料只顯示幾個城市 | CDN未新增`X-Forwarded-For`標頭 |
| 不重複訪客計數意外增加 | CDN會移除Adobe Cookie、變更`Host`標頭或變更Cookie網域 |
| 報告遺失大量資料 | 個人資料移除或WAF規則會移除太多每個請求 |

## 常見問題

+++此頁面是否適用於Adobe Analytics以外的產品？

有。 本頁適用於使用Adobe資料收集的所有Adobe產品，包括Customer Journey Analytics、Adobe Experience Platform、Adobe Target和Adobe Journey Optimizer。

+++

+++Adobe可以拒絕未透過我的CDN傳送的資料嗎？

沒有。 Adobe目前沒有提供方式限制將資料收集限制在來自CDN的請求中。

+++

+++Adobe可以提供或驗證我的CDN的設定嗎？

沒有。 CDN設定選項因提供者而異，而且會隨著時間而改變。 請連絡您的CDN提供者，以取得設定CDN的協助，並參閱[檢查您的資料](#check)，以取得識別設定問題的方式。

+++
