---
description: 了解 Adobe Experience Cloud 中的 Adobe Analytics Cookie。
solution: Experience Cloud,Analytics,Target
title: Adobe Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bc8ce894-f98c-4475-8a07-d74ae76f7451
source-git-commit: 2691f0dc91e48a8f817467e334d9028f2e506e70
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 16%

---

# Adobe Analytics Cookie

Adobe Analytics 使用 Cookie 來區分不同瀏覽器的請求，以及儲存應用程式之後可使用的有用資訊。 它們也可用來將瀏覽資訊與客戶記錄相關聯。

Analytics會使用Cookie以匿名方式定義新訪客、協助分析點按資料流資料，以及追蹤網站上的歷史活動，例如對特定行銷活動的回應或銷售週期的長度。

| Cookie 名稱 | 有效期限 | 大小 | 位置 | 說明 |
| --- | --- | --- | --- | --- |
| **`s_ecid`** | 2 年 | 45 位元組 | 第一方 | 儲存Experience CloudID (ECID)或MID。 由HTTP回應設定。 MID儲存於 `s_ecid=MCMID` 格式。 在使用者端設定AMCV Cookie之後設定。 它允許永久性的第一方ID追蹤，並在AMCV Cookie過期時作為參考ID使用。 此Cookie不適用於第三方Cookie實施。 `SameSite` 設為「Lax」。 |
| **`s_cc`** | Session | 4 位元組 | 第一方 | 判斷是否已啟用Cookie。 由JavaScript設定。 |
| **`s_sq`** | Session | 100-200位元組 | 第一方 | 由Activity Map使用。 它包含訪客點按的上一個連結相關資訊。 由JavaScript設定。 |
| **`s_vi`** | 2 年 | 44 位元組 | 第一方，或 `*.omtrdc.net` （協力廠商） | 儲存不重複訪客ID和時間戳記。 由HTTP回應設定。 每個訪客ID都與Adobe伺服器上的訪客資料相關聯。 無論訪客ID Cookie過期與否，訪客閒置1年後都會刪除其訪客資料。 此 `Secure` 旗標設定時機 `SameSite` 為「無」且連線為HTTPS。 `SameSite` 第一方Cookie預設為「Lax」。 `SameSite` 使用協力廠商Cookie時為「無」，例如 `omtrdc.net` 或 `2o7.net`. 設定 `SameSite` 設為「無」（使用單一CNAME追蹤多個網域或屬性時）。 |
| **`s_fid`** | 2 年 | 33 位元組 | 第一方 | 儲存遞補不重複訪客ID和時間戳記。 若為標準，則由JavaScript設定 `s_vi` 由於第三方Cookie限制，無法設定Cookie。 不用於第一方Cookie實作。 |

{style="table-layout:auto"}

## 外掛程式設定的 Cookie

有些實施會使用外掛程式，這些程式碼片段可為Analytics提供額外功能。 這些外掛程式可設定上方未列出的Cookie。 另請參閱 [Analytics外掛程式概述](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/plugins/impl-plugins) 以取得可用外掛程式及其設定的Cookie清單。
