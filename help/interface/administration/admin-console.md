---
title: 用戶和產品許可證管理
description: 在 Admin Console 中管理 Experience Cloud 應用程式的使用者和產品授權資訊。
application: Experience Cloud
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: c82821c4-aa5d-48ae-8bef-5937fede8db2
TQID: https://experienceleague.adobe.com/ojHy0Am9T1T7Zu5EpR3jLynQ-dotvhcn6usRynb5TXo
product_v2:
  - id: e1971122-7081-4556-9222-8a31bd71800c
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 06923be2a98a9301a3d3e16c47c50cd34f7a05e9
workflow-type: tm+mt
source-wordcount: 747
ht-degree: 7%

---

# 使用者和產品管理

您可以在Adobe[Admin Console](https://adminconsole.adobe.com/enterprise/)中管理用戶和產品許可證。 有關適用於所有Adobe應用程式的常規身份管理幫助，請參閱[企業和團隊管理指南](https://helpx.adobe.com/tw/enterprise/admin-guide.html)。

此頁提供了對Experience Cloud管理員特別有用的資訊，定義了角色，並提供了指向企業指南中常見用戶和產品管理主題的連結。

## Admin Console中的管理角色

該Admin Console提供三個主要管理角色，每個角色具有特定級別的訪問權限和責任：

| 角色 | 說明 |
| ------- | ------- |
| 系統管理員 | 完全訪問 — 管理控制台的所有方面。 <br>關鍵責任： <br><ul><li>添加、刪除和管理用戶。</li><li>分配和撤消產品許可證。</li><li>配置身份和身份驗證設定</li><li>查看和管理開單資訊。</li><li>設定其他管理員和委派角色。</li></ul> **最適合：** IT管理員或團隊負責人監督整個組織的Adobe環境。 |
| 產品管理員 | 特定於產品的管理 — 控制特定Adobe產品的訪問權限。<br>關鍵責任：<ul><li>為特定產品分配和管理許可證。</li><li>建立和管理產品配置檔案。</li><li>添加或刪除分配產品中的用戶。</li></ul>   **最適合：**&#x200B;團隊/用戶管理特定軟體，如Marketo Engage或Adobe Creative Cloud。 |
| 產品配置檔案管理員 | 細粒度角色管理 — 重點管理產品中的用戶組和權限。<br>關鍵責任：<ul><li>建立和管理產品配置檔案。</li><li>在配置式內分配權限和功能訪問。</li><li>在配置檔案中添加或刪除用戶。</li></ul> **最適合：**&#x200B;部門領導或團隊經理，負責監督具有專門需求的較小組。 <br>管理員可以根據組織要求組合角色以獲得更大的靈活性。 |

## Admin ConsoleExperience Cloud

要管理Experience Cloud應用程式的標識和產品許可證，請導航到[Admin Console](https://adminconsole.adobe.com/enterprise/)。

以下是您作為管理員開始Admin Console時可能需要的資源：

### 設定資源

| 幫助連結 | 說明 |
| ------- | ------ |
| [設定標識和單一登錄](https://helpx.adobe.com/tw/enterprise/using/set-up-identity.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Settings]** <br>瞭解如何設定具有不同ID類型的用戶帳戶(使用或不使用單一登錄(SSO))。 為Adobe軟體設定SSO，配置SAML設定，並查看最常見的問題和錯誤。 |
| [通過目錄信任設定組織](https://helpx.adobe.com/tw/enterprise/using/directory-trust.html) | 根據其他組織已聲明的域對用戶進行身份驗證。 有關查找和切換組織的資訊，請參閱[Experience Cloud中的組織](organizations.md)。 |
| [身份驗證設定（企業）](https://helpx.adobe.com/tw/enterprise/using/authentication-settings.html) | Admin Console支援多種密碼保護級別和策略，以確保安全性和安全性。 您可以指定使用密碼保護級別來應用於組織中的所有用戶。 |
| [隱私和安全聯繫人](https://helpx.adobe.com/tw/enterprise/using/security-contacts.html) | Protect您的組織和用戶資料。 如果發生涉及我們軟體解決方案的安全事件，則通知會發送給相應的合規官。 企業的人員角色特定於資料保護、完整性和其他法規遵從性事項。 因此，此類人員的聯繫資訊對於確保在發生安全事件時及時通知至關重要。 |

### 使用者管理

| 幫助連結 | 說明 |
| ------- | ------- |
| [重置您的Adobe ID](https://helpx.adobe.com/tw/account/individual/sign-in-and-security/security-and-recovery/cant-sign-in-to-adobe-account.html) | 註銷，然後按一下&#x200B;**[!UICONTROL Get help signing in]** > **[!UICONTROL Reset your password]**。 |
| [管理多個用戶](https://helpx.adobe.com/tw/enterprise/using/bulk-upload-users.html) | **[!UICONTROL Admin Console]** > **[!UICONTROL Users]** <br>瞭解如何通過CSV批量上載到Admin Console中管理多個用戶。 |
| [標識類型](https://helpx.adobe.com/tw/enterprise/using/identity.html) | 標識類型允許組織對用戶帳戶和資料的不同控制級別。 您選擇的身份模型會影響組織儲存和共用資產的方式。 當Federated ID和Enterprise ID模型由組織建立和管理時，AdobeID由個人建立和管理。 |
| [用戶同步工具](https://helpx.adobe.com/tw/enterprise/using/user-sync.html)&#x200B;(UST) | Adobe用戶同步工具是一種案頭應用程式，用於自動在組織的身份管理系統（如Active Directory）和Adobe Admin Console之間同步用戶資料。 該工具允許管理員跨Adobe產品優化用戶配置、更新和停用。 |
| [查看用戶詳細資訊（管理工具）](admin-tool-experience-cloud.md) | 查看所有Experience Cloud用戶和策略的可排序和可篩選清單，其詳細資訊位於[!UICONTROL Admin Tool]中。 |

### 報告和日誌

| 幫助連結 | 說明 |
| ------- | ------- |
| [審核日誌](https://helpx.adobe.com/tw/enterprise/using/audit-logs.html) | **[!UICONTROL Insights]** > **[!UICONTROL Logs]** > **[!UICONTROL Audit Log]** <br>跟蹤Admin Console中所做的所有更改。 |


## 特定於應用程式的資源

這些連結可幫助您查找特定Experience Cloud應用程式的管理資訊。

<!--
| Application | Link to resource|
| ------- | ------- |
|  [!DNL Analytics] <p>Customer Journey Analytics| [Analytics in the Adobe Admin Console overview](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-console/home) <p>[Administration requirements](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace) |
| [!DNL Audience Manager] | [Audience Manager user migration to Admin Console](https://experienceleague.adobe.com/zh-hant/docs/audience-manager/user-guide/features/administration/admin-console-migration) |
| [!DNL Campaign] v8 |  [Get started with permissions](https://experienceleague.adobe.com/en/docs/campaign/campaign-v8/admin/permissions/gs-permissions) |
| [!DNL Campaign Standard] to [!DNL Campaign v8] | [User access management from Campaign Standard to Campaign V8](https://experienceleague.adobe.com/zh-hant/docs/campaign-web/acs-to-ac/user-management-acs) |
| [!DNL Commerce] | [Configure the Commerce Admin Integration with Adobe ID](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/start/admin/ims/adobe-ims-config) |
| [!DNL Dynamic Media Classic] | [Administration setup](https://experienceleague.adobe.com/zh-hant/docs/dynamic-media-classic/using/setup/administration-setup#user_administration) |
| [!DNL Experience Manager as a Cloud Service] |  [Accessing the Admin Console](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console) |
| [!DNL Experience Platform] <p>[!DNL Data Collection] | [Access control UI overview](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/overview) <p>[Permission management for data collection in Experience Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/permissions)|
| [!DNL GenStudio for Performance Marketing] | [Provision Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning) |
| [!DNL Journey Optimizer] | [Manage users and roles](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/access-control/permissions) |
| [!DNL Journey Optimizer B2B Edition] | [User management](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-b2b/user/admin/user-management) |
|[!DNL  Journey Orchestration] | [Access management](https://experienceleague.adobe.com/zh-hant/docs/journeys/using/starting-with-journeys/access-management) |
| [!DNL Marketo Engage] | [Understanding Marketo Subscription and User Migration to the Adobe Admin Console](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console) |
| [!DNL Marketo Measure] | [Adobe Admin Console Setup](https://experienceleague.adobe.com/zh-hant/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup) |
| [!DNL Mix Modeler] | [Access controls](https://experienceleague.adobe.com/zh-hant/docs/mix-modeler/using/data-governance/access-controls) |
| [!DNL Pass] | [Get started with Account IQ](https://experienceleague.adobe.com/en/docs/pass/aiq-help/get-started) |
| [!DNL Target] | [Administrator first steps](https://experienceleague.adobe.com/zh-hant/docs/target/using/administer/start-target) <p> [User management](https://experienceleague.adobe.com/zh-hant/docs/target/using/administer/manage-users/user-management) |
| [!DNL Workfront] | [Manage users in the Adobe Admin Console](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console) |

-->

* [廣告搜索、社交和Commerce](https://experienceleague.adobe.com/zh-hant/docs/advertising/search-social-commerce/target/user-administration)
* [Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics/admin/admin-console/home)
* [Customer Journey Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-workspace/workspace-faq/frequently-asked-questions-analysis-workspace)
* [Audience Manager](https://experienceleague.adobe.com/zh-hant/docs/audience-manager/user-guide/features/administration/admin-console-migration)
* [Campaign v8](https://experienceleague.adobe.com/zh-hant/docs/campaign/campaign-v8/permissions/gs-permissions)
* [Campaign Standard](https://experienceleague.adobe.com/zh-hant/docs/campaign-web/acs-to-ac/user-management-acs)
* [Commerce](https://experienceleague.adobe.com/zh-hant/docs/commerce-admin/start/admin/ims/adobe-ims-config)
* [Dynamic Media Classic](https://experienceleague.adobe.com/zh-hant/docs/dynamic-media-classic/using/setup/administration-setup#user_administration)
* [Experience Manager as a Cloud Service](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-cloud-service/content/onboarding/journey/admin-console)
* [Experience Platform](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/overview)和[資料收集](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/permissions)
* [GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/intro/product-provisioning)
* [JOURNEY OPTIMIZER](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/access-control/permissions)
* [Journey OptimizerB2B版](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-b2b/user/admin/user-management)
* [Journey Orchestration](https://experienceleague.adobe.com/zh-hant/docs/journeys/using/starting-with-journeys/access-management)
* [MARKETO ENGAGE](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console)
* [MARKETO MEASURE](https://experienceleague.adobe.com/zh-hant/docs/marketo-measure/using/configuration-and-setup/getting-started-with-marketo-measure/adobe-admin-console-setup)
* [MIX MODELER](https://experienceleague.adobe.com/zh-hant/docs/mix-modeler/using/data-governance/access-controls)
* [Target](https://experienceleague.adobe.com/zh-hant/docs/target/using/administer/start-target)
* [Workfront](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/administration-and-setup/add-users/create-manage-users/admin-console)

[企業和團隊管理指南](https://helpx.adobe.com/tw/enterprise/admin-guide.html)記錄了所有Adobe應用程式的大多數管理員控制台幫助。

