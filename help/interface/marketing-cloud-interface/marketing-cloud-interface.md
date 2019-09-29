---
description: Experience Cloud 的新功能和更新的概述。
keywords: 核心服務
seo-description: Experience Cloud 的新功能和更新的概述。
seo-title: Experience Cloud 的新功能
solution: Experience Cloud
title: Experience Cloud 的新功能
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# Experience Cloud 的新功能

Experience Cloud 的新功能和更新的概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

2018 年 8 月的修正和改良。

* 改善 Creative Cloud 和 Experience Cloud 上的資產註解同步功能。(CORE - 15971)

* 新增功能標記以控制 Experience Cloud 與 Creative Cloud 之間的資產同步。(CORE - 15938)

* 改善對象區段的建立，包含更完善的搜尋和列表體驗。(CORE-5833、CORE-14278)
* 修正封鎖從 MAC 到 Creative Cloud 資料夾共用作業的高優先順序問題。(CORE - 16677)


## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

2018 年 7 月的修正和改良。

* 部署後端功能以控制 Marketing Cloud 至 AEM 與 Marketing Cloud 至 Creative Cloud 之間的資產共用。(CORE - 14386)

* 修正部分環境阻擋佈建新租用戶的問題。(CORE - 15509)

* 修正透過 [!DNL marketing.adobe.com] 而非 [!DNL experiencecloud.adobe.com] (安全) 存取 [!DNL http] 時將使用者重新導向至 [!DNL https] 的問題。(CORE - 15587)

* 修正部分新租用戶通知遭封鎖的問題。(CORE - 15240)


## 2018 年 6 月 14 日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018 年 6 月的修正和改良。

* 為管理員啟用 GDPR 存取權的連結。(CORE - 11731)

* 更新 Beta 回饋功能，以限制可附加至回饋的檔案類型。(CORE - 10474)

* 修正從受眾程式庫刪除受眾時的問題。(CORE - 12792)

* 修正使用 Federated ID 存取 Workspace 連結時導致空白畫面的問題。(CORE - 11620)

## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 介面中的新功能和修正。

| 功能 | 說明 |
|--- |--- |
| 全新的管理登陸頁面 | 當您登入 Experience Cloud 並瀏覽至管理頁面時，全新的直覺式介面可以幫您快速的存取自己的 Experience Cloud 解決方案與核心服務。 |
**修正**

* 已修正影像上傳因 Scene7 更新而失敗的問題。(CORE - 12746)

* 已遵照 PCI 授權，更新為停止支援 TLS 1.0 通訊協定，以消除安全性漏洞。(CORE - 7695)


## 2017 年 10 月 26 日 {#section_11195859B4094177A939C0561428B525}

**已知問題**

許多與排程維護作業/產品更新相關的維護通知並未列在電子郵件通知摘要中。我們正在處理這項問題，以確保電子郵件摘要中包含所有維護通知。

## 2017 年 8 月 8 日 {#section_2313A875454044F490B418506DD24593}

| 功能 | 說明 |
|--- |--- |
| 通知 - 精細設定 | 您可以啟用產品和解決方案事件與活動的通知，包括[「客戶屬性」](../attributes/attributes.md)上傳活動的相關通知。        |
| 通知 – 維護通知 | 在「通知」設定中，您可以啟用產品和解決方案的維護通知。 |
| Experience Cloud 解決方案的 Admin Console | Experience Cloud 新客戶可開始使用 Admin Console，Admin Console 可供您集中管理全組織的 Adobe 權益。<br>移轉至 Admin Console 來管理使用者的程序會按階段進行。Adobe 會在需要進行移轉時與您 (系統管理員) 聯絡。<br>Analytics 管理員請參閱 [Analytics 移轉](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)。 |

## 2017 年 5 月 22 日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 說明 |
|--- |--- |
| 大量報表套裝對應 | 在「管理 &gt; 報表套裝對應」中，您現已可選取多個報表套裝，然後將它們對應至某個組織(之前您必須個別對應這些報表套裝。)<br>[將報表套裝對應至單一組織有助於在 Experience Cloud 中啟用跨解決方案功能及服務。](../core-services/core-services.md) |
| Experience Cloud 對象的更新 | **套用報表套裝**<br>您現已可將報表套裝套用至所有[受眾規則](../audience-library/t-audience-create.md)。(之前您必須在每個規則定義中指定一個報表套裝。)<br>**Prop 和變數**<br>您現已可在即時受眾中包含 Analytics Prop 和預設變數 (以及原有的 eVar 和事件)。 |

## 2016 年 11 月 8 日 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 說明 |
|--- |--- |
| 個人資料和密碼更新 | 使用者無法再到「編輯個人資料 &gt; 個人資料和密碼」編輯「個人詳細資料」底下的 IMS 使用者個人資訊。系統會改將使用者重新導向至 `accounts.adobe.com`。這適用於所有身分類型 (Adobe ID、Enterprise 及 Federated)。        |

**修正**

* 修正造成 Creative Cloud 和 Experience Cloud 資料夾共用錯誤的技術密碼問題。(MAC-31067、MAC-32014)
* 修正在 10 月發行資產核心服務後發現的特定檔案類型 (包括 PDF) 上傳問題。(MAC-32517)

