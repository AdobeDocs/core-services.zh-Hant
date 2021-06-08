---
description: 了解如何搭配 Experience Cloud 中不同的解決方案和服務實作 DNS 預先擷取，以縮短頁面載入時間。
solution: Experience Cloud
title: '搭配不同的解決方案和服務使用 DNS 預先擷取 '
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
feature: 客戶屬性
topic: 管理
role: Administrator
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: c7ed1324015beb7ebcf7a4ee21b05601e36e608f
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 88%

---

# 搭配不同的解決方案和服務使用 DNS 預先擷取

實作 DNS 預先擷取以縮短不同解決方案和服務的頁面載入時間。

## 了解 DNS 預先擷取 {#section_772BF9CB7C4141DE9B0355146E2CD962}

瀏覽器會使用 DNS 預先擷取功能，自動將網頁上連結的網域名稱解析為其對應的 IP 位址。預先擷取程序會在瀏覽器載入網頁時開始執行。例如，假設您的頁面包含連結至`www.adobe.com`的可點按連結。 瀏覽器載入此網頁時，會透過 [DNS 系統](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)來尋找已連結的網域名稱，並將其解析為相應的數值 IP 位址。DNS 預先擷取功能有助於改善頁面效能，因為網站訪客點按該連結或按鈕之前，網域名稱已解析為 IP 位址。DNS 預先擷取程序向使用者公開呈現。

## DNS 預先擷取和 Adobe Experience Cloud 解決方案 {#section_202A07F9F79F4ABDA44B98BA1DDCD516}

DNS 預先擷取可自動與頁面上的靜態內嵌連結搭配使用。這也表示自動 DNS 預先擷取不適用於不同的 [!UICONTROL Experience Cloud] 解決方案和服務，原因如下：

* 每個 Experience Cloud 解決方案或服務會在頁面載入時以動態方式產生 DNS 呼叫。
* 發出這些呼叫之前，瀏覽器無法將網域名稱解析為 IP 地址。

不過，您可以使用 Experience Cloud 解決方案手動實作 DNS 預先擷取。做法是將 HTML `<dns-prefetch>` 標籤新增至網頁代碼的 `<head>` 區段，如下所示。若正確實作，DNS 預先擷取便有助於節省數毫秒的網頁載時間。

## DNS 預先擷取程式碼範例 {#section_E886F7B2861E48BA9EF3D8B3CE32B345}

以下範例顯示如何為不同的 [!DNL Experience Cloud] 解決方案和服務產生 DNS 預先擷取調用次數。部分預先擷取的調用次數需要提供您的 [!DNL Adobe] 組織 ID 或追蹤伺服器資訊。在以下範例中，*斜體*&#x200B;代碼表示變數的預留位置。您可以使用自己的[!DNL Adobe]合作夥伴ID、客戶代碼或追蹤伺服器資訊等來取代該代碼。

* **Analytics：**`<link rel="dns-prefetch" href="//insert tracking server name here">`。

   如果您使用不安全和安全的追蹤伺服器，請為每個 DNS 名稱新增個別的標籤。

* **Audience Manager：**`<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience Cloud ID 服務：**`<link rel="dns-prefetch" href="//fast. *`請在此處插入合作夥伴 ID`*.demdex.net">`

* **動態標籤管理員** (DTM)：不需要。頁面載入時，DTM連結即可使用。

* **Media Optimizer(Advertising Cloud):**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttechnet">`


* **[!DNL Target]：**`<link rel="dns-prefetch" href="//insert customer code here.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* [DNS 預先擷取](https://www.chromium.org/developers/design-documents/dns-prefetching)

