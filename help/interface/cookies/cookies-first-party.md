---
description: 了解 Analytics 如何使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics
title: '"第一方 Cookie "'
index: y
snippet: y
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
translation-type: tm+mt
source-git-commit: 4e3d6e605df4d1861f1dffb4cde5311eea283ee3
workflow-type: tm+mt
source-wordcount: '1499'
ht-degree: 86%

---

# 關於第一方 Cookie

Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。這些無害的 Cookie 源自由 Adobe 託管的網域，稱之為第三方 Cookie。

許多瀏覽器與反間諜軟體應用程式在設計上會拒絕及刪除第三方 Cookie，包括 Analytics 為收集資料所使用的 Cookie。若要支援您追蹤訪客與網站互動的方式，您可以實作第一方 Cookie。

實作第一方 Cookie 有兩種選項：

* Experience Platform ID Service。ID Service 可使用 JavaScript 在第一方情境中設定 Cookie。
* 貴公司 DNS 伺服器上的 DNS 項目，用於設定 Adobe 所託管網域的 CNAME 別名。請注意，雖然有多項 Adobe 產品支援使用 CNAME，但在所有情況下，CNAME 都是用來為特定客戶建立受信任的第一方端點，且擁有權屬於該客戶。如果該客戶控制著多個網域，他們可能會使用單一 CNAME 端點來追蹤跨其網域的使用者，但這需要 CNAME 網域以外的所有網域使用第三方 Cookie，如此一來，當第三方 Cookie 遭到封鎖就會無法運作，因此不建議使用。Adobe CNAME 永遠不會用於追蹤跨不同客戶所擁有網域中的個人或裝置。

>[!NOTE]
>
>對於這兩個選項，Apple的Intelligent Tracking Prevention(ITP)程式會讓第一方Cookie在ITP管轄的瀏覽器上短暫存留，這些瀏覽器包括MacOS上的Safari以及iOS和iPadOS上的所有瀏覽器。 自2020年11月起，這兩種Cookie都有7天的到期日。 此過期日期可能會變更。

針對使用 CNAME 的第二個選項，如果您的網站具有使用 HTTPS 通訊協定的安全頁面，您可以與 Adobe 合作取得 SSL 憑證以實作第一方 Cookie。Adobe 強烈建議您只使用 HTTPS 來資料收集，因為我們將於 2020 年下半年停止支援以 HTTP 收集。

SSL 憑證簽發過程複雜難懂，而且耗時。因此，Adobe 與業界領先的憑證授權機構 (CA) DigiCert 建立合作關係，並開發出整合程序，將憑證的購買和管理作業自動化。

取得您的許可後，我們就會與我們的 CA 合作，為您核發、部署及管理新的 SHA-2 SSL 憑證。Adobe 會繼續管理此憑證，並確保未預期的過期、撤銷或安全性疑慮等問題不會影響貴組織安全收集資料的相關作業。

## Adobe Managed Certificate Program

Adobe Managed Certificate Program 是為第一方 Cookie 實作新第一方 SSL 憑證的建議程序。

Adobe Managed Certificate Program 可讓您免費對第一方 Cookie 實作新的第一方 SSL 憑證 (前 100 個 CNAME)。如果您目前已有自己的客戶託管 SSL 憑證，請向 Adobe 客戶服務洽詢移轉至 Adobe Managed Certificate Program 的相關資訊。

### 實作

以下說明如何為第一方 Cookie 實作新的第一方 SSL 憑證：

1. 填寫[第一方 Cookie 請求表單](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)並請客戶服務開立支援工單，要求在 Adobe Managed Program 上設定第一方 Cookie。每個欄位在文件中都有範例解說。

2. 建立 CNAME 記錄 (請參閱下方說明)。

   收到票證後，客戶服務代表應提供您CNAME記錄。 請在您公司的 DNS 伺服器上設定這些記錄，Adobe 才能代表您購買憑證。CNAME將類似下列：

   **安全** - 例如主機名稱 `smetrics.example.com` 指向：`example.com.adobedc.net`。

>[!NOTE]
> 過去，我們建議客戶為HTTPS設定兩個CNAME，為HTTP設定一個。 由於這是加密流量的最佳實務，而且大部分的瀏覽器都強烈阻礙HTTP，因此我們不再建議為HTTP設定CNAME。 如果您需要，則會顯示如下：
>    **非安全** —主機名`metrics.example.com`指向：`example.com.adobedc.net`。

1. 當CNAME到位時，Adobe將與DigiCert合作，在Adobe的生產伺服器上購買並安裝證書。

   如果您已有實作，可考慮將訪客移轉以保留現有的訪客。在 Adobe 的生產環境中將憑證上線後，您就可以將追蹤伺服器變數更新為新主機名稱。換句話說，如果網站不安全 (HTTP)，請更新 `s.trackingServer`。如果網站安全 (HTTPS)，請更新 `s.trackingServer` 和 `s.trackingServerSecure` 這兩個變數。

2. [驗證主機名稱轉送](#validate) (請參閱下文)。

3. [更新實作程式碼](#update) (請參閱下文)。

### 維護和更新

SSL 憑證每年到期，表示 Adobe 必須每年為各實作購買新憑證。實作即將到期前，組織內所有支援的使用者都會收到電子郵件通知。若希望 Adobe 續約您的主機名稱，需由一名支援的使用者代表回覆 Adobe 的電子郵件，並說明貴組織打算繼續使用該即將到期的主機名稱來收集資料。如此一來，Adobe 就會自動購買並安裝新憑證。

### 常見問題

| 問題 | 回答 |
|---|---|
| **此程序是否安全？** | 是，Adobe Managed Program 不會在 Adobe 和核發憑證授權機構以外的地方傳遞憑證或私密金鑰，因此會比舊方法更安全。 |
| **Adobe 如何為網域購買憑證？** | 唯有當您將指定的主機名稱 (例如 `telemetry.example.com`) 指向 Adobe 擁有的主機名稱時，才能購買憑證。基本上，這等於是將此主機名稱委派給 Adobe，並允許 Adobe 代表您購買憑證。 |
| **我可以要求撤銷憑證嗎？** | 可以。您身為網域所有者，有權要求我們撤銷憑證。您只需請客戶服務開立支援工單，即可完成此程序。 |
| **此憑證是否會使用 SHA-2 加密？** | 是，Adobe 會與 DigiCert 合作，核發 SHA-2 憑證。 |
| **這是否會產生額外費用？** | 不會，Adobe 目前免費提供此服務給所有現有的 Adobe Digital Experience 客戶。 |

## 建立 CNAME 記錄

您組織的網路營運團隊應建立新 CNAME 記錄，以設定 DNS 伺服器。每個主機名稱都會將資料轉寄給 Adobe 的資料收集伺服器。

FPC專員會提供您已設定的主機名稱，以及要指向的CNAME。 例如：

* **SSL 主機名稱**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> 如果您仍使用非安全功能，則會顯示為此。
> * **非 SSL 主機名稱**：`metrics.mysite.com`
> * **非 SSL CNAME**：`mysite.com.adobedc.net`


只要實作程式碼未變更，此步驟就不會影響資料收集作業，並可在更新實作程式碼後完成。

>[!NOTE]
>
>Experience Cloud訪客ID服務提供設定CNAME以啟用第一方Cookie的替代方式。

## 驗證主機名稱轉送 {#validate}

下列方法可用於進行驗證：

### 使用瀏覽器進行驗證

如果您已設定 CNAME 且已安裝憑證，便可使用瀏覽器進行驗證：

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>如果未安裝憑證，系統會顯示安全性警告。

### 使用 [!DNL curl] 進行驗證

Adobe 建議從命令列使用 [[!DNL curl]](https://curl.haxx.se/)。([!DNL Windows] 使用者可從以下位置安裝 [!DNL curl]：<https://curl.haxx.se/windows/>)。

如果您已設定 CNAME 但未安裝憑證，請執行：
`curl -k https://smetrics.adobe.com/_check`
回應：`SUCCESS` 

(`-k` 值會停用安全性警告)。

如果您已設定 CNAME 且已安裝憑證，請執行：
`curl https://smetrics.adobe.com/_check`
回應：`SUCCESS`

### 使用 [!DNL nslookup] 進行驗證

您可以使用 `nslookup` 進行驗證。以 `smetrics.adobe.com` 為例，開啟命令提示並輸入 `nslookup smetrics.adobe.com`

如果一切皆設定成功，您會看到系統傳回類似下列的內容：

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

編輯網站程式碼以使用第一方 Cookie 前，請先完成下列必要條件：

* 依照 [Adobe Managed Certificate Program](#adobe-managed-certificate-program) 的&#x200B;*實作*&#x200B;一節中所述步驟操作，請求 SSL 憑證。
* 建立 CNAME 記錄 (請參閱上方)。
* 驗證主機名稱 (請參閱上文)。

確認主機名稱會回應並將資料轉寄給 Adobe 資料收集伺服器後，您就可以變更實作，指向您自己的資料收集主機名稱。

1. 開啟您的核心 JavaScript 檔案 (`s_code.js/AppMeasurement.js`)。
1. 如果您要更新程式碼版本，請以較新版本取代整個 `s_code.js/AppMeasurement.js` 檔案，並汰換任何外掛程式或自訂項目 (如果有的話)。**或者**，如果您只想更新第一方 Cookie 相關程式碼，請找到 s.trackingServer 和 s.trackingServerSecure (如果使用 SSL) 變數，將其指向您新的資料收集主機名稱。以 mysite.com 為例：`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 將更新後的核心 JavaScript 檔案上傳至您的網站。

1. 如果您要從長期實作改為第一方 Cookie，或變更成其他第一方收集主機名稱，建議您將訪客從舊有網域移轉到新網域。

請參閱「Analytics 實作指南」中的[訪客移轉](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/visitor-migration.html)。

在您上傳 JavaScript 檔案後，系統就會執行第一方 Cookie 資料收集所需的所有設定。建議您在接下來幾小時監控 Analytics 報告，以確認系統能繼續正常收集資料。如果未正常運作，請確認前述所有步驟均已完成，並推派組織的任何一名支援使用者連絡客戶服務。
