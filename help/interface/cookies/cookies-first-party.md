---
description: Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
keywords: Cookie;隱私
seo-description: Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
seo-title: First-Party Cookies
solution: Experience Cloud、Analytics
title: First-Party Cookies
index: y
snippet: y
translation-type: tm+mt
source-git-commit: 2bdc4b7287ccacfc4d968278b2c3ffdaeddfc105

---


# 關於第一方Cookie

Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。這些無害的 Cookie 源自 Adobe 所經營的網域，稱為第三方 Cookie。

許多瀏覽器和反間諜軟體應用程式旨在拒絕和刪除第三方Cookie，包括用於Analytics資料收集的Cookie。若要規避瀏覽器和程式所施加的追蹤限制，您可以實施第一方Cookie。

有兩個選項可用來實施第一方Cookie

* Experience Platform ID服務。ID服務可使用JavaScript在第一方上下文中設定Cookie。
* 您公司DNS伺服器上的DNS項目。
* 如果您的網站使用通訊 `https:` 協定而有安全頁面，而您未使用Experience Platform ID Service，則可與Adobe合作取得SSL憑證，以實施第一方Cookie

SSL憑證簽發程序通常會造成混淆和浪費。因此，Adobe與業界領先認證授權機構Digicert(CA)建立合作關係，並開發了一個整合程序，供這些憑證的購買和管理自動化。

在您的許可下，我們將與我們的CA合作，為您核發、部署和管理新的SHA-2SSL憑證。Adobe將繼續管理此憑證，並確保意外到期、撤銷或安全性顧慮不會危及貴組織安全收集的可用性。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program是建置第一方Cookie的新第一方SSL憑證的建議程序。

Adobe Managed Certificate Program可讓您免費為第一方Cookie實施新的第一方SSL憑證。如果您目前擁有自己的客戶管理SSL憑證，請洽詢Adobe客戶服務，以移轉至Adobe Managed Certificate Program。

### 實作

以下是如何為第一方Cookie實施新的第一方SSL憑證：

1. 填寫 [第一方Cookie請求表單](/help/interface/cookies/assets/FPC_Request_Form.xlsx) 並開立票證，並向客戶服務要求在Adobe Managed Program上設定第一方Cookie。每個欄位在文件中都有範例解說。

1. 建立CNAME記錄(請參閱下面的指示)。在收到票證時，FPSSL專員應該提供您一組CNAME記錄。這些記錄必須在您公司的DNS伺服器上設定，Adobe才能代表您購買憑證。CNAME類似下列： **安全** -例如，主機名稱 `smetrics.example.com` 指向： `example.com.ssl.d1.omtrdc.net`。**不安全** -例如，主機名稱 `metrics.example.com` 指向： `example.com.d1.omtrdc.net`。

1. 當這些CNAME就位時，Adobe將會與Digicert搭配使用，在Adobe的生產伺服器上購買並安裝憑證。如果您有現有實施，應考慮「訪客移轉」以維護現有訪客。將憑證推送至Adobe的生產環境後，您就可以將追蹤伺服器變數更新為新主機名稱。也就是說，如果網站不安全(https)，請更新 `s.trackingServer`。如果網站是安全的(https)，請更新這兩 `s.trackingServer` 個和 `s.trackingServerSecure` 變數。

1. Ping the hostname(請參閱下面)。

1. 更新實施程式碼(請參閱下文)。

### 維護和更新

SSL憑證每年到期，表示Adobe必須每年為每個實施購買新憑證。當實施接近有效期時，組織內所有受支援的使用者都會收到電子郵件通知。對於Adobe為您的主機名稱續約，一個受支援使用者必須回覆來自Adobe的電子郵件，並指出您打算繼續使用過期的主機名稱來收集資料。此時，Adobe會自動購買並安裝新憑證。

### 常問的問題

| 問題 | 回答 |
|---|---|
| **此程序是否安全？** | 是的，Adobe受管理計劃比我們舊有的方法更安全，因為不會在Adobe以外和核發憑證授權機構以外的位置手動變更憑證或私密金鑰。 |
| **Adobe如何為我們的網域購買憑證？** | 只有當您將指定的主機名稱(例如smetrics.example.com)指向Adobe擁有的主機名稱時，才能購買憑證。這基本上是將此主機名稱委派給Adobe，並允許Adobe代表您購買憑證。 |
| **我可以要求撤銷憑證嗎？** | 是的，身為網域的擁有者，您有權要求我們撤銷憑證。您只需要開立客戶服務票證，即可完成此程序。 |
| **此憑證是否會使用SHA-2加密？** | 是的，Adobe將會使用Digicert核發SHA-2憑證。 |
| **這是否會產生額外費用？** | 否，Adobe目前不提供任何額外的費用給所有的Analytics客戶。 |

## 建立CNAME記錄

貴組織的網路營運團隊應建立新的CNAME記錄，以設定DNS伺服器。每個主機名稱都會轉送資料至Adobe的資料收集伺服器。

FPC專員提供您設定的主機名稱，以及要指向的CNAME。例如:

* **SSL主機名稱**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.ssl.d1.sc.omtrdc.net`
* **非SSL主機名稱**：`metrics.mysite.com`
* **非SSL CNAME**：`mysite.com.d1.sc.omtrdc.net`

只要實施代碼未變更，此步驟將不會影響資料收集，而且可在更新實施程式碼後隨時執行。

>[!Nte：] Experience Cloud訪客ID服務提供設定CNAME以啓用第一方Cookie的替代方法。

## Ping the hostname

Ping the hostname name to確保正確轉送。所有主機名稱都必須回應ping，以免資料遺失。

正確設定CNAME記錄後，Adobe已確認安裝憑證，開啓命令提示字元並ping您的主機名稱。Using `mysite.com` as an example: `ping metrics.mysite.com`

如果一切設定順利，則會傳回如下畫面:

```Pinging mysite.com.112.2o7.net [66.235.132.232] with 32 bytes of data:
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246
Reply from 66.235.132.232: bytes=32 time=19ms TTL=246

Ping statistics for 66.235.132.232: Packets: Sent = 4, Received = 4, Lost = 0 (0% loss),
Approximate round trip times in milli-seconds: Minimum = 19ms, Maximum = 19ms, Average = 19ms
```

如果 CNAME 記錄未正確設定或未啟用，則會傳回如下畫面:

`Ping request could not find the host. Please check the name and try again.`

>[!Nte：] 如果您使用 `https:// protocol`，Ping只會在FPC專員指定的上傳日期之後回應。此外，請務必ping安全主機名稱和非安全主機名稱，以確保兩者都能正常運作，然後再更新您的實施。

## 更新實施程式碼

在您的網站上編輯程式碼以使用第一方Cookie之前，請先完成這些必要條件：

* 要求SSL憑證，如上述Adobe Managed Certificate Program實施步驟中所述。
* 建立CNAME記錄(請參閱上文)。
* Ping the hostname name(請參閱上文)。

確認您的主機名稱回應並轉送至Adobe資料收集伺服器後，您就可以變更實施，指向您自己的資料收集主機名稱。

1. Open your core JavaScript file (`s_code.js/AppMeasurement.js`).
1. 如果您要更新程式碼版本，請將整個 `s_code.js/AppMeasurement.js` 檔案取代為較新版本，並取代任何外掛程式或自訂 (如果有的話)。**或者，**&#x200B;如果您只想更新與第一方Cookie相關的程式碼，請找出s. trackingServer和s. trackingServerSecure(如果使用SSL)變數，並將它們指向您新的資料收集主機名稱。Using mysite.com as an example:`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 將更新的核心JavaScript檔案上傳至您的網站。

1. 如果您要從長期實施移至第一方Cookie，或變更為不同的第一方系列主機名稱，建議您將訪客從上一個網域移轉至新網域。

請參閱 [Analytics實施指南中的訪客移轉](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html) 。

上傳JavaScript檔案後，所有的項目都會設定為第一方Cookie資料收集。我們建議您監控Analytics報告數小時，以確保資料收集繼續正常運作。如果沒有，請確認上述所有步驟已完成，並讓您組織的受支援使用者之一聯絡客戶服務。
