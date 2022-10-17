---
description: 了解 Adobe Analytics 如何使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。
solution: Experience Cloud,Analytics
title: "第一方 Cookie "
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: f5cead10ecfeefeb560e92881524650e55bd938d
workflow-type: tm+mt
source-wordcount: '1636'
ht-degree: 78%

---

# 關於第一方 Cookie

Analytics 會使用 Cookie，針對未跨影像請求與瀏覽器作業存留的變數和元件提供相關資訊。Adobe 會在可能的情況下使用第一方 Cookie 來記錄您網站上的活動。 若要記錄不同網站 (例如您可能擁有的其他網域) 上的活動，則需要第三方 Cookie。

許多瀏覽器與反間諜軟體應用程式在設計上會拒絕及刪除第三方 Cookie。 Adobe 會確保總是可以設定 Cookie，即便在第三方 Cookie 被封鎖時。 具體行為會依您使用Experience Platform身分識別服務（ECID服務）或Analytics的舊版識別碼（亦稱為s_vi Cookie）而有所不同：

* [Experience Platform Identity Service (ECID Service)](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=en) 將會自動設定第一方 Cookie，無論您的收集網域是否符合您網站的網域。 如果不相符，Identity Service會使用JavaScript在您網站的網域中設定Cookie。
* 如果您正在使用 [Analytics 舊型識別碼](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=en) (亦即 `s_vi` Cookie)，則將取決於您已設定您的資料收集伺服器的方式。 如果資料收集伺服器符合您網站的網域，則 Cookie 會設定為第一方。如果資料收集伺服器不符合您目前的網域，則 Cookie 會設定為協力廠商。 在此情況下，如果第三方 Cookie 被封鎖，Analytics 會設定第一方[備援 ID (s_fid)](cookies-analytics.md)，而不是標準「s_vi」Cookie。

若您想要確保您的收集伺服器符合您網站的網域，您可以使用CNAME實作，該實作將啟用從CNAME實作中指定的自訂網域，到Adobe的收集伺服器的轉送。 這涉及到貴公司的 DNS 設定變更，以便設定 CNAME 別名來指向 Adobe 代管網域。 請注意，雖然有多項 Adobe 產品支援使用 CNAME，但在所有情況下，CNAME 都是用來為特定客戶建立受信任的第一方端點，且擁有權屬於該客戶。 如果您控制多個網域，這些網域可能會使用單一 CNAME 端點來追蹤其網域中的使用者，但只要網站網域不符合 CNAME 網域，Cookie 就會設定為協力廠商。 

>[!NOTE]
>
>無論您的收集網域是否符合網站網域，Apple的智慧型追蹤預防(ITP)程式都會讓由Adobe設定的第一方Cookie在受ITP控管的瀏覽器上短暫存留，包括macOS上的Safari以及iOS和iPadOS上的所有瀏覽器。 截至 2020 年 11 月，透過 CNAME 設定的 Cookie 也與透過 JavaScript 設定的 Cookie 具有相同有效期。 此有效期可能會有變動。

如果您想要為資料收集建立 CNAME，而且您的網站具有使用 HTTPS 通訊協定的安全頁面，您可以與 Adobe 合作來取得 SSL 憑證。

SSL 憑證簽發過程複雜難懂，而且耗時。因此，Adobe 與業界領先的憑證授權機構 (CA) DigiCert 建立合作關係，並開發出整合程序，將憑證的購買和管理作業自動化。

取得您的許可後，我們就會與我們的 CA 合作，為您核發、部署及管理新的 SHA-2 SSL 憑證。Adobe 會繼續管理此憑證，並確保未預期的過期、撤銷或安全性疑慮等問題不會影響貴組織安全收集資料的相關作業。

## Adobe 託管的證書計劃

Adobe Managed Certificate Program 是設定 CNAME 實作所需的第一方 SSL 憑證的建議程序，好讓您確保您的 Adobe 資料收集伺服器與您網站的網域相符。

Adobe Managed Certificate Program 可讓您針對您的前 100 個 CNAME 免費實作新的第一方 SSL 憑證。 如果您目前已有自己的客戶託管 SSL 憑證，請向 Adobe 客戶服務洽詢移轉至 Adobe Managed Certificate Program 的相關資訊。

### 實作

以下說明如何為第一方資料收集實作新的第一方 SSL 憑證：

1. 填寫[第一方網域請求表單](/help/interface/cookies/assets/First_Part_Domain_Request_Form.xlsx)，並請客戶服務人員開立支援服務單，要求在 Adobe Managed Program 上設定第一方資料收集。 

   每個欄位在文件中都有範例解說。

1. 建立 CNAME 記錄 (請參閱下方說明)。

   客戶服務代表在收到支援服務單後，應該會提供您 CNAME 記錄。 您必須在貴公司的 DNS 伺服器上設定這些記錄，Adobe 才能代表您購買憑證。 CNAME 類似於以下內容：

   **安全** - 例如主機名稱 `smetrics.example.com` 指向：`example.com.adobedc.net`。

   >[!NOTE]
   > 過去，Adobe建議客戶設定兩個CNAME，一個用於HTTPS，一個用於HTTP。 由於這是加密流量的最佳實務，而且大部分的瀏覽器都強烈阻止HTTP，因此我們不建議再為HTTP設定CNAME。 現在，將兩者設為最佳實務 `trackingServer` 和 `trackingServerSecure` 的CNAME。 例如，兩者 `trackingServer` 和 `trackingServerSecure` 會設為 `smetrics.example.com`. 僅允許第三方主機名使用HTTP。

1. 完成 CNAME 設定後，Adobe 會與 DigiCert 合作來購買憑證，並安裝到 Adobe 的生產伺服器上。

   如果您已有實作，可考慮將訪客移轉以保留現有的訪客。將憑證上線推送至Adobe的生產環境後，您可以將追蹤伺服器變數更新為新主機名稱。 換句話說，如果網站不安全 (HTTP)，請更新 `s.trackingServer`。如果網站安全 (HTTPS)，請更新 `s.trackingServer` 和 `s.trackingServerSecure` 這兩個變數。

1. [驗證主機名稱轉送](#validate) (請參閱下文)。

1. [更新實作程式碼](#update) (請參閱下文)。

### 維護和更新

第一方憑證過期的30天前，Adobe會驗證CNAME是否仍有效且正在使用中。 若是如此，Adobe會假設您要繼續使用服務並代表您自動重新更新憑證。

目前，如果CNAME已移除且不再有效，Adobe不會更新憑證，且系統中的項目會標示為要移除。 如果已移除CNAME,Adobe會知道尚未使用該URL進行追蹤，因此可安全地移除。

### 常見問答

| 問題 | 回答 |
|---|---|
| **此程序是否安全？** | 是，Adobe Managed Program 不會在 Adobe 和核發憑證授權機構以外的地方傳遞憑證或私密金鑰，因此會比舊方法更安全。 |
| **Adobe 如何為網域購買憑證？** | 唯有當您將指定的主機名稱 (例如 `telemetry.example.com`) 指向 Adobe 擁有的主機名稱時，才能購買憑證。基本上，這等於是將此主機名稱委派給 Adobe，並允許 Adobe 代表您購買憑證。 |
| **我可以要求撤銷憑證嗎？** | 是，您身為網域的擁有者，有權要求撤銷憑證。 請向客戶服務開立票證，以完成此作業。 |
| **此憑證是否會使用 SHA-2 加密？** | 是的，Adobe會與DigiCert合作，核發SHA-2憑證。 |
| **這是否會產生額外費用？** | 不會，Adobe 目前免費提供此服務給所有現有的 Adobe Digital Experience 客戶。 |

{style=&quot;table-layout:auto&quot;}

## 建立 CNAME 記錄

您組織的網路營運團隊應建立 CNAME 記錄，以便設定 DNS 伺服器。每個主機名稱都會將資料轉寄給 Adobe 的資料收集伺服器。

FPC 專員會提供您已設定的主機名稱，以及主機名稱要指向的 CNAME。 例如：

* **SSL 主機名稱**：`smetrics.mysite.com`
* **SSL CNAME**：`mysite.com.adobedc.net`

>[!NOTE]
> 如果您還是使用不安全的機制，可以進行如下的設定：
> * **非 SSL 主機名稱**：`metrics.mysite.com`
> * **非 SSL CNAME**：`mysite.com.adobedc.net`


只要實作程式碼未變更，此步驟就不會影響資料收集作業，並可在更新實作程式碼後完成。

## 驗證主機名稱轉送 {#validate}

下列方法可用於進行驗證：

### 使用瀏覽器進行驗證

如果您已設定 CNAME 且已安裝憑證，便可使用瀏覽器進行驗證：

`https://smetrics.adobe.com/_check`

>[!NOTE]
>
>如果未安裝憑證，系統會顯示安全性警告。

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

在您編輯網站程式碼以使用第一方資料收集前，請先完成下列必要條件：

* 依照 [Adobe 託管憑證計劃](#adobe-managed-certificate-program)的&#x200B;*實施*&#x200B;一節所述步驟操作，請求取得 SSL 憑證。
* 建立 CNAME 記錄 (請參閱上方)。
* 驗證主機名稱 (請參閱上方)。

確認主機名稱會回應並將資料轉寄給 Adobe 資料收集伺服器後，您就可以變更實作，指向您自己的資料收集主機名稱。

1. 開啟您的核心 JavaScript 檔案 (`s_code.js/AppMeasurement.js`)。
1. 如果您要更新程式碼版本，請以較新版本取代整個 `s_code.js/AppMeasurement.js` 檔案，並汰換任何外掛程式或自訂項目 (如果有的話)。**或者**&#x200B;如果您只想更新第一方資料收集的相關程式碼，請找到 s.trackingServer 和 s.trackingServerSecure (如果使用 SSL) 變數，將其指向新的資料收集主機名稱。 以 mysite.com 為例：`s.trackingServer = "metrics.mysite.com"` `s.trackingServerSecure = "smetrics.mysite.com"`

1. 將更新後的核心 JavaScript 檔案上傳至您的網站。

1. 如果您要從長期實作中改為第一方資料收集，或變更成其他第一方資料收集主機名稱，Adobe 建議您將訪客從舊有網域移轉到新網域。

請參閱「Analytics 實作指南」中的「[訪客移轉](https://experienceleague.adobe.com/docs/analytics/technotes/visitor-migration.html?lang=en)」。

在您上傳 JavaScript 檔案後，系統就會執行第一方資料收集所需的所有設定。 Adobe 建議您在接下來幾小時監控 Analytics 報告，以確認系統能繼續正常收集資料。如果未正常運作，請確認前述所有步驟均已完成，並推派組織的任何一名支援使用者連絡客戶服務。
