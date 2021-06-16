---
description: 了解 Analytics 如何使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics
title: '"第一方 Cookie "'
index: y
snippet: y
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 145040facf70c6bde5c6c3fae9c7ed7f520c188d
workflow-type: tm+mt
source-wordcount: '1579'
ht-degree: 60%

---

# 關於第一方 Cookie

Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。Adobe 會在可能的情況下使用第一方 Cookie 來記錄您網站上的活動。 若要記錄不同網站 (例如您可能擁有的其他網域) 上的活動，則需要第三方 Cookie。

許多瀏覽器和反間諜軟體應用程式的設計目的是拒絕和刪除第三方Cookie，包括[!DNL Analytics]資料收集中使用的Cookie。 若要支援追蹤您的訪客與您網站互動的方式，您應該確保已設定您的資料收集使用第一方 Cookie：

實作第一方 Cookie 有兩個選項：

* 如果您使用Experience PlatformIdentity服務（ECID服務），則會使用JavaScript在第一方內容中自動設定Cookie。
* 如果您使用[!DNL Analytics]舊版識別碼（亦稱為`s_vi` Cookie），則取決於您如何設定資料收集伺服器。 如果資料收集伺服器符合您網站的網域，則Cookie會設為第一方。 如果收集伺服器與您目前的網域不符，則會將Cookie設為第三方。 在此情況下，如果第三方Cookie遭到封鎖，[!DNL Analytics]會設定第一方[備援id(s_fid)](cookies-analytics.md)，而非標準的&quot;s_vi&quot; Cookie。

若要確保您的收集伺服器符合您網站的網域，您可以使用CNAME實作，在第一方內容中設定Cookie。 這涉及到貴公司的 DNS 設定變更，以便設定 CNAME 別名來指向 Adobe 代管網域。 請注意，雖然有多項 Adobe 產品支援使用 CNAME，但在所有情況下，CNAME 都是用來為特定客戶建立受信任的第一方端點，且擁有權屬於該客戶。 如果您控制多個網域，他們可能會使用單一CNAME端點來追蹤跨其網域的使用者，但只要網站網域不符合CNAME網域Cookie的位置，就會設為第三方。

>[!NOTE]
>
>針對這兩個選項，Apple的智慧型追蹤預防(ITP)程式會讓第一方Cookie在由ITP管理的瀏覽器上短暫存留，這些瀏覽器包括macOS上的Safari，以及iOS和iPadOS上的所有瀏覽器。 截至 2020 年 11 月，這兩種 Cookie 都有七天的有效期。 此有效期可能會有變動。

針對使用 CNAME 的第二個選項，如果您的網站具有使用 HTTPS 通訊協定的安全頁面，您可以與 Adobe 合作取得 SSL 憑證以實作第一方 Cookie。Adobe強烈建議您只使用HTTPS來收集資料，因為Adobe在2020年下半年停止支援HTTP收集。

SSL 憑證簽發過程複雜難懂，而且耗時。因此，Adobe與業界領先的證書頒發機構(CA)DigiCert建立了合作關係，並開發了一個整合流程，通過該流程可以自動購買和管理這些證書。

在您的許可下，我們會與CA合作，為您核發、部署及管理新的SHA-2 SSL憑證。 Adobe會持續管理此憑證，並確保未預期的過期、撤銷或安全性疑慮等問題不會影響貴組織安全收集資料的相關作業。

## Adobe管理證書程式

Adobe Managed Certificate Program 是為第一方 Cookie 實作新第一方 SSL 憑證的建議程序。

Adobe Managed Certificate Program 可讓您免費對第一方 Cookie 實作新的第一方 SSL 憑證 (前 100 個 CNAME)。如果您目前有自己的客戶管理SSL憑證，請向Adobe客戶服務洽詢移轉至Adobe管理憑證方案的相關事宜。

### 實作

以下說明如何為第一方 Cookie 實作新的第一方 SSL 憑證：

1. 填寫[第一方Cookie請求表單](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx) ，並請客戶服務開立支援工單，要求在Adobe管理程式上設定第一方Cookie。 每個欄位在文件中都有範例解說。

2. 建立 CNAME 記錄 (請參閱下方說明)。

   客戶服務代表在收到支援服務單後，應該會提供您 CNAME 記錄。 您必須在貴公司的 DNS 伺服器上設定這些記錄，Adobe 才能代表您購買憑證。 CNAME類似下列：

   **安全** - 例如主機名稱 `smetrics.example.com` 指向：`example.com.adobedc.net`。

>[!NOTE]
> 過去，Adobe建議客戶設定兩個CNAME（一個用於HTTPS，一個用於HTTP）。 由於這是加密流量的最佳做法，且大多數瀏覽器都強烈勸阻使用 HTTP，所以我們不再建議為 HTTP 設定 CNAME。 如果您需要，則會如下所示：
>    **不安全** -- 主機名稱 `metrics.example.com` 指向：`example.com.adobedc.net`。

1. CNAME就緒後，Adobe會與DigiCert合作，購買憑證並安裝在Adobe的生產伺服器上。

   如果您已有實作，可考慮將訪客移轉以保留現有的訪客。在 Adobe 的生產環境中將憑證上線後，您就可以將追蹤伺服器變數更新為新主機名稱。換句話說，如果網站不安全 (HTTP)，請更新 `s.trackingServer`。如果網站安全 (HTTPS)，請更新 `s.trackingServer` 和 `s.trackingServerSecure` 這兩個變數。

2. [驗證主機名稱轉送](#validate) (請參閱下文)。

3. [更新實作程式碼](#update) (請參閱下文)。

### 維護和更新

SSL 憑證每年到期，表示 Adobe 必須每年為各實作購買新憑證。實作即將到期時，組織內所有支援的使用者都會收到電子郵件通知。 若希望 Adobe 續約您的主機名稱，需由一名支援的使用者代表回覆 Adobe 的電子郵件，並說明貴組織打算繼續使用該即將到期的主機名稱來收集資料。如此一來，Adobe 就會自動購買並安裝新憑證。

### 常見問答

| 問題 | 回答 |
|---|---|
| **此程序是否安全？** | 是的，Adobe管理程式比舊方法更安全，因為Adobe和核發憑證授權機構之外沒有憑證或私密金鑰變更。 |
| **Adobe 如何為網域購買憑證？** | 唯有當您將指定的主機名稱 (例如 `telemetry.example.com`) 指向 Adobe 擁有的主機名稱時，才能購買憑證。基本上，這等於是將此主機名稱委派給 Adobe，並允許 Adobe 代表您購買憑證。 |
| **我可以要求撤銷憑證嗎？** | 可以。您身為網域所有者，有權要求我們撤銷憑證。您只需請客戶服務開立支援工單，即可完成此程序。 |
| **此憑證是否會使用 SHA-2 加密？** | 是，Adobe 會與 DigiCert 合作，核發 SHA-2 憑證。 |
| **這是否會產生額外費用？** | 不會，Adobe 目前免費提供此服務給所有現有的 Adobe Digital Experience 客戶。 |

{style=&quot;table-layout:auto&quot;}

## 建立 CNAME 記錄

貴組織的網路營運團隊應建立CNAME記錄，以設定DNS伺服器。 每個主機名稱都會將資料轉寄給 Adobe 的資料收集伺服器。

FPC 專員會提供您已設定的主機名稱，以及主機名稱要指向的 CNAME。 例如：

* **SSL 主機名稱**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> 如果您仍使用不安全，則會顯示如下：
> * **非 SSL 主機名稱**：`metrics.mysite.com`
> * **非 SSL CNAME**：`mysite.com.adobedc.net`


只要實作程式碼未變更，此步驟就不會影響資料收集作業，並可在更新實作程式碼後完成。

>[!NOTE]
>
>Experience Cloud Visitor ID 服務有提供設定 CNAME 的其他方法，以協助啟用第一方 Cookie。

## 驗證主機名稱轉送 {#validate}

下列方法可用於進行驗證：

### 使用瀏覽器進行驗證

如果您已設定 CNAME 且已安裝憑證，便可使用瀏覽器進行驗證：

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>如果未安裝證書，系統會向您發出安全警告。

### 使用 [!DNL curl] 進行驗證

Adobe 建議從命令列使用 [[!DNL curl]](https://curl.se/)。([!DNL Windows] 使用者可從以下位置安裝 [!DNL curl]：<https://curl.se/windows/>)。

如果您已設定 CNAME 但未安裝憑證，請執行：
`curl -k https://smetrics.adobe.com/_check`
回應：`SUCCESS` 

(`-k` 值會停用安全性警告)。

如果您已設定 CNAME 且已安裝憑證，請執行：
`curl https://smetrics.adobe.com/_check`
回應：`SUCCESS`

### 使用 [!DNL nslookup] 進行驗證

您可以使用 `nslookup` 進行驗證。以 `smetrics.adobe.com` 為例，開啟命令提示並輸入 `nslookup smetrics.adobe.com`

如果一切皆已成功設定，您會看到類似以下的傳回：

```
nslookup smetrics.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

smetrics.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## 更新實作程式碼 {#update}

編輯網站程式碼以使用第一方Cookie之前，請先完成下列必要條件：

* 請依照[Adobe管理憑證方案](#adobe-managed-certificate-program)的&#x200B;*實作*&#x200B;一節中所述步驟，請求SSL憑證。
* 建立 CNAME 記錄 (請參閱上方)。
* 驗證主機名稱（請參閱上文）。

在您確認主機名稱會回應並轉送至Adobe資料收集伺服器後，您可以變更實作，指向您自己的資料收集主機名稱。

1. 開啟您的核心 JavaScript 檔案 (`s_code.js/AppMeasurement.js`)。
1. 如果您要更新程式碼版本，請以較新版本取代整個 `s_code.js/AppMeasurement.js` 檔案，並汰換任何外掛程式或自訂項目 (如果有的話)。**或者**，如果您只想更新第一方 Cookie 相關程式碼，請找到 s.trackingServer 和 s.trackingServerSecure (如果使用 SSL) 變數，將其指向您新的資料收集主機名稱。以 mysite.com 為例：`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 將更新後的核心 JavaScript 檔案上傳至您的網站。

1. 如果您要從長期實作移轉至第一方Cookie，或變更為不同的第一方收集主機名稱，Adobe建議將訪客從舊有網域移轉至新網域。

請參閱「Analytics 實作指南」中的[訪客移轉](https://experienceleague.adobe.com/docs/analytics/implementation/javascript-implementation/visitor-migration.html?lang=en)。

在您上傳 JavaScript 檔案後，系統就會執行第一方 Cookie 資料收集所需的所有設定。Adobe建議您在接下來的數小時內監控Analytics報表，以確保資料收集可正常進行。 如果未正常運作，請確認前述所有步驟均已完成，並推派組織的任何一名支援使用者連絡客戶服務。
