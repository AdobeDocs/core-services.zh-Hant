---
description: '了解如何登入以及Experience Cloud中的中央介面元件。 了解全域搜尋、您的帳戶偏好設定，以及如何導覽介面和取得說明。 '
solution: Experience Cloud
title: 'Experience Cloud 中央 UI 元件 '
feature: 「中央介面元件」
topic: 管理
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: c9a6059b0af9c6229fd72580f997c1c6f2dfbbe4
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 51%

---

# Experience Cloud 介面說明

Experience Cloud 的中央介面元件包括可讓您進行以下操作的功能：

* 登入及存取您的應用程式和服務
* 使用全域搜尋尋找產品說明和商業物件
* 管理您的帳戶偏好設定 (警示、通知和訂閱)

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

## 登入 Experience Cloud {#signin}

登入並確認您隸屬於正確的[組織](organizations.md)。

1. 瀏覽至 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 選擇&#x200B;**[!UICONTROL 使用Adobe ID]**&#x200B;登錄。
1. 確認您所在的組織正確無誤。

   ![](assets/organizations-menu.png)

   若要確認您已登入您的正確[organization](organizations.md)，請按一下您的設定檔頭像以查看組織名稱。 如果您可以存取多個組織，也可以在標題列中檢視並切換至另一個組織。

   如果貴組織使用Federated ID,Experience Cloud可讓您使用組織的單一登入進行登入，而無須輸入您的電子郵件地址和密碼。 若要這麼做，請將`#/sso:@domain`新增至Experience CloudURL(`https://experience.adobe.com`)。

   例如，對於具有Federated ID和網域`adobecustomer.com`的組織，請將URL連結設為`https://experience.adobe.com/#/sso:@adobecustomer.com`。 您也可以將此URL加入書籤並附加應用程式路徑，直接前往特定應用程式。 (例如，針對Adobe Analytics, `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

## 存取 Experience Cloud 應用程式 {#navigation}

在登入 Experience Cloud 之後，您可以從統一的標頭快速存取您的所有應用程式、服務和組織。

選擇應用程式選擇器![](assets/menu-icon.png)以訪問您擁有的Experience Cloud服務。

![](assets/platform-core-services.png)

## Experience Cloud 中的搜尋和支援 {#search}

Experience Cloud 搜尋可讓您搜尋 [Experience League](https://experienceleague.adobe.com/?lang=zh-Hant#home) 上的說明 (文件、教學課程和其他課程)。

![](assets/search-menu.png)

「[!UICONTROL 說明]」選單也可讓您存取：

* **[!UICONTROL 支援]：**&#x200B;建立支援服務單或使用 Twitter 聯絡[!UICONTROL 支援人員]。
* **[!UICONTROL 意見反應]：**&#x200B;使用「意見反應」聯絡 Adobe 並讓我們知道您的想法。
* **[!UICONTROL 狀態]：**&#x200B;瀏覽至 `https://status.adobe.com/experience_cloud` 並檢查產品操作狀態及[!UICONTROL 管理訂閱]。
* **[!UICONTROL 開發人員文件]：**&#x200B;瀏覽至 `adobe.io` 並尋找開發人員文件。

## 帳戶偏好設定 {#account-menu}

您可以在「帳戶偏好設定」選單中進行以下操作：

* 指定深色主題 (並非所有應用程式都支援這個主題)
* 搜尋[組織](organizations.md)
* 登出
* 設定帳戶[偏好設定、通知和訂閱](#preferences)

### 管理 Experience Cloud [!UICONTROL 偏好設定] {#preferences}

Experience Cloud 偏好設定包括通知、訂閱和警示。

從帳戶菜單![](assets/preferences-icon-sm.png)中選擇&#x200B;**[!UICONTROL 首選項]**&#x200B;以管理首選項。

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

選擇&#x200B;**[!UICONTROL 通知]**&#x200B;以查看對您而言重要的通知以及來自Adobe的公告。

![](assets/notifications-menu-small.png)

您可以在「[Experience Cloud 偏好設定](#preferences)」中設定通知。
