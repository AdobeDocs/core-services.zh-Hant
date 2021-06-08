---
description: Experience Cloud 的新功能和更新的概述。
keywords: 核心服務
seo-description: Experience Cloud 的新功能和更新的概述。
seo-title: Experience Cloud 的新功能
solution: Experience Cloud
title: 'Experience Cloud 的新功能 '
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
source-git-commit: ebefd433e96da422674e7ee71c8988d4011fed11
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 89%

---


# Experience Cloud 的新功能

Experience Cloud 的新功能和更新的概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

2018年8月的修正和改良。

* 改善 Creative Cloud 和 Experience Cloud 間的資產註解同步。(CORE - 15971)

* 新增功能標記以控制 Experience Cloud 與 Creative Cloud 之間的資產同步。(CORE - 15938)

* 改善「受眾」區段的建立方式，包括更優異的搜尋和清單體驗。(CORE-5833、CORE-14278)
* 修正封鎖從 Experience Cloud 到 Creative Cloud 資料夾共用作業的高優先順序問題。(CORE - 16677)


## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

2018年7月的修正和改良。

* 部署後端功能，可控制 Marketing Cloud 對 AEM 和 Marketing Cloud 對 Creative Cloud 之間的資產共用。(CORE - 14386)

* 修正某些環境中無法提供新租戶的問題。(CORE - 15509)

* 修正透過 [!DNL experiencecloud.adobe.com] 而非 [!DNL experiencecloud.adobe.com] (安全) 存取 [!DNL http] 時將使用者重新導向至 [!DNL https] 的問題。(CORE - 15587)

* 修正某些新租戶的通知遭封鎖的問題。(CORE - 15240)


## 2018年6月14日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018年6月的修正和改良。

* 為管理員啟用 GDPR 存取的連結。(CORE - 11731)

* 更新測試版意見反應，限制可附加至意見反應的檔案類型。(CORE - 10474)

* 修正從受眾程式庫中刪除受眾的問題。(CORE - 12792)

* 修正使用 Federated ID 存取 Workspace 連結時導致空白畫面的問題。(CORE - 11620)


## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 介面中的新功能和修正。

| 功能 | 說明 |
|--- |--- |
| 全新管理登陸頁面 | 登入 Experience Cloud 並導覽至「管理」頁面時，可使用全新的直覺式介面，幫助您快速存取 Experience Cloud 解決方案和核心服務。 |

**修正**

* 修正因 Scene7 更新而導致影像上傳失敗的問題。(CORE - 12746)

* 依照 PCI 的規定更新 TLS 1.0 通訊協定的支援，消除了安全弱點。(CORE - 7695)


## 2017 年 10 月 26 日 {#section_11195859B4094177A939C0561428B525}

**已知問題**

通知電子郵件摘要中遺失許多有關排程維護/產品更新的維護通知。我們正致力確保所有維護通知都包含在電子郵件摘要中。

## 2017 年 8 月 8 日 {#section_2313A875454044F490B418506DD24593}

| 功能 | 說明 |
|--- |--- |
| 通知 - 粒度設定 | 您可以啟用產品和解決方案事件與活動的通知，包括[「客戶屬性」](attributes.md)上傳活動的相關通知。        |
| 通知 - 維護通知 | 在「通知」設定中，您可以啟用產品和解決方案的維護通知。 |
| 適用於 Experience Cloud 解決方案的 Admin Console | 新的 Experience Cloud 客戶可以開始使用 Admin Console，這是管理整個組織中 Adobe 權限的集中位置。<br>移轉至 Admin Console 來管理使用者的程序會按階段進行。Adobe在需要遷移時與您（系統管理員）聯繫。<br>Analytics 管理員請參閱 [Analytics 移轉](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=en)。 |

## 2017 年 5 月 22 日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 說明 |
|--- |--- |
| 大量報表套裝對應 | 在「管理 > 報表套裝對應」中，您現已可選取多個報表套裝，然後將它們對應至某個組織(之前您必須個別對應這些報表套裝。)<br>[將報表套裝對應至單一組織有助於在 Experience Cloud 中啟用跨解決方案功能及服務。](core-services.md) |
| Experience Cloud Audiences 的更新 | **套用報表套裝**<br>&#x200B;您現已可將報表套裝套用至所有[受眾規則](t-audience-create.md)。(之前您必須在每個規則定義中指定一個報表套裝。)<br>**Prop 和變數**<br>&#x200B;您現已可在即時受眾中包含 Analytics Prop 和預設變數 (以及原有的 eVar 和事件)。 |

## 2016年11月8日 — 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 說明 |
|--- |--- |
| 設定檔與密碼更新 | 使用者無法再到「編輯個人資料 > 個人資料和密碼」編輯「個人詳細資料」底下的 IMS 使用者個人資訊。系統會改將使用者重新導向至 `accounts.adobe.com`。此更新適用於所有身分類型(Adobe ID、Enterprise及Federated)。 |

**修正**

* 修正造成 Creative Cloud 和 Experience Cloud 之間資料夾共用發生錯誤的技術密碼問題。(MAC-31067、MAC-32014)
* 修正 10 月發行版本後 Assets 核心服務中某些檔案類型 (包括 PDF) 的上傳問題。(MAC-32517)

