---
description: Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。
keywords: Cookie;隱私
seo-description: Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。
seo-title: Analytics Cookie
solution: Marketing Cloud, Analytics, Target, Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7e6-2331f2aed8e0
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: f59badcd3423ada51a3fe0c605158a009d5b1d64

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。

尤其是，Analytics 會使用 Cookie 來匿名定義新訪客、輔助分析點按資料流資料，並追蹤網站上的歷史活動，例如特定促銷活動的反應或銷售週期的長度。

* [Cookie 名稱: s_ecid](../cookies/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名稱: AMCV_###@AdobeOrg](../cookies/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名稱: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_cc](../cookies/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_sq](../cookies/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名稱: s_vi](../cookies/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名稱: s_fid](../cookies/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [外掛程式設定的 Cookie](../cookies/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Analytics 說明內有更多關於[第一方 Cookie](/help/interface/cookies/cookies-first-party.md) 的詳細資訊。

## Cookie 名稱: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

| 屬性 | 說明 |
|--- |--- |
| 儲存資訊 | 包含 Experience Cloud ID (ECID) 或 MID 副本。MID儲存在遵循此語法的機碼值配對中，s_ ecid= MCMID | <ECID> |
| 過期 | 2 年 |
| 使用狀況 | 此 Cookie 是在用戶端設定 AMCV Cookie 後，由客戶的網域所設定。此 Cookie 的目的是允許在第一方狀態中進行永久性 ID 追蹤，並在 AMCV Cookie 過期時，作為參考 ID 使用。請在此查看 AMCV Cookie，以了解詳細資訊。 |
| 位置 | 僅限 CNAME 客戶。不適用於第三方藍本。Cookie 會儲存在您的網域中，此網域與 CNAME 和 Analytics 影像要求所使用的網域相同。 |
| 大小 | 45 位元組 |

## Cookie 名稱: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 屬性 | 說明 |
|--- |--- |
| 儲存資訊 | 該 Cookie 由 JavaScript 代碼設定並讀取，可確定是否啟用了 Cookie (只需設為「True」)  |
| 過期 | 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期 |
| 使用狀況 | 所有帳戶只有一個 Cookie |
| 位置 | 該 Cookie 儲存在頁面的網域上 |
| 大小 | 4 位元組 |

## Cookie 名稱: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

| 屬性 | 說明 |
|--- |--- |
| 儲存資訊 | 該 Cookie 由 JavaScript 代碼設定並讀取 (當啟用 ClickMap 功能時)，其包含使用者先前所點按連結之相關資訊 |
| 過期 | 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期 |
| 使用狀況 | 所有帳戶只有一個 Cookie |
| 位置 | 該 Cookie 儲存在頁面的網域上 |
| 大小 | 視頁面URL大小而定，但通常為100-200位元組 |

## Cookie 名稱: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

| 屬性 | 說明 |
|--- |--- |
| 儲存資訊 | 獨特訪客 ID 時間/日期戳記 |
| 過期 | 2 年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客   |
| 位置 | 系統會將此 Cookie 儲存在影像請求的網域中。如果您正在使用第三方 Cookie，通常會儲存在 2O7.net 中；如果正在使用第一方 Cookie，則會儲存在您的網域中。 |
| 大小 | 44 位元組 |

>[!NOTE]
>
>每個 Analytics 訪客 ID 都與 Adobe 伺服器上的訪客資料相關聯。無論訪客 ID Cookie 過期與否，訪客閒置 1 年以上就會刪除其訪客資料。

## Cookie 名稱: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

| 屬性 | 說明 |
|--- |--- |
| 儲存資訊 | 後援唯一訪客 ID 時間/日期戳記 |
| 過期 | 5 年 |
| 使用狀況 | 該 Cookie 用於識別獨特訪客  如果標準的 s_vi Cookie 因第三方 Cookie 限制而無法取用。不適用於使用第一方 Cookie 的執行。 |
| 位置 | 此 Cookie 儲存於您的網域，作為第一方 Cookie。 |
| 大小 | 33 位元組 |

## 外掛程式設定的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

視 Analytics 外掛程式的使用，可設定其他 Cookie。這些 Cookie 是供用戶端於多種情況下使用之代碼的片段。這些情況包括: 從 URL 擷取值、串連傳送至 Analytics 的值、擷取表單捨棄等。如需各外掛程式設定之 Cookie 的詳細資訊，請連絡 ClientCare。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *外掛程式使用的* Cookie。

僅當電子郵件用戶端和網頁瀏覽器共用相同的 Cookie 空間時，方能正確識別未使用 JavaScript 而傳入影像請求的 Conversion 變數 (eVarX)，例如置入電子郵件內的代碼。
