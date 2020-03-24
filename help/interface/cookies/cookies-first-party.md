---
description: Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
keywords: cookies;privacy
seo-description: Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
seo-title: First-Party Cookies
solution: Experience Cloud,Analytics
title: First-Party Cookies
index: y
snippet: y
translation-type: tm+mt
source-git-commit: b6ef7f0b7ef3b43b437524b20cee940889c26ba8

---


# 關於第一方 Cookie

Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。這些無害的Cookie源自Adobe代管的網域，稱為第三方Cookie。

許多瀏覽器與反間諜軟體應用程式在設計上會拒絕及刪除第三方 Cookie，包括 Analytics 為收集資料所使用的 Cookie。若要支援您追蹤訪客與網站的互動方式，您可以實作第一方Cookie。

實作第一方Cookie有兩個選項：

* Experience Platform ID 服務。ID 服務可使用 JavaScript 在第一方情境中設定 Cookie。
* 您公司DNS伺服器上的DNS項目，以設定Adobe代管網域的CNAME別名。 請注意，雖然使用CNAME的Adobe產品支援各種不同，但在所有情況下，CNAME都會用來為特定客戶建立受信任的第一方端點，並歸該客戶所有。 如果該客戶控制多個網域，他們可能會使用單一CNAME端點來追蹤跨網域的使用者，但由於這需要CNAME網域以外所有網域的協力廠商Cookie，因此當協力廠商Cookie遭到封鎖時，就無法運作，因此不建議使用。 Adobe CNAME永遠不會用於追蹤不同客戶所擁有網域中的個人或裝置。

即使將第一個選項與Experience Cloud ID服務搭配使用，Apple的ITP也會讓第一方Cookie短暫存在，因此最好搭配第二個選項使用。

對於使用CNAME的第二個選項，如果您的網站有使用HTTPS通訊協定的安全頁面，您可以與Adobe合作取得SSL憑證，以實作第一方Cookie。 Adobe強烈建議您只使用HTTPS來收集資料，因為我們將於2020年下半年停止支援HTTP收集。

SSL 憑證簽發過程複雜難懂，而且耗時。因此，Adobe 與業界領先的憑證授權機構 (CA) DigiCert 建立合作關係，並開發出整合程序，將憑證的購買和管理作業自動化。

取得您的許可後，我們就會與我們的 CA 合作，為您核發、部署及管理新的 SHA-2 SSL 憑證。Adobe將繼續管理此憑證，並確保意外到期、撤銷或安全性顧慮不會威脅貴組織安全收集的可用性。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program 是為第一方 Cookie 實作新第一方 SSL 憑證的建議程序。

Adobe Managed Certificate Program 可讓您免費對第一方 Cookie 實作新的第一方 SSL 憑證。如果您目前已有自己的客戶託管 SSL 憑證，請向 Adobe 客戶服務洽詢移轉至 Adobe Managed Certificate Program 的相關資訊。

### 實作

以下說明如何為第一方 Cookie 實作新的第一方 SSL 憑證:

1. 填寫[第一方 Cookie 請求表單](/help/interface/cookies/assets/FPC_Request_Form.xlsx)並請客戶服務開立支援工單，要求在 Adobe Managed Program 上設定第一方 Cookie。每個欄位在文件中都有範例解說。

1. 建立 CNAME 記錄 (請參閱下方說明)。

   收到票證後，客戶服務代表應提供您一對CNAME記錄。 請在您公司的 DNS 伺服器上設定這些記錄，Adobe 才能代表您購買憑證。CNAMES將類似於：

   **Secure** —— 例如，主機名指 `smetrics.example.com` 向： `example.com.ssl.d1.omtrdc.net`。

   **不安全** - 例如，主機名稱 `metrics.example.com` 指向: `example.com.d1.omtrdc.net`。

1. 這些 CNAME 設定完成時，Adobe 會與 DigiCert 合作，購買憑證並安裝到 Adobe 的生產伺服器。

   如果您有現有的實作，則應考慮訪客移轉，以維護現有訪客。 將憑證即時推送至Adobe的生產環境後，您可以將追蹤伺服器變數更新為新的主機名稱。 Meaning, if the site is not secure (HTTP), update the `s.trackingServer`. If the site is secure (HTTPS), update both `s.trackingServer` and `s.trackingServerSecure` variables.

1. [驗證主機名稱轉送](#validate) （請參閱下面）。

1. [更新實作代碼](#update) （請參閱下文）。

### 維護和更新

SSL 憑證每年到期，表示 Adobe 必須每年為各實作購買新憑證。實作即將到期前，組織內所有支援的使用者都會收到電子郵件通知。若要讓Adobe續約您的主機名稱，一位受支援的使用者必須回覆Adobe寄出的電子郵件，並指出您打算繼續使用即將到期的主機名稱來收集資料。 如此一來，Adobe 就會自動購買並安裝新憑證。

### 常見問題

| 問題 | 回答 |
|---|---|
| **此程序是否安全?** | 是，Adobe Managed Program 不會在 Adobe 和核發憑證授權機構以外的地方傳遞憑證或私密金鑰，因此會比舊方法更安全。 |
| **Adobe 如何為網域購買憑證?** | 唯有當您將指定的主機名稱 (例如 smetrics.example.com) 指向 Adobe 擁有的主機名稱時，才能購買憑證。基本上，這等於是將此主機名稱委派給 Adobe，並允許 Adobe 代表您購買憑證。 |
| **我可以要求撤銷憑證嗎?** | 可以。您身為網域所有者，有權要求我們撤銷憑證。您只需請客戶服務開立支援工單，即可完成此程序。 |
| **此憑證是否會使用 SHA-2 加密?** | 是，Adobe 會與 DigiCert 合作，核發 SHA-2 憑證。 |
| **這是否會產生額外費用?** | 否。Adobe目前免費為所有Adobe數位體驗客戶提供此服務。 |

## 建立 CNAME 記錄

您組織的網路營運團隊應建立新 CNAME 記錄，以設定 DNS 伺服器。每個主機名稱都會將資料轉寄給 Adobe 的資料收集伺服器。

FPC 專員會提供您設定完成的主機名稱，以及主機名稱要指向的 CNAME。例如:

* **SSL 主機名稱**:`smetrics.mysite.com`
* **SSL CNAME**:`mysite.com.ssl.sc.omtrdc.net`
* **非 SSL 主機名稱**:`metrics.mysite.com`
* **非 SSL CNAME**:`mysite.com.sc.omtrdc.net`

只要實作程式碼未變更，此步驟就不會影響資料收集作業，並可在更新實作程式碼後完成。

>[!N注意：]
>
>Experience Cloud訪客ID服務提供設定CNAME以啟用第一方Cookie的替代方式，但由於最近Apple ITP變更，因此即使使用Experience Cloud ID服務，仍建議您分配CNAME。

## 驗證主機名轉發 {#validate}

下列方法可供驗證：

### 使用瀏覽器驗證

如果您已設定CNAME並安裝憑證，則可使用瀏覽器進行驗證：

`https://sstats.adobe.com/_check`

>[!N注意：]
>
>如果未安裝憑證，您會看到安全性警告。

### 驗證使用 [!DNL curl]

Adobe建議從命令列使 [用[!DNL](https://curl.haxx.se/)curl]。 (使[!DNL Windows] 用者可從以下 [!DNL curl] 位置安裝： <https://curl.haxx.se/windows/>)

如果您有CNAME但未安裝憑證，請執行：回`curl -k https://sstats.adobe.com/_check`應： `SUCCESS`

(此值 `-k` 會停用安全性警告。)

如果您已設定CNAME且已安裝憑證，請執行：回`curl https://sstats.adobe.com/_check`應： `SUCCESS`

### 驗證使用 [!DNL nslookup]

您可以用 `nslookup` 於驗證。 以 `sstats.adobe.com`示例，開啟命令提示符並鍵入 `nslookup sstats.adobe.com`

如果一切皆已成功設定，您會看到類似下列的回訪：

```
nslookup sstats.adobe.com
Server:             10.30.7.247
Address:     10.30.7.247#53

sstats.adobe.com    canonical name = adobe.com.ssl.d1.sc.omtrdc.net.
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.218.180.161
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 52.39.8.230
Name:  adobe.com.ssl.d1.sc.omtrdc.net
Address: 54.187.216.46
```

## 更新實作程式碼 {#update}

編輯網站程式碼以使用第一方 Cookie 前，請先完成下列必要條件:

* 請求SSL憑證，請遵循 *Adobe Managed Certificate Program的「實作* 」區段中所述的 [步驟](#adobe-managed-certificate-program)。
* 建立 CNAME 記錄 (請參閱上方)。
* 驗證主機名稱（請參閱上文）。

確認主機名稱會回應並將資料轉寄給 Adobe 資料收集伺服器後，您就可以變更實作，指向您自己的資料收集主機名稱。

1. 開啟您的核心 JavaScript 檔案 (`s_code.js/AppMeasurement.js`)。
1. 如果您要更新程式碼版本，請以較新版本取代整個 `s_code.js/AppMeasurement.js` 檔案，並汰換任何外掛程式或自訂項目 (如果有的話)。**或者**，如果您只想更新第一方 Cookie 相關程式碼，請找到 s.trackingServer 和 s.trackingServerSecure (如果使用 SSL) 變數，將其指向您新的資料收集主機名稱。以 mysite.com 為例:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 將更新後的核心 JavaScript 檔案上傳至您的網站。

1. 如果您要從長期實作改為第一方 Cookie，或變更成其他第一方收集主機名稱，建議您將訪客從舊有網域移轉到新網域。

請參 [閱Analytics實作指南](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) 中的訪客移轉。

在您上傳 JavaScript 檔案後，系統就會執行第一方 Cookie 資料收集所需的所有設定。建議您在接下來幾小時監控 Analytics 報告，以確認系統能繼續正常收集資料。如果未正常運作，請確認前述所有步驟均已完成，並推派組織的任何一名支援使用者連絡客戶服務。
