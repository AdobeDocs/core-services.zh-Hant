---
title: 管理使用者和產品
description: 了解如何登入Admin Console及管理Experience Cloud使用者權限和產品設定檔。 了解如何將管理權限委派給Experience Cloud使用者，以及Experience Cloud的瀏覽器支援。
solution: Admin
index: true
feature: Admin Console
topic: 管理
role: Administrator
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: c32cc6783b53cc6e57bba0810a49038561ac9dcd
workflow-type: tm+mt
source-wordcount: '1168'
ht-degree: 46%

---

# 管理 Experience Cloud 使用者和產品

了解如何登入 Admin Console、管理 Experience Cloud 的使用者權限和產品設定檔以及瀏覽器支援。

>[!IMPORTANT]
>
>以下資訊專門用於Experience Cloud應用程式。 此資訊補充了[《企業管理使用手冊》](https://helpx.adobe.com/tw/enterprise/admin-guide.html)中所有Adobe雲產品的更廣泛管理資訊。

您可以在「管理工具」中檢視所有Experience Cloud使用者及其詳細資訊的可排序和可篩選清單。 請參閱[在管理工具中檢視 Experience Cloud 使用者](admin-tool-experience-cloud.md)。

## 什麼是產品設定檔？ {#section_AB50558124D541CF80A0D3D76D35A4BF}

[!UICONTROL 產] 品設定檔是您可指派給使用者的產品和服務群組。在Experience Cloud中，權限是根據產品的設定檔，而非使用者。 （不過，您可以將管理權限委派給特定使用者。）

例如，在Analytics中，您可以設定報表工具的集合，例如Analysis Workspace和Report Builder，以及報表套裝、量度和維度。 您可以將使用者新增至設定檔，借此將權限授予產品設定檔。

* 請參閱本頁面的[將 Analytics 存取權指派給產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391)。
* 請參閱本頁的[委派管理角色給使用者](#delegate-rights)

## 管理Experience Cloud產品設定檔 {#task_16335111C52D40E9BAC73D0699584DBF}

您可以建立產品設定檔並將其指派至權限群組。

邀請使用者加入組織時，可提供產品和產品設定檔的存取權給使用者。您也可以委派有限的管理權限給使用者。同樣地，您可以建立使用者群組，然後將群組新增至產品設定檔以啟用存取權。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，按一下&#x200B;**[!UICONTROL 「產品」]**。
1. 按一下您的組織名稱。
1. 按一下&#x200B;**[!UICONTROL 「新增設定檔」]**。
1. 配置配置檔案詳細資訊，然後按一下&#x200B;**[!UICONTROL Save]**。

如需詳細資訊(以及Creative Cloud和Document Cloud產品管理的說明)，請參閱[管理使用手冊](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/users.ug.html)中的[身分](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/identity.ug.html)。

**相關說明**

* [管理使用手](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html) 冊中的產品和設定檔。
* Adobe Target 說明中的[企業使用者權限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)會提供詳細資訊。
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/tw/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

<!-- ## What's new in Experience Cloud user management {#concept_06A0A13362F644FB90F947238407637A}

Learn about the latest features in Experience Cloud user and product management.

### Business ID type

Adobe is introducing an identity type called Business ID. This identity type improves the control of user and product management. Adobe is migrating all Adobe IDs (owned by individuals) that are used for business to the new enterprise Business IDs owned by your organization.

If you are an existing Experience Cloud customer, Adobe will migrate all your users with Adobe IDs in the Admin Console to Business IDs. If you are a new enterprise or teams customer, you will add users to the Admin Console using one of the available identity types: Business ID, Enterprise ID, or Federated ID.

What to do

* Your users will need to accept Terms of Use (TOU) changes prior to accounts being migrated to Type2e. 
* Users that belong to multiple organizations might see a Profile Selection screen during the login workflow and need to select the correct one. This ensures that they are logging into the correct organization. (There might be multiple profiles to choose from if a user was a member of multiple organizations before the migration.)

Beginning May 2020, enterprise administrators cannot use the Adobe ID for new organizations created in the Admin Console. Latest: https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=engage&title=Type2e+DX+GTM-->

## 委派管理角色給使用者 {#delegate-rights}

在 Admin Console 中，您可以將有限的管理權限委派給組織中的其他人。委派角色可讓使用者管理軟體對使用者的存取權、提供存取部署功能，且可當成支援委派者。

例如，您可以：

* 允許您的創意總監授予 Creative Cloud 的存取權。
* 允許您的行銷總監授予 Experience Cloud 的存取權。
* 將這兩個角色分開，這樣它們就不能超越彼此的角色。

使用這些角色，您便可同時將管理作業委派給其他人，無需提供超出其所需的功能。

1. 在 Admin Console 中，按一下&#x200B;**[!UICONTROL 「使用者」]**，然後按一下使用者的姓名。

   ![](assets/edit-admin-rights.png)

1. 按一下&#x200B;**[!UICONTROL 「編輯管理權限」]**。

   ![](assets/edit-admin-rights-page.png)

1. 指定使用者的管理權限。
1. 按一下&#x200B;**[!UICONTROL 「儲存」]**。

## 管理Analytics使用者和產品 {#section_97DE101F92CD494AB073893680992F1A}

您可以將Analytics報表存取權（報表套裝、量度、維度等）指派至產品設定檔。

例如，您可以建立包含多個Analytics工具([!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics]和[!UICONTROL Report Builder])的產品設定檔。 這些設定檔包含特定量度和維度（包括eVar）的權限，以及區段或計算量度建立等功能。

1. 登入[Admin Console](https://adminconsole.adobe.com/enterprise)，然後按一下&#x200B;**[!UICONTROL 產品]**。
1. 在[!UICONTROL 產品]頁面上，按一下您的產品，然後按一下，然後按一下&#x200B;**[!UICONTROL 權限]**（僅供管理員使用）。
1. 設定設定檔的權限：

| 元素 | 說明 |
|--- |--- |
| 報表套裝 | 啟用特定報表套裝的權限。 |
| 量度 | 為流量、轉換、自訂事件、解決方案事件、內容感知等項目啟用權限。 |
| 維度 | 在粒度層級自訂使用者存取，包括 eVar、流量報表、解決方案報表和路徑報表。 |
| 報表套裝工具 | 為網站服務、報表套裝管理、工具和報表與儀表板項目啟用使用者權限。 |
| Analytics 工具 | 啟用「一般」項目（帳單、日誌等）、公司管理、工具、網站服務存取、Report Builder和Data Connectors整合的使用者權限。 來自自訂管理控制台類別的公司設定已移至分析工具。 |

<!-- **User Account Migration**

An Analytics user ID migration tool is available to help Analytics administrators migrate user accounts from Analytics User Management to the [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/).

The account migration is being rolled out to customers in phases. Adobe will notify and assist you when it is your time to migrate existing user accounts from **[!UICONTROL Admin Tools]** > **[!UICONTROL User Management]** to the Admin Console.

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experience.adobe.com](https://experience.adobe.com). If users attempt to sign in via legacy logins ([!DNL my.omniture.com], [!DNL sc.omniture.com] and [!DNL experiencecloud.adobe.com]) they are redirected to [!DNL experience.adobe.com].

**Related help**  -->

如需詳細資訊，請參閱[Analytics使用者ID移轉](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=en)

## 管理Adobe Target — 產品設定檔與工作區 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Adobe Target 中，Workspace 是產品設定檔，可讓組織將特定一組使用者指派至特定一組屬性。Workspace 有許多地方與 Adobe Analytics 報表套裝相似。

請參閱：

* [企業使用者權限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [管理產品和設定檔](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 管理Campaign產品設定檔、租用戶和安全性群組 {#section_09CDF75366444CF5810CF321B7C712F3}

行銷活動中的&#x200B;*租用戶*&#x200B;在 Admin Console 的&#x200B;*產品*&#x200B;頁面中會顯示為產品。

*安全群組* (Security group)會顯示為產品設定檔。

有關安全群組和將使用者指派至安全群組的資訊，請參閱[管理群組和使用者](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=en)。

## 管理Experience Platform資料收集（啟動） {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform[!UICONTROL 資料收集]([!UICONTROL Launch])顯示在[!UICONTROL Admin Console]的[!UICONTROL 產品]頁面上。 您可以在 Launch 產品設定檔中加入其他解決方案和服務。

邀請使用者加入 [!UICONTROL Platform Launch] 並指派使用者角色和權限。

請參閱[使用者權限](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html?lang=zh-Hant#admin) ，以取得Admin Console中的使用者權限，以及如何設定Launch專用選項（包括指派設定檔的權限）的相關資訊。

## Experience Manager as a Cloud Service

Adobe企業客戶在Adobe[!UICONTROL Admin Console]中表示為組織。 Experience Manager(AEM)客戶可以使用Adobe[!UICONTROL Admin Console]來管理產品權益和IMS驗證，以Experience Manager為[!UICONTROL Cloud Service]。

請參閱 [AEM as a Cloud Service 的 IMS 支援](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=en)。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

建立 Audience Manager 使用者並將其指派至群組。您也可以檢視限制 (特徵、區段、目的地和 [!DNL AlgoModel])。

請參閱 Audience Manager說明中的[管理](https://experienceleague.adobe.com/docs/dtm/using/admin/users.html?lang=en)。

## 受支援的Experience Cloud

* [!DNL Microsoft® Edge] (Microsoft®已 [停止](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) 支援Internet Explorer 8、9和10。因此，Adobe不會修正針對這些特定版本Internet Explorer所回報的問題。)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：** 雖然Experience Cloud介面可支援這些瀏覽器，但個別應用程式不支援所有瀏覽器。(例如 [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en) 不支援 [!DNL Opera]，而 [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en) 不支援 [!DNL Safari])。

### 解決方案和產品要求

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=en)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
