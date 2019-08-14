---
description: Survey 使用 Cookie 來區別不同瀏覽器的請求，以及儲存可用來深入了解客戶情緒的有用資訊。
keywords: Cookie;隱私
seo-description: Survey 使用 Cookie 來區別不同瀏覽器的請求，以及儲存可用來深入了解客戶情緒的有用資訊。
seo-title: Survey Cookie
solution: Marketing Cloud, Analytics, Target, Social
title: Survey Cookie
uuid: e57d9b58-3c62-463a-ad52-e2a0de2e1ee1
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Survey Cookie{#survey-cookies}

Survey 使用 Cookie 來區別不同瀏覽器的請求，以及儲存可用來深入了解客戶情緒的有用資訊。

* [Cookie 名稱: s_sv_sid](../cookies-overview/cookies-survey.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s_sv_s1](../cookies-overview/cookies-survey.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Cookie 名稱: s_sv_p1](../cookies-overview/cookies-survey.md#section-05d1c52c478541609f4a18a9c1eb032f)

## Cookie 名稱: s_sv_sid {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 屬性 | 說明 |
|---|---|
| 儲存資訊 | 儲存唯一號碼以確保用於在瀏覽器內轉譯調查的 JavaScript 檔案能適當快取。 |
| 過期 | 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期。 |

## Cookie 名稱: s_sv_s1 {#section-14ad50dfcd7342f9ac80283b1f0d3400}

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 儲存資訊 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_350369AFBEFF49938026D7D25D012A88"> 
      <li id="li_EA3D03382BFA474B802D1EE2054FABDB">儲存當系統提示訪客參加調查時，訪客按一下「稍後」予以延遲之調查的 ID。 </li> 
      <li id="li_6111E8D568D64D7CBFB906046134025C"> 儲存於網站後續頁面中啟動之調查的 ID。 </li> 
      <li id="li_A16519F487654435B50577DA08654E70">儲存已開始啟動之調查的 ID。 </li> 
      <li id="li_8322C91846AB4A65B277C435D61660BF">儲存 Survey 系統開始執行 (針對延遲調查) 的時間。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期。 </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: s_sv_p1 {#section-05d1c52c478541609f4a18a9c1eb032f}

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 儲存資訊 </td> 
   <td colname="col2"> <p> 
     <ul id="ul_A2717AD89DA540468963E9E7FBD382D5"> 
      <li id="li_21B0165911C74BA796111E9C93142B95">儲存已參加或拒絕的調查 ID。 </li> 
      <li id="li_DD966285CAE7438C9E43AFC4E91569F8">儲存指出訪客是否符合取樣率的資訊。 </li> 
      <li id="li_27BD16FE78BC46C3846BFFE4DF65BCB3">儲存不斷增加的號碼；在啟動「離開網站」調查以確認訪客離開網站時會用到這個號碼。 </li> 
      <li id="li_0C9FF8939615407BB9A0DB24C7C31CE6">儲存指出訪客是否達到客戶指定之疲勞設定，因此應排除在調查之外的標幟。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 此 Cookie 為永久性 Cookie。 </td> 
  </tr> 
 </tbody> 
</table>

<a id="section_488AFFB899004968A2479B2423E6EEB7"></a>

>[!NOTE]
>
>如果要儲存在 s_sv_s1 或 s_sv_p1 中的資訊過大，系統會視情況分割資訊，將資訊儲存在 s_sv_s2、s_sv_s3 或 s_sv_p2、s_sv_p3 等其他 Cookie 中。

