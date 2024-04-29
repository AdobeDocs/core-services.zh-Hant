---
description: 了解 Adobe Target 如何使用 Cookie 來讓網站營運人員測試哪些線上內容和優惠方案與訪客的關聯性較強。
solution: Target
title: Adobe Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: 9ee4d9b0e670dec35cda530892c49e36bf7cc107
workflow-type: tm+mt
source-wordcount: '627'
ht-degree: 18%

---

# Adobe Target Cookie

Adobe Target 使用 Cookie 讓網站操作人員能夠測試哪些線上內容和方案與訪客的關聯性較強。

>[!NOTE]
>
>本文資訊僅適用於 [Adobe Target JavaScript資料庫](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (`at.js`)。 另請參閱 [Adobe Experience Platform Web SDK Cookie](web-sdk.md) 以取得有關使用Web SDK的Target實作的資訊。
>
>如有需要，您可以變更本文中討論的設定，但Cookie持續時間除外。 [請洽詢您的客戶代表](https://experienceleague.adobe.com/docs/target/using/cmp-resources-and-contact-information.html){target=_blank} 變更Cookie設定時。

## 第一方 Cookie

下列第一方Cookie會儲存在客戶的網域上：

| Cookie | 詳細資料 |
| --- | --- |
| `mbox` | 儲存訪客的匿名識別碼。<P>**Cookie網域**：您提供mbox的網域。 因為此Cookie來自您公司的網域，所以此Cookie是第一方Cookie。 如果您的網域名稱包含國碼，例如 `example.co.uk`，搭配使用者端服務進行設定 `at.js` 以支援此程式碼。 如需自訂Cookie網域的詳細資訊，請參閱 `cookieDomain` 在 [targetGlobalSettings](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} (在Adobe Target開發人員指南中)。<P>**伺服器網域**： `clientcode.tt.omtrdc.net`，使用您Adobe Target帳戶的使用者端代碼。<P>**Cookie持續時間**：Cookie會保留在訪客的瀏覽器上達兩年時間，期限從上次登入算起。 Cookie 持續時間無法變更。<P>Cookie會保留一些值，用於管理訪客的體驗 [!DNL Target] 活動：<P>**session ID**：指定使用者工作階段的唯一識別碼。 根據預設，工作階段會在閒置 30 分鐘後過期。 如果您正在產生 `sessionId` 您自己(例如 [伺服器端實作](https://experienceleague.adobe.com/docs/target-dev/developer/server-side/server-side-overview.html){target=_blank})，確定以下事項：<ul><li>工作階段ID可以是任何可列印的字串，除了空格、問號( ？ ) 或正斜線 ( / ) 以外。</li><li>工作階段ID的長度應該介於1到128個字元之間。</li><li>針對特定工作階段，Cookie的值在多個要求中必須維持不變。</li><li>絕不應該有並行工作階段(相異 `sessionIds`)。</li></ul>路由傳送到邊緣叢集內的特定節點是使用工作階段ID完成的。<ul><li>工作階段在伺服器端會維持 30 分鐘的有效狀態。 因此，您不應該針對特定使用不同的工作階段ID `tntId/thirdPartyId` 使用發出上一個要求後的30分鐘內 `tntId/thirdPartyId`. 否則，基本資料的變更可能會不一致且無法預測。</li><li>訪客閒置30分鐘後，必須使用該新的工作階段ID。</li><li>搭配多個使用相同工作階段ID `tntIds/thirdPartyIds` 可能會對所識別的基本資料造成無法預測的變更。 `tntId/thirdPartyIDs`.</li></ul>注意：請參閱 [並行請求數目的限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html#content-delivery){target=_blank} 指定工作階段ID的。<P>**pc ID**：訪客瀏覽器的半永久ID。 持續到手動刪除 Cookie 為止。<P>**check**：用來判斷訪客是否支援Cookie的簡單測試值。 每次訪客請求頁面時都會進行設定。<P>**disable**：如果訪客的載入時間超過at.js檔案中所設定的逾時時間，則設定此選項。 根據預設，此逾時會持續一小時。 |
| `at_check` | 臨時Cookie ，用於檢查瀏覽器上是否已啟用Cookie讀取/寫入功能。 |
| `mboxEdgeCluster` | 此Cookie僅在/如果 [overrideMboxEdgeServer設定](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/at-js-implementation/functions-overview/targetglobalsettings.html){target=_blank} 設為 `true`. |

無法使用 `HTTPOnly` 在這些第一方Cookie上。 此 `at.js` JavaScript程式庫需要讀取/寫入這些Cookie。 這些Cookie的建立者為 `at.js` 且不是從伺服器設定。

此 `secure` 您可使用以下程式碼在所有這些Cookie上啟用設定： `secureOnly: true` 中的設定 `at.js`.

## 第三方 Cookie

Adobe Target使用者可建立自訂的第三方Cookie。 下列第三方Cookie會儲存在 `tt.omtrdc.net`：

| Cookie | 詳細資料 |
| --- | --- |
| `customerclientcode!mboxPC` | 在啟用跨網域時顯示。 |
| `customerclientcode!mboxSession` | 在啟用跨網域時顯示。 |

這些協力廠商Cookie是HTTPnly開箱即用，並由Adobe Target資料收集伺服器設定。

此 `secure` 可使用在所有Cookie上啟用設定 `secureOnly: true` 中的設定 `at.js`.
