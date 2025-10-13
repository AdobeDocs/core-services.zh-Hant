---
description: 取得有關Adobe Experience Cloud中Adobe Analytics和Adobe Target中 [!DNL Customer Attributes] 常見問題的解答。
solution: Experience Cloud
title: 關於  [!DNL Customer Attributes] 的常見問題集
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 6031e544-822b-4843-b3d8-98a36a3c40e8
source-git-commit: bd718358c6db1ea4a6150d019773072418b629f9
workflow-type: tm+mt
source-wordcount: '1050'
ht-degree: 76%

---

# 關於 [!DNL Customer Attributes] 的常見問題集

在 Adobe Analytics 和 Adobe Target 中，關於 [!DNL Customer Attributes] 的常見問題集和最佳實務。

## 最佳實務和限制 {#best_practices}

使用 [!DNL Customer Attributes] 時的指導和限制。

| 問題 | 說明 |
|--- |--- |
| [!DNL Customer Attributes] [訂閱](subscription.md)限制 | 升級至 Analytics Premium 後，必須等待 24 小時才能使用更多屬性。在這段延遲期間，您可能會看到已核發的[!UICONTROL 屬性訂閱上限]錯誤。 |
| 同一部裝置上多次登入 | 使用 [!DNL Customer Attributes] 將客戶輪廓上傳至資料來源時，Adobe 不建議使用者共用裝置 (亦即使用同一個 Experience Cloud ID)。Experience Cloud ID (ECID) 會留存於裝置上。如果共用裝置，可能使多個使用者連結至相同的 ECID，導致 [!DNL Target] 出現非預期的結果。**注意：**&#x200B;若使用行動裝置，行動應用程式安裝後 ECID 會永久存在。重新安裝應用程式以產生新的 ECID。若使用網頁，系統會在瀏覽器 Cookie 清除後產生新的 ECID。 |
| 每日頻率上傳限制 | Adobe 建議每天只需更新一次 [!DNL Customer Attributes]。您至少必須等待 24 小時，才能為同一組輪廓上傳另一個客戶輪廓資料檔案。 |
| 自訂 Analytics ID (`s.visitorID`) | 使用`s.visitorID`設定客戶ID是在Adobe Analytics中識別使用者的方法。 不過，在使用 `s.visitorID.`<br> 識別訪客時，透過 ID Service 匯出或匯入 [!DNL Analytics] 資料的整合功能無法使用，其中包含但不限於共用 Audiences、Adobe Target (A4T) 的 [!DNL Analytics] 和 [!DNL Customer Attributes]。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
|  中的字元長度限制[!DNL Analytics] | 建立[!DNL Analytics] [訂閱](subscription.md)時，已上傳檔案的欄位長度會截斷為255。 |

{style="table-layout:auto"}

## 關於 [!DNL Customer Attributes] 的常見問題集 {#section_E47866EEA83348E09FE43CEC5E44C461}

| 問題 | 回答 |
|--- |--- |
| 我是否可以收到關於 [!DNL Customer Attributes] 上傳狀態的通知？ | 可以。 |
| 我要如何開始使用 [!DNL Customer Attributes]？ | <ol><li>完成佈建程序。如果您是Adobe Analytics客戶，Adobe正在布建您[!DNL Customer Attributes]。 如果您只使用Adobe Target而沒有使用Analytics，請聯絡客戶服務，申請布建核心服務。</li> <li>與您的 CRM 團隊溝通。了解您想要在 Analytics 和整個 Experience Cloud 使用的客戶資料中有哪些類型可用。</li><li>實作核心服務。</li></ol> 在上傳資料之前，請先參閱[必要條件](t-crs-usecase.md#prerequisites-for-using-customer-attributes)，瞭解如何讓使用者使用此功能。 |
| 我可以使用多少個客戶屬性？ | 您可以將數百個 `.csv` 欄上傳至客戶屬性服務。但是在設定訂閱及選取屬性時，系統會根據您擁有的應用程式套用以下限制 (針對每個報表套裝)：  <ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：200 個</li><li>Adobe Target Standard：5 個</li><li>Adobe Target Premium：200 個</li></ul> |
| 是否需要移轉至 Experience Cloud ID Service？ | 是否需移轉取決於您使用的應用程式。 <ul><li>Adobe Analytics：強烈建議 </li><li>Adobe Target：必須移轉。 </li></ul>使用Experience Cloud ID服務會啟用最新的Experience Cloud功能，包括即時受眾、Adobe Target現代化、Analytics整合和視訊活動訊號追蹤。 |
| 客戶屬性功能與 Adobe Audience Manager 有何關係？ | 雖然 Audience Manager 可接收資料以辨識受眾，但無法執行將屬性與過往行為資料關聯的分析功能，亦無法提供 Adobe Analytics 中可使用的報表、分析和分段功能。[!DNL Customer Attributes]可讓不同應用程式的豐富資料繫結在一起，並與單一ID建立關聯，以便在Experience Cloud中使用。 <br>在 Adobe Target 中，客戶屬性會顯示為個別屬性，可與其他規則結合以建立客群。共用給 [!UICONTROL People] 服務的客群是無法修改的完整客群。 |
| **(僅限Adobe Analytics)**&#x200B;此功能與Analytics Premium中提供的功能有何不同？ | 過去，有意將客戶屬性資料與Analytics資料結合的客戶，為了這項功能對Data Workbench的依賴程度很高。 [!DNL Customer Attributes]在Report Builder中提供客戶屬性作為維度和量度，因此可讓更廣大的受眾運用此功能。 Analytics Standard 客戶可存取 [!DNL Customer Attributes]，但可用的功能受限。Analytics Premium 客戶可使用完整功能。 |
| **(僅限 Adobe Target)** 我是否可以預先載入或上傳 Adobe Target 從未看過的客戶資料？ | 可以。訪客第一次向 Adobe Target 提出請求時，系統會從 [!DNL Customer Attributes] 擷取與 Adobe 有關的現有資訊，並使用這些資料進行目標鎖定。**注意：**&#x200B;如果訪客是第一次與 Adobe Target 互動，則擷取此資料可能需花費最長達 20 分鐘。 |
| **(僅限 Adobe Target)** 我是否可藉由結合客戶屬性資料和共用的客群資料來建立超級客群？ | 不會。共用的客群資料是已完成的客群。 |
| **(僅限Adobe Target)** [!DNL Customer Attributes]與Adobe Target的大量設定檔API有何不同？ | 大量輪廓 API 可以透過 API 以個別或大量的方式直接更新 Adobe Target 輪廓。此功能與 [!DNL Customer Attributes] 類似，主要差異如下：<ul><li>輪廓 API 是一種 REST API 呼叫，而 [!DNL Customer Attributes] 會使用 FTP。</li><li>Adobe Target 的輪廓 API 只會將資料傳送至 Adobe Target，而非整個 Experience Cloud。</li><li>[!DNL Customer Attributes] 提供簡單的介面，用於建立和管理這些外部資料。</li></ul> |
| **(僅限 Adobe Target)** 以 [!DNL Customer Attributes] 將資料上傳至 Adobe Target 是否會延長 Adobe Target 訪客的輪廓存留期限？ | 是。請參閱 Adobe Target 說明中的[訪客輪廓存留期](https://experienceleague.adobe.com/docs/target/using/audiences/visitor-profiles/visitor-profile.html?lang=zh-Hant)。 |
| **(僅限 Adobe Target)** 我是否可在透過客戶 ID 識別訪客後，立即鎖定 [!DNL Customer Attributes] 所上傳的資料？ | 可以。對Adobe Target發出伺服器呼叫時（包括mbox第三方ID），所有客戶屬性資料都可供使用。 |
| **(僅限 Adobe Target)** 對於已上傳至客戶屬性來源的檔案而言，**[!UICONTROL 同步狀態]**&#x200B;欄代表什麼？ | 對特定屬性檔案選取「同步狀態」圖示，即可檢視 Adobe Target 所發佈和同步的記錄數。 `Sync %` 是即時量度，可指明 Adobe Target 中已同步的輪廓百分比。<br> **注意：**&#x200B;與 Adobe Target 同步屬性可能需花費最多 24 小時。 |
| 「[!DNL Customer Attributes] 來源」中的檔案上傳量度代表什麼？ | 在下列量度的協助下，您可以檢查已上傳至 [!DNL Customer Attributes] 的屬性之狀態： <ul><li>記錄數：屬性檔案中的記錄數。</li><li>**新記錄數：**&#x200B;屬性檔案中存在的新記錄數。</li> <li>**更新記錄數：** N存在於 [!DNL Customer Attributes] 中且檔案中有更新值的記錄數。</li><li>**所有資料 (記錄) 數：**&#x200B;已成功上傳至 [!DNL Customer Attributes] 的記錄總數。</li></ul> |

{style="table-layout:auto"}
