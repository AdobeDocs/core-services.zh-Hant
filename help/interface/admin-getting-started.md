---
title: 管理使用者和產品
description: 瞭解如何登錄Admin Console並管理Experience Cloud用戶權限和產品配置檔案。 了解如何委派管理權限給 Experience Cloud 使用者以及有關瀏覽器對 Experience Cloud 的支援。
solution: Admin
index: true
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: af9eda5b-d984-44b7-a7b3-52dfc4e03d8f
source-git-commit: 84822a497a3138e4f10a383e54ae2cc13cc4bf77
workflow-type: tm+mt
source-wordcount: '1565'
ht-degree: 69%

---

# 管理 Experience Cloud 使用者和產品

瞭解如何登錄Admin Console、管理Experience Cloud用戶權限和產品配置檔案以及瀏覽器支援。

>[!IMPORTANT]
>
>以下是 Experience Cloud 應用程式專屬資訊。 這項資訊可補充所有 Adobe 雲端產品的[企業版管理使用手冊](https://helpx.adobe.com/tw/enterprise/admin-guide.html)中更廣泛的管理資訊。

您可以在管理工具中檢視所有 Experience Cloud 使用者及其詳細資訊，且可將清單加以排序及篩選。 請參閱「[在管理工具中檢視 Experience Cloud 使用者](admin-tool-experience-cloud.md)」。

## Experience Cloud用戶身份驗證（計畫遷移）{#migration}

從2022年2月開始，Adobe正在更新其檔案管理系統，以便各組織能夠更好地管理個人檔案的業務權利。 因此，具有個人配置檔案(與單個Adobe ID（類型1）相對應)的所有用戶都將遷移到新的業務配置檔案。 此配置檔案與 _業務ID_ （類型2e）。

請參閱 [Adobe Admin Console上的身份類型](https://helpx.adobe.com/tw/enterprise/using/identity.html) 的子菜單。

### 遷移過程

遷移時間到時，組織管理員將在遷移前30天收到通知電子郵件。 此電子郵件將包括您的遷移日期。

* 遷移計畫在晚上10點之間進行。 — 上午6:00，根據組織的主要時區或週末。
* 在遷移期間，Experience Cloud應用程式可能無法訪問15分鐘，Admin Console可能無法訪問30分鐘。 否則，此遷移將是無縫的。

### 遷移後的更改

Admin Console

* 具有多個帳戶的管理員登錄時可能會看到配置檔案選擇器 [!UICONTROL Admin Console]。
* 單個Adobe ID用戶將更新為業務ID。
* 業務ID目錄將添加到 **[!UICONTROL 設定]** > **[!UICONTROL 身份]** > **[!UICONTROL 目錄]**。

   ![Admin Console標識 — 業務ID](assets/identity-home.png)

### 遷移後登錄

您的登錄體驗不會隨此更新而改變：

1. 登錄位置 `experience.adobe.com` 使用相同的憑據。

1. 將建立與業務ID關聯的新配置檔案。 系統將提示您 **[!UICONTROL 立即加入]** 或 **[!UICONTROL 跳過]**。

1. 選擇其中一個選項可帶來現有登錄頁體驗。

1. Adobe配置檔案與每個業務計畫相關聯，並提供了組織從其他Adobe雲產品(Creative Cloud和Document Cloud)建立的資產的能力。

有關詳細資訊，請參見 [介紹Adobe配置檔案](https://helpx.adobe.com/enterprise/kb/introducing-adobe-profiles.html)。

## 什麼是產品配置檔案？ {#section_AB50558124D541CF80A0D3D76D35A4BF}

_[!UICONTROL 產品描述檔]_&#x200B;是您可以指派給使用者的產品和服務群組。 在 Experience Cloud 中，權限取決於產品描述檔，而不是使用者。 (然而，您可以委派管理權限給特定使用者。)

例如，在 Analytics 中，您可以設定一系列報表工具，例如 Analysis Workspace 和 Report Builder，以及報表套裝、量度和維度。 您可以通過向配置檔案添加用戶來授予對產品配置檔案的權限。

* 請參閱 [將分析訪問權限分配給產品配置檔案](admin-getting-started.md#task_040673FE3E3E429B9531FBCB8B6A4391) 在此頁上。
* 請參閱本頁面的「[委派管理角色給使用者](#delegate-rights)」

## 管理Experience Cloud產品配置檔案 {#task_16335111C52D40E9BAC73D0699584DBF}

您可以建立產品配置檔案並將其分配給權限組。

在邀請用戶加入組織時，您可以授予用戶對產品和產品配置檔案的訪問權限。 您也可以委派有限的管理權限給使用者。同樣，您可以建立用戶組，然後將組添加到產品配置檔案中以啟用訪問。

1. 在 [Admin Console](https://adminconsole.adobe.com/enterprise/) 中，選取「**[!UICONTROL 產品]**」。
1. 選取您的組織名稱。
1. 選取「**[!UICONTROL 新描述檔]**」。
1. 設定描述檔詳細資料，然後選取「**[!UICONTROL 儲存]**」。

如需詳細資訊 (以及有關 Creative Cloud 和 Document Cloud 產品管理的說明)，請參閱「[身分](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/identity.ug.html)」(在[管理使用手冊](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/users.ug.html)中)。

**相關說明**

* 管理使用手冊中的「[管理產品和描述檔](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)」。
* Adobe Target 說明中的「[企業使用者權限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=zh-Hant)」會提供詳細資訊。
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/tw/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 委派管理角色給使用者 {#delegate-rights}

在 Admin Console 中，您可以將有限的管理權限委派給組織中的其他人。委派角色可讓使用者管理軟體對使用者的存取權、提供存取部署功能，且可當成支援委派者。

例如，您可以：

* 允許您的創意總監授予 Creative Cloud 的存取權。
* 允許您的行銷總監授予 Experience Cloud 的存取權。
* 將這兩個角色分開，這樣才不會超越彼此的角色。

使用這些角色，您便可同時將管理作業委派給其他人，無需提供超出其所需的功能。

1. 在 Admin Console 中，選取「**[!UICONTROL 使用者]**」，然後選取使用者的名稱。

   ![Admin Console 中的管理員權限](assets/edit-admin-rights.png)

1. 選取「**[!UICONTROL 編輯管理員權限]**」。

   ![在 Admin Console 中編輯管理員權限](assets/edit-admin-rights-page.png)

1. 指定使用者的管理權限。
1. 選取「**[!UICONTROL 儲存]**」。

## 管理 Analytics 使用者和產品 {#section_97DE101F92CD494AB073893680992F1A}

您可以將分析報告訪問權限（報告套件、度量、維度等）分配給產品配置檔案。

例如，您可以建立包含多個分析工具的產品配置檔案([!UICONTROL Analysis Workspace]。 [!UICONTROL 報告和分析], [!UICONTROL Report Builder])。 這些描述檔包含特定量度和維度 (包括 eVar) 的權限，以及類似區段或建立計算量度等功能。

1. 登入 [Admin Console](https://adminconsole.adobe.com/enterprise)，然後選取「**[!UICONTROL 產品]**」。
1. 在「[!UICONTROL 產品]」頁面上，選取您的產品，然後選取「**[!UICONTROL 權限]**」(僅供管理員使用)。
1. 設定個人資料的權限：

| 元素 | 說明 |
|--- |--- |
| 報表套裝 | 啟用特定報表套裝的權限。 |
| 量度 | 為流量、轉換、自訂事件、應用程式事件、內容感知等項目啟用權限。 |
| 維度 | 在粒度層級自訂使用者存取，包括 eVar、流量報表、應用程式報表和路徑報表。 |
| 報表套裝工具 | 為網站服務、報表套裝管理、工具和報表與儀表板項目啟用使用者權限。 |
| Analytics 工具 | 啟用「一般」項目 (帳單、日誌等)、公司管理、工具、Web 服務存取、Report Builder 和資料連接器整合的使用者權限。 「自訂 Admin Console」類別中的公司設定已移至 Analytics 工具。 |

**使用者帳戶移轉**

Analytics 使用者 ID 移轉工具可協助 Analytics 管理員將使用者帳戶從 Analytics 使用者管理移轉到 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise/)。

帳戶移轉功能會分階段向客戶推出。Adobe 會在您需要進行移轉時通知您，並協助您從&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 使用者管理]**&#x200B;將現有使用者帳戶移轉到 Admin Console。

移轉後，使用者可以在 [experience.adobe.com](https://experience.adobe.com) 使用他們的 Adobe ID (或 Enterprise ID) 登入，並針對其 Experience Cloud 應用程式和服務進行驗證。 如果使用者嘗試透過舊的登入進行登入 ([!DNL my.omniture.com]、[!DNL sc.omniture.com] 和 [!DNL experiencecloud.adobe.com])，則會被重新導向 [!DNL experience.adobe.com]。

**相關說明**

如需詳細資訊，請參閱「[Analytics 使用者 ID 移轉](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/migrate-users/c-migration-tool.html?lang=zh-Hant)」。

## 管理Adobe Target — 產品配置檔案與工作區 {#section_3860AF177C9E4C7E9C390D36A414F353}

在Adobe Target，工作區是產品配置檔案。 可讓組織將特定一組使用者指派至特定一組屬性。Workspace 有許多地方與 Adobe Analytics 報表套裝相似。

請參閱：

* [企業使用者權限](https://experienceleague.adobe.com/docs/target/using/administer/manage-users/enterprise/property-channel.html?lang=en)
* [管理產品和個人資料](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-products.ug.html)
* 影片：[如何在 Adobe Admin Console 中設定 Adobe Target Workspace](https://helpx.adobe.com/target/kb/how-to-configure-target-workspaces-in-adobe-admin-console0.html)

## 管理市場活動產品配置檔案、租戶和安全組 {#section_09CDF75366444CF5810CF321B7C712F3}

行銷活動中的&#x200B;*租用戶*&#x200B;在 Admin Console 的&#x200B;*產品*&#x200B;頁面中會顯示為產品。

*安全組* 顯示為產品配置檔案。

有關安全群組和將使用者指派至安全群組的資訊，請參閱[管理群組和使用者](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/users-and-security/managing-groups-and-users.html?lang=zh-Hant)。

## 管理 Experience Platform Data Collection (Launch) {#section_F2DA6778DD2D48AA8F794041971EE6B1}

Experience Platform [!UICONTROL Data Collection] ([!UICONTROL Launch]) 會顯示在 [!UICONTROL Admin Console] 的「[!UICONTROL 產品]」頁面上。 您可以在產品發佈配置檔案中包括其他應用程式和服務。

邀請使用者加入 [!UICONTROL Platform Launch] 並指派使用者角色和權限。

如需 Admin Console 中的使用者權限，以及設定 Launch 專用選項 (包括指派描述檔的權限) 的相關資訊，請參閱「[使用者權限](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html?lang=zh-Hant)」。

## Experience Manager as a Cloud Service

Adobe 企業客戶在 Adobe [!UICONTROL Admin Console] 中會呈現為「組織」。 Experience Manager 客戶可使用 Adobe [!UICONTROL Admin Console] 管理其產品權益以及 Experience Manager as a [!UICONTROL Cloud Service] 的 IMS 驗證。

請參閱「[Experience Manager as a Cloud Service 的 IMS 支援](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/security/ims-support.html?lang=zh-Hant)」。

## Audience Manager {#section_C31E3FA8A1E14463B1B3E07235F1983C}

建立 Audience Manager 使用者並將其指派至群組。您也可以檢視限制 (特徵、區段、目的地和 [!DNL AlgoModel])。

請參閱 Audience Manager 說明中的「[管理](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/administration/administration-overview.html?lang=zh-Hant)」。

## Experience Cloud 中支援的瀏覽器

* [!DNL Microsoft® Edge] (Microsoft® 已[終止支援](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Internet Explorer 8、9 和 10。 有鑑於此，Adobe 將不會修正針對這些特定 Internet Explorer 版本所回報的問題。)
* [!DNL Google Chrome]
* [!DNL Firefox]
* [!DNL Safari]
* [!DNL Opera]

**注意：**&#x200B;雖然 Experience Cloud 介面可支援這些瀏覽器，但個別應用程式並非所有瀏覽器都有支援。 (例如 [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=zh-Hant) 不支援 [!DNL Opera]，而 [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=zh-Hant) 不支援 [!DNL Safari])。

### 解決方案和產品要求

* [Analytics](https://experienceleague.adobe.com/docs/analytics/admin/sys-reqs.html?lang=en)
* [Report Builder](https://experienceleague.adobe.com/docs/analytics/analyze/report-builder/report-builder-setup/system-requirements.html?lang=zh-Hant)
* [Adobe Target](https://experienceleague.adobe.com/docs/target/using/implement-target/before-implement/supported-browsers.html?lang=en)
