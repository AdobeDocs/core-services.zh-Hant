---
title: Adobe Experience Platform Web SDK Cookie
description: 瞭解Web SDK如何使用適用於您實作的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
TQID: 'https://experienceleague.adobe.com/jysQ5m7o0cI3ECKz2RWZB4Kt3own7XAPm04pr4yLh-k'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
    internal-label: Getting started
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 7b12d5debfccd62ab7b416e9a6fe278d251a4ca5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 0%
---
# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie來儲存實作特有的值。

| 名稱 | 最大年齡 | 大小 | 說明 |
| --- | --- | --- | --- |
| **`AMCV_###@AdobeOrg`** | 由網路SDK撰寫時的33696000 （390天） | 由Web SDK (`MCMID\|<ECID>`)寫入時為44位元組；由`VisitorAPI.js`寫入時較大 | 當啟用[`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled) （預設）時出現。 當網站某些部分仍使用`VisitorAPI.js`時，轉換至網頁SDK會有所幫助。 網頁SDK會讀取此Cookie以重複使用現有的ECID。 Edge Network傳回ECID後，如果該Cookie遺失或包含其他ECID，則Web SDK會將其寫入此Cookie。 |
| **`com.adobe.alloy.getTld`** | 無（工作階段Cookie，立即刪除） | 22位元組 | 臨時協助程式Cookie，供Web SDK內部使用，以判斷目前網站的頂層網域。 Web SDK會在程式庫載入時、執行`configure`命令之前，以及評估同意之前寫入及刪除此Cookie，因此Cookie掃描程式可以在同意之前將其回報為設定。 Cookie僅包含其專屬名稱，不會儲存行為或設定檔資料。 |
| **`demdex`** | 15552000 （180天） | 因情況而異 | `demdex.net`網域上的第三方Cookie。 啟用[`thirdPartyCookiesEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/thirdpartycookiesenabled) （預設）且瀏覽器預設允許協力廠商Cookie （例如Chrome或Edge）時出現。 在此情況下，Web SDK會將身分要求傳送至`adobedc.demdex.net`，由它設定此Cookie。 Audience Manager使用此Cookie來指派唯一ID，並支援ID同步、細分、建模和報告。 檢視[Audience Manager Cookie](audience-manager.md)中的`demdex`。 |
| **`kndctr_<orgId>_identity`** | 34128000 （395天） | 100-120位元組（變數） | 儲存該裝置的ECID和其他相關資訊。 |
| **`kndctr_<orgId>_cluster`** | 1800 （30分鐘） | 3-5位元組 | 儲存Edge Network區域（位置提示），用於提供目前使用者的請求。 URL路徑會使用地區，這樣Edge Network就能將請求路由至正確的地區。 如果使用者在Cookie期限內，以不同的IP位址連線，請求會再次路由至最接近的區域。 |
| **`kndctr_<orgId>_consent`** | 15552000 （180天） | 10-11位元組 | 儲存訪客的同意偏好設定。 無論同意與否一律設定，因為它會儲存同意偏好設定本身。 |
| **`kndctr_<orgId>_consent_check`** | 7200 （2小時） | | 工作階段範圍的協助程式，用於在TTL過期後訊號Edge Network重新檢查伺服器端的同意書。 它會在快取同意時強制執行TTL。 |
| **`kndctr_<orgId>_personalization`** | 34128000 （395天） | | 儲存Adobe Target用來個人化內容的工作階段資訊。 |
| **`kndctr_<orgId>_advertising`** | 31622400 （366天），每次更新Cookie時都會更新 | 80位元組至1 KB （變數） | 當Adobe Advertising元件（測試版）包含在您的Web SDK組建中，且訪客的同意為`in`時出現。 網頁SDK會在頁面URL包含Adobe Advertising點選引數（`s_kwcid`或`ef_id`）或設定[Adobe Advertising DSP](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)廣告商時，寫入此Cookie。 它會儲存URL編碼的JSON，其中可包含搜尋點按資料(`_les_lsc`)、雜湊IP位址、LiveRamp RampID信封（若已設定RampID JavaScript路徑）以及用於限制重複轉換的轉換時間戳記。 在預設允許第三方Cookie的瀏覽器中，它也會儲存Adobe Advertising瀏覽者ID並顯示點按資料(`ev_lcc`)。 此Cookie只會設定在目前的主機名稱上。 元件也會從`pixel.everesttech.net`、`www.everestjs.net` （設定ID5合作夥伴ID時）及您的RampID `ats.js`路徑載入資源。 這些資源可以設定自己的Cookie，但此頁面未列出這些Cookie。 |
| **`kndctr_<orgId>_bc_session_id`** | 無（工作階段Cookie） | | 於使用Brand Concierge元件(Beta)時呈現。 儲存Brand Concierge聊天工作階段ID。 Web SDK僅在啟用[`stickyConversationSession`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/conversation)時才讀取此Cookie，因此聊天工作階段會在頁面載入之間持續存在。 |
| **`mbox`** | 63072000 （2年） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)啟用時出現。 它允許網頁SDK設定Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **`mboxEdgeCluster`** | 1800 （30分鐘） | | [`targetMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/targetmigrationenabled)啟用時出現。 它可讓Web SDK將正確的邊緣叢集通訊給`at.js`，以便在使用者瀏覽網站時，Target設定檔可以保持同步。 當`kndctr_<orgId>_cluster` Cookie不存在時，Web SDK也會讀取此Cookie，以將請求路由到相符的Edge Network區域。 |
| **`s_ecid`** | 63115200 （2年） | ~45 位元組 | 包含格式為`s_ecid=MCMID\|<ECID>`的CX Enterprise ID (ECID/MID)復本。 主要針對CNAME （第一方）案例，用作ECID的第一方備份。 啟用[`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/collection/js/commands/configure/idmigrationenabled)時，Web SDK會讀取此Cookie以重複使用現有的ECID。 |
| **Audience Manager Cookie目的地** （名稱不盡相同） | 864000 （10天），除非目的地指定不同的存留期 | 因情況而異 | 當Edge Network傳回訪客的Audience Manager [Cookie目的地](https://experienceleague.adobe.com/en/docs/audience-manager/user-guide/features/destinations/custom-destinations/create-cookie-destination)時出現。 Web SDK會使用目的地中定義的Cookie名稱、值和網域來寫入第一方Cookie。 值採用URL編碼，與Audience Manager Data Integration Library (DIL)一致。 |

Edge Network使用`secure`和`sameSite="none"`屬性來設定其所有Cookie。 如果您的網站上目前同時有安全和非安全區段，則使用者識別可能會不準確。 當使用者從網站的安全區段導覽到不安全的區段時，Edge Network會使用請求產生新的`ECID`。

Web SDK自行建立的Cookie （而非根據Edge Network的方向建立）會使用不同的屬性。 `AMCV_###@AdobeOrg` Cookie和Audience Manager Cookie目的地僅包含HTTPS頁面上的`secure`和`sameSite="none"`屬性。 `com.adobe.alloy.getTld`和`kndctr_<orgId>_advertising` Cookie使用瀏覽器的預設屬性。
