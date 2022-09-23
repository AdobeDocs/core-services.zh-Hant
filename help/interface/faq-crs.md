---
description: Adobe Experience Cloud 中 Adobe Analytics 和 Adobe Target 客戶屬性的常見問題。
solution: Experience Cloud
title: 獲得有關客戶屬性的常見問題解答
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: eb2ad8a8255915be47b6002a78cc810b522170d2
workflow-type: tm+mt
source-wordcount: '1176'
ht-degree: 100%

---

# 關於[!UICONTROL 客戶屬性]的常見問答

Adobe Analytics 和 Adobe Target 中[!UICONTROL 客戶屬性]的常見問題和最佳做法。

## 最佳做法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用[!UICONTROL 客戶屬性]的相關指引和限制。

| 問題 | 說明 |
|--- |--- |
| [!UICONTROL 客戶屬性]訂閱限制 | 升級至 Analytics Premium 後，必須等待 24 小時才能使用更多屬性。在這段延遲期間，您可能會看到已核發的[!UICONTROL 屬性訂閱上限]錯誤。 |
| 同一部裝置上多次登入 | 使用[!UICONTROL 客戶屬性]將客戶個人資料上傳至資料來源時，Adobe 不建議使用者共用相同的裝置 (亦即相同的 Experience Cloud ID)。Experience Cloud ID (ECID) 會留存於裝置上。如果共用裝置，可能使多個使用者連結至相同的 ECID，導致 [!DNL Target] 出現非預期的結果。**注意：**&#x200B;若使用行動裝置，行動應用程式安裝後 ECID 會永久存在。重新安裝應用程式以產生新的 ECID。若使用網頁，系統會在瀏覽器 Cookie 清除後產生新的 ECID。 |
| 每日頻率上傳限制 | Adobe 建議每天只需更新一次客戶屬性。您至少必須等待 24 小時，才能為同一組個人資料上傳另一個客戶個人資料資料檔案。 |
| 自訂 Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，使用 `s.visitorID.`<br> 來識別訪客時，透過 ID Service 匯出或匯入 [!DNL Analytics] 資料的整合功能無法使用，其中包含但不限於共用對象、Adobe Target (A4T) 的 [!DNL Analytics] 和[!UICONTROL 客戶屬性]。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
|  中的字元長度限制[!DNL Analytics] | 建立 [!DNL Analytics] 訂閱時，已上傳檔案的欄位長度會截斷為 255。 |

{style=&quot;table-layout:auto&quot;}

## 客戶屬性的相關常見問題集 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我能否收到客戶屬性上傳狀態的通知？ | 可以。 |
| 該如何開始使用客戶屬性？ | <ol><li>完成佈建程序。如果您是 Analytics 客戶，Adobe 會針對客戶屬性為您完成佈建。如果您只使用 Adobe Target 而沒有使用 Analytics，請連絡客戶服務，申請佈建核心服務。</li> <li>與您的 CRM 團隊溝通。了解在 Analytics 和整個 Experience Cloud 可用的客戶資料中，有哪些您想要使用。</li><li>實作核心服務。 如需如何導入最新實作的步驟，請參閱[為核心服務啟用您的應用程式](core-services.md)。(如需重要資訊，請參閱同步化客戶 ID 的相關章節)。</li></ol> **注意：**[這裡](faq.md)提供實作核心服務的管理員常見問題集。 |
| 我可以使用多少個客戶屬性？ | 您可以將數百個 `.csv` 欄上傳至客戶屬性服務。但是在設定訂閱及選取屬性時，系統會根據您擁有的應用程式套用以下限制 (針對每個報表套裝)：  <ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：200 個</li><li>Adobe Target Standard：5 個</li><li>Adobe Target Premium：200 個</li></ul> |
| 是否需要移轉至 Experience Cloud ID Service？ | 是否需移轉取決於您使用的應用程式。 <ul><li>Adobe Analytics：強烈建議 </li><li>Adobe Target：必須移轉。 </li></ul><br>使用 Experience Cloud ID 服務會啟用最新的 Experience Cloud 功能，包括即時對象、Adobe Target 現代化、Analytics 整合和視訊活動訊號追蹤。<br>如需詳細資訊，請參閱[為核心服務啟用您的應用程式](core-services.md)。 <br>**注意：**[Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant) 是前身為 _Analytics 訪客 ID 服務_&#x200B;的新式實作。 |
| 客戶屬性功能與 Adobe Audience Manager 有何關係？ | 雖然 Audience Manager 可接收資料以辨識對象，但無法執行將屬性與過往行為資料關聯的分析功能，亦無法提供 Adobe Analytics 中可使用的報表、分析和分段功能。[!UICONTROL People] 可讓不同應用程式的豐富資料繫結在一起，並與單一 ID 建立關聯，以便在 Experience Cloud 中使用。 <br>Adobe Target 中，客戶屬性會顯示為個別屬性，可與其他規則結合以建立對象。共用給 [!UICONTROL People] 服務的對象是無法修改的完整對象。 |
| **(僅限 Analytics)** 此功能與 Analytics Premium 中提供的功能有何不同？ | 過去，有意將客戶屬性資料與 Analytics 資料結合的客戶，為了這項功能對 Data Workbench 的依賴程度很高。[!UICONTROL 客戶屬性]可作為 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 的維度和量度使用，因此可供更廣大的對象運用。Analytics Standard 客戶可存取客戶屬性，但可用的功能有限。Analytics Premium 客戶可使用完整功能。 |
| **(僅限 Adobe Target)** 我是否可以預先載入或上傳 Adobe Target 從未看過的客戶資料？ | 可以。訪客第一次向 Adobe Target 提出請求時，系統會從「客戶屬性」擷取與 Adobe 有關的現有資訊，並使用這些資料進行目標鎖定。**注意：**&#x200B;如果訪客是第一次與 Adobe Target 互動，則擷取此資料可能需花費最長達 20 分鐘。 |
| **(僅限 Adobe Target)** 我是否可藉由結合客戶屬性資料和共用的對象資料來建立超級對象？ | 不可以。共用的對象資料是已完成的對象。 |
| **(僅限 Adobe Target)**[!UICONTROL  客戶屬性功能與 Adobe Target 的大量個人資料 API 有何不同？] | 大量個人資料 API 可以透過 API 以個別或大量的方式直接更新 Adobe Target 個人資料。此功能與客戶屬性類似，主要差異如下：<ul><li>個人資料 API 是一種 REST API 呼叫，而客戶屬性會使用 FTP。</li><li>Adobe Target 的個人資料 API 只會將資料傳送至 Adobe Target，而非整個 Experience Cloud。</li><li>客戶屬性提供簡單的介面，用於建立和管理這些外部資料。</li></ul> |
| **(僅限 Adobe Target)** 以客戶屬性將資料上傳至 Adobe Target 是否會延長 Adobe Target 訪客的個人資料存留期？ | 是。請參閱 Adobe Target 說明中的[訪客個人資料存留期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=zh-Hant)。 |
| **(僅限 Adobe Target)** 我是否可在透過客戶 ID 識別訪客後，立即鎖定客戶屬性所上傳的資料？ | 可以。對 Adobe Target 發出伺服器呼叫時 (包括 mbox 協力廠商 ID)，所有客戶屬性資料都可供使用。 |
| **(僅限 Adobe Target)** 對於已上傳至客戶屬性來源的檔案而言，**[!UICONTROL 同步狀態]**&#x200B;欄代表什麼？ | 對特定屬性檔案選取「同步狀態」圖示，即可檢視 Adobe Target 所發佈和同步的記錄數。 `Sync %` 是即時量度，可指明 Adobe Target 中已同步的個人資料百分比。<br> **注意：**&#x200B;與 Adobe Target 同步屬性可能需花費最多 24 小時。 |
| 「客戶屬性來源」中的檔案上傳量度代表什麼？ | 在下列量度的協助下，您可以檢查已上傳至「客戶屬性」的屬性之狀態： <ul><li>記錄數：屬性檔案中的記錄數。</li><li>**新記錄數：**&#x200B;屬性檔案中存在的新記錄數。</li> <li>**更新記錄數：** 存在於客戶屬性中且檔案中有更新值的記錄數。</li><li>**所有資料 (記錄) 數：**&#x200B;已成功上傳至客戶屬性的記錄總數。</li></ul> |

{style=&quot;table-layout:auto&quot;}