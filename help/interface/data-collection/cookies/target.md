---
description: 了解 Adobe Target 如何使用 Cookie 來讓網站營運人員測試哪些線上內容和產品建議與訪客的關聯性較強。
solution: Target
title: Adobe Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 2fbf283e5ef06314a679b364fd3f0dfc262a884d
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 16%

---

# Adobe Target Cookie

Adobe Target 使用 Cookie 讓網站操作人員能夠測試哪些線上內容和方案與訪客的關聯性較強。

>[!NOTE]
>
>本文中的資訊僅適用於[Adobe Target JavaScript資料庫](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`)。 請參閱[Adobe Experience Platform Web SDK Cookie](web-sdk.md)，取得使用Web SDK的Target實作資訊。
>
>如有需要，您可以變更本文中討論的設定，但Cookie持續時間除外。 [變更Cookie設定時，請洽詢您的帳戶代表](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank}。

## 第一方Cookie

下列第一方Cookie會儲存在客戶的網域上：

| Cookie | 詳細資料 |
| --- | --- |
| `mbox` | 儲存訪客的匿名識別碼。<P>**Cookie網域**：您提供mbox的網域。 因為此Cookie來自您公司的網域，所以此Cookie是第一方Cookie。 如果您的網域名稱包含國碼（例如`example.co.uk`），請和客戶服務代表合作設定`at.js`以支援此代碼。 如需有關自訂Cookie網域的資訊，如有必要，請參閱Adobe Target開發人員指南中[targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}底下的`cookieDomain`。<P>**伺服器網域**： `clientcode.tt.omtrdc.net`，使用您Adobe Target帳戶的使用者端代碼。<P>**Cookie持續時間**：自上次登入起，Cookie會保留在訪客的瀏覽器上兩年。 Cookie 持續時間無法變更。<P>Cookie會保留一些值，用於管理訪客體驗[!DNL Target]活動的方式：<P>**工作階段識別碼**：特定使用者工作階段的唯一識別碼。 根據預設，工作階段會在閒置 30 分鐘後過期。 如果您要自行產生`sessionId` （例如，針對[伺服器端實作](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank}），請確定下列事項：<ul><li>工作階段ID可以是任何可列印的字串，除了空格、問號( ？ )、大括弧( { } )或正斜線( / )。</li><li>工作階段ID的長度應該介於1到128個字元之間。</li><li>針對特定工作階段，Cookie的值在多個要求中必須維持不變。</li><li>特定訪客在任何時間點絕對不應該有平行工作階段（不同的`sessionIds`）。</li></ul>路由傳送到邊緣叢集內的特定節點是使用工作階段ID完成的。<ul><li>工作階段在伺服器端會維持 30 分鐘的有效狀態。 因此，您不應在與`tntId/thirdPartyId`發出上次要求後的30分鐘內，針對特定`tntId/thirdPartyId`使用不同的工作階段ID。 否則，輪廓的變更可能會不一致且無法預測。</li><li>訪客閒置30分鐘後，必須使用該新的工作階段ID。</li><li>搭配多個`tntIds/thirdPartyIds`使用相同工作階段ID可能會對`tntId/thirdPartyIDs`所識別的基本資料造成無法預測的變更。</li></ul>注意：請參閱指定工作階段識別碼的並行要求數目[限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank}。<P>**電腦ID**：訪客瀏覽器的半永久ID。 持續到手動刪除 Cookie 為止。<P>**check**：用來判斷訪客是否支援Cookie的簡單測試值。 每次訪客請求頁面時都會進行設定。<P>**停用**：如果訪客的載入時間超過at.js檔案中所設定的逾時時間，則設定此選項。 根據預設，此逾時會持續一小時。 |
| `at_check` | 臨時Cookie ，用於檢查瀏覽器上是否已啟用Cookie讀取/寫入功能。 |
| `mboxEdgeCluster` | 只有當[overrideMboxEdgeServer設定](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank}設為`true`時，此Cookie才會出現。 |

無法在這些第一方Cookie上使用`HTTPOnly`。 `at.js` JavaScript程式庫需要讀取/寫入這些Cookie。 這些Cookie是由`at.js`建立的，而且不是從伺服器設定的。

可以使用`at.js`中的`secureOnly: true`設定，在所有這些Cookie上啟用`secure`設定。

## 第三方Cookie

Adobe Target使用者可建立自訂的第三方Cookie。 下列第三方Cookie儲存在`tt.omtrdc.net`上：

| Cookie | 詳細資料 |
| --- | --- |
| `customerclientcode!mboxPC` | 在啟用跨網域時顯示。 |
| `customerclientcode!mboxSession` | 在啟用跨網域時顯示。 |

這些協力廠商Cookie是HTTPnly開箱即用，並由Adobe Target資料收集伺服器設定。

可以使用`at.js`中的`secureOnly: true`設定，在所有Cookie上啟用`secure`設定。
