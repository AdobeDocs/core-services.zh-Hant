---
title: 使用者和產品授權管理
description: 在Admin Console中管理Experience Cloud應用程式的使用者和產品授權。
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
source-git-commit: 77841faeb5b005e4913408edb3e9cfbbdfc8961d
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 5%

---

# 使用者管理和產品授權

本頁提供Experience Cloud管理員專屬資訊，以及一般使用者和產品管理檔案的連結。

如需適用於所有Adobe應用程式的一般身分管理說明，請參閱[企業和團隊管理指南](https://helpx.adobe.com/tw/enterprise/admin-guide.html)。

## Admin Console中的管理角色

Admin Console提供三種主要管理角色，各具有特定存取層級和職責：

| 角色 | 說明 |
| ------- | ------- |
| 系統管理員 | 完整存取 — 管理主控台的所有層面。 <br>主要職責： <br><ul><li>新增、移除和管理使用者。</li><li>指派及撤銷產品授權。</li><li>設定身分和驗證設定</li><li>檢視及管理帳單資訊。</li><li>設定其他管理員和委派角色。</li></ul> **最適合的：** IT管理員或團隊負責人負責監督整個組織的Adobe環境。 |
| 產品管理員 | 產品特定管理 — 控制特定Adobe產品的存取權和許可權。<br>主要職責：<ul><li>指派和管理特定產品的授權。</li><li>建立和管理產品設定檔。</li><li>在指派的產品中新增或移除使用者。</li></ul>   **最適合於：**&#x200B;管理特定軟體(如Marketo Engage或Adobe Creative Cloud)的團隊/使用者。 |
| 產品設定檔管理員 | 精細角色管理 — 著重於管理產品內的使用者群組和許可權。<br>主要職責：<ul><li>建立和管理產品設定檔。</li><li>在設定檔中指派許可權和功能存取權。</li><li>在設定檔中新增或移除使用者。</li></ul> **最適合：**&#x200B;部門主管或團隊經理，負責監督有特殊需求的小型群組。 根據組織需求，<br>管理員可以合併角色，以獲得更大的彈性。 |

## 適用於Experience Cloud的Admin Console

若要管理Experience Cloud應用程式的身分和產品授權，請導覽至[Admin Console](https://adminconsole.adobe.com/enterprise/)。

以下是您在Admin Console中作為管理員快速入門時可能需要的資源：

### 設定資源

| 說明連結 | 說明 |
| ------- | ------ |
| [設定身分和單一登入](https://helpx.adobe.com/tw/enterprise/using/set-up-identity.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL 設定]** <br>瞭解如何設定包含或不包含單一登入(SSO)之不同ID型別的使用者帳戶。 為Adobe軟體設定SSO、設定SAML設定，並處理最常見的問題和錯誤。 |
| [透過目錄信任設定組織](https://helpx.adobe.com/enterprise/using/directory-trust.html) | 針對其他組織已宣告的網域驗證您的使用者。 如需尋找和切換組織的相關資訊，請參閱[Experience Cloud中的組織](organizations.md)。 |
| [驗證設定（企業）](https://helpx.adobe.com/enterprise/using/authentication-settings.html) | Admin Console支援數個密碼保護層級和原則，以確保安全性和安全性。 您可以指定使用密碼保護層級，以套用至整個組織的所有使用者。 |
| [隱私權與安全性連絡人](https://helpx.adobe.com/enterprise/using/security-contacts.html) | 保護您組織和使用者的資料。 如果發生與我們的軟體解決方案有關的安全性事件，系統會將通知傳送給適當的合規專員。 企業擁有專門負責資料保護、完整性和其他規範事務的人員。 因此，這類人員的聯絡資訊非常重要，有助於確保在發生安全性事件時能及時通知。 |

### 使用者管理

| 說明連結 | 說明 |
| ------- | ------- |
| [管理多個使用者](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL 使用者]** <br>瞭解如何透過CSV大量上傳至Admin Console來管理多個使用者。 |
| [身分型別](https://helpx.adobe.com/tw/enterprise/using/identity.html) | 身分型別可讓組織以不同層級控制使用者的帳戶和資料。 您選擇的身分模型會影響貴組織儲存和共用資產的方式。 雖然Federated ID和Enterprise ID模型是由組織建立和管理的，但Adobe ID是由個人建立和管理的。 |
| [使用者同步工具](https://helpx.adobe.com/enterprise/using/user-sync.html) (UST) | Adobe使用者同步工具是案頭應用程式，用來在組織的身分管理系統（例如Active Directory）與Adobe Admin Console之間自動同步使用者資料。 此工具可讓管理員簡化跨Adobe產品的使用者布建、更新和停用。 |
| [檢視使用者詳細資訊（管理工具）](admin-tool-experience-cloud.md) | 檢視所有Experience Cloud使用者和原則的可排序和可篩選清單，其中包含[!UICONTROL 管理工具]中的詳細資料。 |

### 報告和記錄

| 說明連結 | 說明 |
| ------- |------- |
| [稽核記錄](https://helpx.adobe.com/enterprise/using/audit-logs.html) | **[!UICONTROL 深入分析]** > **[!UICONTROL 記錄檔]** > **[!UICONTROL 稽核記錄檔]** <br>追蹤在Admin Console中所做的所有變更。 |


## 應用程式特定資源

這些連結可協助您尋找特定Experience Cloud應用程式的管理資訊。

<!-- | Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/en/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

 -->

* [Analytics](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/zh-hant/docs/campaign/campaign-v8/admin/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/en/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/en/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/en/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/ui/overview)和[資料彙集](https://experienceleague.adobe.com/en/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [Journey Optimizer](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/permissions)
* [Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/en/docs/journeys/using/starting-with-journeys/access-management)
* [Marketo Engage](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [Marketo Measure](https://experienceleague.adobe.com/en/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [Mix Modeler](https://experienceleague.adobe.com/en/docs/mix-modeler/using/data-governance/access-controls)
* [Adobe Pass](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started)
* [Target](https://experienceleague.adobe.com/en/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)

所有Adobe應用程式的大部分Admin Consol說明都記錄在[企業和團隊管理指南](https://helpx.adobe.com/tw/enterprise/admin-guide.html)中。
