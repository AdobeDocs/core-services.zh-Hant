---
description: 關於的常見問題 [!DNL Customer Attributes] Adobe Experience Cloud中的Adobe Analytics和Adobe Target專用。
solution: Experience Cloud
title: 關於的常見問題 [!DNL Customer Attributes]
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: f229ec33ff721527e6a4c920ea63eabb4102935a
workflow-type: tm+mt
source-wordcount: '1102'
ht-degree: 64%

---

# 關於的常見問題 [!DNL Customer Attributes]

常見問題集和最佳作法 [!DNL Customer Attributes] 在Adobe Analytics和Adobe Target中。

## 最佳做法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

使用時的指引和限制 [!DNL Customer Attributes].

| 問題 | 說明 |
|--- |--- |
| [!UICONTROL 客戶屬性]訂閱限制 | 升級至 Analytics Premium 後，必須等待 24 小時才能使用更多屬性。在這段延遲期間，您可能會看到已核發的[!UICONTROL 屬性訂閱上限]錯誤。 |
| 同一部裝置上多次登入 | 使用時 [!DNL Customer Attributes] 若要將客戶設定檔上傳至資料來源，Adobe不建議使用者共用裝置(亦即使用相同的Experience CloudID)。 Experience Cloud ID (ECID) 會留存於裝置上。如果共用裝置，可能使多個使用者連結至相同的 ECID，導致 [!DNL Target] 出現非預期的結果。**注意：**&#x200B;若使用行動裝置，行動應用程式安裝後 ECID 會永久存在。重新安裝應用程式以產生新的 ECID。若使用網頁，系統會在瀏覽器 Cookie 清除後產生新的 ECID。 |
| 每日頻率上傳限制 | Adobe建議您更新 [!DNL Customer Attributes] 一天僅一次。 您至少必須等待 24 小時，才能為同一組個人資料上傳另一個客戶個人資料資料檔案。 |
| 自訂 Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，整合功能若使 [!DNL Analytics] 使用ID服務匯出或匯入的資料在訪客的識別方式為時無法正常運作 `s.visitorID.`<br>這種狀況包括但不限於共用受眾， [!DNL Analytics] 適用於Adobe Target (A4T)，以及 [!DNL Customer Attributes].<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
|  中的字元長度限制[!DNL Analytics] | 建立 [!DNL Analytics] 訂閱時，已上傳檔案的欄位長度會截斷為 255。 |

{style="table-layout:auto"}

## 常見問題集關於 [!DNL Customer Attributes] {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我能否收到關於上傳狀態的通知？ [!DNL Customer Attributes]？ | 可以。 |
| 我該怎麼做才能開始使用 [!DNL Customer Attributes]？ | <ol><li>完成佈建程序。如果您是Analytics客戶，Adobe會針對以下專案為您進行布建 [!DNL Customer Attributes]. 如果您只使用 Adobe Target 而沒有使用 Analytics，請連絡客戶服務，申請佈建核心服務。</li> <li>與您的 CRM 團隊溝通。瞭解在Analytics和整個Experience Cloud中可以使用哪些可用的客戶資料。</li><li>實作核心服務。 如需如何導入最新實作的步驟，請參閱[為核心服務啟用您的應用程式](core-services.md)。(如需重要資訊，請參閱同步化客戶 ID 的相關章節)。</li></ol> **注意：**[這裡](faq.md)提供實作核心服務的管理員常見問題集。 |
| 數量 [!DNL Customer Attributes] 我可以使用嗎？ | 您可以將數百個 `.csv` 欄上傳至客戶屬性服務。但是在設定訂閱及選取屬性時，系統會根據您擁有的應用程式套用以下限制 (針對每個報表套裝)：  <ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：200 個</li><li>Adobe Target Standard：5 個</li><li>Adobe Target Premium：200 個</li></ul> |
| 是否需要移轉至 Experience Cloud ID Service？ | 是否需移轉取決於您使用的應用程式。 <ul><li>Adobe Analytics：強烈建議 </li><li>Adobe Target：必須移轉。 </li></ul><br>使用 Experience Cloud ID 服務會啟用最新的 Experience Cloud 功能，包括即時對象、Adobe Target 現代化、Analytics 整合和視訊活動訊號追蹤。<br>如需詳細資訊，請參閱[為核心服務啟用您的應用程式](core-services.md)。 <br>**注意：**[Experience Cloud ID Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant) 是前身為 _Analytics 訪客 ID 服務_&#x200B;的新式實作。 |
| 客戶屬性功能與 Adobe Audience Manager 有何關係？ | 雖然 Audience Manager 可接收資料以辨識對象，但無法執行將屬性與過往行為資料關聯的分析功能，亦無法提供 Adobe Analytics 中可使用的報表、分析和分段功能。[!UICONTROL 人員] 可讓不同應用程式的豐富資料繫結在一起，並與單一ID建立關聯，以便跨Experience Cloud使用。 <br>在Adobe Target中， [!DNL Customer Attributes] 會顯示為個別屬性，可與其他規則結合以建立對象。 共用給 [!UICONTROL People] 服務的對象是無法修改的完整對象。 |
| **(僅限 Analytics)** 此功能與 Analytics Premium 中提供的功能有何不同？ | 過去，有意將客戶屬性資料與 Analytics 資料結合的客戶，為了這項功能對 Data Workbench 的依賴程度很高。[!DNL Customer Attributes] 藉由提供 [!DNL Customer Attributes] 做為Reports &amp; Analytics、Ad Hoc Analysis和Report Builder中的維度和量度。 Analytics Standard客戶可以存取 [!DNL Customer Attributes]，但功能有限。 Analytics Premium 客戶可使用完整功能。 |
| **(僅限 Adobe Target)** 我是否可以預先載入或上傳 Adobe Target 從未看過的客戶資料？ | 可以。訪客首次向Adobe Target提出請求時，系統會從Adobe擷取與他們有關的現有資訊 [!DNL Customer Attributes] 並使用該資料進行目標定位。 **注意：**&#x200B;如果訪客是第一次與 Adobe Target 互動，則擷取此資料可能需花費最長達 20 分鐘。 |
| **(僅限 Adobe Target)** 我是否可藉由結合客戶屬性資料和共用的對象資料來建立超級對象？ | 不可以。共用的對象資料是已完成的對象。 |
| **(僅限Adobe Target)** 如何 [!DNL Customer Attributes] 與Adobe Target的大量設定檔API相較之下的功能嗎？ | 大量個人資料 API 可以透過 API 以個別或大量的方式直接更新 Adobe Target 個人資料。此功能類似於 [!DNL Customer Attributes]，主要差異如下：<ul><li>設定檔API是REST API呼叫，而 [!DNL Customer Attributes] 使用FTP。</li><li>Adobe Target 的個人資料 API 只會將資料傳送至 Adobe Target，而非整個 Experience Cloud。</li><li>[!DNL Customer Attributes] 提供簡單的介面來建立和管理這些外部資料。</li></ul> |
| **(僅限Adobe Target)** 上傳資料來自 [!DNL Customer Attributes] 來延長Adobe Target訪客的Adobe Target設定檔存留期？ | 是。請參閱 Adobe Target 說明中的[訪客個人資料存留期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=zh-Hant)。 |
| **(僅限Adobe Target)** 我是否可鎖定在中上傳的資料？ [!DNL Customer Attributes] 在透過客戶ID識別訪客後立即執行？ | 可以。對 Adobe Target 發出伺服器呼叫時 (包括 mbox 協力廠商 ID)，所有客戶屬性資料都可供使用。 |
| **(僅限 Adobe Target)** 對於已上傳至客戶屬性來源的檔案而言，**[!UICONTROL 同步狀態]**&#x200B;欄代表什麼？ | 對特定屬性檔案選取「同步狀態」圖示，即可檢視 Adobe Target 所發佈和同步的記錄數。 `Sync %` 是即時量度，可指明 Adobe Target 中已同步的個人資料百分比。<br> **注意：**&#x200B;與 Adobe Target 同步屬性可能需花費最多 24 小時。 |
| 檔案上傳量度代表什麼 [!DNL Customer Attributes] 來源？ | 您可以檢查已上傳到的屬性狀態 [!DNL Customer Attributes] 並透過以下量度協助撰寫： <ul><li>記錄數：屬性檔案中的記錄數。</li><li>**新記錄數：**&#x200B;屬性檔案中存在的新記錄數。</li> <li>**更新的記錄：** 中存在的記錄數 [!DNL Customer Attributes] ，其中包含檔案中更新的值。</li><li>**所有資料（記錄）：** 已成功上傳到的記錄總數 [!DNL Customer Attributes].</li></ul> |

{style="table-layout:auto"}