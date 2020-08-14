---
description: 了解如何登入 Admin Console、管理 Experience Cloud 的使用者權限和產品設定檔以及瀏覽器支援。
keywords: core services
seo-description: 了解如何登入 Admin Console、管理 Experience Cloud 的使用者權限和產品設定檔以及瀏覽器支援。
seo-title: 管理 Experience Cloud 使用者和產品
solution: Experience Cloud
title: 管理 Experience Cloud 使用者和產品
index: true
translation-type: tm+mt
source-git-commit: 1d3f4449f1f3b939e5dc61ad9838475be73f0cfa
workflow-type: tm+mt
source-wordcount: '1455'
ht-degree: 100%

---


# 管理 Experience Cloud 使用者和產品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

了解如何登入 Admin Console、管理 Experience Cloud 的使用者權限和產品設定檔以及瀏覽器支援。

>[!IMPORTANT]
>
>Admin Console 中的使用者管理引進了新的詞語、介面和導覽。下列資訊說明了這些變更，並提供額外說明資源的連結，有助於補充所有 Adobe 雲端產品的[企業版管理使用手冊](https://helpx.adobe.com/tw/enterprise/managing/user-guide.html)之資訊。

## Experience Cloud 使用者管理的新功能 {#concept_06A0A13362F644FB90F947238407637A}

了解 Experience Cloud 使用者管理中的最新功能。

<!-- ### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

### 管理工具

管理員可以在管理工具中，檢視所有 Experience Cloud 使用者及其詳細資訊，且可將清單加以排序及篩選。請參閱[在管理工具中檢視 Experience Cloud 使用者](admin-tool-experience-cloud.md)。

## 登入 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理員不再需要於管理解決方案中管理使用者。Experience Cloud 的使用者和產品管理現在需在 Admin Console 中進行。

登入 Admin Console 的方式：

1. 導覽至 [/](https://adminconsole.adobe.com/enterprise/#)https://adminconsole.adobe.com/enterprise/#。
1. 輸入您的 [Adobe ID 或 Enterprise ID](https://helpx.adobe.com/tw/enterprise/help/identity.html) 和密碼。

或者，從 Experience Cloud 功能表登入 (![](assets/menu-icon.png) 按一下&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 啟動 Admin Console]**。

**相關說明**

Creative Cloud 和 Document Cloud 的[管理使用手冊](https://helpx.adobe.com/tw/enterprise/using/users.html)。有些資訊與 Experience Cloud 使用者管理相關，例如[管理身分類型](https://helpx.adobe.com/tw/enterprise/help/identity.html)。

[登入並管理您的設定檔設定](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0)，以管理密碼、組織和通知。

## 產品設定檔和群組 {#section_AB50558124D541CF80A0D3D76D35A4BF}

產品設定檔的加入，代表著先前管理解決方案產品與服務的方式 (使用群組進行管理) 有所轉變。在 Admin Console 中，權限是以產品設定檔為基礎，而產品設定檔是您可指派給使用者的產品和服務群組。

例如，在 Analytics 中，您可以設定報表工具的集合，例如 Analysis Workspace 和 Report Builder，以及報表套裝、量度、維度等項目。您可以透過將使用者新增至設定檔來授予產品設定檔的權限給使用者。請參閱[將 Analytics 存取權指派至產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)。

**相關說明**

[委派有限的管理權限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 使用者和產品權限。

[將 Analytics 存取權指派至產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (請參考本頁)。

**使用者帳戶移轉**

Analytics 使用者 ID 移轉工具可協助 Analytics 管理員將使用者帳戶從 Analytics 使用者管理移轉到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

帳戶移轉功能會分階段向客戶推出。Adobe 會在您需要進行移轉時通知您，並協助您從&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 使用者管理]**&#x200B;將現有使用者帳戶移轉到 Admin Console。

移轉後，使用者可以在 [experiencecloud.adobe.com](https://experiencecloud.adobe.com) 使用他們的 Adobe ID (或 Enterprise ID) 登入，並針對其 Experience Cloud 解決方案和服務進行驗證。如果使用者嘗試透過舊版登入頁面 ([!DNL my.omniture.com] 和 [!DNL sc.omniture.com]) 登入，則會被重新導向至 [!DNL experiencecloud.adobe.com]。

**相關說明**

[Analytics 使用者 ID 移轉](https://docs.adobe.com/content/help/zh-Hant/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Adobe Target - 產品設定檔與 Workspace{#section_3860AF177C9E4C7E9C390D36A414F353}

在 Adobe Target 中，Workspace 是產品設定檔，可讓組織將特定一組使用者指派至特定一組屬性。Workspace 有許多地方與 Adobe Analytics 報表套裝相似。

請參閱：
* [企業使用者權限](https://docs.adobe.com/content/help/zh-Hant/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理產品和設定檔](https://helpx.adobe.com/tw/enterprise/using/manage-products-and-profiles.html)
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/tw/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 行銷活動 - 產品設定檔、租用戶和安全性群組 {#section_09CDF75366444CF5810CF321B7C712F3}

行銷活動中的&#x200B;*租用戶*&#x200B;在 Admin Console 的&#x200B;*產品*&#x200B;頁面中會顯示為產品。

*安全群組* (Security group)會顯示為產品設定檔。

有關安全群組和將使用者指派至安全群組的資訊，請參閱[管理群組和使用者](https://helpx.adobe.com/tw/campaign/standard/administration/using/managing-groups-and-users.html)。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform Launch 會顯示在 Admin Console 的「產品」頁面上。您可以在 Launch 產品設定檔中加入其他解決方案和服務。

如需 Admin Console 中的使用者權限，以及設定 Launch 專用選項 (包括指派設定檔的權限) 的相關資訊，請參閱[使用者管理](https://docs.adobelaunch.com/launch-reference/administration/user-permissions)。

## Experience Manager 雲端服務

Adobe 企業客戶在 Adobe Admin Console 中會顯示為 IMS 組織。Adobe 客戶可使用此入口網站管理使用者和群組的產品權益。AEM 客戶可使用 Adobe Admin Console 管理其產品權益以及 AEM 雲端服務的 IMS 驗證。

請參閱 [AEM 雲端服務的 IMS 支援](https://docs.adobe.com/content/help/zh-Hant/experience-manager-cloud-service/security/ims-support.html#managing-products-and-user-access-in-admin-console)。

## Dynamic Tag Manager {#section_3A41CF2BD5994B9891537D063571D4ED}

邀請使用者加入 Dynamic Tag Management，並指派使用者角色與新增使用者至群組。

若要了解如何邀請使用者加入 Dynamic Tag Management，及為群組指派使用者角色及新增使用者，請參閱[使用者與權限](https://docs.adobe.com/content/help/zh-Hant/dtm/using/admin/users.html)。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

建立 Audience Manager 使用者並將其指派至群組。您也可以檢視限制 (特徵、區段、目的地和 [!DNL AlgoModel])。

請參閱 Audience Manager說明中的[管理](https://docs.adobe.com/content/help/zh-Hant/dtm/using/admin/users.html)。

## 管理 Experience Cloud 產品 {#task_16335111C52D40E9BAC73D0699584DBF}

建立產品設定檔並將其指派至權限群組。

邀請使用者加入組織時，可提供產品和產品設定檔的存取權給使用者。您也可以委派有限的管理權限給使用者。同樣地，您可以建立使用者群組，然後將群組新增至產品設定檔以啟用存取權。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，按一下&#x200B;**[!UICONTROL 產品]**。
1. 按一下&#x200B;**[!UICONTROL 新增設定檔]**。
1. 設定設定檔的詳細資料，然後按一下&#x200B;**[!UICONTROL 下一步]**。
1. 按一下&#x200B;**[!UICONTROL 完成]**。

如需更多說明，請參閱：

* [管理產品和設定檔](https://helpx.adobe.com/tw/enterprise/using/manage-products-and-profiles.html)
* Adobe Target 說明中的[企業使用者權限](https://docs.adobe.com/content/help/zh-Hant/target/using/administer/manage-users/enterprise/property-channel.html)以取得詳細資訊。
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/tw/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 將 Analytics 存取權指派至產品設定檔 {#task_040673FE3E3E429B9531FBCB8B6A4391}

將 Analytics 報表存取權 (報表套裝、量度、維度等等) 指派至產品設定檔。

例如，您可以建立含有多個 Analytics 工具 ([!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 及 [!UICONTROL Report Builder]) 的產品設定檔、具有特定量度和維度 (包括 eVar) 之權限，並具有區段或計算量度建立等功能。

1. 登入 [Admin Console](https://adminconsole.adobe.com/enterprise)，然後按一下&#x200B;**[!UICONTROL 產品]** (或按一下您的產品名稱)。
1. 然後，在產品設定檔中，按一下&#x200B;**[!UICONTROL 權限]** (僅限管理員使用)。
1. 設定設定檔的權限：

| 元素 | 說明 |
|--- |--- |
| 報表套裝 | 啟用特定報表套裝的權限。 |
| 量度 | 為流量、轉換、自訂事件、解決方案事件、內容感知等項目啟用權限。 |
| 維度 | 在粒度層級自訂使用者存取，包括 eVar、流量報表、解決方案報表和路徑報表。 |
| 報表套裝工具 | 為網站服務、報表套裝管理、工具和報表與儀表板項目啟用使用者權限。 |
| Analytics 工具 | 啟用「一般」項目 (帳單、日誌等)、公司管理、工具、網站服務存取、Report Builder 和 Data Connectors 整合的使用者權限。來自自訂管理控制台類別的公司設定已移至分析工具。 |

## 委派管理角色給使用者 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在 Admin Console 中，您可以將有限的管理權限委派給組織中的其他人。委派角色可讓使用者管理軟體對使用者的存取權、提供存取部署功能，且可當成支援委派者。

例如，您可以：

* 允許您的創意總監授予 Creative Cloud 的存取權。
* 允許您的行銷總監授予 Experience Cloud 的存取權。
* 將這兩個角色分開，這樣它們就不能超越彼此的角色。

使用這些角色，您便可同時將管理作業委派給其他人，無需提供超出其所需的功能。

1. 在 Admin Console 中，按一下&#x200B;**[!UICONTROL 使用者]**，然後按一下使用者的姓名。
1. 按一下&#x200B;**[!UICONTROL 編輯管理權限]**。
1. 設定使用者的管理權限。
1. 按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以檢閱設定，然後按一下&#x200B;**[!UICONTROL 儲存]**。

## 支援的瀏覽器和系統需求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud 中支援的瀏覽器。

* [!DNL Microsoft Edge] (Microsoft 即將[停止支援](https://www.microsoft.com/zh-tw/WindowsForBusiness/End-of-IE-support) Internet Explorer 8、9 和 10。有鑑於此，Adobe 將不會修正針對這些特定版本 Internet Explorer 所回報的問題。)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;雖然 Experience Cloud 介面可支援這些瀏覽器，但個別解決方案可能不會支援所有瀏覽器(例如 [Analytics](https://docs.adobe.com/content/help/zh-Hant/analytics/admin/sys-reqs.html) 不支援 [!DNL Opera]，而 [Adobe Target](https://docs.adobe.com/help/zh-Hant/target/using/implement-target/before-implement/supported-browsers.html) 不支援 [!DNL Safari])。

### 解決方案和產品要求

* [Analytics](https://docs.adobe.com/content/help/zh-Hant/analytics/admin/sys-reqs.translate.html)
* [Report Builder](https://docs.adobe.com/content/help/zh-Hant/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/zh-Hant/target/using/implement-target/before-implement/supported-browsers.translate.html)
