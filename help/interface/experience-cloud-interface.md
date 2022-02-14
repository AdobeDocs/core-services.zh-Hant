---
description: '了解如何登入以及有關 Experience Cloud 中的中央介面元件。 了解全域搜尋、您的帳戶偏好設定，以及如何瀏覽介面及取得說明。 '
solution: Experience Cloud
title: 'Experience Cloud 中央 UI 元件 '
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner, Intermediate, Experienced
source-git-commit: 5281aededf07508cb49ecd4f3017ccec3d4851fb
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 100%

---

# Experience Cloud 介面說明

Experience Cloud 的中央介面元件包括可讓您進行以下操作的功能：

* 登入及存取您的應用程式和服務
* 使用全域搜尋尋找產品說明和商業物件
* 管理您的帳戶偏好設定 (警示、通知和訂閱)

## Experience Cloud 中的瀏覽器支援 {#browser}

為了提供最佳效能，Experience Cloud 已針對最熱門的瀏覽器 (包括最新版本及前兩個版本) 最佳化。

* Chrome
* Edge
* Firefox
* Opera
* Safari

如果這裡未列出您使用的瀏覽器，該瀏覽器可能還是有受到支援，但建議您使用這裡列出的其中一個瀏覽器。

>[!NOTE]
>
>並非在 Experience Cloud 網域上執行的所有應用程式都可支援所有瀏覽器。 如果您不確定，請查閱特定應用程式的文件。

## Experience Cloud 中的語言支援 {#languages}

Experience Cloud 可支援每個使用者偏好的語言，如同您的 Adobe 使用者帳戶偏好設定中所設定。 目前支援的語言如下：

* 中文
* 英文
* 法文
* 德文
* 義大利文
* 日文
* 韓文
* 葡萄牙語
* 西班牙文
* 繁體中文 (台灣)

雖然所有應用程式團隊都致力於提供全球語言的支援，但並非所有應用程式都有提供上述的所有語言版本。 如果 Experience Cloud 應用程式不支援您的主要語言，您也可以將次要語言設定為預設語言 (如適用)。 您可以在 [Experience Cloud 使用者偏好設定](https://experience.adobe.com/preferences)中進行這項設定。

## 登入 Experience Cloud {#signin}

登入並確認您隸屬於正確的[組織](organizations.md)。

1. 瀏覽至 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 選取「**[!UICONTROL 使用 Adobe ID 登入]**」。
1. 確認您隸屬於正確的組織。

   ![確認您的組織](assets/organizations-menu.png)

   若要確認您已登入正確的[組織](organizations.md)，請按一下您的個人資料頭像，以查看組織名稱。 如果您可以存取多個組織，您也可以在標題列中檢視並切換到其他組織。

   如果貴組織使用 Federated ID，Experience Cloud 可讓您使用組織的單一登入進行登入，而不需要輸入您的電子郵件地址和密碼。 若要這樣做，請將 `#/sso:@domain` 新增到 Experience Cloud URL (`https://experience.adobe.com`)。

   例如，如果組織擁有 Federated ID 和網域 `adobecustomer.com`，請將您的 URL 連結設定為 `https://experience.adobe.com/#/sso:@adobecustomer.com`。 您也可以將此 URL (有附加應用程式路徑) 加入書籤，即可直接前往特定的應用程式。 (例如，Adobe Analytics 的 URL 為 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

## 存取 Experience Cloud 應用程式 {#navigation}

在登入 Experience Cloud 之後，您可以從統一的標頭快速存取您的所有應用程式、服務和組織。

選取應用程式選擇器 ![](assets/menu-icon.png)，存取您擁有的 Experience Cloud 服務。

![存取 Experience Cloud 應用程式](assets/platform-core-services.png)

## Experience Cloud 中的搜尋和支援 {#search-support}

Experience Cloud 搜尋可讓您搜尋 [Experience League](https://experienceleague.adobe.com/#home) 上的說明 (文件、教學課程和其他課程)。

![Experience Cloud 中的搜尋和支援](assets/search-menu.png)

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

從您的帳戶選單 ![](assets/preferences-icon-sm.png) 選取「**[!UICONTROL 偏好設定]**」可管理偏好設定。

![管理 Experience Cloud](assets/preferences-page.png)

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

選取「**[!UICONTROL 通知]**」可查看對您重要的通知以及來自 Adobe 的公告。

![通知和公告](assets/notifications-menu-small.png)

您可以在「[Experience Cloud 偏好設定](#preferences)」中設定通知。
