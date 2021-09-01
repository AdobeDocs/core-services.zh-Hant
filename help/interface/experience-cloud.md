---
description: 了解關於 Experience Cloud 中央介面元件。此說明包含 Admin Console 中的使用者和產品管理、啟用 Experience Cloud 服務的應用程式，以及了取得關於對象庫、客戶屬性、Experience Cloud Assets 等說明。
solution: Experience Cloud
title: Experience Cloud 介面說明和文件
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 4534f764ea821576c3ac5cd1959d387a3689e837
workflow-type: tm+mt
source-wordcount: '1303'
ht-degree: 63%

---

# Experience Cloud 中央介面元件指南

[Experience Cloud](https://experience.adobe.com) 為 Adobe 的整合式數位行銷應用程式產品和服務系列。若要直觀式介面，您可快速存取您的雲端應用程式、產品特性和服務。

![Experience Cloud](assets/landing.png)

在 Experience Cloud 標題中，您可以：

* 存取您的應用程式和服務
* 搜尋產品文件、教學課程和社群貼文
* 使用全域搜尋功能在全域搜尋商業物件 (僅適用於 Experience Platform 使用者)。
* 管理您的帳戶偏好設定 (警示、通知和訂閱)

## 登入 Experience Cloud {#signin}

登入並確認您隸屬於正確的[組織](organizations.md)。

1. 瀏覽至 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 選擇&#x200B;**[!UICONTROL 使用Adobe ID]**&#x200B;登錄。
1. 確認您所在的組織正確無誤。

   ![](assets/organizations-menu.png)

   **驗證您的組織**

   若要確認您已登入您的正確[organization](organizations.md)，請按一下您的設定檔頭像以查看組織名稱。 如果您可以存取多個組織，也可以在標題列中檢視並切換至另一個組織。

   如果貴組織使用Federated ID,Experience Cloud可讓您使用組織的單一登入進行登入，而無須輸入您的電子郵件地址和密碼。 若要這麼做，請將`#/sso:@domain`新增至Experience CloudURL(`https://experience.adobe.com`)。

   例如，對於具有Federated ID和網域`adobecustomer.com`的組織，請將URL連結設為`https://experience.adobe.com/#/sso:@adobecustomer.com`。 您也可以將此URL加入書籤並附加應用程式路徑，直接前往特定應用程式。 (例如，針對Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

## 存取 Experience Cloud 應用程式 {#navigation}

在登入 Experience Cloud 之後，您可以從統一的標頭快速存取您的所有應用程式、服務和組織。

若要存取組織內布建的Experience Cloud應用程式和服務，請前往應用程式選取器![](assets/menu-icon.png)。

![](assets/platform-core-services.png)

## 瀏覽器支援Experience Cloud {#browser}

為獲得最佳效能，Experience Cloud已針對最熱門的瀏覽器最佳化，包括最新版本以及兩個舊版。

* Chrome
* Edge
* Firefox
* Opera
* Safari

如果您的瀏覽器未列出，則可能仍受支援，但建議您使用所列的其中一個瀏覽器。

>[!NOTE]
>
>並非所有在Experience Cloud網域上執行的應用程式都支援所有瀏覽器。 如果您不確定，請查看特定應用程式的檔案。

## 語言支援Experience Cloud {#languages}

Experience Cloud支援每位使用者的偏好語言，如Adobe使用者帳戶偏好設定中所設定。 目前支援的語言包括：

* 中文
* 英文
* 法文
* 德文
* 義大利文
* 日文
* 韓文
* 葡萄牙語
* 西班牙文
* 台灣

儘管所有應用程式團隊都致力於提供全球語言支援，但並非所有應用程式都以上述所有語言提供。 如果Experience Cloud應用程式不支援您的主要語言，您也可以將次要語言設為預設（若適用）。 這可在[Experience Cloud用戶首選項](https://experience.adobe.com/preferences)中完成。

## 取得說明和支援 {#support}

使用標題中的「說明」圖示(![asset](assets/help-icon.png))存取學習與說明，包括[Experience League](https://experienceleague.adobe.com/#home)上的說明內容（檔案、教學課程和課程），以及個別應用程式的其他資源。 您還可以提交開放式意見並建立有優先權的支援票證。

![](assets/search-menu.png)

「[!UICONTROL 說明]」選單也可讓您存取：

* **[!UICONTROL 支援]：**&#x200B;建立支援服務單或使用 Twitter 聯絡[!UICONTROL 支援人員]。
* **[!UICONTROL 意見反應]：**&#x200B;分享您對 Experience Cloud 體驗的意見。您的意見是用來改善 Adobe 產品和服務。
* **[!UICONTROL 狀態]：**&#x200B;瀏覽至 `https://status.adobe.com/experience_cloud` 並檢查產品操作狀態及[!UICONTROL 管理訂閱]。
* **[!UICONTROL 開發人員文件]：**&#x200B;瀏覽至 `adobe.io` 並尋找開發人員文件。

## 全域搜索對象和實體 {#search}

全域搜尋可讓您採用一鍵式的無縫一致體驗，尋找可搜尋的商業物件或實體。此搜尋會出現在您最近存取的物件。

![](assets/platform-search.png)

>[!NOTE]
>
>全局搜索並非在所有Experience Cloud應用程式中都可用，但隨著更多內容已編製索引，它將被添加到相關應用程式中。 自2021年7月起推出：

* Experience Platform
* Journey Optimizer

## 使用者設定檔和帳戶偏好設定 {#preferences}

Experience Cloud 偏好設定包括通知、訂閱和警示。您可以在「帳戶偏好設定」選單中進行以下操作：

* 指定深色主題 (並非所有應用程式都支援這個主題)
* 搜尋[組織](organizations.md)
* 登出
* 設定帳戶偏好設定、通知和訂閱

要管理首選項，請從帳戶菜單![](assets/preferences-icon-sm.png)中選擇&#x200B;**[!UICONTROL 首選項]**。

![](assets/preferences-page.png)

您可以在「[!UICONTROL Experience Cloud 偏好設定]」上設定以下功能：

| 功能 | 說明 |
|--- |--- |
| 預設[組織](organizations.md) | 選取當您啟動 Experience Cloud 時想要看到的組織。 |
| [!UICONTROL 訂閱] | 選取您想要訂閱的產品和類別。 您的電子郵件中的「[!UICONTROL 通知]」快顯視窗中的通知。 |
| [!UICONTROL 優先順序] | 選取您希望被視為高優先順序的類別。 這些類別會以「高」優先順序標記標記，而且可以設定為像警示一樣遞送。 |
| [!UICONTROL 警示] | 選取您想要看到警示顯示在瀏覽器的通知。 警示會出現在視窗的右上角幾秒鐘。 |
| 電子郵件 | 指定您想要接收通知電子郵件的頻率。 (未傳送、即時、每天或每週。) |

{style=&quot;table-layout:auto&quot;}

## 通知和公告 {#notifications}

選取&#x200B;**[!UICONTROL 通知]**&#x200B;以收到相關且可操作的更新的警報，包括產品發行、維護通知、共用項目和核准請求。

![](assets/notifications-menu-small.png)

## Experience Cloud網域 {#domains}

Experience Cloud使用下列主機來傳送應用程式、改善效能和產品體驗。 Adobe建議將這些網域新增至防火牆的允許清單，以獲得最佳體驗。 特定Experience Cloud應用程式(例如Adobe Analytics)也可能會使用其他網域。 如需詳細資訊，請查閱這些應用程式的檔案。

| 技術 | 網域 |
|--- |--- |
| Adobe Experience Cloud網域 | `adobe.com`、`adobe.net`、`adobe.io` |
| AdobeIdentity Management服務(IMS) | `adobelogin.com` |
| Experience Cloud字型 | `typekit.net` |
| Gainsight（產品指引和說明） | `esp.aptrinsic.com` |

## 取得管理和跨應用程式服務的說明

本指南讓您存取 Admin Console 中 Experience Cloud 使用者和產品管理功能的說明，此功能可啟用平台服務的解決方案。您也可以存取對象庫、客戶屬性、Experience Cloud Assets 等的說明：

* [[!UICONTROL 對象庫]](audience-library.md)
* [[!UICONTROL Customer Attributes]](attributes.md)
* [[!UICONTROL 觸發器]](triggers.md)
* [Experience Cloud [!UICONTROL Assets]](experience-cloud-assets.md)
* [Experience Cloud Cookie](cookies-privacy.md)
* [使用者和產品管理](admin-getting-started.md) (Admin Console)
* [啟用核心服務的解決方案](core-services.md)
* [常見問答](admin-getting-started.md)
* [組織和帳戶綁定](organizations.md)
* [整合](marketing-cloud-integrations.md)
* [將 Adobe Target 與 Experience Cloud 整合](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hant)
* [Experience Cloud 隱私權及安全性總覽](assets/Adobe-Marketing-Cloud-Privacy-and-Security-Overview.pdf)
* [DNS 預先擷取](admin-getting-started.md#concept_6BC8C6856E3644F8956D7AD0A96383B7)

## 指南

相關 Experience Cloud 指南包括：

* [Adobe Mobile](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=zh-Hant)
* [Experience Platform Co-op Graph](https://experienceleague.adobe.com/docs/device-co-op/using/home.html?lang=zh-Hant)
* [Exchange](https://exchange.adobe.com/experiencecloud)
* [Experience Cloud ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)
* [Experience Platform Data Collection/Launch](https://experienceleague.adobe.com/docs/launch.html?lang=zh-Hant)
* [Experience Cloud Debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html?lang=zh-Hant)
* [一般資料保護規範 (GDPR) API](https://www.adobe.io/apis/experiencecloud/gdpr.html)
* [[!UICONTROL 動態標記管理]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant)

## 教學課程

運用 Experience League 中的自助教學課程和快速操作說明：

* [Experience League 的所有教學課程](https://experienceleague.adobe.com/???lang=zh-Hant#quick-how-tos)
* [Experience Platform 教學課程](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=zh-Hant)
* [即時客戶資料平台](https://experienceleague.adobe.com/docs/platform-learn/tutorials/application-services/rtcdp/understanding-the-real-time-customer-data-platform.html?lang=zh-Hant)

## 發行說明和相關 Experience Cloud 說明

* [所有 Experience Cloud 解決方案的產品文件](https://experienceleague.adobe.com/docs/home.html?lang=zh-Hant) - 瀏覽 Experience Cloud 學習與支援以取得說明
* [發行說明和產品更新](https://experienceleague.adobe.com/docs/release-notes/experience-cloud/current.html?lang=zh-Hant) - Experience Cloud 的新功能，以及訂閱以取得更新
* [實作核心服務的教學課程](https://experienceleague.adobe.com/docs/launch-learn/tutorials/overview.html?lang=en) - 探索有關核心服務的影片和教學課程
* [Experience League 的專家協助](https://experienceleague.adobe.com/) - 與專家和社群進行引導式學習
* [教育與訓練](https://helpx.adobe.com/tw/learning.html?promoid=KAUDK) - 與 Adobe 互動，確保您充分運用 Adobe 的產品
* [客戶體驗部落格](https://blog.adobe.com/en/topics/digital-transformation.html) - 閱讀 Experience Cloud 部落格
* [客戶服務](https://experienceleague.adobe.com/?support-solution=General#support) - 連絡 Adobe 客戶服務
