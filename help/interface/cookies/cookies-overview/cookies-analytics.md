---
description: Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。
keywords: Cookie；隱私權
seo-description: Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。
seo-title: Analytics Cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Analytics Cookie
uuid: e2d3d61d-2708-48b2-a7 e6-2331f2 aed8 e0
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Analytics Cookie{#analytics-cookies}

Adobe Analytics 使用 Cookie 來區別不同瀏覽器的請求，並儲存可供應用程式稍後使用的有用資訊。它們也能用來建立瀏覽資訊和客戶記錄之間的關聯。

尤其是，Analytics 會使用 Cookie 來匿名定義新訪客、輔助分析點按資料流資料，並追蹤網站上的歷史活動，例如特定促銷活動的反應或銷售週期的長度。

* [Cookie名稱：s_ ecid](../cookies-overview/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名稱: AMCV_###@AdobeOrg](../cookies-overview/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)
* [Cookie 名稱: s_cc](../cookies-overview/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_cc](../cookies-overview/cookies-analytics.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_sq](../cookies-overview/cookies-analytics.md#section-8abfff3a302d494f81a3cfb91e3b09ff)
* [Cookie 名稱: s_vi](../cookies-overview/cookies-analytics.md#section-5d50a078de444d12b7d927d68ff3b679)
* [Cookie 名稱: s_fid](../cookies-overview/cookies-analytics.md#section-65e33f9bfc264959ac1513e2f4b10ac7)
* [外掛程式設定的 Cookie](../cookies-overview/cookies-analytics.md#section-a6b1cae8454945fab9eea5c7884c40fc)

Analytics 說明內有更多關於[第一方 Cookie](https://marketing.adobe.com/resources/help/en_US/whitepapers/first_party_cookies/fpcookies_overview.html) 的詳細資訊。

## Cookie Name: s_ecid {#section-32fd753c3fa54452acd62b021434919a}

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> 包含Experience Cloud ID(ECID)或MID副本。MID儲存在遵循此語法的機碼值配對中，s_ ecid= MCMID|&lt; ECID&gt; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p>此Cookie是由客戶設定AMCV Cookie後的網域所設定。此Cookie的目的是允許在1^ st^方狀態中進行永久性ID追蹤，並作為參考ID(如果AMCV Cookie已過期)。請在這裡查看AMCV Cookie以取得詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p>僅限CNAME客戶。不適用於3^ rd^ party藍本。Cookie會儲存在您的網域中，此網域與CNAME和Analytics影像要求所使用的網域相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p>45 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: s_cc {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

<table id="table_34AA90F2FFB84500A77D8F4C5008D453"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 由 JavaScript 代碼設定並讀取，可確定是否啟用了 Cookie (只需設為「True」)  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p> 所有帳戶只有一個 Cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 儲存在頁面的網域上 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 4 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: s_sq {#section-8abfff3a302d494f81a3cfb91e3b09ff}

<table id="table_05EEB54B5EA2409DB1D071FD1484E8F9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 由 JavaScript 代碼設定並讀取 (當啟用 ClickMap 功能時)，其包含使用者先前所點按連結之相關資訊 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p> 所有帳戶只有一個 Cookie </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 儲存在頁面的網域上 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 因頁面 URL 大小而異，但通常為 100-200 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: s_vi {#section-5d50a078de444d12b7d927d68ff3b679}

<table id="table_774F04AA9E3847D9AE7803520B5AAAE3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> 獨特訪客 ID 時間/日期戳記 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p> 2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 用於識別獨特訪客 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 系統會將此 Cookie 儲存在影像請求的網域中。如果您正在使用第三方 Cookie，通常會儲存在 2O7.net 中；如果正在使用第一方 Cookie，則會儲存在您的網域中。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 44 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>每個Analytics訪客ID都與Adobe伺服器上的訪客描述檔相關聯。無論訪客 ID Cookie 過期與否，訪客閒置 1 年以上就會刪除其訪客資料。

## Cookie 名稱: s_fid {#section-65e33f9bfc264959ac1513e2f4b10ac7}

<table id="table_B0EDB50677D14A86A1BFB7CCAAE95C88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> 後援唯一訪客 ID 時間/日期戳記 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p>5 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 用於識別獨特訪客 如果標準的 <span class="codeph">s_vi</span> Cookie 因第三方 Cookie 限制而無法取用。不適用於使用第一方 Cookie 的執行。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 儲存於您的網域，作為第一方 Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 33 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 外掛程式設定的 Cookie {#section-a6b1cae8454945fab9eea5c7884c40fc}

視 Analytics 外掛程式的使用，可設定其他 Cookie。這些 Cookie 是供用戶端於多種情況下使用之代碼的片段。這些情況包括: 從 URL 擷取值、串連傳送至 Analytics 的值、擷取表單捨棄等。如需各外掛程式設定之 Cookie 的詳情，請聯絡 ClientCare。例如，[!DNL s_vh]Set Once Per *和* Set and Get Last Value *外掛程式使用的* Cookie。

僅當電子郵件用戶端和網頁瀏覽器共用相同的 Cookie 空間時，方能正確識別未使用 JavaScript 而傳入影像請求的 Conversion 變數 (eVarX)，例如置入電子郵件內的代碼。
