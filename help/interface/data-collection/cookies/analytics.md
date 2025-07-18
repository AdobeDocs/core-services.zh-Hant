---
description: 了解 Adobe Experience Cloud 中的 Adobe Analytics Cookie。
solution: Analytics
title: Adobe Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: d3a559ca2f7963256d48a25cd51099edb5e3fe76
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 11%

---

# Adobe Analytics Cookie

Adobe Analytics 使用 Cookie 來區分不同瀏覽器的請求，以及儲存應用程式之後可使用的有用資訊。 它們也可用來將瀏覽資訊與客戶記錄相關聯。

Analytics會使用Cookie以匿名方式定義新訪客、協助分析點按資料流資料，以及追蹤網站上的歷史活動，例如對特定行銷活動的回應或銷售週期的長度。

| Cookie 名稱 | 有效期限 | 大小 | 位置 | 說明 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 13 個月 | 45 位元組 | 第一方 | 儲存Experience Cloud ID (ECID)或MID。 由HTTP回應設定。 MID是以`s_ecid=MCMID`格式儲存。 在使用者端設定AMCV Cookie之後設定。 它允許永久性的第一方ID追蹤，並在AMCV Cookie過期時作為參考ID使用。 `SameSite`已設為「Lax」。 如果您使用Web SDK來實作Adobe Analytics，Cookie有效期限會設為2年；不過，大部分的現代化瀏覽器都會將有效期限截斷為13個月。 |
| **`s_cc`** | Session | 4 位元組 | 第一方 | 判斷是否已啟用Cookie。 由JavaScript設定。 |
| **`s_sq`** | Session | 100-200位元組 | 第一方 | 由Activity Map使用。 它包含訪客點按的上一個連結相關資訊。 由JavaScript設定。 |
| **`s_vi`** | 2 年 | 44 位元組 | 第一方，或`*.omtrdc.net` （第三方） | 儲存不重複訪客ID和時間戳記。 由HTTP回應設定。 每個訪客ID都與Adobe伺服器上的訪客資料相關聯。 無論訪客ID Cookie過期與否，訪客閒置1年後都會刪除其訪客資料。 當`Secure`為「None」且連線為HTTPS時，`SameSite`旗標已設定。 第一方Cookie的`SameSite`預設為「Lax」。 使用協力廠商Cookie時，`SameSite`為「無」，例如在`omtrdc.net`或`2o7.net`上。 使用單一CNAME追蹤多個網域或屬性時，將`SameSite`設為「無」。 |
| **`s_fid`** | 2 年 | 33 位元組 | 第一方 | 儲存遞補不重複訪客ID和時間戳記。 如果因協力廠商Cookie限制而無法設定標準`s_vi` Cookie，則由JavaScript設定。 不用於第一方Cookie實作。 |
| **`s_ac`** | 立即 | 1位元組 | 第一方 | 協助判斷正確網域以設定AppMeasurement Cookie。 包含靜態值`"1"`。 設定此Cookie後，便會立即刪除。 |

## 外掛程式設定的 Cookie

有些實施會使用外掛程式，這些程式碼片段可為Analytics提供額外功能。 這些外掛程式可設定上方未列出的Cookie。 如需可用外掛程式及其設定的Cookie清單，請參閱[Analytics外掛程式總覽](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins)。

## 刪除Analytics Cookie的後果

如果訪客刪除其Analytics Cookie，請考慮下列事項：

* **訪客識別遺失：**&#x200B;刪除Cookie時，Adobe Analytics無法識別再度訪問的訪客。 使用者下次造訪您的網站時，即會計為新訪客。 [跨裝置分析](https://experienceleague.adobe.com/en/docs/analytics/components/cda/overview)可協助減輕此影響。
* **工作階段連續性中斷：**&#x200B;任何以工作階段為基礎或多次造訪的分析（例如歸因或轉換追蹤）都會中斷。 Cookie刪除後發生的事件和轉換無法由相同使用者繫結至先前的活動。
* **Personalization和分段受到影響：**&#x200B;根據訪客歷史記錄或行為的區段或個人化體驗會重設，因為先前的資料不再與目前的造訪相關聯。
* **跨網域追蹤已中斷：**&#x200B;若是第三方Cookie，刪除它們會讓Adobe Analytics無法連結您擁有之多個網域的使用者活動。
