---
title: Adobe Experience Platform Web SDK Cookie
description: 瞭解Web SDK如何使用適用於您實作的Cookie。
solution: Experience Cloud
feature: Cookies
topic: Administration
role: Admin
level: Experienced
source-git-commit: 66f78a04674a82335f5df20c4c15d983b6ebdc66
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 2%

---

# Adobe Experience Platform Web SDK Cookie

Adobe Experience Platform Web SDK使用Cookie來儲存實作特有的值。

| 名稱 | 最大年齡 | 說明 |
|---|---|---|
| **kndct_orgid_identity** | 34128000 （395天） | 儲存ECID以及與ECID相關的其他資訊。 |
| **kndctr_orgid_consent_check** | 7200 （2小時） | 代表伺服器尋找同意偏好設定的伺服器端。 |
| **kndctr_orgid_consent** | 15552000 （180天） | 儲存使用者對網站的同意偏好設定。 |
| **kndctr_orgid_cluster** | 1800 (30 分鐘) | 儲存Edge Network區域，為目前使用者的請求提供服務。 URL路徑會使用地區，這樣Edge Network就能將請求路由至正確的地區。 如果使用者使用不同的IP位址或在不同的工作階段中連線，則請求會再次路由到最近的區域。 |
| **mbox** | 63072000 （2年） | 目標移轉設定設為true時出現。 它允許Target [mbox Cookie](https://developer.adobe.com/target/implement/client-side/atjs/atjs-cookies/) 將由Web SDK設定。 |
| **mboxEdgeCluster** | 1800 (30 分鐘) | 目標移轉設定設為true時出現。 它可讓Web SDK將正確的邊緣叢集通訊至 `at.js` 如此一來，當使用者在網站上導覽時，Target設定檔便可保持同步。 |
| **AMCV_###@AdobeOrg** | 34128000 （395天） | 顯示時機 [`idMigrationEnabled`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/idmigrationenabled) 已啟用。 在網站某些部分仍在使用時，若轉換到Web SDK會很有幫助 `visitor.js`. |

Edge Network會使用設定所有Cookie `secure` 和 `sameSite="none"` 屬性。 如果您的網站上目前同時有安全和非安全區段，則使用者識別可能會不準確。 當使用者從網站的安全區段導覽到不安全的區段時，Edge Network會產生新的 `ECID` 透過要求。
