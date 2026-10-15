---
title: 選擇資料收集網域
description: 瞭解可用於將資料傳送至Adobe的網域，以及如何尋找貴組織的租使用者ID。
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
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: e1185eeafc809b036b10955880536db7a576ca0b
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 3%
---
# 選擇資料收集網域

您的資料收集網域是實施作業傳送資料的目標主機名稱。 所有使用Adobe資料收集的Adobe CX Enterprise產品（例如Adobe Analytics、Customer Journey Analytics、Adobe Experience Platform、Adobe Target和Adobe Journey Optimizer）都仰賴此網域。

## 資料收集網域選項

| 選項 | 實作網域 | 區域鎖定的[RDC](rdc.md) | 憑證維護 |
| --- | --- | --- | --- |
| [協力廠商網域](#third-party) | `example.data.adobedc.net` | 不支援 | 無 |
| 第一方網域具有[Adobe管理的憑證](adobe-managed-cert.md) | `data.example.com` | 支援 | 無（Adobe會自動更新憑證） |
| 具有[客戶管理憑證](customer-managed-cert.md)的第一方網域 | `data.example.com` | 支援 | 您的組織會更新憑證並將其提供給Adobe |
| [具有協力廠商來源的內容傳遞網路(CDN)](cdn.md#third-party-origin) | `data.example.com` | 不支援 | 無 |
| [具有第一方來源的CDN](cdn.md#first-party-origin) | `data.example.com` | 支援 | 您的組織會更新憑證並將其提供給Adobe |

## 協力廠商資料收集網域 {#third-party}

如果您未使用第一方網域，請將資料傳送至`data.adobedc.net`的子網域。 Adobe建議使用您組織的[租使用者ID](#tenant-id)作為子網域。 例如 `example.data.adobedc.net`。 當您[透過CDN](cdn.md)路由資料收集時，此網域也是建議的原始網域。

* 協力廠商網域一律使用預設的[RDC型別](rdc.md#third-party-data-collection)。
* 請勿使用比`example.data.adobedc.net`更深入的子網域。 例如，`custom.example.data.adobedc.net`不是有效的資料收集網域。
* 較舊的實作可能使用`sc.omtrdc.net`或`2o7.net`等網域。 雖然這些網域仍然有效，但Adobe建議儘可能使用`data.adobedc.net`。

### 尋找您的租使用者ID {#tenant-id}

1. 使用您的Adobe ID認證登入[Adobe CX Enterprise](https://experience.adobe.com)。
1. 在CX Enterprise介面中的任何位置，按下`[Cmd]` + `[I]` (macOS)或`[Ctrl]` + `[I]` (Windows)。
1. 出現&#x200B;**[!UICONTROL 使用者資料偵錯工具]**。 選取&#x200B;**[!UICONTROL 指派的組織]**&#x200B;索引標籤。
1. 展開所需的IMS組織。
1. 找到&#x200B;**[!UICONTROL 租使用者]**&#x200B;欄位。 此值是您的租使用者ID。

您的租使用者ID與您的IMS組織ID不同，其結尾為`@AdobeOrg`。 每個IMS組織擁有一個租使用者ID。 如果您的公司使用多個IMS組織，則每個組織都有自己的租使用者ID。

## 更新您的實作 {#update-implementation}

當您變更資料收集網域時，請更新每個將資料傳送至Adobe的實作：

* **Web SDK標籤擴充功能**：設定擴充功能時更新[[!UICONTROL Edge網域]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/general)欄位。
* **網頁SDK (alloy)**：更新`configure`命令中的[`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/edgedomain)屬性。
* **Adobe Analytics擴充功能**：設定擴充功能時更新[[!UICONTROL SSL追蹤伺服器]](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/analytics/overview)欄位。 請確定您已安裝[訪客ID服務標籤擴充功能](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/id-service/overview)。 如需詳細資訊，請參閱[使用Analytics標籤延伸識別訪客](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/analytics-extension)。
* **AppMeasurement**：更新[`trackingServerSecure`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserversecure)設定變數。 確定您也使用`VisitorAPI.js`實作[訪客ID服務](https://experienceleague.adobe.com/zh-hant/docs/id-service/using/home)。 如需詳細資訊，請參閱[使用AppMeasurement的訪客身分識別](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/appmeasurement)。
* **其他實作**：更新將資料傳送至Adobe的任何其他實作中的資料收集網域，例如行動應用程式或伺服器端實作。

如果您的實作不使用訪客ID服務或網頁SDK，變更您的資料收集網域會變更訪客Cookie的網域，而回頭的訪客可計為新訪客。

如果您的網站使用多種實作方法，且您無法同時更新所有方法，請考慮設定寬限期。 請參閱[訪客ID服務移轉考量事項](https://experienceleague.adobe.com/en/docs/analytics/implementation/id/migration)，以取得如何防止訪客在您的網站上被計為新訪客的其他步驟。
