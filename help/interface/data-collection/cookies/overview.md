---
description: 了解 Adobe Experience Cloud 中的解決方案和服務如何使用 Cookie。
title: Experience Cloud中Cookie的使用方式
uuid: 4255a13a-917b-4b5f-a7d4-4b2e7521d189
exl-id: 60f1a89e-d989-461b-a6a3-c1df022cd30b
source-git-commit: b4d7cc357393798f2265e09885dd4ea2f80ab31e
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 58%

---

# Experience Cloud中使用的Cookie

Adobe Experience Cloud 中的許多服務都會使用 Cookie。Cookie 是網站向網頁瀏覽器顯示的一小段資料。瀏覽器會儲存這段資料，讓網站在需要時可參考其資料。 此動作會在之後每次收到頁面和影像請求時執行。

Cookie 可用來在使用者造訪網站期間或多次造訪網站之間保留資訊。Cookie 可做為裝置與其他檢視網站之瀏覽器之間獨特的區別。

法律、法規及自我規範原則可能會要求您先徵詢訪客同意，才能儲存或擷取電腦或其他與 Web 連線之裝置的資訊。Adobe建議您與組織的法律顧問一起檢閱哪些法律、法規和原則可控制您對Cookie的使用。

## 關於第一方 Cookie

Adobe Experience Cloud服務會使用Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。 Adobe會儘可能使用第一方Cookie來記錄您網站上的活動。 若要記錄不同網站 (例如您可能擁有的其他網域) 上的活動，則需要第三方 Cookie。

許多瀏覽器與反間諜軟體應用程式在設計上會拒絕及刪除第三方 Cookie。 Adobe可確保即使第三方Cookie遭到封鎖，仍可隨時設定Cookie。 此特定行為會因您使用的是Experience PlatformIdentity服務（ECID服務）還是Analytics的舊型識別碼（例如`s_vi` Cookie）而異：

* [Experience Platform識別服務（ECID服務）](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant)會自動設定第一方Cookie，無論您的收集網域是否符合您網站的網域。 如果兩者不符，Identity Service會使用JavaScript在您網站的網域上設定Cookie。
* 如果您使用[Analytics舊型識別碼](analytics.md) （例如`s_vi` Cookie），則將取決於您已如何設定您的資料收集伺服器。 如果資料收集伺服器符合您網站的網域，則 Cookie 會設定為第一方。如果資料收集伺服器不符合您目前的網域，則Cookie會設定為第三方。 在此情況下，如果第三方Cookie遭到封鎖，Analytics會設定第一方備援ID (`s_fid`)，而非標準`s_vi` Cookie。

如果您想要確保您的資料收集伺服器符合您網站的網域，您可以使用CNAME實作，好讓您可以從CNAME實作中指定的自訂網域轉送到Adobe的資料收集伺服器。 此工作涉及貴公司的DNS設定變更，以便設定CNAME別名來指向Adobe代管網域。 請注意，雖然有多項 Adobe 產品支援使用 CNAME，但在所有情況下，CNAME 都是用來為特定客戶建立受信任的第一方端點，且擁有權屬於該客戶。 如果您控制多個網域，這些網域可能會使用單一CNAME端點來追蹤其網域中的使用者，但只要網站網域不符合CNAME網域，Cookie就會設定為協力廠商。

>[!NOTE]
>
>無論您的資料收集網域是否符合您網站的網域，Apple的智慧型追蹤預防(ITP)計畫會使得Adobe設定的第一方Cookie在受ITP控管的瀏覽器上短暫存在，其中包括macOS上的Safari以及iOS和iPadOS上的所有瀏覽器。 截至 2020 年 11 月，透過 CNAME 設定的 Cookie 也與透過 JavaScript 設定的 Cookie 具有相同有效期。 此有效期可能會有變動。

## Cookie 與隱私權

維護客戶隱私和資料安全是 Adobe 的首要任務。 Adobe 加入多個隱私權機構，並與隱私權監管機構合作，以及採取自我監管原則。這項合作包括數位廣告聯盟 Adchoices 計劃，為客戶提供有關如何使用他們資訊的訊息，以及關於資訊使用的選擇。

Experience Cloud 產品設定的 Cookie 大多不含可識別的個人資訊。這些 Cookie 和相關資料安全無虞，且僅用於貴公司的報表，以及提供相關的內容和廣告。除非用於彙總的產業報告，否則協力廠商或其他 Adobe 客戶無法取得這些資料。例如，[!DNL Digital Marketing Insight Report] 會分析各個零售商的彙整匿名資料。

Adobe 不會合併各家公司的瀏覽器層級資訊。為了保護客戶資料的隱私和安全，Experience Cloud 中有些服務能讓公司針對每個追蹤的網站使用個別的 Cookie 集合。部分產品專案也讓客戶能使用其專屬的網域名稱作為Cookie的擁有者。 此做法可額外建立一層隱私與安全性，因為會使 Experience Cloud Cookie 成為永久屬於該公司網站的&#x200B;*第一方 Cookie*。

Cookie 只能儲存和提供先前儲放在 Cookie 中的資訊，無法執行程式碼或存取儲存在電腦上的其他資訊。同時，網頁瀏覽器會限制 Cookie 資料的存取。瀏覽器會強制執行 Cookie 安全性原則，讓所有 Cookie 資料僅供最初設定資訊的網站使用。

例如，Adobe.com 網站中 Cookie 集所包含的資料，不能讓 Adobe.com 以外的任何其他網站檢視。

下圖說明標準影像請求的 Cookie 使用方式：

![標準影像請求的 Cookie 使用方式](assets/CookiesProcessGraphic-01.png)

下圖說明直接影像請求 (用於未載入 JS 檔案的情況) 的 Cookie 使用方式：

![直接影像請求的 Cookie 使用方式](assets/CookiesProcessGraphic2.png)
