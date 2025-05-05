---
title: Adobe Experience Platform Web SDK Cookie
description: 瞭解Web SDK如何使用適用於您實作的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 14f06dc9-255e-4a6c-adec-471107cf202e
source-git-commit: d69af76f6deff4f2b73e67ee7b69b9fee1ee3a2e
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie來儲存實作特有的值。

| 名稱 | 最大年齡 | 大小 | 說明 |
|---|---|---|---|
| **kndctr_&lt;ORG_ID>_identity** | 34128000 （395天） | 100-120位元組（變數） | 儲存ECID以及與ECID相關的其他資訊。 |
| **kndctr_&lt;ORG_ID>_consent** | 15552000 （180天） | 10-11位元組 | 儲存使用者對網站的同意偏好設定。 |
| **kndctr_&lt;ORG_ID>_cluster** | 1800 （30分鐘） | 3-5位元組 | 儲存Edge Network區域，為目前使用者的請求提供服務。 URL路徑會使用地區，這樣Edge Network就能將請求路由至正確的地區。 如果使用者使用不同的IP位址或在不同的工作階段中連線，則請求會再次路由到最近的區域。 |
| **mbox** | 63072000 （2年） | | 目標移轉設定設為true時出現。 它允許Web SDK設定Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/)。 |
| **mboxEdgeCluster** | 1800 （30分鐘） | | 目標移轉設定設為true時出現。 它可讓Web SDK將正確的邊緣叢集通訊給`at.js`，以便在使用者瀏覽網站時，Target設定檔可以保持同步。 |
| **AMCV_###@AdobeOrg** | 34128000 （395天） | | [`idMigrationEnabled`](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled)啟用時出現。 當網站某些部分仍在使用`visitor.js`時，轉換為Web SDK會有所幫助。 |

Edge Network會設定具有`secure`和`sameSite="none"`屬性的所有Cookie。 如果您的網站上目前同時有安全和非安全區段，則使用者識別可能會不準確。 當使用者從網站的安全區段導覽到不安全的區段時，Edge Network會使用請求產生新的`ECID`。
