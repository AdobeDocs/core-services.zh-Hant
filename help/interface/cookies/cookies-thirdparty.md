---
description: 了解第三方 Cookie 支援如何在各瀏覽器上日益受限。
keywords: cookies;privacy
solution: Experience Cloud,Analytics,Target
title: '第三方 Cookie 支援的變更會如何影響客戶 '
uuid: 27332e0d-6932-4a6e-b97b-0adeced0b050
translation-type: ht
source-git-commit: 3f26c1af19a0838913eec2b4135304f5f3fcf0b4
workflow-type: ht
source-wordcount: '295'
ht-degree: 100%

---


# 第三方 Cookie 支援的變更會如何影響客戶{#how-changes-to-third-party-cookie-support-impacts-customers}

由於不同瀏覽器上的第三方 Cookie 支援愈來愈受限，Adobe 正致力於開發新的解決方案，在客戶需求與客戶於不同 Adobe Experience Cloud 解決方案的隱私權之間謹慎取得平衡。

下列清單概述第三方 Cookie 支援如何影響目前 Adobe Experience Cloud 解決方案的實作：

## Adobe Analytics 和 Adobe Target

* 使用[第一方實作](/help/interface/cookies/cookies-first-party.md)的客戶大致上不受影響。
* 若客戶未使用第一方實作，可實作 [Experience Platform ID Service](https://docs.adobe.com/content/help/zh-Hant/id-service/using/implementation/implementation-guides.html)，將 ID Cookie 儲存為第一方 Cookie，如此便不需使用第一方實作。

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

* 社交：

   * 對 Facebook 市集廣告沒有影響。
   * Facebook Exchange (FBX) 受到的影響將與顯示廣告投放相同。
