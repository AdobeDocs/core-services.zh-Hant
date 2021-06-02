---
description: Adobe Experience Cloud 中 Adobe Analytics 和 Adobe Target 客戶屬性的常見問題。
keywords: 客戶屬性
solution: Experience Cloud
title: '獲得有關客戶屬性的常見問題解答 '
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: 客戶屬性
topic: 管理
role: Administrator
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '1216'
ht-degree: 73%

---

# 關於[!UICONTROL 客戶屬性]的常見問題

Adobe Analytics和Adobe Target中[!UICONTROL 客戶屬性]的常見問題和最佳作法。

## 最佳做法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用[!UICONTROL 客戶屬性]的相關指引和限制。

| 問題 | 說明 |
|--- |--- |
| [!UICONTROL 客戶屬性]訂閱限制 | 升級至 Analytics Premium 後，必須等待 24 小時才能使用更多屬性。在此延遲期間，您可能會看到發生[!UICONTROL 屬性訂閱上限]錯誤。 |
| 同一部裝置上多次登入 | 使用[!UICONTROL 客戶屬性]將客戶設定檔上傳至資料來源時，Adobe不建議使用者共用裝置(亦即使用相同的Experience CloudID)。 Experience Cloud ID (ECID) 會留存於裝置上。如果共用裝置，可能使多個使用者連結至相同的 ECID，導致 [!DNL Target] 出現非預期的結果。**注意：**&#x200B;若使用行動裝置，行動應用程式安裝後 ECID 會永久存在。您必須重新安裝應用程式，才能產生新的 ECID。若使用網頁，系統會在瀏覽器 Cookie 清除後產生新的 ECID。 |
| 每日頻率上傳限制 | Adobe 建議每天只需更新一次客戶屬性。您至少必須等待 24 小時，才能為同一組設定檔上傳另一個客戶設定檔資料檔案。 |
| 自訂 Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，使用`s.visitorID.`<br>來識別訪客時，透過ID Service匯出或匯入[!DNL Analytics]資料的整合無法運作。這包括但不限於共用受眾、Adobe Target適用的[!DNL Analytics]和[!UICONTROL 客戶屬性]。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
|  中的字元長度限制[!DNL Analytics] | 建立[!DNL Analytics]訂閱時，上傳檔案的欄位長度會截斷為255。 |

## 客戶屬性的相關常見問題集 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我能否收到客戶屬性上傳狀態的通知？ | 可以。請參閱[管理通知](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html?lang=en)。 |
| 該如何開始使用客戶屬性？ | <ol><li>完成佈建程序。如果您是 Analytics 客戶，Adobe 會針對客戶屬性為您完成佈建。如果您只使用 Adobe Target 而沒有使用 Analytics，請連絡客戶服務，申請佈建核心服務。</li> <li>與您的 CRM 團隊溝通。了解在 Analytics 和整個 Experience Cloud 可用的客戶資料中，有哪些您想要使用。</li><li>實作核心服務。如需導入最新實作的步驟，請參閱[啟用核心服務的解決方案](https://experienceleague.adobe.com/docs/core-services/interface/about-core-services/core-services.html?lang=en)(如需重要資訊，請參閱同步化客戶 ID 的相關章節)。</li></ol> **注意：**[這裡](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/faq.html?lang=en)提供實作核心服務的管理員常見問題集。 |
| 我可以使用多少個客戶屬性？ | 您可以將數百個 `.csv` 欄上傳至客戶屬性服務。但是在設定訂閱與選取屬性時，系統會根據您擁有的解決方案，套用以下欄數限制 (針對每個報表套裝)：  <ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：200 個</li><li>Adobe Target Standard：5 個</li><li>Adobe Target Premium：200 個</li></ul> |
| 是否需要移轉至 Experience Cloud ID Service？ | 是否需移轉取決於您使用的解決方案。 <ul><li>Adobe Analytics：強烈建議 </li><li>Adobe Target：必須移轉。 </li></ul><br>使用 Experience Cloud ID 服務會啟用最新的 Experience Cloud 功能，包括即時受眾、Adobe Target 現代化、Analytics 整合和視訊活動訊號追蹤。<br> 如需詳細資訊，請參閱[啟用核心服務的解決方案](https://experienceleague.adobe.com/docs/core-services/interface/about-core-services/core-services.html?lang=en)。<br>**注意：**[Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en) 是前身為 _Analytics 訪客 ID 服務_&#x200B;的新式實作。 |
| 客戶屬性功能與 Adobe Audience Manager 有何關係？ | 雖然 Audience Manager 可接收資料以辨識受眾，但無法執行將屬性與過往行為資料關聯的分析功能，亦無法提供 Adobe Analytics 中可使用的報表、分析和分段功能。[!UICONTROL People] 可讓不同解決方案的豐富資料繫結在一起，並與單一 ID 建立關聯，以便在 Experience Cloud 中使用。<br>Adobe Target 中，客戶屬性會顯示為個別屬性，可與其他規則結合以建立受眾。共用給 [!UICONTROL People] 服務的受眾是無法修改的完整受眾。 |
| **(僅限 Analytics)** 此功能與 Analytics Premium 中提供的功能有何不同？ | 過去，有意將客戶屬性資料與Analytics資料結合的客戶，對這項功能大量依賴Data Workbench工具。 [!UICONTROL 「客] 戶屬性」可將「客戶屬性」作為Reports &amp; Analytics、Ad Hoc Analysis和Report Builder中的維度和量度，借此將此功能賦予更廣大的受眾。Analytics Standard客戶可存取客戶屬性，但功能有限。 Analytics Premium 客戶可使用完整功能。 |
| **(僅限 Adobe Target)** 我是否可以預先載入或上傳 Adobe Target 從未看過的客戶資料？ | 是。當訪客首次向Adobe Target提出請求時，系統會從客戶屬性擷取Adobe現有的相關資訊，並使用該資料進行目標定位。 **注意：**&#x200B;如果訪客是第一次與 Adobe Target 互動，則擷取此資料可能需花費最長達 20 分鐘。 |
| **(僅限 Adobe Target)** 我是否可藉由結合客戶屬性資料和共用的受眾資料來建立超級受眾？ | 不會。共用的受眾資料是已完成的受眾。 |
| **(僅限 Adobe Target)**[!UICONTROL  客戶屬性功能與 Adobe Target 的大量設定檔 API 有何不同？] | 大量設定檔 API 可以透過 API 以個別或大量的方式直接更新 Adobe Target 設定檔。此功能與客戶屬性類似，主要差異如下：<ul><li>設定檔 API 是一種 REST API 呼叫，而客戶屬性會使用 FTP。</li><li>Adobe Target 的設定檔 API 只會將資料傳送至 Adobe Target，而非整個 Experience Cloud。</li><li>客戶屬性提供簡單的介面，可建立和管理此外部資料。</li></ul> |
| **(僅限 Adobe Target)** 以客戶屬性將資料上傳至 Adobe Target 是否會延長 Adobe Target 訪客的設定檔存留期？ | 是。請參閱 Adobe Target 說明中的[訪客設定檔存留期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=en)。 |
| **(僅限 Adobe Target)** 我是否可在透過客戶 ID 識別訪客後，立即鎖定客戶屬性所上傳的資料？ | 可以。在對Adobe Target的伺服器呼叫（包括mbox協力廠商ID）上，所有客戶屬性資料皆可用。 |
| **(僅限 Adobe Target)** 對於已上傳至客戶屬性來源的檔案而言，**[!UICONTROL 同步狀態]**&#x200B;欄代表什麼？ | 對特定屬性檔案按一下「同步狀態」圖示，即可檢視 Adobe Target 所發佈和同步的記錄數。`Sync %` 是即時量度，指定已在Adobe Target中同步的設定檔百分比。<br> **注意：**&#x200B;與 Adobe Target 同步屬性可能需花費最多 24 小時。 |
| 「客戶屬性來源」中的檔案上傳量度代表什麼？ | 在下列量度的協助下，您可以檢查已上傳至「客戶屬性」的屬性之狀態： <ul><li>記錄數：屬性檔案中的記錄數。</li><li>**新記錄數：**&#x200B;屬性檔案中存在的新記錄數。</li> <li>**更新記錄數：** 客戶屬性中存在且檔案中有更新值的記錄數。</li><li>**所有資料 (記錄) 數：**&#x200B;已成功上傳至客戶屬性的記錄總數。</li></ul> |
