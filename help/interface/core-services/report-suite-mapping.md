---
description: 瞭解如何將一個或多個報表套裝對應至組織。
seo-description: 瞭解如何將一個或多個報表套裝對應至組織。
seo-title: 將報表套裝對應至組織
title: 將報表套裝對應至組織
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
translation-type: tm+mt
source-git-commit: b6ef7f0b7ef3b43b437524b20cee940889c26ba8

---


# 將報表套裝對應至組織 {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

瞭解如何將一個或多個報表套裝對應至組織。

Experience Cloud服務（例如Experience Cloud ID服務和People核心服務）與組織相關聯，而非個別報表套裝。 若要確保這些服務能正確運作，每個 Analytics 報表套裝都必須對應至組織。對應程序:

* 將 Experience Cloud 組織設為報表套裝的主要組織。
* 不要變更能存取報表套裝的使用者 (每位使用者的存取權仍然由 Adobe Analytics 登入帳戶所決定)

**需求**

您必須是登入公司的 Analytics 管理員，且該公司擁有要對應之報表套裝的存取權。此外，此帳戶必須[連結至 Experience Cloud 組織](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)，才能將報表套裝對應至該組織。

如果您沒有可存取特定報表套件組織的登入公司之 Analytics 管理員權限，組織一區則會顯示灰色。

## 將報表套裝對應至組織 {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. Click **[!UICONTROL Experience Cloud]** > **[!UICONTROL Administration]** > **[!UICONTROL Report Suite Mapping]**

1. 若要查看可存取每個報表套裝的登入公司資訊，請按一下&#x200B;**[!UICONTROL 只有登入公司能看見]**。

   此檢視模式的目的在於協助您在對應上做出明智的決策。

1. 按一下報表套裝旁邊&#x200B;**[!UICONTROL 「已對應組織」]**&#x200B;欄中的下拉式清單，並選取您要對應的組織。

   如需選取 Experience Cloud 組織的相關秘訣，請參閱下一節。

## 將多個報表套裝對應至組織 {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. 按一下&#x200B;**[!UICONTROL 「Experience Cloud]** > **[!UICONTROL 管理]** > **[!UICONTROL 報表套裝對應」]**。

1. 選取您要對應的報表套裝。

   ![](assets/rs-mapping-multiple.png)

1. 選取組織 (在此範例中為 Outdoors Inc)，然後按一下&#x200B;**[!UICONTROL 選取]**。

   如需選取 Experience Cloud 組織的相關秘訣，請參閱下一節。

1. 按一下&#x200B;**[!UICONTROL 儲存對應]**。

## 選取 Experience Cloud 組織的秘訣 {#mapping-tips}

本節包含的秘訣可協助您選取應對應至報表套裝的 Experience Cloud 組織。

**我應該選擇哪個組織?**

If the Experience Cloud ID Service is currently deployed on the report suite, ensure the organization you select in the Report Suite Mapping tool is the same organization specified in the [!DNL visitorAPI.js] file on your site. 您可以透過[測試並驗證 Experience Cloud ID 服務](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/test-verify.html)中的指示，來尋找由訪客 ID 服務使用的組織 ID。

如果訪客 ID 服務尚未在為報表套裝收集資料的網站上部署，而您希望在日後部署 Experience Cloud 訪客 ID 服務，您需要確認您的部署與報表套裝對應工具中所選擇的組織相同。

**為什麼有些組織顯示灰色?**

迠代表您沒有足夠權限對應至顯示灰色的報表套裝。考量下列範例:

![](assets/rs-mapping.png)

此圖表中，藍色圖例表示管理權限，灰線表示可見性。

這位使用者擁有兩個 Experience Cloud 組織的存取權，他執行下列事項:

* Linked his admin account in the [!UICONTROL chapek] Analytics login company to his [!UICONTROL Chapek] Corp Experience Cloud organization account.
* Linked his non-admin account in the [!UICONTROL doohan] Analytics login company to his [!UICONTROL Chapek] Corp Experience Cloud organization account.
* 將他在 nigel Analytics 登入公司的非管理員帳戶連結至其 Nigel Inc Experience Cloud 組織帳戶。

以下幾點列出了此使用者可以對這些報表套裝執行的對應動作，以及無法執行的對應動作:

* [!UICONTROL Chapek-prod] report suite可以映射至 [!UICONTROL Chapek] Corp org，因為此使用者是連結Analytics登入公司([!UICONTROL chapek])的管理員，且其帳戶連結至此組織。
* [!UICONTROL 由於使用者並非可以檢視此報表套裝之登入公司的管理員，因此使用者無法連結 Nigel-prod 報表套裝。]
* [!UICONTROL Doohan-prod] Report Suite可映射至 [!UICONTROL Chapek Corp] ，因為此使用者是連結至Experience Cloud組織的登入公司([!UICONTROL chapek])的管理員（請注意，他並非Doohan Analytics登入公司的管理員）。 It is important to be aware that the [!UICONTROL doohan-prod] report suite is also eligible to be mapped to the Nigel Inc Experience Cloud org, even though this user cannot perform that mapping. In this case, both Experience Cloud organizations are displayed in the list, but [!UICONTROL Nigel Inc] is grayed out. 進行對應前，此使用者應洽詢 nigel 登入公司的管理員，以判斷最合適的對應組織。如果您選取的組織與報表套裝原本建立的組織不同，UI 則會顯示「可能會發生衝突」的警告。

## 常問的問題 {#section_099E485805994C929FF9C9F75219BEE1}

**為什麼我看不到所有報表套裝?**

部分報表套裝可能供不同登入公司檢視。您可以透過畫面上方的下接單變更目前的登入公司。

**如果我不認識其中一個報表套裝下拉式清單中的某些組織，這時該怎麼辦?**

清單會顯示您報表套裝可對應的所有*可能*組織，即使您並未擁有這些報表套裝的權限。如果您不確定報表套裝是否應對應至清單上其中一個顯示灰色的組織，請洽詢貴組織的 Experience Cloud 管理員以做出最適當的選擇。

**如果我不認識「只有登入公司能看見」欄中列出的某些報表套裝的登入公司，這時該怎麼辦?**

某些時候，此報表套裝會與另一個可能隸屬不同 Experience Cloud 組織的另一個登入公司共用。

**另一個組織產生關於報表套裝的「可能會發生衝突」的錯誤代表什麼? 為什麼要加以注意?**

該通知能協助您在報表套裝對應上做出明智的決策。我們希望您注意到該報表套裝原本建立在不同的組織下，或許該組織更適合此報表套裝。

**我如何得知報表套裝已對應?**

已對應的報表套裝會以非編輯格式顯示，如果您需要變更對應，請聯絡客戶服務。

**如果我只知道 Experience Cloud 組織的組織 ID，這時該怎麼辦? 我要如何查詢組織 ID 的名稱?**

您可以在[組織和帳戶設定](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html)中找到您的組織名稱。

**我在「已對應資料」欄中看到一個日期。這資料由誰進行對應?**

您可以參閱 Analytics 介面的「報表套裝變更記錄」以查看進行變更的使用者 ID。尋找事件「與 IMS 組織關聯的套裝」。
