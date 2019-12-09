---
description: 瞭解如何登入 Admin Console 以及管理 Experience Cloud 的使用者權限和產品設定檔。
keywords: core services
seo-description: 瞭解如何登入 Admin Console 以及管理 Experience Cloud 的使用者權限和產品設定檔。
seo-title: 管理 Experience Cloud 使用者和產品
solution: Marketing Cloud
title: 管理 Experience Cloud 使用者和產品
uuid: aea4e4c3-f543-4e8d-b553-d838418477d6
translation-type: tm+mt
source-git-commit: ae97db27349940a8df7ee2ba6678683f57585678

---


# 管理 Experience Cloud 使用者和產品 {#topic_3FCB4099640647E3B2411ADBFCE81909}

瞭解如何登入 Admin Console 以及管理 Experience Cloud 的使用者權限和產品設定檔。

>[!IMPORTANT]
>
>Admin Console 中的使用者管理引進了新的詞語、介面和導覽。下列資訊說明了這些變更，並提供額外說明資源的連結，有助於補充所有 Adobe 雲端產品的[企業版管理指南](https://helpx.adobe.com/enterprise/managing/user-guide.html)之資訊。

## Experience Cloud 使用者管理的新功能 {#concept_06A0A13362F644FB90F947238407637A}

瞭解 Experience Cloud 使用者管理中的最新功能。

## 登入 Admin Console {#section_705072FD4EBE4B70BC69EC81F2BB8669}

管理員不再於解決方案中管理使用者。現在，管理員會透過 Admin Console 進行 Experience Cloud 的使用者和產品管理。

**若要登入 Admin Console**

1. Navigate to [https://adminconsole.adobe.com/enterprise/](https://adminconsole.adobe.com/enterprise/#).
1. 輸入您的 [Adobe ID 或 Enterprise ID](https://helpx.adobe.com/enterprise/help/identity.html) 和密碼。

或者，從 Experience Cloud 功能表 ( ![](assets/menu-icon.png)) 按一下&#x200B;**[!UICONTROL 管理]** &gt; **[!UICONTROL 啟動 Admin Console]**。

**相關說明**

Creative Cloud 和 Document Cloud 的[管理員使用手冊](https://helpx.adobe.com/enterprise/using/users.html)。某些資訊與 Experience Cloud 使用者管理相關，例如[管理身份類型](https://helpx.adobe.com/enterprise/help/identity.html)。

[登入並管理您的設定檔設定](../admin-getting-started/getting-started-experience-cloud.md#topic_AC564B6795334DE39359ADD87F52F2E0)以管理密碼、組織和通知。

## 產品設定檔和群組 {#section_AB50558124D541CF80A0D3D76D35A4BF}

加入產品設定檔改變了解決方案產品和服務過往的管理方式 (透過群組)。在 Admin Console 中，權限依據產品設定檔 (即您可以指派至使用者的產品和服務群組) 來劃分。

例如在 Analytics 中，您可以設定報表工具集合，例如 Analysis Workspace 和 Report Builder 以及報表套裝、量度、維度等等。您可以將使用者新增至設定檔，藉此授與他們權限。請參閱[將 Analytics 存取權指派至產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391).

**相關說明**

[委派有限的管理權限](../admin-getting-started/admin-getting-started.md#task_3A072C4AA9734BC59FFA7E015271BC7E)

## Analytics {#section_97DE101F92CD494AB073893680992F1A}

在 Admin Console 中管理 Analytics 使用者和產品權限。

[將 Analytics 存取權指派至產品設定檔](../admin-getting-started/admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) (請參考本頁)。

**使用者帳戶移轉**

Analytics 使用者 ID 移轉工具可協助 Analytics 管理員將使用者帳戶從 Analytics 使用者管理移轉到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

帳戶移轉功能會分階段向客戶推出。Adobe 會在您需要進行移轉時通知您，並協助您從&#x200B;**[!UICONTROL 管理工具]** &gt; **[!UICONTROL 使用者管理]**&#x200B;將現有使用者帳戶移轉到 Admin Console。

After the migration, users sign in using their Adobe ID (or Enterprise ID) and authenticate to their Experience Cloud solutions and services at [experiencecloud.adobe.com](https://experiencecloud.adobe.com). 如果使用者嘗試透過舊版登入頁面 ([!DNL my.omniture.com] 和 [!DNL sc.omniture.com]) 登入，則會被重新導向至 [!DNL experiencecloud.adobe.com]。

**相關說明**

[Analytics 使用者 ID 移轉](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)

## Target - 產品設定檔與工作區 {#section_3860AF177C9E4C7E9C390D36A414F353}

在 Target 中，工作區即產品設定檔，可讓組織將特定一組使用者指派至特定一組屬性。工作區有許多地方皆與 Adobe Analytics 報表套裝相似。

請參閱:
* [企業使用者權限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)
* [管理產品和設定檔](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* 影片: [如何在 Adobe Admin Console 設定 Target 工作區](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 促銷活動 - 產品設定檔、租用戶和安全性群組 {#section_09CDF75366444CF5810CF321B7C712F3}

行銷活動中的&#x200B;*租用戶*&#x200B;在 Admin Console 的產品頁面上會顯示為&#x200B;*產品*。

*安全性群組*&#x200B;會顯示為產品設定檔。

有關安 [全組和將用戶分配給安全組的資訊](https://helpx.adobe.com/campaign/standard/administration/using/managing-groups-and-users.html) ，請參閱管理組和用戶。

## Experience Platform Launch {#section_F2DA6778DD2D48AA8F794041971EE6B1}

「Launch，由 Adobe 提供」會顯示在 Admin Console 的產品頁面上。您可以在 Launch 產品設定檔上包含其他解決方案和核心服務。

See [User Management](https://docs.adobelaunch.com/launch-reference/administration/user-permissions) for information about user permissions in the Admin Console and set up Launch-specific options, including assigning rights to profiles.

## 動態標籤管理 {#section_3A41CF2BD5994B9891537D063571D4ED}

邀請使用者加入動態標籤管理，並指派使用者角色與新增使用者至群組。

See [Users and Permissions](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) for information about how to invite users to Dynamic Tag Management and assign user roles and add users to groups.

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

建立 Audience Manager 使用者並將其指派至群組。您也可以檢視限制 (特徵、區段、目的地和 AlgoModel)。

請參 [閱Audience](https://docs.adobe.com/content/help/en/dtm/using/admin/users.html) manager說明中的管理。

## 管理 Experience Cloud 產品 {#task_16335111C52D40E9BAC73D0699584DBF}

建立產品設定檔並將其指派至權限群組。

當您邀請使用者加入組織時，您可以向使用者授與產品和產品設定檔的存取權。您也可以委派有限的管理權限給使用者。同樣的，您可以建立使用者群組，然後新增群組至產品設定檔以啟用存取權。

1. In the [Admin Console](https://adminconsole.adobe.com/enterprise/), click **[!UICONTROL Products]**.
1. 按一下&#x200B;**[!UICONTROL 新增設定檔]**。
1. 設定設定檔的詳細資料，然後按一下&#x200B;**[!UICONTROL 下一步]**。
1. 按一下&#x200B;**[!UICONTROL 完成]**。

您可以在以下地方找到更多說明:

* [管理產品和設定檔](https://helpx.adobe.com/enterprise/using/manage-products-and-profiles.html)
* 請參閱 Target 說明中的[企業使用者權限](https://docs.adobe.com/content/help/en/target/using/administer/manage-users/enterprise/property-channel.html)以瞭解更多資訊。
* 影片: [如何在 Adobe Admin Console 設定 Target 工作區](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 將 Analytics 存取權指派至產品設定檔 {#task_040673FE3E3E429B9531FBCB8B6A4391}

將 Analytics 報表存取權 (報表套裝、量度、維度等等) 指派至產品設定檔。

例如，您可以建立含有多個 Analytics 工具 ([!UICONTROL Analysis Workspace]、[!UICONTROL Reports &amp; Analytics] 及 [!UICONTROL Report Builder]) 的產品設定檔、具有特定量度和維度 (包括 eVar) 之權限，並具有區段或計算量度建立等功能。

1. 登入 [Admin Console](https://adminconsole.adobe.com/enterprise)，然後按一下&#x200B;**[!UICONTROL 產品]** (或按一下您的產品名稱)。
1. 然後，在產品設定檔中，按一下&#x200B;**[!UICONTROL 權限]** (僅限管理員使用)。
1. 設定設定檔的權限:

| 元素 | 說明 |
|--- |--- |
| 報表套裝 | 對特定報表套裝啟用權限。 |
| 量度 | 為流量、轉換、自訂事件、解決方案事件、內容感知等等啟用權限。 |
| 維度 | 在粒度層級自訂使用者存取，包括 eVar、流量報表、解決方案報告和路徑報告。 |
| 報表套裝工具 | 為網頁服務、報表套裝管理、工具和報告及控制面板項目啟用使用者權限。 |
| Analytics 工具 | 啟用「一般」項目 (帳單、日誌等)、公司管理、工具、網站服務存取、Report Builder 和 Data Connectors 整合的使用者權限。來自自訂管理控制台類別的公司設定已移至分析工具。 |

## 委派管理角色給使用者 {#task_3A072C4AA9734BC59FFA7E015271BC7E}

在 Admin Console 中，您可以將有限的管理權限委派給組織的其他使用者。受委派角色可讓使用者管理一般使用者的軟體存取權、提供存取部署功能，以及支援委派。

例如，您可以:

* 可讓您的創意總監授與 Creative Cloud 的存取權。
* 可讓您的行銷總監授予 Experience Cloud 的存取權。
* 將這兩個角色分開，可避免他們干涉彼此的職責。

使用這些角色可同時委派管理能力給其他人，但又無需提供過多功能給他們。

1. 在 Admin Console 中，按一下&#x200B;**[!UICONTROL 使用者]**，然後按一下使用者的姓名。
1. 按一下&#x200B;**[!UICONTROL 編輯管理權限]**。
1. 設定使用者的管理權限。
1. 按一下&#x200B;**[!UICONTROL 下一步]**&#x200B;以檢閱設定，然後按一下&#x200B;**[!UICONTROL 儲存]**。

## 支援的瀏覽器和系統需求 {#concept_CDC4371EB9BF433E9534F8716DC8A088}

Experience Cloud 中支援的瀏覽器。

**Experience Cloud 核心服務**

* Microsoft 的最新 Internet Explorer。(Microsoft 即將[停止支援](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Internet Explorer 8、9 和 10。有鑑於此，Adobe 將不修正針對這些特定版本 Internet Explorer 所回報的問題。)
* Google Chrome
* Mozilla Firefox
* Apple Safari

**解決方案和產品需求**

* [Analytics](https://docs.adobe.com/content/help/en/analytics/admin/sys-reqs.html) （包括Adobe Social）
* [Report Builder](https://docs.adobe.com/content/help/en/analytics/analyze/report-builder/report-builder-setup/system-requirements.html)
* [Adobe Target](https://docs.adobe.com/help/en/target/using/implement-target/before-implement/supported-browsers.html)
