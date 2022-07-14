---
description: 了解組織 (IMS 組織 ID) 以及將解決方案帳戶連結至 Experience Cloud。
keywords: Adobe Experience Cloud 服務
solution: Experience Cloud
title: '組織和帳戶連結 '
uuid: ae47ad18-ac33-4efa-8b68-2bfaf77397aa
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 6eb58530-2a7a-48c7-9a5b-48a6e980a034
source-git-commit: c6884ade4a793f1cedbc5d497cb9c8ea798a7408
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 80%

---

# Experience Cloud 中的組織

了解如何在 Experience Cloud 中管理及切換組織。

## 識別組織 {#concept_384D169B0B724B799D573B8ECB5C39BF}

安 *組織* （組織ID）是使管理員能夠配置組和用戶並控制Experience Cloud中的單一登錄的實體。 組織的作用就像一間登入公司，涵蓋所有 Experience Cloud 產品和應用程式。 通常組織就是您的公司名稱，但是一間公司可以有多個組織。

若要確認您已登入正確的組織，請按一下您的個人資料頭像，以查看組織名稱。 如果您可以存取多個組織，您也可以在標題列中檢視並切換到其他組織。

如果貴組織使用 Federated ID，Experience Cloud 可讓您使用組織的單一登入進行登入，而不需要輸入您的電子郵件地址和密碼。 若要這樣做，請將 `#/sso:@domain` 新增到 Experience Cloud URL (`https://experience.adobe.com`)。

例如，如果組織擁有 Federated ID 和網域 `adobecustomer.com`，請將您的 URL 連結設定為 `https://experience.adobe.com/#/sso:@adobecustomer.com`。 您也可以將此 URL (有附加應用程式路徑) 加入書籤，即可直接前往特定的應用程式。 (例如，Adobe Analytics 的 URL 為 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

![步驟結果](assets/organization-switch.png)

## 查看您的組織ID {#concept_EA8AEE5B02CF46ACBDAD6A8508646255}

為了支援目的，您可能需要查找分配的組織ID。 您可以使用「**[!UICONTROL 組織]**」選單來確認自己所在的組織是否正確，或者切換組織。

組織 ID 是與已佈建 Experience Cloud 公司相關聯的 ID。此 ID 是 24 個字元的英數字串，後面接著 (而且必須包含) `@AdobeOrg`。

您可以使用鍵盤快捷方式查看組織ID以及其他帳戶資訊 **Ctrl+i** 從任何頁 `https://experience.adobe.com`。

**查看組織ID**

1. 在 [Experience Cloud](https://experience.adobe.com)按 **Ctrl+i** 鍵盤上。

   ![指派的組織 ID](assets/assigned-organization.png)

1. 下 **[!UICONTROL 用戶資訊]**，查找 **[!UICONTROL 當前組織ID]**，您將看到組織ID。

   或者，管理員可以登錄Admin Console(導航到 [https://adminconsole.adobe.com](https://adminconsole.adobe.com))並查看URL中的組織ID。

   舉例來說，在以下網址中：

   `https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

   ID 是：

   `C538193582390300A495CC9@AdobeOrg`

## 將應用程式帳戶連結至 Adobe ID {#task_FD389E78640848919E247AC5E95B8369}

通常 Experience Cloud 管理員會授予應用程式和服務的存取權。 在少數情況下，您可能需要將應用程式認證連結至 Adobe ID。

1. 依照邀請您前往 Experience Cloud 的電子郵件中的步驟進行。
1. 使用您的 Adobe ID 或 Enterprise ID 登入。
1. 選取應用程式選擇器 ( ![](assets/menu-icon.png))。

   ![將應用程式帳戶連結至 Adobe ID](assets/solutions-active.png)

   系統會將您有權存取的應用程式標上顏色。
1. 選取所需的應用程式。

   ![選取所需的應用程式](assets/analytics-link-accounts.png)

   如果您隸屬於適當的群組 (並擁有應用程式的權限)，但尚未將帳戶認證與 Adobe ID 綁定，系統就會顯示這類訊息。
1. 選取「**[!UICONTROL 連結帳戶]**」，然後提供您的認證。

## 指定預設機構和登陸頁面 {#concept_6A191B42A9874A9780882903BA18F071}

您可指定在登入時使用的預設組織和登陸頁面。

在您的個人資料中，選取「**[!UICONTROL 編輯個人資料]**」。

![編輯個人資料](assets/edit-profile.png)

在「預設組織和登陸頁面」下方，您可以自訂登入體驗。

![預設組織和登陸頁面](assets/default-organization.png)

## 帳戶連結問題疑難排解 {#concept_DFCB29A3B4834FC59AA29E0BBA301584}

帳戶連結所產生問題的說明。

通常帳戶連結之所以失敗，是因為 Adobe ID 已連結至先前的使用者。帳戶連結失敗時，您可以：

* [聯絡 Adobe 支援](https://experienceleague.adobe.com/?lang=zh-Hant?support-solution=General#support)。
* 在問題待解決之際，您仍可使用標準登入存取應用程式。
