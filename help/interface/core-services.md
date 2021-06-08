---
description: 更新您的 Adobe Analytics 和 Adobe Target 解決方案，提供跨解決方案服務。了解如何開始使用 Experience Cloud 服務。
keywords: 核心服務;客戶屬性
solution: Experience Cloud
title: 讓您的解決方案提供跨解決方案服務
index: true
feature: 客戶屬性
topic: 管理
role: Administrator
level: Experienced
exl-id: 48e79e23-b339-4143-b3b1-969c370efeff
source-git-commit: c714a5549bc5377c584721404b11a394625c519f
workflow-type: tm+mt
source-wordcount: '2334'
ht-degree: 72%

---

# 啟用 Experience Cloud 服務實作

如果您最近曾使用 Experience Platform Launch 實作 Experience Cloud，即已完成客戶屬性和 Experience Cloud 受眾的相關設定。您也可以在 Admin Console 中管理使用者和產品。

現有客戶可導入最新的解決方案實作並實作Experience Cloud。 如此一來，您就能跨Adobe Analytics、Audience Manager和Adobe Target使用客戶屬性和受眾功能。 若要完成此實作，請執行以下作業：

1. [加入 Experience Cloud 並成為管理員](#section_2423F0BD3DF642658103310EE5EA6154)
1. [實作 Experience Cloud ID Service](#section_3C9F6DF37C654D939625BB4D485E4354)
1. [將報表套裝對應至 Experience Cloud 組織](#section_7B08516B01BA421681DF03D0E86CE3BA)
1. [更新 Analytics AppMeasurement 程式碼](#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [更新 Adobe Target 實作](#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [驗證實施](#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理使用者和產品](#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [開始共用屬性和受眾資料](#section_960C06093623462E8EA247B3E97274A1)

## 加入 Experience Cloud 並成為管理員 {#section_2423F0BD3DF642658103310EE5EA6154}

若要加入 Experience Cloud，您必須先執行下列動作：

1. 確定您具有適當的 Adobe Analytics 或 Adobe Target SKU。

   * **Adobe Analytics：** Standard 或 Premium 版 (非舊版 [!DNL SiteCatalyst] SKU)。
   * **Adobe Target：** Standard 或 Premium 版。

   >[!NOTE]
   >
   >若使用 [!DNL Target]，需從 [!DNL mbox.js] 移轉至 at.js。請參閱[從 at.js 1.x 升級為 at.js 2.x](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/at-js-implementation/upgrading-from-atjs-1x-to-atjs-20.html?lang=en)。

1. 最實化實作，並取得已佈建的管理員。

   * 請依照下文「[實作 [!UICONTROL Experience Cloud ID Service]](core-services.md#section_3C9F6DF37C654D939625BB4D485E4354)」中的步驟操作。
   * 請連絡您的客戶經理，並開始進行 Experience Cloud 佈建流程。

1. 在 [!UICONTROL Admin Console] 中管理使用者和產品。

### 管理員登入

成為管理員後，即可登入[experience.adobe.com](https://experience.adobe.com)。

**[!UICONTROL Admin Console]**&#x200B;連結可在Experience Cloud功能表導覽中使用。

如需詳細資訊，請參閱 [Experience Cloud 的使用者和產品管理](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 使用者登入

若要登入 Experience Cloud，您的使用者必須：

* 擁有貴公司的 Adobe ID (或 Enterprise ID)。
* 在[experience.adobe.com](https://experience.adobe.com)登入。
* 屬於對應至企業群組的解決方案群組。
* 視需要將其解決方案帳戶連結至其 Adobe ID (如下所述)。

### 選用：連結現有的使用者帳戶。

最有可能的情況是，您的使用者已是解決方案群組的成員，例如您先前在 [!UICONTROL Analytics] >[!UICONTROL 管理工具]中管理的 Analytics 群組。

將這些群組對應至 Experience Cloud 企業群組時，這些使用者必須手動將其解決方案帳戶憑證連結至其 Adobe ID。

請參閱[在 Experience Cloud 中連結帳戶](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)

>[!NOTE]
>
>在企業和解決方案群組對應後，新使用者會自動產生連結(系統會自動建立解決方案憑證並連結至其 Adobe ID)。

以下各節將說明如何導入最新實作。導入最新實作以啟用 Experience Cloud 中的核心服務。

## 實作 [!UICONTROL Experience Cloud ID Service] {#section_3C9F6DF37C654D939625BB4D485E4354}

[!UICONTROL Experience Cloud ID Service] 提供的通用 ID 可用於跨解決方案整合。它提供跨網域訪客身分識別，以及根據透過[!UICONTROL 客戶屬性]上傳的 CRM 資料跨裝置/瀏覽器鎖定目標和個人化的路徑。

啟用 Experience Cloud 核心服務最簡單的方法，就是透過 [!UICONTROL Experience Platform Launch] 中的 [Experience Cloud ID Service 擴充功能](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html?lang=zh-Hant#extensions-ref)，為 Analytics 和 Adobe Target 自動啟用

如需完整的 Experience Cloud ID Service 說明 (先前稱為訪客 ID)，請前往[這裡](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant#intro)。

**沒有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management] 嗎？**

如果您沒有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，請透過 JavaScript 部署 ([!DNL VisitorAPI.js]) 手動實作 ID 服務，如下所述：

| 任務 | 說明 |
| -----------| ---------- |  
| [實作適用於 Analytics 的 Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=en) | Adobe 也建議設定其他[客戶 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en)。這些 ID 與每個訪客相關聯，實現了 Experience Cloud 中的現有和未來功能。 |
| 將現有的 [!DNL s_code] 更新為 H.27.3 或更新版本，或將現有的 [!DNL AppMeasurement.js] 更新為 1.4 或更新版本。 | 這些檔案可在 Analytics 分析管理工具的[代碼管理器](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/code-manager-admin.html?lang=en)中下載。(如果您需要更多 [!DNL AppMeasurement.js] 的相關資訊，請參閱 [JavaScript 實作](https://experienceleague.adobe.com/docs/analytics/implementation/js/overview.html?lang=en#js)指南。) |
| 同步 Analytics 的客戶 ID | 請參閱 [Analytics - 同步客戶 ID](core-services.md#section_AD473A6A21C1446498E700363F9A8437) (下文)。 |

### Analytics 與 Adobe Target - 同步客戶 ID {#section_AD473A6A21C1446498E700363F9A8437}

Adobe 建議您針對 Analytics 和 [!DNL Target]，將[客戶 ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html?lang=en) 與 Experience Cloud 進行同步，作為設定 Experience Cloud ID Service 的步驟之一。

在Adobe Target中，`mbox3rdpartyid`必須取得客戶ID並將其傳送至[!DNL Target]。 (請參閱 [!DNL Target] 中的[使用客戶屬性](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/working-with-customer-attributes.html?lang=en)。)

當訪客在您的網站上進行驗證或以其他方式識別自己身分時，您的實作必須將該人的CRM客戶ID公開給頁面或應用程式。 然後，您可以使用適當的函數呼叫，將客戶 ID 同步至 Experience Cloud。此同步會將訪客的 CRM 客戶 ID 儲存在 Experience Cloud 中，並啟動該客戶的屬性以用於 Experience Cloud。

例如，假設在 CRM 系統中 Bob 的 Customer ID 為 `52mc210tr42`。當您的網站驗證 Bob 時，您必須在頁面上公開此 ID，然後以下述方法之一使用此 ID 進行同步化：

* 使用訪客 ID 服務呼叫 `visitor.setCustomerIDs({"crm_id":"52mc210tr42"})`。或,
* 在 prop 或 eVar 中填入 *`Customer ID (52mc210tr42)`*。

在每個已知客戶 ID 的 [!DNL Analytics] 伺服器呼叫上皆必須設定客戶 ID。

### 行動 SDK

請參閱&#x200B;*Experience CloudID服務*&#x200B;一節，以取得有關如何在[Android™](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=en)和[iOS](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=en)行動應用程式中設定其他客戶ID的語法範例。

### 啟用歷史資料的屬性

訪客登入後，即可使用客戶屬性資料。如果您尚未實作ID服務，且過去一直在prop或eVar中追蹤客戶ID，您可以請求將歷史登入資料傳送至Experience Cloud的程式。 此程序可讓您立即開始使用客戶屬性。

請連絡客戶服務以啟用歷史資料。

## 將報表套裝對應至 Experience Cloud 組織 {#section_7B08516B01BA421681DF03D0E86CE3BA}

>[!NOTE]
>
>報表套裝對應功能已於 2020 年 11 月終止支援。如有任何疑問，請聯絡客戶支援。

Experience Cloud 服務 (例如 Experience Cloud ID Service 和 [!UICONTROL People 服務]) 與 Experience Cloud 組織相關聯而非個別 Analytics 報表套裝。為確保這些服務正常運作，每個 Analytics 報表套裝都必須對應至一個 Experience Cloud 組織。

## 更新 Analytics AppMeasurement 程式碼 {#section_1798D9D0F05C47E29816AC4EEB9A0913}

如果您使用 Analytics，請確認您是否位於地區資料收集 (RDC)。如果您的資料收集網域為 [!DNL omtrdc.net]，或將 CNAME 對應至 [!DNL omtrdc.net]，則表示您位於 RDC。如需詳細資訊，請參閱[轉換為 RDC](https://experienceleague.adobe.com/docs/analytics/technotes/rdc/regional-data-collection.html?lang=en)。如果您使用第一方 Cookie，請參閱 [CNAME 和 Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=en)，取得資料收集 CNAME 和跨網域追蹤的相關資訊。

建議您更新 JavaScript 程式庫 (包括訪客 API)，以將 Analytics 實作最新化。要達到+632581，最簡單的方式是在「動態標籤管理」中新增[!DNL Adobe Analytics]工具，需指定&#x200B;*`Automatic`*&#x200B;作為設定方法。

在 [!UICONTROL Dynamic Tag Management] 中，按一下「**`<Web Property Name>`**> **[!UICONTROL 概述]** > **[!UICONTROL 新增工具]** > **[!UICONTROL Adobe Analytics]**」。如需部署資訊，請參閱 Dynamic Tag Management 中的 [Adobe Analytics 設定](https://experienceleague.adobe.com/docs/dtm/using/tools/analytics-dtm.html?lang=en)。

## 更新 Adobe Target 實作 {#section_C2F4493C7A36406DAE2266B429A4BD24}

* 建議您在 [!UICONTROL Experience Platform Launch] 中新增 [Adobe Target 擴充功能](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/targetv2-extension/adobe-target-extension-v2.html?lang=en)，以便讓資料庫擷取作業自動執行。您也可以使用 [!UICONTROL Experience Platform Launch]，為 Adobe Target (及其他解決方案) 設定 [Experience Cloud ID Service 擴充功能](https://experienceleague.adobe.com/docs/launch/using/extensions-ref/adobe-extension/id-service-extension/overview.html?lang=en)。**必須**&#x200B;為 Adobe Target 更新 [!UICONTROL Experience Cloud ID Service]，才能使用核心服務。(如果您使用 [!UICONTROL Dynamic Tag Management]，請新增 [Adobe Target 工具](https://experienceleague.adobe.com/docs/dtm/using/tools/target.html?lang=en)。您也可以使用 [!UICONTROL Dynamic Tag Management] 來為 Adobe Target 部署 Experience Cloud ID Service。)
* 如果您沒有使用 [!UICONTROL Experience Platform Launch] 或 [!UICONTROL Dynamic Tag Management]，請手動[更新 mbox 程式庫](https://experienceleague.adobe.com/docs/target/using/implement-target/client-side/mbox-implement/target-download-config-mbox.html?lang=en)。
* 請求存取權以使用 Adobe Analytics 作為 [!DNL Adobe Target] 的報表來源。[!DNL Target] 與 資料會在處理期間結合到相同的伺服器呼叫上，使訪客可在兩個解決方案之間連接。[!DNL Analytics]請參閱 [Analytics for Target 實作](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hant)。

   >[!IMPORTANT]
   >
   >所有 Analytics 客戶皆已佈建完成，可使用客戶屬性等核心服務。如果您還不是 Analytics 客戶，請連絡客戶服務，請他們幫您進行佈建。

## 驗證實施 {#section_E641782A0F4F44AF8C9C91216BE330D5}

請使用下列程式，確保Experience CloudID服務已在您的網站上正確實作。

1. 清除您網站的Cookie，以便查看對Experience CloudID服務的要求（要求會在第一次造訪時提出，然後每週每位訪客提出一次）。
1. 使用封包分析工具或網頁瀏覽器偵錯工具中的網路面板，尋找傳至 [!DNL dpm.demdex.net] 的請求。
1. 確認回應中包含 `d_mid` 和一個值，例如：`_setMarketingCloudFields({"d_mid":"4235...`
1. 確認 Analytics 請求中包含 `mid` 參數 (Experience Cloud ID)。在寬限期內 (如果已啟用)，您應該也會看到 `aid` 參數 (Analytics 訪客 ID)。

包含 Experience Cloud ID 的預期回應：

![](assets/mac_id_response.png)

包含 Experience Cloud ID (亦稱為 `mid` 或 _訪客 ID_) 的 Analytics 影像請求：

![](assets/mid.png)

mbox 請求中的 Experience Cloud ID：

![](assets/mbox_request.png)

### 寬限期為何？

部署 Experience Cloud ID Service 後，新的訪客將不會再收到從您的資料收集伺服器傳來的 Analytics Experience Cloud ID。如果您的網站有某些區段尚未實作 ID Service，當訪客瀏覽到這些區段時，將無法識別 Experience Cloud ID，且系統會為訪客指派舊有的 Analytics 訪客 ID。這可能會造成潛在問題，包括重複造訪次數和不正確的歸因。

例如，若您網站的支援區段是在獨立的 CMS 中進行管理，則此區段的 Analytics JavaScript 檔案可能會不同。如果您在將ID服務部署至支援網站之前，先在主網站上部署了Experience CloudID，新訪客造訪支援區段時會收到舊有的Analytics ID。跨兩個網站區段的瀏覽會報告為不同的瀏覽。

將Experience CloudID服務部署在使用多個JavaScript檔案或其他技術(例如Flash)的網站上，可能會造成協調方面的問題。 發生這些問題是因為您必須同時在網站的所有區段上啟用Experience CloudID服務。 借由寬限期的設定，新訪客將繼續從ID服務接收Analytics訪客ID。可在您未升級為使用訪客ID服務的網站區段上，持續識別訪客。

## 管理使用者和產品 {#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF}

在您上手並執行應用程式之後，請導覽至 [Admin Console](https://adminconsole.adobe.com/)，您可在這裡管理使用者和產品設定檔。

![](assets/menu-administration-shell.png)

請參閱 [Experience Cloud 的使用者和產品管理](admin-getting-started.md#topic_3FCB4099640647E3B2411ADBFCE81909)。

### 客戶屬性

新增至[!UICONTROL 客戶屬性]群組的使用者可在Experience Cloud左側看到[!UICONTROL 客戶屬性]功能表項目。

## 開始共用屬性和受眾資料 {#section_960C06093623462E8EA247B3E97274A1}

善用以下核心服務功能。

### [!UICONTROL People > 客戶屬性]

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，請使用[!DNL Adobe Analytics]和[!DNL Adobe Target]中的資料。

請參閱[客戶屬性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1)

### [!UICONTROL People] > [!UICONTROL 受眾程式庫]

Experience Cloud [!UICONTROL Audiences] 介面可讓您建立受眾、組合現有受眾以建立複合受眾，以及檢視所有共用受眾。

請參閱[受眾](audience-library.md#topic_679810123CAA4E0CA4FA3417FB0100C7)

## 資料儲存和隱私洩露

如果您在[!DNL Experience Cloud]Adobe內使用受眾資料即時設定及其他核心服務，則使用這些服務可能會影響您資料所在的資料中心（和國家/地區）。 具體來說，因為[!DNL Experience Cloud]使用Audience Manager,[!UICONTROL People]服務中使用的資料必須位於美國的Audience Manager伺服器。

使用透過[!UICONTROL People]服務提供的服務時，從其他Adobe產品傳送至受眾管理的資料類型為：

* [!DNL Analytics] 金鑰/值配對 (小道具、eVars、清單變數等等)。依預設，記錄行包含 IP 位址，包含 IP 的最後一組八位數 (假設未以 Adobe [!DNL Analytics] 中的 IP 混淆設定修改 IP 位址)。
* 根據 Audience Manager 中設定的規則，訪客符合資格的特徵和區段。
* (選用) 您的一或多個 ID。視您實作的 ID 服務而定，您可能也會傳入一或多個 ID，例如 CRM ID 或雜湊的電子郵件地址。若將此資料傳入 Adobe [!DNL Analytics]，則會將其轉移至 Adobe 受眾管理。Adobe 不建議您將個人資料提供給 Adobe [!DNL Analytics]。更建議先使用單向雜湊來將資料遮罩，再傳送給 Adobe。
* 透過後端區段分享功能，在 [!DNL Analytics] 中建立的區段
* 如未封鎖第三方 cookie，則會設置 demdex.net cookie。`AMCV_###@AdobeOrg` 第一方 Cookie 一律以 Experience Cloud ID Service 設定。

所有這些資料元素都會以記錄檔形式傳送至 Adobe Audience Manager。Audience Manager 會在美國境內處理和儲存這些資料。Audience Manager 不提供在美國境外儲存或處理這些資料的選項。

### Cookie 和退出宣告

使用即時受眾設定檔時，除了使用[!DNL Analytics]和[!DNL Target]的Cookie外，還會使用Audience ManagerCookie。

若要提供適當的退出宣告能力，您網站的訪客必須將 Audience Manager 退出宣告新增至您現有的退出宣告程序。

請參閱 [Adobe Experience Cloud - 實作 Adobe 選擇退出](https://experienceleague.adobe.com/docs/analytics/implementation/js/opt-out.html)以取得指示。

請參閱[資料收集 CNAME 和跨網域追蹤](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/cname.html?lang=en)，以取得啟用跨網域追蹤的相關資訊。
