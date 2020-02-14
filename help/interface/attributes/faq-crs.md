---
description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
keywords: customer attributes
seo-description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
seo-title: 常見問題、限制和最佳作法
solution: Experience Cloud
title: 常見問題、限制和最佳作法
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 670ceb31b40250215d47857102a09c9dfecfb131

---


# 常見問題、限制和最佳作法

Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。

## 最佳作法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

客戶屬性使用指南和限制。

| 問題 | 說明 |
|--- |--- |
| 客戶屬性訂閱限制 | 升級至 Analytics Premium 後，您必須等待 24 小時才可使用其他屬性。在這段期間，您可能會看到已達到屬性訂閱上限錯誤。 |
| 同一裝置上多次登入 | 當使用客戶屬性將客戶個人檔案上傳至資料來源時，Adobe建議使用共用相同裝置的使用者（亦即相同的Experience Cloud ID）。 這麼做可能會導致ECID服務（此服務在裝置上持續存在）在相同的Experience Cloud ID下連結多個使用者，造成非預期的結果 [!DNL Target]。 **** 注意：對於Mobile,ECID在安裝Mobile應用程式後是永久的，您必須重新安裝應用程式才能產生新的ECID。 若是網頁，則會在清除瀏覽器Cookie後產生新的ECID。 |
| 每日頻率上傳限制 | Adobe建議您每天只更新一次客戶屬性。 您至少必須等待24小時，才能為同一組個人檔案上傳另一個客戶個人檔案資料檔案。 |
| Custom Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，當使用 `s.visitorID.`<br>This includes（但不限於）共用觀眾、Analytics for Target(A4T)和客戶屬性來識別訪客時，使用ID服務匯出或匯入Analytics資料的整合將無法運作。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
| Analytics 的字元長度限制 | 建立 Analytics 訂閱時，已上傳檔案的欄位長度會遭到截斷，僅能顯示 255 個字元。 |

## 客戶屬性常見問題 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我能夠收到客戶屬性上傳狀態的相關通知嗎? | 是。請參閱[管理通知](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 剛開始使用客戶屬性時該做什麼? | <ol><li>取得佈建。如果您是 Analytics 客戶，Adobe 會為您佈建客戶屬性。如果您只使用 Target 而且沒有 Analytics，則須聯絡客戶服務，請他們幫您佈建核心服務。</li> <li>與您的 CRM 團隊討論。找出適用於 Analytics 和整個 Experience Cloud 中所需的客戶資料種類。</li><li>實作核心服務。如需 [如何最新化實作的步驟](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) ，請參閱啟用核心服務的解決方案。 (請參閱同步客戶 ID 做為重要資訊一節)</li></ol> **附註:** 有關實作核心服務的管理員常見問題集可在[此處](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)取得。 |
| 我可以使用多少個客戶屬性? | You can upload hundreds of `.csv` columns to the customer attribute service. 不過，在設定訂閱和選取屬性時，會根據您擁有的解決方案，套用下列限制（每個報表套裝）:  <ul><li>Foundation: 0 個</li><li>Select: 3 個</li><li>Prime: 15 個</li><li>Ultimate: 200 個</li><li>Standard 版: 共 3 個</li><li>Premium:200</li><li>Target Standard: 5 個</li><li>Target Premium: 200 個</li></ul> |
| 一定要移轉至 Experience Cloud ID 服務嗎? | 是否移轉取決於您使用的解決方案。 <ul><li>Adobe Analytics: 強烈建議 </li><li>Adobe Target: 必要。 </li></ul><br>使用 ID 服務可提升功能，開啟一道使用最新 Experience Cloud 功能的方便之門，包括即時受眾、Target 最新化、Analytics 整合、視訊心率追蹤。<br> 如需詳細資訊，請 [參閱啟用核心服務的解決方案](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** [Experience Cloud ID服務是先前稱為](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html)_Analytics訪客ID服務的現代化實作。_ |
| 客戶屬性功能與 Adobe Audience Manager 有何關係? | Audience Manager 可以接收資料以執行受眾識別，但不能執行將屬性聯結至歷史行為資料的分析功能，也不能提供 Adobe Analytics 中的報告、分析及區隔功能。「People」核心服務將來自各解決方案的豐富資料串連起來，並與單一 ID 建立關聯，以便在整個 Experience Cloud 之中使用。<br>在 Adobe Target 中，客戶屬性顯示為個別屬性，可與其他規則結合以建立受眾。「People」核心服務中共用的受眾是無法修改的完整受眾。 |
| **(僅限 Analytics)**&#x200B;這項功能與 Analytics Premium 提供的有何差異? | 在過去，有意結合客戶屬性資料與 Analytics 資料的客戶，十分依賴此功能的資料工作台工具。客戶屬性提供客戶屬性做為 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 中的維度和度量，將此功能開放給更廣大的受眾。Analytics Standard 的客戶將可存取客戶屬性，但可使用的功能有限。Analytics Premium 的客戶則可使用完整功能。 |
| **(僅限 Target)** 我是否能為客戶預先載入或上傳 Target 中不曾出現的資料嗎? | 是。訪客第一次向 Taget 提出要求時，系統會從「客戶屬性」擷取現有的相關資料，並使用此資料進行鎖定。**附註:** 如果訪客是第一次與 Target 互動，則擷取此資料可能需花費 20 分鐘。 |
| **(僅限 Target)** 我是否能結合客戶屬性資料和共用的受眾資料來建立超級受眾? | 不會。共用的受眾資料已經是建立完畢的受眾。 |
| **(僅限 Target)**&#x200B;客戶屬性功能與 Target 大量設定檔 API 有何差異? | 大量設定檔 API 可以透過 API 以個別或大量的方式直接更新 Target 設定檔。其功能類似於客戶屬性，但有下列幾點重要差異:<ul><li>設定檔 API 是 REST API 呼叫，而客戶屬性使用 FTP。</li><li>Target 的設定檔 API 只會傳送資料給 Target，而非整個 Experience Cloud。</li><li>客戶屬性提供簡單介面，用於建立和管理此外部資料。 | </li></ul> |
| **(僅限 Target)** 從客戶屬性上傳資料至 Adobe Target 是否能延長 Target 訪客設定檔期限? | 是。請參閱 Adobe Target 說明中的[訪客設定檔期限](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **(僅限 Target)** 從客戶 ID 辨別出訪客後，我可以立即鎖定上傳至客戶屬性中的資料嗎? | 是。在對 Target 進行的伺服器呼叫後，由於此呼叫包含 mbox 第三方 ID，因此所有客戶屬性資料都可供使用。 |
| **（僅限Target）** 「同步狀態」欄 **** 對於「客戶屬性來源」中上傳的檔案代表什麼？ | 按一下特定屬性檔案的「同步狀態」圖示，即可檢視Target所發佈和同步的記錄數。 `Sync %` 是一個即時度量，它指定在Target中同步的設定檔百分比。<br> **** 注意：屬性與Target同步可能需要24小時。 |
| 檔案上傳量度在「客戶屬性來源」中代表什麼？ | 您可以透過下列度量的協助，檢查上傳至「客戶屬性」的屬性狀態： <ul><li>記錄： 屬性檔案中的記錄數。</li><li>**** 新記錄：屬性檔案中存在的新記錄數。</li> <li>**** 更新記錄：客戶屬性中已存在且檔案中具有更新值的記錄數。</li><li>**** 所有資料（記錄）:成功上傳至客戶屬性的記錄總數。</li></ul> |
