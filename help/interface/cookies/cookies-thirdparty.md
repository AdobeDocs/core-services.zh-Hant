---
description: 由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。
keywords: Cookie;隱私
seo-description: 由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。
seo-title: 第三方 Cookie 支援的變更如何影響客戶
solution: Marketing Cloud, Analytics, Target, Social
title: 第三方 Cookie 支援的變更如何影響客戶
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# 第三方 Cookie 支援的變更會如何影響客戶{#how-changes-to-third-party-cookie-support-impacts-customers}

由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。

下列清單概述第三方 Cookie 支援如何影響目前 Adobe Experience Cloud 解決方案的實作:

## Adobe Analytics 和 Adobe Target

* 使用[第一方實作](/help/interface/cookies/cookies-first-party.md)的客戶大致上不受影響。
* Customers that are not using first-party implementation can implement the [Experience Platform ID Service](https://docs.adobe.com/content/help/en/id-service/using/implementation-guides/implementation-guides.html) to store the ID cookie as a first-party cookie without a first-party implementation.

## Adobe Experience Manager

* 由於 Adobe Experience Manager 全於客戶網域內運作，與第三方 Cookie 的互動極少，所以幾乎不受影響。

## Adobe Social

* 只要客戶擁有最新版的程式碼，Social 就不受影響。

## Adobe Advertising Cloud

* 搜尋:

   * 若搜尋是根據 Adobe Analytics 資料而最佳化，則受到的影響和 Adobe Analytics 相同。
   * 轉換資料的收集應不受影響。

* 顯示內容:

   * 現今重新行銷的顯示內容全取決於第三方 Cookie 的使用。
   * 顯示內容也大多取決於不同廣告網路 Cookie 同步化的可用性。
   * 整體影響不得而知。然而，以第一點看來，顯示內容受到的影響比其他服務還多。
   * 我們內部正努力研究，同時也與的廣告合作夥伴一同評估廣告投放所受影響的全部範圍。

* 社交:

   * 對 Facebook market­place 廣告並未造成影響。
   * 對 Facebook Exchange (FBX) 造成的影響與對顯示廣告傳送造成的影響相同。

