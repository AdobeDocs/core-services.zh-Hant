---
description: 瞭解CX Enterprise （先前稱為Experience Cloud）。 涵蓋登入、導覽、搜尋、偏好設定、管理以及對象庫、客戶屬性和Assets等共用服務。
title: CX企業介面與管理指南
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
TQID: https://experienceleague.adobe.com/7vFfu0DyoTnsrlrWVApm0LLW4jsC0LoXb55jJ3jdxeY
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 25446910430bf15dcfa0fc70e25e0681f9faeb95
workflow-type: tm+mt
source-wordcount: 548
ht-degree: 45%

---

# Adobe CX Enterprise介面與管理指南

[Adobe CX Enterprise](https://experience.adobe.com) (Customer Experience Enterprise)是Adobe的整合式數位行銷應用程式產品和服務系列。 您可透過它的直觀式介面，快速存取您的雲端應用程式、產品功能和服務。

<!-- ![CX Enterprise](assets/landing.png) -->

從CX Enterprise標頭，您可以：

* 存取您的所有CX Enterprise應用程式和服務
* 在「說明」選單中搜尋產品文件、教學課程和社群貼文。 在 Experience League 中檢視結果。
* 在「搜尋」欄位使用全域搜尋功能，全域搜尋商業物件 (僅適用於 Experience Platform 使用者)。
* 管理您的帳戶[偏好設定](features/account-preferences.md) (警示、通知和訂閱)

## 登入CX Enterprise

登入並確認您隸屬於正確的[組織](administration/organizations.md)。

1. 導覽至[Adobe CX Enterprise](https://experience.adobe.com)。
1. 輸入您的Adobe電子郵件地址，然後按一下&#x200B;**[!UICONTROL Continue]**。
1. 按一下帳戶。
1. 輸入密碼。
1. 確認您隸屬於正確的組織。

   ![確認您隸屬於正確的組織](assets/organizations-menu.png)

   **確認您的組織**

   [組織](administration/organizations.md)顯示在介面封面中。

   如果您的組織使用Federated ID，CX Enterprise可讓您使用組織的單一登入進行登入，而不需要輸入您的電子郵件地址和密碼。 將`#/sso:@domain`新增至CX Enterprise URL (`https://experience.adobe.com`)以完成此工作。

   例如，如果組織擁有 Federated ID 和網域 `example.com`，請將您的 URL 連結設定為 `https://experience.adobe.com/#/sso:@example.com`。 您也可以將此 URL (有附加應用程式路徑) 加入書籤，即可直接前往特定的應用程式。 (例如，Adobe Analytics 的 URL 為 `https://experience.adobe.com/#/sso:@example.com/analytics`。)

   **注意：**&#x200B;您組織的管理員可能會依IP位址限制對Adobe產品的存取。 若是如此，您登入CX Enterprise或切換到已啟用此功能的組織後，可能會收到錯誤。 如需詳細資訊，請參閱[依IP位址限制產品存取](https://helpx.adobe.com/enterprise/using/ip-based-access.html)。


## 存取CX企業應用程式

在登入CX Enterprise後，您可以從統一標題快速存取您的所有應用程式、服務和組織。

若要存取貴組織內為您布建的CX Enterprise應用程式和服務，請移至應用程式選擇器![功能表](assets/apps-icon.png)。

![存取CX Enterprise應用程式](assets/platform-core-services.png)

## 取得說明和支援

使用標頭中的&#x200B;**[!UICONTROL Help center]** （![資產](assets/help-icon.png)）來存取學習和說明，包括有關[Experience League](https://experienceleague.adobe.com/#home)的說明內容（檔案、教學課程和其他課程），以及個別應用程式的其他資源。 您還可以提交開放式意見回饋，並建立有優先權的支援服務單。

![取得說明和支援](assets/search-menu.png)

[!UICONTROL Help]功能表也可讓您存取：

* **[!UICONTROL Support]：**&#x200B;建立支援票證或使用Twitter聯絡[!UICONTROL Support]。
* **[!UICONTROL Feedback]：**&#x200B;分享您對CX Enterprise體驗的意見。 您的意見回饋會用於改善 Adobe 產品和服務。
* **[!UICONTROL Status]：**&#x200B;瀏覽至`https://status.adobe.com/experience_cloud`並檢查產品操作狀態和[!UICONTROL Manage Subscriptions]。
* **[!UICONTROL Developer Connection]：**&#x200B;瀏覽至`adobe.io`並尋找開發人員檔案。

## 管理您的使用者設定檔

在[!UICONTROL Profile]功能表中，您可以：

* 指定深色主題 (並非所有應用程式都支援這個主題)
* 管理CX Enterprise [偏好設定](features/account-preferences.md)
* 選取或搜尋「[組織](administration/organizations.md)」
* 檢視[!UICONTROL Legal Notices]
* 登出
* 設定帳戶偏好設定、通知和訂閱

## 檢視產品內通知及公告

按一下鈴鐺圖示，檢視通知和公告。 公告可能會提供相關且可操作的更新資訊，包括產品發行版本、維護通知、共用項目及核准請求。

![通知和公告](assets/notifications-menu-small.png)

若要管理通知和警報，請參閱「[帳戶偏好設定和通知](features/account-preferences.md)」


