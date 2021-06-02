---
description: 了解第三方 Cookie 支援如何在各瀏覽器上日益受限。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics,Target
title: '第三方 Cookie 支援的變更會如何影響客戶 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: 3d12a1b1-c952-4b42-815d-f64b31429cec
source-git-commit: f720e37b693da2c657cb1efab45620c60bfa81a4
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 59%

---

# 第三方 Cookie 支援的變更會如何影響客戶{#how-changes-to-third-party-cookie-support-impacts-customers}

跨瀏覽器對協力廠商Cookie的支援已變得更為有限。 因此，Adobe一直在開發新的解決方案，在客戶需求與消費者的跨Experience Cloud應用程式隱私權之間謹慎平衡。

下列清單概述協力廠商Cookie支援如何影響目前的Experience Cloud應用程式實作：

## Adobe Analytics 和 Adobe Target

* Analytics和Target基本上不受影響，因為相同的網站活動僅依賴第一方Cookie。 需要第三方Cookie才能了解跨網域的使用者活動。 若為已封鎖第三方Cookie的瀏覽器，則無法使用Cookie進行跨網域追蹤。

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
   * Adobe正與我們的廣告合作夥伴進行內部合作，評估對廣告投放的完整影響。
