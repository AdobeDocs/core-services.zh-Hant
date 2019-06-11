---
description: 實作 Experience Cloud 並成為管理員。此程序可針對客戶屬性和對象等核心服務功能，將您的解決方案現代化。
keywords: 核心服務；客戶屬性
seo-description: 實作 Experience Cloud 並成為管理員。此程序可針對客戶屬性和對象等核心服務功能，將您的解決方案現代化。
seo-title: 為核心服務啓用Experience Cloud解決方案
solution: Experience Cloud
title: 啟用核心服務的解決方案
uuid: 5820060f-9b18-4339-81e0-401d964f7a03
translation-type: tm+mt
source-git-commit: b4809ff0b4546f105ac6270eca1bfce2b6467876

---


# 啟用核心服務的解決方案

實作 Experience Cloud 並成為管理員。此程序可針對客戶屬性和對象等核心服務功能，將您的解決方案現代化。

<!-- <p>https://marketing-beta.adobe.com/resources/help/core/core-services.html </p> 
<p>https://adobe.sharepoint.com/sites/AGSConsulting/CoreServices/PA/_layouts/15/start.aspx#/ </p> -->

<!-- Core services architecture and data flow wiki: https://wiki.corp.adobe.com/pages/viewpage.action?pageId=1004285689 -->

## 步驟 1. 加入 Experience Cloud 並成為管理員 {#section_2423F0BD3DF642658103310EE5EA6154}

若要加入 Experience Cloud，您必須先執行下列動作:

![](assets/step1_icon.png) 確定您具有適當的 Adobe Analytics 或 Adobe Target SKU。

* **Adobe Analytics:** Standard 或 Premium 版 (非舊版 SiteCatalyst SKU)。
* **Adobe Target:** Standard 或 Premium 版。



>[!NOTE]
>
>針對Target， [從mbox. js移轉至at. js](https://marketing.adobe.com/resources/help/en_US/target/ov2/t_target-migrate-atjs.html)。


![](assets/step2_icon.png)最實化實作，並取得已佈建的管理員。


1. 請依以下[部署 Experience Cloud ID 服務](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)的步驟進行。
1. 請聯絡帳戶管理，並開始 Experience Cloud 的佈建程序。

![](assets/step3_icon.png) 在 Admin Console 中管理使用者和產品.

**管理員存取**

成為管理員後，即可登入.[marketing.adobe.com](https://marketing.adobe.com)。

您會在 Experience Cloud 功能表導覽中看到 **[!UICONTROL 管理]連結。**

如需說明，請參閱 [Experience Cloud使用者和產品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909) 。

**使用者存取權**

若要登入 Experience Cloud，您的使用者必須:


1. 有 Adobe ID。
1. 登入 [!DNL marketing.adobe.com]。
1. 屬於對應至企業群組的解決方案群組。
1. 視需要將他們的解決方案帳戶連結至各自的 Adobe ID (如下所述)。

![](assets/step4_icon.png) 選用: 連結現有的使用者帳戶。

您很可能有使用者已屬於在「Analytics &gt; 管理工具」中管理之某個解決方案群組的成員，例如 Analytics 群組。

當您將這些群組對應至 Experience Cloud 企業群組時，這些使用者必須以手動方式將他們的解決方案帳戶認證連結至其 Adobe ID。

請參閱[在 Experience Cloud 連結帳戶](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

> [!NOTE]
> 
> 在企業和解決方案群組對應後，新使用者就會自動連結。(系統會自動建立解決方案認證並連結至其 Adobe ID)。

下列章節說明如何最新化實作。最新化實作可以啟用 Experience Cloud 中的核心服務。

## 步驟 2.使用Dynamic Tag Manager或Launch，實施Experience Cloud ID服務 {#section_3C9F6DF37C654D939625BB4D485E4354}

若要啟用 Experience Cloud 核心服務，最簡單的方式是透過動態標笉管理中的 [Experience Cloud ID 服務工具](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-dtm-implement.html) 自動為 Analytics 和 Target 啟用。(或 Launch，由 Adobe 提供。)

![](assets/menu-activation-shell.png)

如需完整的 Experience Cloud ID 服務 (先前稱為訪客 ID)，請前往[這裡](https://marketing.adobe.com/resources/help/en_US/mcvid/)。

另外，新一代標籤管理是 [Launch，由 Adobe 提供](https://marketing.adobe.com/resources/help/en_US/experience-cloud/launch/)

**未使用動態標籤管理或 Launch 嗎?**

如果您沒有使用動態標籤管理，請透過 JavaScript 部署 ([!DNL VisitorAPI.js]) 手動實作 ID 服務 (如下所述):

1. 執行[為 Analytics 執行 Experience Cloud ID 服務](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-setup-analytics.html)中所述步驟。

   Adobe 也建議設定額外的[客戶 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html)。這些 ID 與每個訪客關聯，以利 Experience Cloud 核心服務中的現有和未來功能的運作。

1. 將現有的 [!DNL s_code] 更新為 H.27.3 或更新版本，或將現有的 [!DNL AppMeasurement.js] 更新為 1.4 或更新版本。

   這些檔案位於 Analytics「管理工具」的[代碼管理器](https://marketing.adobe.com/resources/help/en_US/reference/index.html?f=code_manager_admin)中，可供下載。

   (如果您需要 [ 的相關詳細資訊，請參閱 ](https://marketing.adobe.com/resources/help/en_US/sc/implement/js_implementation.html)JavaScript 實作[!DNL AppMeasurement.js]指南)。

1. 為 Analytics 同步化客戶 ID。請參閱 [Analytics - 同步化客戶 ID](../core-services/core-services.md#section_AD473A6A21C1446498E700363F9A8437) (下文)。

## Analytics 和 Target - 同步化客戶 ID {#section_AD473A6A21C1446498E700363F9A8437}

Adobe 建議您針對 Analytics 和 Target，將[客戶 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid-authenticated-state.html) 與 Experience Cloud 同步化，做為設定 Experience Cloud ID 服務的步驟之一。

在 Target 中，[!DNL mbox3rdpartyid] 需取得客戶 ID 並將其傳送到 Target。(請參閱 Target 中的[運用客戶屬性](https://marketing.adobe.com/resources/help/en_US/target/target/c_working-with-customer-attributes.html)。)

當您的網站驗證訪客或證實其身份時，您的實作必須將此人的 CRM 客戶 ID 公開給頁面或應用程式。接著，您可以使用適當的功能呼叫，將您的客戶 ID 同步至 Experience Cloud。這個同步化的動作會將該訪客的 CRM 客戶 ID 儲存到 Experience Cloud，然後啟動該客戶的屬性以用於 Experience Cloud。

例如，假設在 CRM 系統中 Bob 的 Customer ID 為 `52mc210tr42`。當您的網站驗證 Bob 時，您必須在頁面上洩露此 ID，然後以下述方法之一使用此 ID 進行同步化:

* 使用 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})` 訪客ID服務進行呼叫。或,
* 將*`Customer ID (52mc210tr42)`*填入 prop 或 eVar。


在每個已知客戶 ID 的 [!DNL Analytics] 伺服器呼叫上皆必須設定客戶 ID。

**行動 SDK**

如需 *如何在*[Android](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods) 和 [iOS](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods) Mobile應用程式中設定額外客戶ID的語法範例，請參閱Experience Cloud ID服務區段。

**啟用歷史資料的屬性**

訪客登入後，即可使用客戶屬性資料。如果您尚未實作最新的 Experience Cloud ID 服務，而且過去都用 prop 或 eVar 追蹤客戶 ID，則可以要求傳送歷史登入至 Experience Cloud 的程序。此程序讓您可以立即開始使用客戶屬性。

請聯絡「客戶服務」以啟用歷史資料。

## 步驟 3. 將報表套裝對應至 Experience Cloud 組織 {#section_7B08516B01BA421681DF03D0E86CE3BA}

Experience Cloud 服務 (例如 Experience Cloud ID 服務及 People) 與 Experience Cloud 組織相關，而非個別的報表套裝。若要確保這些服務能正確運作，每個 Analytics 報表套裝都必須對應至 Experience Cloud 組織。

請參閱[將報表套裝對應至組織](report-suite-mapping.md)。

## 步驟 4. (Adobe Analytics) 最新化 Analytics AppMeasurement 代碼 {#section_1798D9D0F05C47E29816AC4EEB9A0913}

確認您位於區域資料收集 (RDC)。如果您的資料收集網域為 [!DNL omtrdc.net]，或將 CNAME 對應至 [!DNL omtrdc.net]，則表示您位於 RDC。如需詳細資訊，請參閱[切換至 RDC](https://marketing.adobe.com/resources/help/en_US/whitepapers/rdc/?f=rdc_transition)。如果您使用第一方 cookie，若需要有關資料收集 CNAME 和跨網域追蹤的詳細資訊，請參閱 [CNAME 和訪客 ID 服務](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname)。

建議您更新 JavaScript 程式庫 (包括訪客 API)，以將 Analytics 實作最新化。要實現此目的，最簡單的方法是在動態標籤管理中新增 [!DNL Adobe Analytics] 工具，指定 *`Automatic`* 為設定方法。

在動態標籤管理中，按一下 **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL 綜覽]**&gt;**[!UICONTROL 新增工具]**&gt;**[!UICONTROL Adobe Analytics]**。如需部署的詳細資訊，請參閱動態標籤管理中的[Adobe Analytics 設定](https://marketing.adobe.com/resources/help/en_US/dtm/?f=analytics_dtm)。

## 步驟 5. (Adobe Target) 最新化 Adobe Target 實作 {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 建議您在動態標籤管理中新增 [Adobe Target 工具](https://marketing.adobe.com/resources/help/en_US/dtm/target.html)，讓您的程式庫擷取變成自動。在動態標籤管理中，按一下 **[!UICONTROL <Web Property Name>]**&gt;**[!UICONTROL 綜覽]**&gt;**[!UICONTROL 新增工具]**&gt;**[!UICONTROL Adobe Target]**。** 附註:**您也可以使用動態標籤管理，為 Target (及其他解決方案) 部署 Experience Cloud ID 服務。** 必須 **更新 Target 的 Experience Cloud ID 服務才能使用核心服務。
* 如果您不是使用動態標籤管理，請手動[更新 mbox 程式庫](https://marketing.adobe.com/resources/help/en_US/target/ov/?f=t_mbox_download)。
* 要求存取權以使用 Adobe Analytics 做為 Adobe Target 的報表來源。Target 與 Analytics 資料會在處理期間結合到相同的伺服器呼叫上，使訪客可在兩個解決方案之間連接。請參閱 [Analytics 用於 Target 的實作](https://marketing.adobe.com/resources/help/en_US/target/a4t/?f=a4t)。
* 
   >[!IMPORTANT]
   >
   >所有分析客戶都已針對客戶屬性等核心服務布建。如果您還不是 Analytics 客戶，請聯絡客戶服務，請他們幫您進行佈建。

## 步驟 6. 確認核心服務實作 {#section_E641782A0F4F44AF8C9C91216BE330D5}

使用下列程序，可確保 Experience Cloud ID 服務能夠在您的網站上正確實作。

1. 清除您的網站 Cookie，以便查看對 Experience Cloud ID 服務提出的請求 (此請求會在第一次造訪時提出，之後每週每名訪客大約會提出一次)。1. 使用封包分析器或網頁瀏覽器除錯程式中的網路面板，尋找要求 [!DNL dpm.demdex.net]。
1. 確認回應包含 `d_mid` 和值，例如： `_setMarketingCloudFields({"d_mid":"4235...`
1. 確認 Analytics 請求中包含 mid 參數 (Experience Cloud ID)。在寬限期內 (若有啟用)，您應該還會看見 aid 參數 (Analytics 訪客 ID)。

包含 Experience Cloud ID 的預期回應:

![](assets/mac_id_response.png)

包含 Experience Cloud ID (mid) 的 Analytics 影像請求:

![](assets/mid.png)

mbox 請求中的 Experience Cloud ID:

![](assets/mbox_request.png)

**什麼是寬限期?**

在您部署訪客 ID 服務後，新的訪客將不會再從您的資料收集伺服器接收 Analytics 訪客 ID。如果您的網站有某些區段尚未實作訪客 ID 服務，當訪客瀏覽這些區段時，將無法辨識 Experience Cloud ID，並且會為訪客指派舊有的 Analytics 訪客 ID。這樣可能會造成潛在問題，包括重複瀏覽次數和錯誤的屬性。

例如，如果網站的支援區段是由個別的 CMS 所管理，則這個區段可能會有不同的 Analytics JavaScript 檔案。如果您在訪客 ID 服務部署至支援網站之前在主要網站上部署了訪客 ID，則新的訪客在造訪支援區段時將會接收到舊有的 Analytics ID，且橫跨兩個網站區段的造訪將會報告為不同的造訪。

將訪客 ID 服務部署在使用多個 JavaScript 檔案或其他技術 (例如 Flash) 的網站上，可能會導致協調方面的問題，因為您必須同時在網站的所有區段上啟用訪客 ID 服務。藉由寬限期的設定，新訪客將繼續從訪客 ID 服務接收 Analytics 訪客 ID，因而可在您未升級為使用訪客 ID 服務的網站區段上一致地識別訪客。

## 步驟 7.管理使用者和產品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

啓動並執行後，導覽至 **[!UICONTROL 「管理]** &gt; **[!UICONTROL 啓動管理控制台]**」，您可在此處管理使用者和產品設定檔。

![](assets/menu-administration-shell.png)

請參閱 [Experience Cloud使用者和產品管理](../admin-getting-started/admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

**客戶屬性**

<!-- <p> 
 <note type="important">
  To use the Customer Attributes feature, users must belong to the 
  <span class="term"> Adobe Customer Attributes</span> group, and to solution-level groups (Analytics or Target). 
 </note> </p> 
 -->

加入客戶屬性群組的使用者可在 Experience Cloud 介面的左邊看到[!UICONTROL 「客戶屬性」]選單項目

## 步驟 8.開始使用核心服務 {#section_960C06093623462E8EA247B3E97274A1}

善用以下的核心服務功能。

![](assets/menu-audiences-shell.png)

**「人員&gt;客戶屬性」**

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，將資料運用 [!DNL Adobe Analytics] 於和 [!DNL Adobe Target]。

請參閱 [客戶屬性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

**人員&gt;觀眾程式庫**

「Experience Cloud 受眾」介面可讓您建立受眾、組合現有受眾以建立複合受眾，並檢視所有共用受眾。

查看 [觀眾](../audience-library/audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

<!-- aam_mc.xml -->

## 資料儲存和隱私洩露資訊

如果您利用 Adobe [!DNL Experience Cloud] 中的受眾資料即時設定及其他核心服務，則使用這些服務可能會影響您資料所在的資料中心 (和國家/地區)。尤其是 Adobe [!DNL Experience Cloud] 的核心服務會利用 Adobe Audience Manager，因此「People」核心服務中使用的資料必須位於美國的 Audience Manager 伺服器。

透過「People」核心服務利用核心服務時，從其他 Adobe 產品傳送至受眾管理的資料類型為:

* [!DNL Analytics] 金鑰/值配對 (小道具、eVars、清單變數等等)。依預設，記錄行包含 IP 位址，包含 IP 的最後一組八位數 (假設未以 Adobe [!DNL Analytics] 中的 IP 混淆設定修改 IP 位址)。
* 會根據 Audience Manager 中設定的規則來判定訪客是否符合特徵和區隔的規定。
* (選用) 您的一或多個 ID。根據您的 ID 服務實作，您可能另外正在傳入一或多個 ID，例如 CRM ID 或雜湊電子郵件地址。若將此資料傳入 Adobe [!DNL Analytics]，則會將其轉移至 Adobe 受眾管理。Adobe 建議您將個人資料提供給 Adobe [!DNL Analytics]。反之，先使用單向雜湊來虛擬化資料，再傳送給 Adobe。
* 透過後端區隔分享功能，在 [!DNL Analytics] 中建立的區隔。
* 如未封鎖第三方 cookie，則會設置 demdex.net cookie。Experience Cloud 訪客 ID (先前稱為訪客 ID 服務) 一律會設置第一方 Cookie `AMCV_###@AdobeOrg`。


其中所有資料元素都是以記錄檔形式傳遞至 Adobe Audience Manager。Audience Manager 可處理和儲存美國境內的此資料。Audience Manager 不提供在美國境外處理或儲存此資料的選項。

**Cookie 和退出宣告**

使用即時受眾設定檔時，除了可利用使用於 [!DNL Analytics] 和 [!DNL Target]   的 cookie 外，還可利用 Audience Manager 管理 cookie。

若要提供適當的退出宣告能力，您網站的訪客必須將 Audience Manager 退出宣告新增至您現有的退出宣告程序。

請參閱 [Adobe Experience Cloud - 實作 Adobe 退出宣告](https://marketing.adobe.com/resources/help/en_US/sc/implement/opt_out.html)的指示。

如需啟用跨網域追蹤的詳細資訊，請參閱[資料收集 CNAME 和跨網域追蹤](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_cname)。
