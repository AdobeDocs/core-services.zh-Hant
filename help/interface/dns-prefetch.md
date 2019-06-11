---
description: 實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。
seo-description: 實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。
seo-title: 搭配使用DNS預先擷取功能與不同的解決方案和服務
solution: Experience Cloud
title: 搭配使用DNS預先擷取功能與不同的解決方案和服務
uuid: 4220e223-e00 e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: af5339fe58ce884345804574c209907d6504a483

---


# 搭配使用DNS預先擷取功能與不同的解決方案和服務

實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。

## 瞭解DNS預先擷取 {#section_772BF9CB7C4141DE9B0355146E2CD962}

瀏覽器會利用 DNS 預先擷取自動將網頁連結的網域名稱解析為其相應的 IP 位址。瀏覽器載入網頁時便會開始預先擷取程序。例如，假設您的頁面包含可點按的連結 `www.adobe.com`。瀏覽器載入此網頁時，它會透過 [DNS 系統](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)來尋找已連結的網域名稱，並將其解析為相應的數值 IP 位址。DNS 預先擷取會在訪客點選該連結或按鈕前，先將網域名稱解析為 IP 位址，有助改善網頁效能。DNS 預先擷取是一個對使用者透明的程序。

## DNS預先擷取和Adobe Experience Cloud解決方案 {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS 預先擷取會自動搭配網頁上的靜態內嵌連結使用，這意味著自動 DNS 預先擷取並不會搭配不同的 [!UICONTROL Experience Cloud] 解決方案和服務使用，因為:

* 網頁載入時，每個 Experience Cloud 解決方案或服務都會以動態方式產生 DNS 調用次數。
* 在產生這些調用次數之前，瀏覽器無法將網域名稱解析為 IP 位址。

然而，您可以透過 Experience Cloud 解決戶案手動實施 DNS 預先擷取。若要這麼做，請將HTML `<dns-prefetch>` 標記新增至頁面程式碼 `<head>` 的區段，如下所示。若正確實施，DNS 預先擷取便有助於節省數毫秒的網頁載時間。

## DNS預先擷取程式碼範例 {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下範例顯示如何為不同的 [!DNL Experience Cloud] 解決方案和服務產生 DNS 預先擷取調用次數。部分預先擷取的調用次數需要提供您的 [!DNL Adobe] 組織 ID 或追蹤伺服器資訊。在以下範例中，*斜體*代碼表示變數的預留位置。您可以使用自己的 [!DNL Adobe] 合作夥伴 ID、客戶代碼或追蹤伺服器資訊等等來取代該代碼。

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   如果您使用不安全和安全的追蹤伺服器，請為每個 DNS 名稱新增個別的標籤。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID服務：**`<link rel="dns-prefetch" href="//fast. *`在此處插入合作夥伴ID`*.demdex.net">`

* **動態標籤管理器** (DTM)：不需要。網頁載入時便會提供 DTM 連結。

* **Media Optimizer(Ad Cloud)：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **Target:** `<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_贊_ this]
>
>* [DNS 預先擷取](https://www.chromium.org/developers/design-documents/dns-prefetching)

