---
description: Experience Cloud 的新功能和更新的概述。
keywords: core services
seo-description: Experience Cloud 的新功能和更新的概述。
seo-title: Experience Cloud 的新功能
solution: Experience Cloud
title: Experience Cloud 的新功能
uuid: bc1b1542-1a37-4da1-bcfd-fc86af881642
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# Experience Cloud 的新功能

Experience Cloud 的新功能和更新的概述。

## 2018 年 8 月 {#section_7388CDAB723B49809AABEFEE85CF6378}

2018 年 8 月的修正和改良。

* 在Creative Cloud和Experience Cloud之間同步資產注釋，做了改進。 (CORE - 15971)

* 新增功能標記以控制 Experience Cloud 與 Creative Cloud 之間的資產同步。(CORE - 15938)

* 已改善「對象」區段的建立，包括更佳的搜尋和清單體驗。 (CORE-5833、CORE-14278)
* 修正封鎖從 MAC 到 Creative Cloud 資料夾共用作業的高優先順序問題。(CORE - 16677)


## 2018 年 7 月 19 日 {#section_EBB549EBABB7480884A180237ADCCD02}

2018 年 7 月的修正和改良。

* 部署後端功能，以控制Marketing Cloud對AEM和Marketing Cloud對Creative Cloud之間的資產共用。 (CORE - 14386)

* 修正某些環境中無法提供新租戶的問題。 (CORE - 15509)

* 修正透過 [!DNL experiencecloud.adobe.com] 而非 [!DNL experiencecloud.adobe.com] (安全) 存取 [!DNL http] 時將使用者重新導向至 [!DNL https] 的問題。(CORE - 15587)

* 已修正某些新租戶的通知被封鎖的問題。 (CORE - 15240)


## 2018 年 6 月 14 日 {#section_7ABC327992CB46B0B8E4A631B8B68899}

2018年6月的修正與改進。

* 為管理員啟用GDPR存取的連結。 (CORE - 11731)

* 更新測試回饋功能，限制可附加至回饋的檔案類型。 (CORE - 10474)

* 修正從「對象庫」刪除對象的問題。 (CORE - 12792)

* 修正使用Federated ID存取「工作區」連結時產生空白畫面的問題。 (CORE - 11620)


## 2018 年 5 月 10 日 {#section_498AF78DA17C4720AA0F32B51493E550}

[!DNL Adobe Experience Cloud] 介面中的新功能和修正。

| 功能 | 說明 |
|--- |--- |
| 新管理登陸頁面 | 當您登入Experience Cloud並導覽至「管理」頁面時，會提供全新的直覺式介面，幫助您快速存取Experience Cloud解決方案和核心服務。 |

**修正**

* 修正因Scene7更新而導致影像上傳失敗的問題。 (CORE - 12746)

* 已更新TLS 1.0通訊協定的支援，並依照PCI的規定，以消除安全性弱點。 (CORE - 7695)


## 2017 年 10 月 26 日 {#section_11195859B4094177A939C0561428B525}

**已知問題**

通知電子郵件摘要中遺失許多有關排程維護／產品更新的維護通知。 我們正致力於確保所有維護通知都包含在電子郵件摘要中。

## August 8, 2017 {#section_2313A875454044F490B418506DD24593}

| 功能 | 說明 |
|--- |--- |
| 通知——精細設定 | 您可以啟用產品和解決方案事件與活動的通知，包括[「客戶屬性」](../attributes/attributes.md)上傳活動的相關通知。        |
| 通知——維護通知 | 在「通知」設定中，您可以啟用產品和解決方案的維護通知。 |
| Experience Cloud解決方案的Admin Console | 新的Experience Cloud客戶可以開始使用Admin Console，這是管理整個組織中Adobe權益的集中位置。<br>移轉至 Admin Console 來管理使用者的程序會按階段進行。Adobe 會在需要進行移轉時與您 (系統管理員) 聯絡。<br>Analytics管理員，請參閱 [Analytics移轉](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)。 |

## 2017 年 5 月 22 日 {#section_242FE649FA1B4BFA88EC6E353D175ACC}

| 功能 | 說明 |
|--- |--- |
| 大量報表套裝對應 | 在「管理 > 報表套裝對應」中，您現已可選取多個報表套裝，然後將它們對應至某個組織(之前您必須個別對應這些報表套裝。)<br>[將報表套裝對應至單一組織有助於在 Experience Cloud 中啟用跨解決方案功能及服務。](../core-services/core-services.md) |
| Experience Cloud 對象的更新 | **套用報表套裝&#x200B;**<br>您現已可將報表套裝套用至所有[受眾規則](../audience-library/t-audience-create.md)。(之前您必須在每個規則定義中指定一個報表套裝。)<br>**Prop 和變數**<br>您現已可在即時受眾中包含 Analytics Prop 和預設變數 (以及原有的 eVar 和事件)。 |

## 2016 年 11 月 8 日 - 16.11.1 {#section_7065A9BCCDF544C2BB37E9A7D661EA6A}

| 功能 | 說明 |
|--- |--- |
| 更新為設定檔與密碼 | 使用者無法再到「編輯個人資料 > 個人資料和密碼」編輯「個人詳細資料」底下的 IMS 使用者個人資訊。系統會改將使用者重新導向至 `accounts.adobe.com`。這適用於所有身分類型 (Adobe ID、Enterprise 及 Federated)。        |

**修正**

* 修正Creative Cloud和Experience Cloud之間資料夾共用錯誤的技術密碼問題。 (MAC-31067、MAC-32014)
* 修正在「資產核心服務」中10月發行後，上傳某些檔案類型（包括PDF）的問題。 (MAC-32517)

