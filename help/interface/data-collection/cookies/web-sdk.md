---
title: Adobe Experience Platform Web SDK Cookie
description: 瞭解Web SDK如何使用適用於您實作的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k
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
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ce4fa63a4babc195f89c595009adcf19f34cdd9
workflow-type: tm+mt
source-wordcount: 396
ht-degree: 1%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie來儲存實作特有的值。

| 名稱 | 最大年齡 | 大小 | 說明 |
| ---| ---| ---| ---|
| **`AMCV_###@AdobeOrg`** | 34128000 （395天） | 100-120位元組（變數） | [`idMigrationEnabled`](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)啟用時出現。 當網站某些部分仍使用`visitor.js`時，轉換至網頁SDK會有所幫助。 Web SDK在移轉期間會讀取和寫入此Cookie。 |
| **`demdex`** | 15552000 （180天） | 因情況而異 | 在啟用Audience Manager ID同步時顯示。 Audience Manager設定此Cookie以指派唯一ID，並支援ID同步、細分、建模和報告。 檢視`demdex`Audience Manager Cookie[中的](audience-manager.md)。 |
| **`kndctr_<orgId>_identity`** | 34128000 （395天） | 100-120位元組（變數） | 儲存該裝置的ECID和其他相關資訊。 |
| **`kndctr_<orgId>_cluster`** | 1800 （30分鐘） | 3-5位元組 | 儲存Edge Network區域（位置提示），用於提供目前使用者的請求。 URL路徑會使用地區，這樣Edge Network就能將請求路由至正確的地區。 如果使用者在Cookie期限內，以不同的IP位址連線，請求會再次路由至最接近的區域。 |
| **`kndctr_<orgId>_consent`** | 15552000 （180天） | 10-11位元組 | 儲存訪客的同意偏好設定。 無論同意與否一律設定，因為它會儲存同意偏好設定本身。 |
| **`kndctr_<orgId>_consent_check`** | 7200 （2小時） | | 工作階段範圍的協助程式，用於在TTL過期後訊號Edge Network重新檢查伺服器端的同意書。 它會在快取同意時強制執行TTL。 |
| **`kndctr_<orgId>_personalization`** | 34128000 （395天） | | 儲存Adobe Target用來個人化內容的工作階段資訊。 |
| **`mbox`** | 63072000 （2年） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)啟用時出現。 它允許網頁SDK設定Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **`mboxEdgeCluster`** | 1800 （30分鐘） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)啟用時出現。 它可讓Web SDK將正確的邊緣叢集通訊給`at.js`，以便在使用者瀏覽網站時，Target設定檔可以保持同步。 |
| **`s_ecid`** | 63115200 （2年） | ~45 位元組 | 包含格式為`s_ecid=MCMID\|<ECID>`的Experience Cloud ID (ECID/MID)復本。 主要針對CNAME （第一方）案例，用作ECID的第一方備份。 |

Edge Network會設定具有`secure`和`sameSite="none"`屬性的所有Cookie。 如果您的網站上目前同時有安全和非安全區段，則使用者識別可能會不準確。 當使用者從網站的安全區段導覽到不安全的區段時，Edge Network會使用請求產生新的`ECID`。
