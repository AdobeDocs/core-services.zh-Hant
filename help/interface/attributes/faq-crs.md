---
description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
keywords: customer attributes
seo-description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
seo-title: 常見問題、限制和最佳作法
solution: Experience Cloud
title: 常見問題、限制和最佳作法
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 常見問題、限制和最佳作法

Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。

## 最佳作法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用客戶屬性時的指 [!UICONTROL 引和限制]。

| 問題 | 說明 |
|--- |--- |
| [!UICONTROL 客戶屬性] 、訂閱限制 | 當您升級至Analytics Premium時，會有24小時的延遲，才會有其他屬性可用。 在這段期間，您可能會看到已達到屬性訂閱上限錯誤。 |
| 同一裝置上多次登入 | 當使用客戶屬性將客戶個人檔案上傳至資料來源時，Adobe建議使用共用相同裝置的使用者（亦即相同的Experience Cloud ID）。 這麼做可能會導致ECID服務（此服務在裝置上持續存在）在相同的Experience Cloud ID下連結多個使用者，造成非預期的結果 [!DNL Target]。 **注意：** 對於Mobile,ECID在安裝Mobile應用程式後是永久的，您必須重新安裝應用程式才能產生新的ECID。 若是網頁，則會在清除瀏覽器Cookie後產生新的ECID。 |
| 每日頻率上傳限制 | Adobe建議您每天只更新一次客戶屬性。 您至少必須等待24小時，才能為同一組個人檔案上傳另一個客戶個人檔案資料檔案。 |
| 自訂分析ID(`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，當使用 `s.visitorID.`<br>This includes，但不限於共用觀眾、Adobe Target(A4T)的Analytics資料和客戶屬性來識別訪客時，使用ID服務匯出或匯入Analytics資料的整合將無法運作。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
| Analytics中的字元長度限制 | 建立Analytics訂閱時，已上傳檔案的欄位長度會截斷為255。 |

## 關於客戶屬性的常見問答集 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我是否可收到有關客戶屬性上傳狀態的通知？ | 是。請參閱[管理通知](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 我該如何開始使用客戶屬性？ | <ol><li>獲得布建。 如果您是Analytics客戶，Adobe會針對客戶屬性為您布建。 如果您只使用Adobe Target而沒有Analytics，則必須聯絡客戶服務以要求核心服務的布建。</li> <li>與您的CRM團隊進行交談。 瞭解在Analytics和整個Experience Cloud中使用的客戶資料有哪些有趣。</li><li>實作核心服務。 如需 [如何最新化實作的步驟](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html) ，請參閱啟用核心服務的解決方案。 （如需重要資訊，請參閱同步化客戶ID一節。）</li></ol> **注意：** 這裡提供實作核心服務的管理員常見問 [答集](https://docs.adobe.com/content/help/en/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)。 |
| 我可以使用多少個客戶屬性? | You can upload hundreds of `.csv` columns to the customer attribute service. 不過，在設定訂閱和選取屬性時，會根據您擁有的解決方案，套用下列限制（每個報表套裝）:  <ul><li>Foundation: 0 個</li><li>Select: 3 個</li><li>Prime: 15 個</li><li>Ultimate: 200 個</li><li>Standard 版: 共 3 個</li><li>Premium:200</li><li>Adobe Target Standard:5</li><li>Adobe Target Premium:200</li></ul> |
| 是否需要移轉至Experience Cloud ID服務？ | 移轉取決於您使用的解決方案。 <ul><li>Adobe Analytics: 強烈建議 </li><li>Adobe Target:必要。 </li></ul><br> 使用ID服務可增強功能，為使用最新Experience Cloud功能開啟大門，包括即時觀眾、Adobe Target現代化、Analytics整合和視訊心率追蹤。 <br> 如需詳細資訊，請 [參閱啟用核心服務的解決方案](https://docs.adobe.com/content/help/en/core-services/interface/about-core-services/core-services.html)。 <br>**注意：** [Experience Cloud ID服務是先前稱為](https://docs.adobe.com/content/help/en/id-service/using/intro/overview.html)_Analytics訪客ID服務的現代化實作。_ |
| 客戶屬性功能與Adobe Audience Manager有何關係？ | 雖然Audience Manager可接收資料以執行觀眾識別，但無法執行將屬性系結至歷史行為資料的分析功能，或提供Adobe Analytics中可用的報告、分析和區段功能。 People核心服務可讓各解決方案的豐富資料連結在一起，並與單一ID關聯，以便在Experience Cloud中使用。 <br>在Adobe Target中，客戶屬性會顯示為個別屬性，可與其他規則結合以建立觀眾。 「人員」核心服務中共用的觀眾是無法修改的完整觀眾。 |
| **（僅限Analytics）** ，此功能與Analytics Premium中提供的功能有何不同？ | 過去，有意將客戶屬性資料與Analytics資料結合的客戶，對這項功能的依賴度很大。 客戶屬性提供客戶屬性作為報告與分析、臨機分析和報告建立工具中的維度和量度，讓更廣大的觀眾可以看到此功能。 Analytics Standard客戶將可存取客戶屬性，但功能有限。 Analytics Premium客戶可使用完整功能。 |
| **（僅限Adobe Target）** ，我是否可為Adobe Target從未看過的客戶預先載入或上傳資料？ | 是。當訪客第一次向Adobe Target要求時，系統會從「客戶屬性」擷取我們現有的有關他們的資訊，並使用該資料進行定位。 **注意：** 從訪客與Adobe Target的首次互動中擷取此資料最多需要20分鐘。 |
| **（僅限Adobe Target）** ，我是否可結合客戶屬性資料和共用的觀眾資料來建立超級觀眾？ | 不會。共用的觀眾資料是已完成的觀眾。 |
| **（僅限Adobe Target）** ，客戶屬性功能與Adobe Target的大量設定檔API有何不同？ | 大量描述檔API可讓Adobe Target描述檔直接透過API更新，不論是個別描述檔或大量更新。 此功能與客戶屬性類似，具有以下主要差異：<ul><li>描述檔API是REST API呼叫，客戶屬性使用FTP。</li><li>Adobe Target的設定檔API只會將資料傳送至Adobe Target，而非整個Experience Cloud。</li><li>客戶屬性提供簡單的介面來建立和管理此外部資料。</li></ul> |
| **（僅限Adobe Target）** ，從客戶屬性上傳資料至Adobe Target是否會延長Adobe Target訪客的描述檔存留期？ | 是。請參閱 Adobe Target 說明中的[訪客設定檔期限](https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **（僅限Adobe Target）** ，我是否可在客戶ID識別訪客後，立即鎖定在客戶屬性中上傳的資料？ | 是。在對Adobe Target的伺服器呼叫（包括mbox協力廠商ID）時，所有客戶屬性資料都將可供使用。 |
| **（僅限Adobe Target）** 「同步狀態」欄 **** 代表哪些檔案已上傳至客戶屬性來源？ | 按一下特定屬性檔案的「同步狀態」圖示，即可檢視Adobe Target所發佈和同步的記錄數。 `Sync %` 是即時度量，可指定在Adobe Target中同步的設定檔百分比。<br> **注意：** 屬性與Adobe Target同步可能需要24小時。 |
| 檔案上傳量度在「客戶屬性來源」中代表什麼？ | 您可以透過下列度量的協助，檢查上傳至「客戶屬性」的屬性狀態： <ul><li>記錄： 屬性檔案中的記錄數。</li><li>**新記錄：** 屬性檔案中存在的新記錄數。</li> <li>**更新記錄：** 客戶屬性中已存在且檔案中具有更新值的記錄數。</li><li>**所有資料（記錄）:** 成功上傳至客戶屬性的記錄總數。</li></ul> |
