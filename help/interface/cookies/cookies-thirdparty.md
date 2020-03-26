---
description: 由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。
keywords: cookies;privacy
seo-description: 由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。
seo-title: 第三方 Cookie 支援的變更如何影響客戶
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: 第三方 Cookie 支援的變更如何影響客戶
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# How changes to third-party cookie support impact customers{#how-changes-to-third-party-cookie-support-impacts-customers}

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

   * 如果搜尋是根據Adobe Analytics資料最佳化，則會以與Adobe Analytics相同的方式影響搜尋。
   * 轉換資料的收集不應受影響。

* 顯示:

   * 今天的顯示再行銷完全取決於第三方Cookie的使用。
   * 顯示還嚴重依賴於各種廣告網路Cookie的可用性，以進行同步。
   * 整體影響未知。 但是，在第一點，顯示受到的影響比其他服務更大。
   * 我們正與廣告合作夥伴進行內部合作，以評估廣告投放的整體影響。

* 社交:

   * 對Facebook市集廣告沒有影響。
   * Facebook Exchange(FBX)將受到與顯示廣告傳送相同的影響。
