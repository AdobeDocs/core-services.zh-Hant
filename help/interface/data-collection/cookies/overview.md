---
description: 了解 Adobe Experience Cloud 中的解決方案和服務如何使用 Cookie。
title: Experience Cloud中Cookie的使用方式
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: d6dc659104b3b24b60495cd97adb21ebb3962fc7
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 10%

---

# Experience Cloud中使用的Cookie

Adobe Experience Cloud使用Cookie。 Cookie是網站傳送給您的瀏覽器的一小段資料，會儲存以供日後使用。 Cookie可協助網站記住您再次造訪或在頁面之間移動時的內容。 Cookie有助於追蹤瀏覽次數，並將一個裝置與其他裝置區分開來。

法律通常要求您先取得許可權，才能在某人的裝置上儲存或使用Cookie。 Adobe建議您洽詢法律團隊，瞭解適用的規則。

## 關於第一方 Cookie

Adobe Experience Cloud使用Cookie來追蹤不會維持在頁面檢視或瀏覽器作業之間的資訊。 Adobe儘可能使用第一方Cookie （與您自己的網站連結）。 若要追蹤您擁有的多個網站或網域中的活動，則需要協力廠商Cookie。

有些瀏覽器和防間諜軟體工具會封鎖協力廠商Cookie。 Adobe有方法可確保Cookie仍然有效，即使Cookie被封鎖也是如此。 其運作方式取決於您使用Experience Platform Identity Service (ECID)還是舊版Analytics Cookie （如`s_vi` Cookie）：

* [Experience Cloud Identity服務](https://experienceleague.adobe.com/zh-hant/docs/id-service/using/intro/overview)： ECID服務一律會設定第一方Cookie，無論您的收集網域是否符合您網站的網域。 它會使用JavaScript將Cookie放在網站的網域上。

* [Analytics舊型識別碼](analytics.md) （例如`s_vi` Cookie）： Cookie是第一方還是第三方取決於您的設定：

   * 如果您的資料收集伺服器符合您網站的網域，則Cookie為第一方。
   * 如果不符，Cookie為協力廠商。 如果第三方Cookie遭到封鎖，Adobe會設定一個備援Cookie (`s_fid`)，而非一般的備援Cookie。

為確保您的集合伺服器符合您網站的網域，您可以使用&#x200B;**CNAME設定**。 這涉及更新您的DNS設定，以將自訂網域（您擁有）指向Adobe的伺服器。 如此一來，追蹤Cookie會顯示為第一方。 雖然一個CNAME可以跨多個網域運作，但任何不符合CNAME的網域仍會設定第三方Cookie。

>[!NOTE]
>
>Apple的智慧型追蹤預防(ITP)會限制Adobe的第一方Cookie持續多久，即使您的收集網域符合您網站的網域亦然。 ITP會影響macOS上的Safari，以及iOS和iPadOS上的所有瀏覽器。 自2020年11月起，使用CNAME設定的Cookie將與使用JavaScript設定的Cookie一樣快速地過期。 此時間限制未來可能會變更。

以下是文字的簡化版本：

## Cookie 與隱私權

Adobe嚴肅看待隱私權與資料安全性。 它可與隱私權組織、監管機構及AdChoices等程式合作，讓使用者掌控其資料的使用方式。

Adobe Experience Cloud的大多數Cookie不會儲存個人資訊。 它們是安全的，僅供您的公司用於報表、內容和廣告。 Adobe不會與其他客戶或第三方共用這些資料，除非是匿名且涵蓋整個產業的報告(例如Digital Marketing Insight報告)。

Adobe不會合併跨不同公司的瀏覽器資料。 為了保護隱私權，有些Adobe工具可讓每個網站使用自己的Cookie集。 有些客戶也允許使用您自己的網域來處理Cookie，使其成為第一方且更安全。

Cookie只能儲存先前儲存於其中的資訊。 他們無法在您的裝置上執行程式碼或讀取其他資料。 此外，網頁瀏覽器僅允許Cookie由設定它們的網站讀取。 例如，只有Adobe.com可以讀取其設定的Cookie。

下圖說明標準影像請求的 Cookie 使用方式：

![標準影像請求的 Cookie 使用方式](assets/CookiesProcessGraphic-01.png)

下圖說明直接影像請求 (用於未載入 JS 檔案的情況) 的 Cookie 使用方式：

![直接影像請求的 Cookie 使用方式](assets/CookiesProcessGraphic2.png)
