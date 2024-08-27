---
description: 了解如何搭配 Experience Cloud 中不同的應用程式和服務實作 DNS 預先擷取，以縮短頁面載入時間。
solution: Experience Cloud
title: 使用DNS預先擷取
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 91%

---

# 使用 DNS 預先擷取

實作 DNS 預先擷取以縮短不同應用程式和服務的頁面載入時間。

## 了解 DNS 預先擷取

瀏覽器會使用 DNS 預先擷取功能，自動將網頁上連結的網域名稱解析為其對應的 IP 位址。預先擷取程序會在瀏覽器載入網頁時開始執行。例如，假設您的網頁含有連結至 `www.adobe.com` 的可選取連結。 瀏覽器載入此網頁時，會透過 [DNS 系統](https://www.networksolutions.com/support/what-is-a-domain-name-server-dns-and-how-does-it-work/)來尋找已連結的網域名稱，並將其解析為相應的數值 IP 位址。DNS 預先擷取功能有助於改善頁面效能，因為網站訪客點按該連結或按鈕之前，網域名稱已解析為 IP 位址。DNS 預先擷取程序向使用者公開呈現。

## DNS 預先擷取和 Adobe Experience Cloud 應用程式

DNS 預先擷取可自動與頁面上的靜態內嵌式連結搭配使用。 這也表示自動DNS預先擷取不適用於其他[!UICONTROL Experience Cloud]應用程式和服務，原因如下：

* 每個 Experience Cloud 應用程式或服務會在頁面載入時以動態方式產生 DNS 呼叫。
* 發出這些呼叫之前，瀏覽器無法將網域名稱解析為 IP 位址。

不過，您可以使用 Experience Cloud 應用程式手動實作 DNS 預先擷取。 做法是將 HTML `<dns-prefetch>` 標記新增至網頁代碼的 `<head>` 區段，如下所示。若正確實作，DNS 預先擷取便有助於節省數毫秒的網頁載時間。

## DNS 預先擷取程式碼範例

以下範例說明如何產生 DNS 預先擷取呼叫來呼叫不同的 [!DNL Experience Cloud] 應用程式和服務。 部分預先擷取的調用次數需要提供您的 [!DNL Adobe] 組織 ID 或追蹤伺服器資訊。在以下範例中，*斜體*&#x200B;代碼表示變數的預留位置。您可以使用自己的 [!DNL Adobe] 合作夥伴 ID、客戶代碼或追蹤伺服器資訊等來取代該代碼。

* **Analytics：**`<link rel="dns-prefetch" href="//data.example.com">`。

  如果您使用不安全和安全的追蹤伺服器，請為每個 DNS 名稱新增個別的標記。

* **Audience Manager：**`<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **Experience CloudID服務：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]：**`<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromium上的[DNS預先擷取](https://www.chromium.org/developers/design-documents/dns-prefetching)
