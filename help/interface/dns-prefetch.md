---
description: 實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。
seo-description: 實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。
seo-title: 搭配不同的解決方案和服務使用 DNS 預先擷取
solution: Experience Cloud
title: 搭配不同的解決方案和服務使用 DNS 預先擷取
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 搭配不同的解決方案和服務使用 DNS 預先擷取

實施 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。

## 瞭解 DNS 預先擷取 {#section_772BF9CB7C4141DE9B0355146E2CD962}

瀏覽器使用DNS預回遷功能，自動將網頁上連結的網域名稱解析為其對應的IP位址。 預回遷過程會在瀏覽器載入網頁時啟動。 例如，您的網頁含有連結至 `www.adobe.com` 的可點按連結。When a browser loads this page, it uses the [DNS system](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/) to look up the linked domain name and resolve it to a corresponding numeric IP address. DNS預回遷有助於改善頁面效能，因為網域名稱已解析為IP位址，網站訪客點按該連結或按鈕。 DNS預取程式對用戶是透明的。

## DNS 預先擷取和 Adobe Experience Cloud 解決方案 {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS預取可自動與頁面上的靜態內嵌連結搭配運作。 這也意味著自動DNS預取不適用於不同的 [!UICONTROL Experience Cloud解決方案和服務] ，因為：

* 每個Experience Cloud解決方案或服務會在頁面載入時動態產生DNS呼叫。
* 在進行這些呼叫之前，瀏覽器無法將域名解析為IP地址。

不過，您可以使用Experience Cloud解決方案手動實作DNS預回遷。 做法是將 HTML `<dns-prefetch>` 標籤新增至網頁代碼的 `<head>` 區段，如下所示。若正確實施，DNS 預先擷取便有助於節省數毫秒的網頁載時間。

## DNS 預先擷取代碼範例 {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下範例顯示如何為不同的 [!DNL Experience Cloud] 解決方案和服務產生 DNS 預先擷取調用次數。部分預先擷取的調用次數需要提供您的 [!DNL Adobe] 組織 ID 或追蹤伺服器資訊。在以下範例中，*斜體*&#x200B;代碼表示變數的預留位置。您可以使用自己的 [!DNL Adobe] 合作夥伴 ID、客戶代碼或追蹤伺服器資訊等等來取代該代碼。

* **Analytics:** `<link rel="dns-prefetch" href="//insert tracking server name here">`.

   如果您使用不安全和安全的追蹤伺服器，請為每個 DNS 名稱新增個別的標籤。

* **Audience Manager:** `<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID服務：** 在此 `<link rel="dns-prefetch" href="//fast. *`插入合作夥伴ID`*.demdex.net">`

* **動態標籤管理員** (DTM): 不需要。網頁載入時便會提供 DTM 連結。

* **Media Optimizer (Ad Cloud):**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]:**`<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORE_LIKE_THIS]
>
>* [DNS預取](https://www.chromium.org/developers/design-documents/dns-prefetching)

