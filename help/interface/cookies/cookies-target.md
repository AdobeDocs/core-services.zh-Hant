---
description: 了解 Adobe Target 如何使用 Cookie 來讓網站營運人員測試哪些線上內容和優惠方案與訪客的關聯性較強。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics,Target,Social
title: 'Adobe Target Cookie '
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: c4399cc0-8333-47b8-b830-2ba7359f464a
translation-type: tm+mt
source-git-commit: dcb6fa5d8458995cba66bc2f89c954aa6bcd5923
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 55%

---

# Adobe Target Cookie{#target-cookies}

Adobe Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和行銷活動與訪客的關聯性較強。

您可以視需要變更這些設定，但Cookie持續時間除外。 變更 Cookie 設定時，請洽詢您的客戶代表。

>[!NOTE]
>
>Adobe Target 使用者也能建立自訂的第三方 Cookie。

| 設定 | 資訊 |
| --- | --- |
| Cookie 名稱 | mbox。 |
| Cookie 網域 | 您提供 mbox 的網域之第二層和頂層。因為是使用公司所提供的網域，所以這些會是第一方 Cookie。範例：`mycompany.com`。 |
| 伺服器網域 | `clientcode.tt.omtrdc.net`[!DNL Adobe Target]，使用您帳戶的用戶端代碼。 |
| Cookie 持續時間 | 自訪客上次登入後的兩年期間，Cookie 仍會留在訪客的瀏覽器上。Cookie 持續時間無法變更。 |



>[!NOTE]
>
>如果您的網域名稱包含國碼 (例如 `mycompany.co.uk`)，請和您的客戶服務代表合作設定您的 [!DNL at.js] 以支援此作業。

Cookie 會保留一些值，用於管理訪客體驗 Adobe Target 行銷活動的方式：

| 值 | 定義 |
| --- | --- |
| session ID | 指定使用者作業的唯一識別碼。 依預設，工作階段會在閒置30分鐘後過期。 如果您是自行產生sessionId（例如，針對伺服器端實施），請確定：<ul><li>作業ID可以是任何可列印的字串，但空格、問號(? )或正斜線(/)。</li><li>*作業ID長度應介於1到128個字元之間。</li><li>對於特定作業，其值必須在多個請求間維持相同</li><li>您絕不應在任何時間點為特定訪客提供平行作業（不同的sessionId）。</li></ul>使用會話ID路由到邊緣群集中的特定節點。<ul><li>在伺服器端，工作階段會持續30分鐘。 因此，您不應在最後一次使用`tntId/thirdPartyId`提出要求後30分鐘內，針對特定`tntId/thirdPartyId`使用不同的工作階段ID。 否則，對描述檔的變更可能不一致且無法預測。</li><li>對多個`tntIds/thirdPartyIds`使用相同的會話ID會對由`tntId/thirdPartyIDs`標識的配置檔案造成不可預知的更改。</li></ul> |
| pc ID | 訪客瀏覽器的半永久 ID。持續到手動刪除 Cookie 為止。 |
| check | 用來判斷訪客是否支援 Cookie 的簡單測試值。每次訪客請求頁面時都會進行設定。 |
| disable | 設定訪客的載入時間是否超過at.js檔案中設定的逾時。 依預設，這會持續 1 個小時。 |

