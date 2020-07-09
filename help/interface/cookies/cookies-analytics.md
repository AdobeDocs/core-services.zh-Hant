---
description: Adobe Analytics 使用 Cookie 來區分不同瀏覽器的請求，以及儲存應用程式之後可使用的有用資訊。Cookie 也可用於為瀏覽資訊與客戶記錄建立關聯。
keywords: cookies;privacy
seo-description: Adobe Analytics 使用 Cookie 來區分不同瀏覽器的請求，以及儲存應用程式之後可使用的有用資訊。Cookie 也可用於為瀏覽資訊與客戶記錄建立關聯。
seo-title: Analytics Cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: ht
source-git-commit: bd118685e1dd65b51a171abdfa4e034dd5b9e181
workflow-type: ht
source-wordcount: '812'
ht-degree: 100%

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 來區分不同瀏覽器的請求，以及儲存應用程式之後可使用的有用資訊。Cookie 也可用於為瀏覽資訊與客戶記錄建立關聯。

尤其 Analytics 會使用 Cookie 以匿名方式定義新訪客、協助分析點按流資料，以及追蹤網站上的歷史活動，例如對特定行銷活動的回應或銷售週期的長度。

* [Cookie 名稱：s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名稱：AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名稱：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱：s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名稱：s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名稱：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [外掛程式設定的 Cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Analytics 說明中提供有關[第一方 Cookie](/help/interface/cookies/cookies-first-party.md) 的詳細資訊。

## Cookie 名稱：s_ecid {#section-32fd753c3fa54452acd62b021434919a}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 包含 Experience Cloud ID (ECID) 或 MID 副本。MID 儲存在遵循語法 s_ecid=MCMID 的機碼值組中 | `<ECID>` |
| 有效期限 | 2 年 |
| 使用狀況 | 此 Cookie 是在用戶端設定 AMCV Cookie 後，由客戶的網域所設定。此 Cookie 的目的是允許在第一方狀態中進行永久性 ID 追蹤，並在 AMCV Cookie 過期時，作為參考 ID 使用。請在此查看 AMCV Cookie，以瞭解詳細資訊。 |
| 位置 | 僅限 CNAME 客戶。不適用於第三方情況。Cookie 會儲存在您的網域中，此網域與 CNAME 和 Analytics 影像要求所使用的網域相同。 |
| 大小 | 45 位元組 |

## Cookie 名稱：s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | JavaScript 程式碼會設定並讀取此 Cookie，用於判斷 Cookie 是否已啟用 (只要設為「True」即可) |
| 過期 | 此 Cookie 是工作階段 Cookie，會在瀏覽器關閉時過期 |
| 使用狀況 | 只有一個 Cookie 供所有帳戶使用 |
| 位置 | 此 Cookie 儲存在頁面的網域中 |
| 大小 | 4 位元組 |

## Cookie 名稱：s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | ClickMap 功能或 Activity Map 功能啟用時，JavaScript 程式碼會設定並讀取此 Cookie；此 Cookie 中包含使用者之前所點按連結的相關資訊 |
| 過期 | 此 Cookie 是工作階段 Cookie，會在瀏覽器關閉時過期 |
| 使用狀況 | 只有一個 Cookie 供所有帳戶使用 |
| 位置 | 此 Cookie 儲存在頁面的網域中 |
| 大小 | 視頁面 URL 大小而定，但通常為 100 到 200 位元組 |

## Cookie 名稱：s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 不重複訪客 ID 時間/日期戳記 |
| 過期 | 2 年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客      |
| 位置 | 此 Cookie 會儲存在影像請求的網域中；如果您使用第三方 Cookie，或您的網域使用第一方 Cookie，通常會是 2o7.net 或 omtrdc.net 底下的客戶專屬子網域。 |
| 大小 | 44 位元組 |

>[!NOTE]
>
>每個 Analytics 訪客 ID 都與 Adobe 伺服器上的訪客資料相關聯。無論訪客 ID Cookie 過期與否，訪客閒置 1 年以上就會刪除其訪客資料。

## Cookie 名稱：s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 備援不重複訪客 ID 時間/日期戳記 |
| 有效期限 | 2 年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客     如果標準的 `s_vi` Cookie 因第三方 Cookie 限制而無法取用。不用於使用第一方 Cookie 的實作。 |
| 位置 | 此 Cookie 會作為第一方 Cookie 儲存在您的網域中。 |
| 大小 | 33 位元組 |

## Cookie 標記

下表說明 Analytics Cookie 的標記：

| Cookie (設定者) | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi   (http 回應) | 無 | 是，當 SameSite 為「None」且連線使用 HTTPS 時 | 使用 CNAME 時預設值為「Lax」。使用 2o7.net 或 omtrdc.net 時為「None」。 |
| s_ecid   (http 回應) | 無 | 無 | &quot;鬆散&quot; |
| s_fid (Javascript) | 無 | 無 | 未設定 |
| s_cc (Javascript) | 無 | 無 | 未設定 |
| s_sq (Javascript) | 無 | 無 | 未設定 |

>[!NOTE]
>
>如果使用單一 CNAME 來追蹤多個網域或屬性，`s_vi` 應將 SameSite 設為「None」。如需變更 Analytics Cookie 設定的協助，請聯絡客戶服務。

## 外掛程式設定的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

視 Analytics 外掛程式的使用情況而定，可設定其他 Cookie。這些 Cookie 是用戶端可用於多種情況的程式碼片段。這些情況包括：從 URL 中擷取值、串連值以傳遞至 Analytics、擷取表單放棄情形等。如需各外掛程式設定之 Cookie 的詳細資訊，請連絡 ClientCare。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *外掛程式使用的* Cookie。

僅當電子郵件用戶端和網頁瀏覽器共用相同的 Cookie 空間時，方能正確識別未使用 JavaScript 而傳入影像請求的 Conversion 變數 (eVarX)，例如置入電子郵件內的代碼。
