---
description: 瞭解如何搭配CX Enterprise中不同的應用程式和服務實作DNS預先擷取，以縮短頁面載入時間。
solution: Experience Cloud
title: 使用DNS預先擷取
uuid: 4220e223-e00e-46b1-8bde-52248913bea1
topic: Administration
role: Admin
level: Experienced
exl-id: caf2ff76-2076-436d-a5a7-aff531464480
TQID: https://experienceleague.adobe.com/oAe81mw-qFetDM0zky2eS6DNf-XZ67H68Qw-Sa8mk0Y
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7bfc22e90d727d1743c2b6b7bc645033d5d38f1b
workflow-type: tm+mt
source-wordcount: 359
ht-degree: 77%

---

# 使用 DNS 預先擷取

實作 DNS 預先擷取以縮短不同應用程式和服務的頁面載入時間。

## 了解 DNS 預先擷取

瀏覽器會使用 DNS 預先擷取功能，自動將網頁上連結的網域名稱解析為其對應的 IP 位址。 預先擷取程序會在瀏覽器載入網頁時開始執行。 例如，假設您的網頁含有連結至 `www.adobe.com` 的可選取連結。 瀏覽器載入此網頁時，會透過 _DNS 系統_&#x200B;來尋找已連結的網域名稱，並將其解析為相應的數值 IP 位址。 DNS 預先擷取功能有助於改善頁面效能，因為網站訪客點按該連結或按鈕之前，網域名稱已解析為 IP 位址。 DNS 預先擷取程序向使用者公開呈現。

## DNS預先擷取和Adobe CX企業版應用程式

DNS 預先擷取可自動與頁面上的靜態嵌入式連結搭配使用。 這也表示自動DNS預先擷取不適用於不同的[!UICONTROL CX Enterprise]應用程式和服務，原因如下：

* 每個CX Enterprise應用程式或服務會在頁面載入時以動態方式產生DNS呼叫。
* 發出這些呼叫之前，瀏覽器無法將網域名稱解析為 IP 位址。

不過，您可以使用CX Enterprise應用程式手動實作DNS預先擷取。 做法是將 HTML `<dns-prefetch>` 標記新增至網頁代碼的 `<head>` 區段，如下所示。 若正確實作，DNS 預先擷取便有助於節省數毫秒的網頁載時間。

## DNS 預先擷取程式碼範例

以下範例說明如何產生 DNS 預先擷取呼叫來呼叫不同的 [!DNL CX Enterprise] 應用程式和服務。 部分預先擷取的調用次數需要提供您的 [!DNL Adobe] 組織 ID 或追蹤伺服器資訊。 在以下範例中，*斜體*&#x200B;代碼表示變數的預留位置。 您可以使用自己的 [!DNL Adobe] 合作夥伴 ID、客戶代碼或追蹤伺服器資訊等來取代該代碼。

* **Analytics：**`<link rel="dns-prefetch" href="//data.example.com">`。

  如果您使用不安全和安全的追蹤伺服器，請為每個 DNS 名稱新增個別的標記。

* **Audience Manager：**`<link rel="dns-prefetch" href="//dpm.demdex.net">`

* **訪客ID服務：** `<link rel="dns-prefetch" href="//fast.examplepartnerid.demdex.net">`

* **Advertising Cloud：**

   * `<link rel="dns-prefetch" href="//pixel.everesttech.net">`
   * `<link rel="dns-prefetch" href="//cm.everesttech.net">`

* **[!DNL Target]：**`<link rel="dns-prefetch" href="//example.tt.omtrdc.net">`

>[!MORELIKETHIS]
>
>* Chromium上的[DNS預先擷取](https://www.chromium.org/developers/design-documents/dns-prefetching)

