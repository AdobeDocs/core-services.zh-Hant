---
description: 了解第三方 Cookie 支援如何在各瀏覽器上受到越來越多限制。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics,Target
title: '第三方 Cookie 支援的變更會如何影響客戶 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: ae14748aa7b0f0d803d48fe980a6743f53d996ab
workflow-type: ht
source-wordcount: '265'
ht-degree: 100%

---

# 第三方 Cookie 支援的變更會如何影響客戶{#how-changes-to-third-party-cookie-support-impacts-customers}

第三方 Cookie 支援在各瀏覽器上受到越來越多限制。因此，Adobe 一直在研究全新的應用程式，以便小心平衡客戶需求及使用 Experience Cloud 應用程式的消費者隱私權。

下列清單概述第三方 Cookie 支援如何影響目前 Experience Cloud 應用程式的實施：

## Adobe Analytics 和 Adobe Target

* 由於相同的網站活動只會依賴第一方 Cookie，所以 Analytics 和 Target 基本上不受影響。 了解跨網域的使用者活動需要第三方 Cookie。 若是已封鎖第三方 Cookie 的瀏覽器，則無法使用 Cookie 進行跨網域追蹤。

## Adobe Experience Manager

* 由於 Adobe Experience Manager 全於客戶網域內運作，與第三方 Cookie 的互動極少，所以幾乎不受影響。

## Adobe Social

* 只要客戶使用最新版的程式碼，Social 就不受影響。

## Adobe Advertising Cloud

* 搜尋：

   * 如果搜尋是根據 Adobe Analytics 資料最佳化，則會以與 Adobe Analytics 相同的方式影響搜尋。
   * 轉換資料的收集應不會受影響。

* 顯示：

   * 當天的顯示再行銷完全取決於第三方 Cookie 的使用情況。
   * 顯示情形也高度取決於同步功能各種廣告網路 Cookie 的可用性。
   * 整體影響未知。但是，根據第一點，顯示受到的影響會比其他服務大。
   * 我們正與廣告合作夥伴進行內部合作，評估對廣告投放造成的整體影響。
