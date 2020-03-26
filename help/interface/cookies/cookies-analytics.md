---
description: Adobe Analytics使用Cookie來區分不同瀏覽器的要求，並儲存應用程式稍後可使用的有用資訊。 它們也可用於將瀏覽資訊與客戶記錄關聯。
keywords: cookies;privacy
seo-description: Adobe Analytics使用Cookie來區分不同瀏覽器的要求，並儲存應用程式稍後可使用的有用資訊。 它們也可用於將瀏覽資訊與客戶記錄關聯。
seo-title: Analytics Cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics使用Cookie來區分不同瀏覽器的要求，並儲存應用程式稍後可使用的有用資訊。 它們也可用於將瀏覽資訊與客戶記錄關聯。

尤其是，Analytics會使用Cookie來匿名定義新訪客、協助分析點按流資料，並追蹤網站上的歷史活動，例如對特定促銷活動的回應或銷售週期的長度。

* [Cookie 名稱: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名稱: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名稱: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie名稱：s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名稱: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie名稱：s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [外掛程式設定的Cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Analytics說明中提供有關第一方Cookie [的詳細資訊](/help/interface/cookies/cookies-first-party.md)。

## Cookie 名稱: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 包含 Experience Cloud ID (ECID) 或 MID 副本。MID 儲存在遵循語法 s_ecid=MCMID 的機碼值組中 | `<ECID>` |
| 有效期限 | 2年 |
| 使用狀況 | 此 Cookie 是在用戶端設定 AMCV Cookie 後，由客戶的網域所設定。此 Cookie 的目的是允許在第一方狀態中進行永久性 ID 追蹤，並在 AMCV Cookie 過期時，作為參考 ID 使用。請在此查看 AMCV Cookie，以了解詳細資訊。 |
| 位置 | 僅限 CNAME 客戶。不適用於第三方情況。Cookie 會儲存在您的網域中，此網域與 CNAME 和 Analytics 影像要求所使用的網域相同。 |
| 大小 | 45 位元組 |

## Cookie 名稱: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | JavaScript程式碼會設定並讀取此Cookie，以判斷Cookie是否已啟用（只要設為&quot;True&quot;即可） |
| 過期 | 此Cookie是作業Cookie，在瀏覽器關閉時過期 |
| 使用狀況 | 所有帳戶只能使用一個Cookie |
| 位置 | 此Cookie儲存在頁面的網域 |
| 大小 | 4 位元組 |

## Cookie Name: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 當ClickMap功能或Activity Map功能啟用時，JavaScript程式碼會設定並讀取此Cookie;它包含使用者點按之前連結的相關資訊 |
| 過期 | 此Cookie是作業Cookie，在瀏覽器關閉時過期 |
| 使用狀況 | 所有帳戶只能使用一個Cookie |
| 位置 | 此Cookie儲存在頁面的網域 |
| 大小 | 視頁面 URL 大小而定，但通常為 100 到 200 位元組 |

## Cookie 名稱: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 獨特訪客ID時間／日期戳記 |
| 過期 | 2年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客     |
| 位置 | 此Cookie會儲存在影像要求的網域中——通常是2o7.net或omtrdc.net下的客戶特定子網域（如果您使用第三方Cookie，或您的網域使用第一方Cookie）。 |
| 大小 | 44 位元組 |

>[!NOTE]
>
>每個 Analytics 訪客 ID 都與 Adobe 伺服器上的訪客資料相關聯。無論訪客 ID Cookie 過期與否，訪客閒置 1 年以上就會刪除其訪客資料。

## Cookie Name: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 屬性 | 說明 |
|--- |--- |
| 儲存的資訊 | 備援獨特訪客ID時間／日期戳記 |
| 有效期限 | 2年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客    如果標準的 `s_vi` Cookie 因第三方 Cookie 限制而無法取用。不用於使用第一方Cookie的實作。 |
| 位置 | 此Cookie會儲存在您的網域中作為第一方Cookie。 |
| 大小 | 33 位元組 |

## Cookie標幟

下表說明Analytics Cookie的旗標：

| Cookie (設定者) | httpOnly | Secure | SameSite |
|--- |--- |--- |--- |
| s_vi（http回應） | 無 | 是，當SameSite為「無」且連線使用HTTPS時 | 使用CNAME時，預設為&quot;Lax&quot;。 使用2o7.net或omtrdc.net時為&quot;None&quot;。 |
| s_ecid（http回應） | 無 | 無 | &quot;鬆散&quot; |
| s_fid(Javascript) | 無 | 無 | 取消設定 |
| s_cc(Javascript) | 無 | 無 | 取消設定 |
| s_sq(Javascript) | 無 | 無 | 取消設定 |

>[!NOTE] 如果使用單一CNAME來追蹤多個網域或屬性，SameSite應設為「無」 `s_vi`。 如需變更Analytics Cookie設定的協助，請連絡客戶服務。

## 外掛程式設定的Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

視Analytics外掛程式的使用而定，可設定其他Cookie。 這些Cookie是用戶端可用的程式碼片段，可用於多種情況。 這些情況包括：從URL中檢索值；串連值以傳遞至Analytics;擷取表單放棄等。 如需各外掛程式設定之 Cookie 的詳細資訊，請連絡 ClientCare。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *外掛程式使用的* Cookie。

僅當電子郵件用戶端和網頁瀏覽器共用相同的 Cookie 空間時，方能正確識別未使用 JavaScript 而傳入影像請求的 Conversion 變數 (eVarX)，例如置入電子郵件內的代碼。
