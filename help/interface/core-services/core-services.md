---
description: 實作 Experience Cloud 並成為管理員。此程序可針對客戶屬性和對象等核心服務功能，將您的解決方案現代化。
keywords: core services;customer attributes
seo-description: 實作 Experience Cloud 並成為管理員。此程序可針對客戶屬性和對象等核心服務功能，將您的解決方案現代化。
seo-title: 啟用核心服務的 Experience Cloud 解決方案
solution: Experience Cloud
title: 啟用核心服務的解決方案
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: 02b0163b95c24eb58bf2379c3e0d9f5f31c40925

---


# 啟用核心服務的解決方案

針對現有客戶，瞭解如何最新化解決方案實作並實作Experience Cloud，讓您能夠使用客戶屬性和受眾等功能。 若要完成此作業，您將：

1. [加入 Experience Cloud 並成為管理員](#section_2423F0BD3DF642658103310EE5EA6154)
1. [實作Experience Cloud ID服務](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [將報表套裝對應至Experience cloud組織](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [更新您的Analytics appMeasurement代碼](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [更新您的Adobe target實作](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [確認核心服務實作](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理使用者和產品](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [開始使用核心服務](#section_960C06093623462E8EA247B3E97274A1)

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## 步驟 1.加入 Experience Cloud 並成為管理員 {#section_2423F0BD3DF642658103310EE5EA6154}

若要加入 Experience Cloud，您必須先執行下列動作:

![](assets/step1_icon.png) 確定您具有適當的 Adobe Analytics 或 Adobe Target SKU。

* **Adobe Analytics:** Standard 或 Premium 版 (非舊版 SiteCatalyst SKU)。
* **Adobe Target:** Standard 或 Premium 版。

>[!NOTE]
>
>若為Target，請從mbox.js移轉至at.js。 請參 [閱從at.js 1升級。 x至at.js 2。 x](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/upgrading-from-atjs-1x-to-atjs-20.html).

![](assets/step2_icon.png)最實化實作，並取得已佈建的管理員。

1. 請依以下[部署 Experience Cloud ID 服務](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)的步驟進行。
1. 請聯絡帳戶管理，並開始 Experience Cloud 的佈建程序。

![](assets/step3_icon.png)[!UICONTROL  在 Admin Console 中管理使用者和產品].

**管理員存取**

After you are an administrator, you can log in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).

您會在 Experience Cloud 功能表導覽中看到&#x200B;**[!UICONTROL 管理]**&#x200B;連結。

如需說明，請參閱 [Experience Cloud 的使用者和產品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**使用者存取權**

若要登入 Experience Cloud，您的使用者必須:

1. 有 Adobe ID。
1. Sign in at [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. 屬於對應至企業群組的解決方案群組。
1. 視需要將他們的解決方案帳戶連結至各自的 Adobe ID (如下所述)。

![](assets/step4_icon.png) 選用: 連結現有的使用者帳戶。

Most likely, you have users who are already members of solution groups, such an Analytics group that you previously managed in [!UICONTROL Analytics] > [!UICONTROL Admin Tools].

當您將這些群組對應至 Experience Cloud 企業群組時，這些使用者必須以手動方式將他們的解決方案帳戶認證連結至其 Adobe ID。

請參閱[在 Experience Cloud 連結帳戶](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> 在企業和解決方案群組對應後，新使用者會自動產生連結。(系統會自動建立解決方案認證並連結至其 Adobe ID)。

下列章節說明如何最新化實作。最新化實作可以啟用 Experience Cloud 中的核心服務。

## 步驟 2.使用 [!UICONTROL Experience Platform Launch] 或動態標 [!UICONTROL 簽管理實]施 [!UICONTROL Experience Cloud ID] 服務 {#section_3C9F6DF37C654D939625BB4D485E4354}

Experience Cloud [!UICONTROL ID服務提供] ，以便跨解決方案整合。 它提供跨網域訪客身分識別，以及根據透過客戶屬性上傳的CRM資料，跨裝置／瀏覽器定位和個 [!UICONTROL 人化的路徑]。

啟用Experience cloud核心服務最簡單的方法，就是透過 [Experience Platform Launch中的](https://docs.adobe.com/content/help/en/launch/using/implement/solutions/idservice-save.html) Experience Cloud ID服務擴充功能，或透過動態標籤管理中的ECID工具，自動為Analytics和Target啟用Experience Cloud 。 （強烈建議使用Experience Platform Launch。）

![](assets/menu-activation-shell.png)

For complete Experience Cloud ID Service help (formerly, visitor ID), go [here](https://docs.adobe.com/content/help/en/id-service/using/home.html).

**不使用[!UICONTROL Experience Platform Launch]或[!UICONTROL 動態標籤管理]?**

If you are not using [!UICONTROL Experience Platform Launch] or [!UICONTROL Dynamic Tag Management], manually implement the ID service via the JavaScript Deployment ([!DNL VisitorAPI.js]), as follows:

| 任務 | 說明 |
| -----------| ---------- |  
| [實作適用於 Analytics 的 Experience Cloud ID 服務](https://docs.adobe.com/content/help/en/id-service/using/implementation/setup-analytics.html) | Adobe 也建議設定額外的[客戶 ID](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html)。這些ID會與每個訪客關聯，並啟用Experience cloud中目前和未來的功能。 |
| 將現有的 [!DNL s_code] 更新為 H.27.3 或更新版本，或將現有的 [!DNL AppMeasurement.js] 更新為 1.4 或更新版本。 | 這些檔案位於 Analytics「管理工具」的[代碼管理器](https://docs.adobe.com/content/help/en/analytics/admin/admin-tools/code-manager-admin.html)中，可供下載。(如果您需要 [ 的相關詳細資訊，請參閱 ](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/javascript-implementation-overview.html)JavaScript 實作[!DNL AppMeasurement.js]指南)。 |
| 同步Analytics的客戶ID | 請參閱 [Analytics - 同步化客戶 ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (下文)。 |

## Analytics 和 Target - 同步化客戶 ID {#section_AD473A6A21C1446498E700363F9A8437}

As a part of setting up the Experience Cloud ID Service, Adobe recommends for Analytics and [!DNL Target] that you synchronize your [customer IDs](https://docs.adobe.com/content/help/en/id-service/using/reference/authenticated-state.html) with the Experience Cloud.

In Adobe Target, the `mbox3rdpartyid` needs to get the customer ID and send it to [!DNL Target]. (See [Working with Customer Attributes](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/working-with-customer-attributes.html) in [!DNL Target].)

當您的網站驗證訪客或證實其身份時，您的實作必須將此人的 CRM 客戶 ID 公開給頁面或應用程式。接著，您可以使用適當的功能呼叫，將您的客戶 ID 同步至 Experience Cloud。這個同步化的動作會將該訪客的 CRM 客戶 ID 儲存到 Experience Cloud，然後啟動該客戶的屬性以用於 Experience Cloud。

例如，假設在 CRM 系統中 Bob 的 Customer ID 為 `52mc210tr42`。當您的網站驗證 Bob 時，您必須在頁面上洩露此 ID，然後以下述方法之一使用此 ID 進行同步化:

* 使用訪客 ID 服務呼叫 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或,
* 將&#x200B;*`Customer ID (52mc210tr42)`*&#x200B;填入 prop 或 eVar。

在每個已知客戶 ID 的 [!DNL Analytics] 伺服器呼叫上皆必須設定客戶 ID。

### 行動 SDK

如需如 *何在Android和* iOS Mobile應用程式中設定其他客戶ID的語法範例，請參閱「 [Experience Cloud ID服務」](https://docs.adobe.com/content/help/en/mobile-services/android/overview.html)[](https://docs.adobe.com/content/help/en/mobile-services/ios/overview.html) 一節。

### 啟用歷史資料的屬性

訪客登入後，即可使用客戶屬性資料。如果您尚未實作最新的Experience Cloud ID服務，而且您過去一直在prop或eVar中追蹤客戶ID，則可以請求傳送歷史登入至Experience cloud的程式。 此程序讓您可以立即開始使用客戶屬性。

請聯絡「客戶服務」以啟用歷史資料。

## 步驟 3.Map report suites to an Experience Cloud Organization {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud services (such as Experience Cloud ID Service and the [!UICONTROL People service]) are associated with an Experience Cloud organization instead of an individual Analytics report suite. 若要確保這些服務能正確運作，每個 Analytics 報表套裝都必須對應至 Experience Cloud 組織。

請參閱[將報表套裝對應至組織](report-suite-mapping.md)。

## 步驟 4.(Adobe Analytics) Update your Analytics AppMeasurement code {#section_1798D9D0F05C47E29816AC4EEB9A0913}

確認您位於區域資料收集 (RDC)。如果您的資料收集網域為 [!DNL omtrdc.net]，或將 CNAME 對應至 [!DNL omtrdc.net]，則表示您位於 RDC。如需詳細資訊，請參閱[切換至 RDC](https://docs.adobe.com/content/help/en/analytics/technotes/rdc/regional-data-collection.html)。If you are using first-party cookies, refer to [CNAME and the Experience Cloud ID Service](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html) for information about data collection CNAMEs and cross-domain tracking.

建議您更新 JavaScript 程式庫 (包括訪客 API)，以將 Analytics 實作最新化。最簡單的實行方式是在動態標籤管理中新增 [!DNL Adobe Analytics] 工具，需指定 *`Automatic`* 做為設定方法。

In [!UICONTROL Dynamic Tag Management], click **[!UICONTROL <Web Property Name>]**>**[!UICONTROL &#x200B;概述&#x200B;]**>**[!UICONTROL &#x200B;新增工具&#x200B;]**>**[!UICONTROL  Adobe Analytics ]**。如需部署的詳細資訊，請參閱動態標籤管理中的[Adobe Analytics 設定](https://docs.adobe.com/content/help/en/dtm/using/tools/analytics-dtm.html)。

## 步驟 5.(Adobe Target) Update your Adobe Target implementation {#section_C2F4493C7A36406DAE2266B429A4BD24}

* It is recommended that you add an [Adobe Target extension](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html) in [!UICONTROL Experience Platform Launch], so that your library retrieval is automatic. 您也可以使用 [Experience Platform Launch，為Target](https://docs.adobe.com/content/help/en/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html) （及其他解決方案）設 [!UICONTROL 定Experience Cloud ID服務擴充功能]。 The [!UICONTROL Experience Cloud ID Service] update **is required** for [!UICONTROL Target] to use core services. (如果您使用 [!UICONTROL 動態標籤管理]，請新增 [Adobe Target工具](https://docs.adobe.com/content/help/en/dtm/using/tools/target.html)。 You can also use [!UICONTROL Dynamic Tag Management] to deploy the Experience Cloud ID Service for Target.)
* 如果您不是使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，請手 [動更新mbox程式庫](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html) 。
* Request access to use Adobe Analytics as the reporting source for [!DNL Adobe Target]. [!DNL Target] 與 資料會在處理期間結合到相同的伺服器呼叫上，使訪客可在兩個解決方案之間連接。[!DNL Analytics]請參閱 [Analytics 用於 Target 的實作](https://docs.adobe.com/content/help/en/target/using/integrate/a4t/a4t.html)。

   >[!IMPORTANT]
   >
   >所有Analytics客戶都已布建核心服務，例如客戶屬性。 如果您還不是 Analytics 客戶，請聯絡客戶服務，請他們幫您進行佈建。

## 步驟 6.確認核心服務實作 {#section_E641782A0F4F44AF8C9C91216BE330D5}

請使用下列程式，以確保Experience Cloud ID服務在您的網站上正確實作。

1. 清除您網站的Cookie，以便您能夠查看對Experience Cloud ID服務的請求（此請求會在第一次瀏覽時提出，然後每週每位訪客大約會提出一次）。
1. 使用封包分析工具或網頁瀏覽器偵錯工具中的網路面板，尋找進入 [!DNL dpm.demdex.net] 的要求。
1. 確認回應中包含 `d_mid` 和一個值，例如: `_setMarketingCloudFields({"d_mid":"4235...`
1. Verify that the Analytics request contains the `mid` parameter (the Experience Cloud ID). During the grace period (if it is enabled), you should also see an `aid` parameter (the Analytics visitor ID).

包含 Experience Cloud ID 的預期回應:

![](assets/mac_id_response.png)

包含Experience Cloud ID（亦稱為訪客ID）的Analytics `mid` 影 _像請求_:

![](assets/mid.png)

mbox 請求中的 Experience Cloud ID:

![](assets/mbox_request.png)

**什麼是寬限期?**

在您部署Experience Cloud ID服務後，新訪客不會再從您的資料收集伺服器接收Analytics Experience Cloud ID。 如果您網站的區段尚未實作Experience Cloud ID服務，當訪客瀏覽至這些區段時，將無法識別Experience Cloud ID，並且會為訪客指派舊有的Analytics訪客ID。 這樣可能會造成潛在問題，包括重複瀏覽次數和錯誤的屬性。

例如，如果網站的支援區段是由個別的 CMS 所管理，則這個區段可能會有不同的 Analytics JavaScript 檔案。如果您在將ID服務部署至支援網站之前，先在主網站上部署Experience Cloud ID，新訪客在造訪支援區段時會收到舊有的Analytics ID，而跨兩個網站區段的造訪會報告為不同的造訪。

將Experience Cloud ID服務部署在使用多個JavaScript檔案或其他技術（例如Flash）的網站上，可能會造成協調問題，因為您需要同時在網站的所有部分上啟用Experience Cloud ID服務。 透過設定寬限期，新訪客可繼續從ID服務接收Analytics訪客ID，如此您就可在尚未升級為使用訪客ID服務的網站區段上一致地識別訪客。

## 步驟 7.管理使用者和產品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

Once you are up and running, navigate to the [Admin Console](https://adminconsole.adobe.com/), where you can manage users and product profiles.

![](assets/menu-administration-shell.png)

請參閱 [Experience Cloud 的使用者和產品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**客戶屬性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

Users that are added to the [!UICONTROL Customer Attributes] group will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface

## 步驟 8.Begin using core services {#section_960C06093623462E8EA247B3E97274A1}

善用以下的核心服務功能。

![](assets/menu-audiences-shell.png)

**[!UICONTROL 人員]>客[!UICONTRO戶屬性]**

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

請參閱[客戶屬性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**[!UICONTROL 人物]>觀[!UICONTROL 眾庫]**

Experience Cloud [!UICONTROL Audiences] is the interface that lets you create audiences, combine existing audiences to create composite audiences, and view all shared audiences.

請參閱[受眾](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## 資料儲存與隱私洩露

如果您利用 Adobe [!DNL Experience Cloud] 中的受眾資料即時設定及其他核心服務，則使用這些服務可能會影響您資料所在的資料中心 (和國家/地區)。Specifically, because the core services of the Adobe [!DNL Experience Cloud] leverage Adobe Audience Manager, data used within the [!UICONTROL People] service must reside within Audience Manager servers in the United States.

When leveraging core services made available via the [!UICONTROL People] service, the types of data sent from other Adobe products to audience management are:

* [!DNL Analytics] 金鑰/值配對 (小道具、eVars、清單變數等等)。依預設，記錄行包含 IP 位址，包含 IP 的最後一組八位數 (假設未以 Adobe [!DNL Analytics] 中的 IP 混淆設定修改 IP 位址)。
* 會根據 Audience Manager 中設定的規則來判定訪客是否符合特徵和區隔的規定。
* (選用) 您的一或多個 ID。根據您的 ID 服務實作，您可能另外正在傳入一或多個 ID，例如 CRM ID 或雜湊電子郵件地址。若將此資料傳入 Adobe [!DNL Analytics]，則會將其轉移至 Adobe 受眾管理。Adobe 建議您將個人資料提供給 Adobe [!DNL Analytics]。反之，先使用單向雜湊來虛擬化資料，再傳送給 Adobe。
* 透過後端區隔分享功能，在 [!DNL Analytics] 中建立的區隔。
* 如未封鎖第三方 cookie，則會設置 demdex.net cookie。The `AMCV_###@AdobeOrg` first-party cookie is always set with the Experience Cloud ID Service.

其中所有資料元素都是以記錄檔形式傳遞至 Adobe Audience Manager。Audience Manager 可處理和儲存美國境內的此資料。Audience Manager 不提供在美國境外處理或儲存此資料的選項。

**Cookie 和退出宣告**

使用即時受眾設定檔時，除了可利用使用於 [!DNL Analytics] 和 [!DNL Target] 的 cookie 外，還可利用 Audience Manager 管理 cookie。

若要提供適當的退出宣告能力，您網站的訪客必須將 Audience Manager 退出宣告新增至您現有的退出宣告程序。

請參閱 [Adobe Experience Cloud - 實作 Adobe 退出宣告](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/data-collection/opt-out.html)的指示。

如需啟用跨網域追蹤的詳細資訊，請參閱[資料收集 CNAME 和跨網域追蹤](https://docs.adobe.com/content/help/en/id-service/using/reference/analytics-reference/cname.html)。
