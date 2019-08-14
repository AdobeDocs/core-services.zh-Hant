---
description: Adobe Experience Cloud 使用 Cookie 來儲存不同 Experience Cloud 解決方案所使用的訪客 ID。
keywords: Cookie;隱私
seo-description: Adobe Experience Cloud 使用 Cookie 來儲存不同 Experience Cloud 解決方案所使用的訪客 ID。
seo-title: Experience Cloud Cookie
solution: Marketing Cloud, Analytics, Target, Social
title: Experience Cloud Cookie
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Experience Cloud Cookie{#experience-cloud-cookies}

Adobe Experience Cloud 使用 Cookie 來儲存不同 Experience Cloud 解決方案所使用的訪客 ID。

## Cookie 名稱: s_ ecid {#section-32fd753c3fa54452acd62b021434919a}

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
   <td colname="col2"> <p> 包含 Experience Cloud ID (ECID) 或 MID 副本。MID 儲存在遵循此語法 (s_ecid=MCMID|&lt;ECID&gt;) 的機碼值組中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p>此 Cookie 是在用戶端設定 AMCV Cookie 後，由客戶的網域所設定。此 Cookie 的目的是允許在第一方狀態中進行永久性 ID 追蹤，並在 AMCV Cookie 過期時，作為參考 ID 使用。請在此查看 AMCV Cookie，以了解詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p>僅限 CNAME 客戶。不適用於第三方情況。Cookie 會儲存在您的網域中，此網域與 CNAME 和 Analytics 影像要求所使用的網域相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p>45 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: AMCV_###@AdobeOrg {#section-a12aa2a9296940ae82d8921b381b8fb0}

[Experience Platform ID服務](https://docs.adobe.com/content/help/en/id-service/using/home.html) 使用JavaScript在目前網站的網域 `AMCV_###@AdobeOrg` 上，將獨特訪客ID儲存在 `###` 代表隨機字元字串的Cookie中。例如, `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg`.也請參閱 [Cookie 和 ID 服務](https://docs.adobe.com/content/help/en/id-service/using/intro/cookies.html)。

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存資訊 </p> </td> 
   <td colname="col2"> <p> Experience Cloud 解決方案使用的唯一訪客 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p> 2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用狀況 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 用於識別獨特訪客   </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 儲存於網站的網域 (而非影像請求的網域)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 不等，大多數客戶預期此 Cookie 的長度大約是 200 位元組。 </p> </td> 
  </tr> 
 </tbody> 
</table>
