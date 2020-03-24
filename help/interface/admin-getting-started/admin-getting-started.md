---
description: 瞭解登入Admin Console、管理Experience Cloud使用者權限和產品設定檔，以及瀏覽器支援。
keywords: core services
seo-description: 瞭解登入Admin Console、管理Experience Cloud使用者權限和產品設定檔，以及瀏覽器支援。
seo-title: 管理 Experience Cloud 使用者和產品
solution: Experience Cloud
title: 管理 Experience Cloud 使用者和產品
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: b6bd75d92ce96e852a6e548362988a9b4d529fb9

---


# 管理 Experience Cloud 使用者和產品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

瞭解登入Admin Console、管理Experience Cloud使用者權限和產品設定檔，以及瀏覽器支援。

>[!IMPORTANT]
>
>Admin Console 中的使用者管理引進了新的詞語、介面和導覽。下列資訊說明了這些變更，並提供額外說明資源的連結，This help supplements the information in the [Enterprise Administration User Guide](https://helpx.adobe.com/enterprise/managing/user-guide.html) for all Adobe cloud products.

## Experience Cloud 使用者管理的新功能 {#concept_06A0A13362F644FB90F947238407637A}

瞭解 Experience Cloud 使用者管理中的最新功能。

<!--

### Business ID type

Adobe is now introducing a new identity type: **Business ID**. This identity type, improves the control of user and product management, and content, while increasing the flexibility of Experience Cloud and Creative Cloud storage usage among your team. With the introduction of this new identity type, Adobe is migrating all Adobe IDs (owned by the individual) used for business to the new Business IDs (owned by the organization).

If you're an existing Creative Cloud for enterprise or teams customer, Adobe will migrate all your users on the Admin Console with Adobe IDs to Business IDs. If you're a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID. 

Beginning May 89, 2020, enterprise admins cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a users was a member of multiple organizations before the migration.)
-->

### 管理工具

管理員可以在「管理工具」中檢視所有Experience Cloud使用者及其詳細資料的可排序和可篩選清單。 請參 [閱「管理工具」中的「檢視Experience Cloud使用者」](admin-tool-experience-cloud.md)。

## 登入 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理員不再管理解決方案中的使用者。 Experience Cloud的使用者和產品管理現在會在Admin Console中進行。

**若要登入Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. 輸入 [您的Adobe ID或Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) 和密碼。

Alternatively, from the Experience Cloud menu ( ![](assets/menu-icon.png)), click **[!UICONTROL Administration]** > **[!UICONTROL Launch Admin Console]**.

**相關說明**

[Creative Cloud和Document Cloud的管理使用指南](https://helpx.adobe.com/enterprise/using/users.html) 。 有些資訊與Experience Cloud使用者管理相關，例如管 [理身分類型](https://helpx.adobe.com/enterprise/help/identity.html)。

[登入並管理您的設定檔設定](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0) ，以管理密碼、組織和通知。

## 產品設定檔和群組 {#section_AB50558124D541CF80A0D3D76D35A4BF}

產品設定檔的新增，標誌著解決方案產品與服務先前的管理方式（使用群組）有所轉變。 在「管理控制台」中，權限是以產品設定檔為基礎，而產品設定檔是您可指派給使用者的產品和服務群組。

例如，在Analytics中，您可以設定報告工具的集合，例如分析工作區和報告建立工具，以及報告套裝、量度、維度等。 您可以透過將使用者新增至描述檔，來授與產品描述檔的權限。 See [Assign Analytics access permissions to a product profile](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**相關說明**

[委派有限的管理權限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 使用者和產品權限。

[將 Analytics 存取權指派至產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (請參考本頁)。

**使用者帳戶移轉**

Analytics 使用者 ID 移轉工具可協助 Analytics 管理員將使用者帳戶從 Analytics 使用者管理移轉到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

帳戶移轉功能會分階段向客戶推出。Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). 如果使用者嘗試透過舊版登入頁面 ([!DNL my.omniture.com] 和 [!DNL sc.omniture.com]) 登入，則會被重新導向至 [!DNL experiencecloud.adobe.com]。

**相關說明**

[Analytics使用者ID移轉](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target - 產品設定檔與工作區 {#section_3860AF177C9E4C7E9C390D36A414F353}

在Target中，工作區是產品設定檔。 它可讓組織指派一組特定使用者給一組特定屬性。 工作區有許多地方皆與 Adobe Analytics 報表套裝相似。

請參閱:
* [企業使用者權限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理產品和個人檔案](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* 影片：如 [何在Adobe Admin Console中設定目標工作區](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 促銷活動 - 產品設定檔、租用戶和安全性群組 {#section_09CDF75366444CF5810CF321B7C712F3}

「促 *銷活動* 」中的租用戶會在「管 *理控制台產品* 」頁面中顯示為產品。

*安全性群組* (Security group)會顯示為產品設定檔。

有關安 [全組和將用戶分配給安全組的資訊](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) ，請參閱管理組和用戶。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

「體驗平台啟動」會顯示在「管理控制台」的「產品」頁面上。 您可以在Launch產品設定檔中加入其他解決方案和服務。

如需 [Admin Console中使用者權限的相關資訊](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) ，請參閱使用者管理，並設定啟動特定選項，包括指派設定檔的權限。

## 動態標籤管理 {#section_3A41CF2BD5994B9891537D063571D4ED}

邀請使用者加入動態標籤管理，並指派使用者角色與新增使用者至群組。

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

建立Audience Manager使用者並將其指派給群組。 您也可以檢視限制（特徵、區段、目的地和AlgoModel）。

請參 [閱Audience](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) Manager說明中的管理。

## 管理 Experience Cloud 產品 {#task_16335111C52D40E9BAC73D0699584DBF}

建立產品描述檔並將其指派給權限群組。

當您邀請使用者加入組織時，您可讓使用者存取產品和產品設定檔。 您也可以委派有限的管理權限給使用者。 同樣地，您也可以建立使用者群組，然後將群組新增至產品設定檔以啟用存取權。

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. 按一下&#x200B;**[!UICONTROL 新增設定檔]**。
1. 設定設定檔的詳細資料，然後按一下&#x200B;**[!UICONTROL 下一步]**。
1. 按一下&#x200B;**[!UICONTROL 完成]**。

如需更多協助，請參閱：

* [管理產品和個人檔案](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* [Target說明中的「企業使用者權限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html) 」，以取得詳細資訊。
* 影片：如 [何在Adobe Admin Console中設定目標工作區](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 將 Analytics 存取權指派至產品設定檔 {#task_040673FE3E3E429B9531FBCB8B6A4391}

將 Analytics 報表存取權 (報表套裝、量度、維度等等) 指派至產品設定檔。

例如，您可以建立含有多個 Analytics 工具 ([!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 及 [!UICONTROL Report Builder]) 的產品設定檔、具有特定量度和維度 (包括 eVar) 之權限，並具有區段或計算量度建立等功能。

1. Sign in to the [Admin Console](https://adminconsole.adobe.com/enterprise), then click **[!UICONTROL Products]** (or click your product name).
1. 然後，在產品設定檔中，按一下&#x200B;**[!UICONTROL 權限]** (僅限管理員使用)。
1. 設定設定檔的權限:

| 元素 | 說明 |
|--- |--- |
| 報表套裝 | 啟用特定報表套裝的權限。 |
| 量度 | 啟用流量、轉換、自訂事件、解決方案事件、內容感知等的權限。 |
| 維度 | 在粒度層級自訂使用者存取，包括 eVar、流量報表、解決方案報表和路徑報表。 |
| 報表套裝工具 | 啟用網站服務、報表套裝管理、工具與報表及控制面板項目的使用者權限。 |
| Analytics 工具 | 啟用「一般」項目 (帳單、日誌等)、公司管理、工具、網站服務存取、Report Builder 和 Data Connectors 整合的使用者權限。來自自訂管理控制台類別的公司設定已移至分析工具。 |

## 委派管理角色給使用者 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在「管理控制台」中，您可以將有限的管理權限委派給組織中的其他人。 委派角色可讓使用者管理對使用者的軟體存取權、提供存取部署功能，並可當成支援委派。

例如，您可以：

* 允許您的創意主管授與Creative Cloud的存取權。
* 允許您的行銷主管授與Experience Cloud的存取權。
* 將這兩個角色分開，這樣它們就不能超越彼此的角色。

使用這些角色，您可以同時將管理委派給其他人，而不必提供超出其所需的功能。

1. 在 Admin Console 中，按一下&#x200B;**[!UICONTROL 使用者]**，然後按一下使用者的姓名。
1. 按一下&#x200B;**[!UICONTROL 編輯管理權限]**。
1. 設定使用者的管理權限。
1. 按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以檢閱設定，然後按一下&#x200B;**[!UICONTROL 儲存]**。

## 支援的瀏覽器和系統需求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud中支援的瀏覽器。

Experience Cloud支援的瀏覽器包括：

* [!DNL Microsoft Edge] (Microsoft已 [停止支援](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Internet Explorer 8、9和10。 因此，Adobe不會修正針對這些特定版本Internet Explorer所回報的問題。)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;雖然 Experience Cloud 介面可支援這些瀏覽器，但個別解決方案可能不會支援所有瀏覽器(例如 [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) 不支援 [!DNL Opera]，[Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html) 不支援 [!DNL Safari])。

**解決方案和產品需求**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html)
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
