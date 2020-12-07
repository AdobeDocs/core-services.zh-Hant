---
description: 有關Adobe Experience Cloud中Adobe Analytics和Adobe Target客戶屬性的常見問題。
keywords: Customer Attributes
solution: Experience Cloud
title: 取得有關客戶屬性的常見問題解答 | Adobe Experience Cloud
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: dae4bbecc05ed6a78470354f82e4e3cd8f003660
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 96%

---


# 常見問題、限制和最佳作法

Adobe Analytics和Adobe Target中客戶屬性的常見問題和最佳實務。

## 最佳作法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用[!UICONTROL 客戶屬性]的相關指引和限制。

| 問題 | 說明 |
|--- |--- |
| [!UICONTROL 客戶屬性]訂閱限制 | 升級至 Analytics Premium 後，必須等待 24 小時才能使用更多屬性。在這段期間，您可能會看到已達到屬性訂閱上限錯誤。 |
| 同一部裝置上多次登入 | 使用客戶屬性將客戶設定檔上傳至資料來源時，Adobe 不建議使用者共用裝置 (亦即使用相同的 Experience Cloud ID)。Experience Cloud ID (ECID) 會留存於裝置上。如果共用裝置，可能使多個使用者連結至相同的 ECID，導致 [!DNL Target] 出現非預期的結果。**注意：**&#x200B;若使用行動裝置，行動應用程式安裝後 ECID 會永久存在。您必須重新安裝應用程式，才能產生新的 ECID。若使用網頁，系統會在瀏覽器 Cookie 清除後產生新的 ECID。 |
| 每日頻率上傳限制 | Adobe 建議每天只需更新一次客戶屬性。您至少必須等待 24 小時，才能為同一組設定檔上傳另一個客戶設定檔資料檔案。 |
| 自訂 Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，使用 `s.visitorID.`<br> 來識別訪客時，透過 ID Service 匯出或匯入 Analytics 資料的整合功能將無法使用，其中包含但不限於共用受眾、Analytics for Adobe Target (A4T) 和客戶屬性。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
| Analytics 中的字元長度限制 | 建立 Analytics 訂閱時，會將已上傳檔案的欄位長度截斷為 255。 |

## 客戶屬性的相關常見問題集 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我能否收到客戶屬性上傳狀態的通知？ | 可以。請參閱[管理通知](https://docs.adobe.com/content/help/zh-Hant/core-services/interface/manage-users-and-products/organizations.html#concept_0105453AD71847B8BFCAF4A40915F157)。 |
| 該如何開始使用客戶屬性？ | <ol><li>完成佈建程序。如果您是 Analytics 客戶，Adobe 會針對客戶屬性為您完成佈建。如果您只使用 Adobe Target 而沒有使用 Analytics，請連絡客戶服務，申請佈建核心服務。</li> <li>與您的 CRM 團隊溝通。了解在 Analytics 和整個 Experience Cloud 可用的客戶資料中，有哪些您想要使用。</li><li>實作核心服務。如需導入最新實作的步驟，請參閱[啟用核心服務的解決方案](https://docs.adobe.com/content/help/zh-Hant/core-services/interface/about-core-services/core-services.html)(如需重要資訊，請參閱同步化客戶 ID 的相關章節)。</li></ol> **注意：**[這裡](https://docs.adobe.com/content/help/zh-Hant/core-services/interface/manage-users-and-products/faq.html#concept_13219B4E51784577B6FF78AAA203DE91)提供實作核心服務的管理員常見問題集。 |
| 我可以使用多少個客戶屬性？ | 您可以將數百個 `.csv` 欄上傳至客戶屬性服務。但是在設定訂閱與選取屬性時，系統會根據您擁有的解決方案，套用以下欄數限制 (針對每個報表套裝)：  <ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：200 個</li><li>Adobe Target Standard：5 個</li><li>Adobe Target Premium：200 個</li></ul> |
| 是否需要移轉至 Experience Cloud ID Service？ | 是否需移轉取決於您使用的解決方案。 <ul><li>Adobe Analytics：強烈建議 </li><li>Adobe Target：必須移轉。 </li></ul><br>使用 Experience Cloud ID 服務會啟用最新的 Experience Cloud 功能，包括即時受眾、Adobe Target 現代化、Analytics 整合和視訊活動訊號追蹤。<br> 如需詳細資訊，請參閱[啟用核心服務的解決方案](https://docs.adobe.com/content/help/zh-Hant/core-services/interface/about-core-services/core-services.html)。<br>**注意：**[Experience Cloud ID Service](https://docs.adobe.com/content/help/zh-Hant/id-service/using/intro/overview.html) 是前身為 _Analytics 訪客 ID 服務_&#x200B;的新式實作。 |
| 客戶屬性功能與 Adobe Audience Manager 有何關係？ | 雖然 Audience Manager 可接收資料以辨識受眾，但無法執行將屬性與過往行為資料關聯的分析功能，亦無法提供 Adobe Analytics 中可使用的報表、分析和分段功能。[!UICONTROL People] 可讓不同解決方案的豐富資料繫結在一起，並與單一 ID 建立關聯，以便在 Experience Cloud 中使用。<br>Adobe Target 中，客戶屬性會顯示為個別屬性，可與其他規則結合以建立受眾。共用給 [!UICONTROL People] 服務的受眾是無法修改的完整受眾。 |
| **(僅限 Analytics)** 此功能與 Analytics Premium 中提供的功能有何不同？ | 過去，有意將客戶屬性資料與 Analytics 資料結合的客戶，為了這項功能對 Data Workbench 的依賴程度很高。客戶屬性可作為 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 的維度和量度使用，因此可供更廣大的受眾運用。Analytics Standard 客戶可存取客戶屬性，但可使用的功能有限。Analytics Premium 客戶可使用完整功能。 |
| **(僅限 Adobe Target)** 我是否可以預先載入或上傳 Adobe Target 從未看過的客戶資料？ | 是。訪客第一次向 Adobe Target 提出請求時，系統會從「客戶屬性」擷取與他們有關的現有資訊，並使用這些資料進行目標鎖定。**注意：**&#x200B;如果訪客是第一次與 Adobe Target 互動，則擷取此資料可能需花費最長達 20 分鐘。 |
| **(僅限 Adobe Target)** 我是否可藉由結合客戶屬性資料和共用的受眾資料來建立超級受眾？ | 不會。共用的受眾資料是已完成的受眾。 |
| **(僅限 Adobe Target)** 客戶屬性功能與 Adobe Target 的大量設定檔 API 有何不同？ | 大量設定檔 API 可以透過 API 以個別或大量的方式直接更新 Adobe Target 設定檔。此功能與客戶屬性類似，主要差異如下：<ul><li>設定檔 API 是一種 REST API 呼叫，而客戶屬性會使用 FTP。</li><li>Adobe Target 的設定檔 API 只會將資料傳送至 Adobe Target，而非整個 Experience Cloud。</li><li>客戶屬性提供簡單的介面，用於建立和管理這些外部資料。</li></ul> |
| **(僅限 Adobe Target)** 以客戶屬性將資料上傳至 Adobe Target 是否會延長 Adobe Target 訪客的設定檔存留期？ | 是。請參閱 Adobe Target 說明中的[訪客設定檔存留期](https://docs.adobe.com/content/help/zh-Hant/target/using/audiences/visitor-profiles/visitor-profile.html)。 |
| **(僅限 Adobe Target)** 我是否可在透過客戶 ID 識別訪客後，立即鎖定客戶屬性所上傳的資料？ | 是。對 Adobe Target 發出伺服器呼叫時 (包括 mbox 第三方 ID)，所有客戶屬性資料都將可供使用。 |
| **(僅限 Adobe Target)** 對於已上傳至客戶屬性來源的檔案而言，**[!UICONTROL 同步狀態]**&#x200B;欄代表什麼？ | 對特定屬性檔案按一下「同步狀態」圖示，即可檢視 Adobe Target 所發佈和同步的記錄數。`Sync %` 是即時量度，指出 Adobe Target 中已同步的設定檔百分比。<br> **注意：**&#x200B;與 Adobe Target 同步屬性可能需花費最多 24 小時。 |
| 「客戶屬性來源」中的檔案上傳量度代表什麼？ | 在下列量度的協助下，您可以檢查已上傳至「客戶屬性」的屬性之狀態： <ul><li>記錄數：屬性檔案中的記錄數。</li><li>**新記錄數：**&#x200B;屬性檔案中存在的新記錄數。</li> <li>**更新記錄數：**&#x200B;客戶屬性中已存在且檔案中有更新值的記錄數。</li><li>**所有資料 (記錄) 數：**&#x200B;已成功上傳至客戶屬性的記錄總數。</li></ul> |
