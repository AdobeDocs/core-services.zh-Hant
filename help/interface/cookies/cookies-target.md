---
description: 了解 Adobe Target 如何使用 Cookie 來讓網站營運人員測試哪些線上內容和優惠方案與訪客的關聯性較強。
solution: Experience Cloud,Analytics,Target
title: Adobe Target Cookie
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
source-git-commit: ea50808d2514ff3c94ffa1bee2d9aa3ddf51f120
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 95%

---

# Adobe Target Cookie{#target-cookies}

Adobe Target 使用 Cookie 讓網站操作人員能夠測試哪些線上內容和方案與訪客的關聯性較強。

如有需要，您可以變更這些設定，但 Cookie 存留期間除外。 變更 Cookie 設定時，請洽詢您的客戶代表。

>[!NOTE]
>
>Adobe Target 使用者也能建立自訂的第三方 Cookie。

| 設定 | 資訊 |
| --- | --- |
| Cookie 名稱 | mbox。 |
| Cookie 網域 | 您提供 mbox 的網域之第二層和頂層。因為是使用公司所提供的網域，所以這些會是第一方 Cookie。範例：`mycompany.com`。 |
| 伺服器網域 | `clientcode.tt.omtrdc.net`，針對您的 [!DNL Adobe Target] 帳戶使用用戶端代碼。 |
| Cookie 持續時間 | 自訪客上次登入後的兩年期間，Cookie 仍會留在訪客的瀏覽器上。Cookie 持續時間無法變更。 |



>[!NOTE]
>
>如果您的網域名稱包含國碼 (例如 `mycompany.co.uk`)，請和您的客戶服務代表合作設定您的 [!DNL at.js] 以支援此作業。

Cookie 會保留一些值，用於管理訪客體驗 Adobe Target 行銷活動的方式：

| 值 | 定義 |
| --- | --- |
| 工作階段 ID | 特定使用者工作階段的唯一識別碼。 根據預設，工作階段會在閒置 30 分鐘後過期。 如果您要自行產生工作階段 ID (例如，針對伺服器端實作)，請確定以下事項：<ul><li>工作階段 ID 可以是任何可列印的字串，除了空格、問號 ( ? ) 或正斜線 ( / ) 以外。</li><li>* 工作階段 ID 的長度應該介於 1 到 128 個字元之間。</li><li>如果是特定工作階段，其值在多個要求中必須保持相同。</li><li>特定訪客在任何時間點絕對不應該有並行工作階段 (不同的工作階段 ID)。</li></ul>路由傳遞給邊緣叢集內的特定節點的工作是使用工作階段 ID 來進行。<ul><li>工作階段在伺服器端會維持 30 分鐘的有效狀態。 因此，您不應針對特定 `tntId/thirdPartyId` 在使用 `tntId/thirdPartyId`. 否則，基本資料的變更可能會不一致且無法預測。</li><li>搭配多個 `tntIds/thirdPartyIds` 使用相同工作階段 ID 可能會對 `tntId/thirdPartyIDs` 所識別的基本資料造成無法預測的變更。</li></ul>**注意**：若要取得特定工作階段 ID，請參閱「[並行要求數目的限制](https://experienceleague.adobe.com/docs/target/using/troubleshoot/target-limits.html?lang=en#content-delivery)」。 |
| pc ID | 訪客瀏覽器的半永久 ID。持續到手動刪除 Cookie 為止。 |
| 檢查 | 用來判斷訪客是否支援 Cookie 的簡單測試值。每次訪客請求頁面時都會進行設定。 |
| 停用 | 如果訪客的載入時間超過 at.js 檔案中所設定的逾時時間，則設定此選項。 根據預設，這會持續 1 個小時。 |

