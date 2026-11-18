---
title: 開始使用CX Enterprise
description: 瞭解如何登入CX Enterprise、啟動您的應用程式，並熟悉統一的標題。 使用這些步驟可快速上手並執行。
solution: CX Enterprise
feature: Central Interface Components
topic: Administration
role: Admin, User
level: Beginner
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: ecde38a8abc308acc666c6a0cb321c716921d2da
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 33%
---
# 開始使用CX Enterprise {#get-started}

登入[Adobe CX Enterprise](https://experience.adobe.com)以啟動您的應用程式，然後使用統一的標題來管理您的設定檔、檢查通知並尋找說明，全部從一處即可完成。

## 開始之前 {#before-you-begin}

您需要已針對您組織的CX Enterprise產品布建的Adobe ID。 如果您無法登入或看不到您期望的應用程式，請連絡您的[!UICONTROL CX Enterprise] [系統管理員](administration/admin-console.md)。

## 登入CX Enterprise {#sign-in}

登入並確認您隸屬於正確的[組織](administration/organizations.md)。

1. 導覽至[Adobe CX Enterprise](https://experience.adobe.com)。
1. 輸入您的Adobe電子郵件地址，然後按一下&#x200B;**[!UICONTROL 繼續]**。
1. 按一下帳戶。
1. 輸入密碼。
1. 確認您隸屬於正確的組織。

   ![確認您隸屬於正確的組織](assets/organizations-menu.png)

   **確認您的組織**

   [組織](administration/organizations.md)顯示在介面封面中。

   如果您的組織使用Federated ID，CX Enterprise可讓您使用組織的單一登入進行登入，而不需要輸入您的電子郵件地址和密碼。 將`#/sso:@domain`新增至CX Enterprise URL (`https://experience.adobe.com`)以完成此工作。

   例如，如果組織擁有 Federated ID 和網域 `example.com`，請將您的 URL 連結設定為 `https://experience.adobe.com/#/sso:@example.com`。 您也可以將此 URL (有附加應用程式路徑) 加入書籤，即可直接前往特定的應用程式。 (例如，Adobe Analytics 的 URL 為 `https://experience.adobe.com/#/sso:@example.com/analytics`。)

   **注意：**&#x200B;您組織的管理員可能會依IP位址限制對Adobe產品的存取。 若是如此，您可能在登入CX Enterprise或切換至啟用此功能的組織後，收到錯誤。 如需詳細資訊，請參閱[依IP位址限制產品存取](https://helpx.adobe.com/enterprise/using/ip-based-access.html)。

## 存取CX Enterprise應用程式 {#applications}

登入CX Enterprise後，您可以從統一的標題快速存取您的所有應用程式、服務和組織。

若要存取貴組織內為您布建的CX Enterprise應用程式和服務，請移至應用程式選擇器![功能表](assets/apps-icon.png)。

![存取CX Enterprise應用程式](assets/application-menu.png)

## 管理您的使用者設定檔 {#profile}

在[!UICONTROL 設定檔]功能表中，您可以：

* 指定深色主題 (並非所有應用程式都支援這個主題)
* 管理CX Enterprise [偏好設定](features/account-preferences.md)
* 選取或搜尋「[組織](administration/organizations.md)」
* 檢視[!UICONTROL 法律注意事項]
* 登出
* 設定帳戶偏好設定、通知和訂閱

## 檢視產品內通知及公告 {#notifications}

按一下鈴鐺圖示，檢視通知和公告。 公告可能會提供相關且可操作的更新資訊，包括產品發行版本、維護通知、共用項目及核准請求。

![通知和公告](assets/notifications-menu-small.png)

若要管理通知和警示，請參閱[帳戶偏好設定和通知](features/account-preferences.md)。

## 取得說明和支援 {#help}

使用標頭中的&#x200B;**[!UICONTROL 說明中心]** （![資產](assets/help-icon.png)）來存取學習和說明，包括有關[Experience League](https://experienceleague.adobe.com/#home)的說明內容（檔案、教學課程和其他課程），以及個別應用程式的其他資源。 您還可以提交開放式意見回饋，並建立有優先權的支援服務單。

![取得說明和支援](assets/search-menu.png)

[!UICONTROL 說明]功能表也可讓您存取：

* **[!UICONTROL 支援]：**&#x200B;建立支援票證或使用Twitter聯絡[!UICONTROL 支援]。
* **[!UICONTROL 意見反應]：**&#x200B;分享您對CX Enterprise體驗的意見。 您的意見回饋會用於改善 Adobe 產品和服務。
* **[!UICONTROL 狀態]：**&#x200B;瀏覽至`https://status.adobe.com/experience_cloud`並檢查產品操作狀態和[!UICONTROL 管理訂閱]。
* **[!UICONTROL Developer Connection]：**&#x200B;瀏覽至`adobe.io`並尋找開發人員檔案。

## 有關此主題的更多說明 {#more-help}

* [Admin Console中的使用者和產品管理](administration/admin-console.md)
* [開始使用People服務](services/getting-started.md)
* [帳戶偏好設定和通知](features/account-preferences.md)
