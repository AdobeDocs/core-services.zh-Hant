---
description: Adobe Experience Cloud使用Cookie儲存跨Experience Cloud解決方案所使用的訪客ID。
keywords: Cookie；隱私權
seo-description: Adobe Experience Cloud使用Cookie儲存跨Experience Cloud解決方案所使用的訪客ID。
seo-title: Experience Cloud Cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Experience Cloud Cookie
uuid: a4788c1c-0402-4fc8-b894-cd24 fa794 f4 f
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Experience Cloud Cookie{#experience-cloud-cookies}

Adobe Experience Cloud使用Cookie儲存跨Experience Cloud解決方案所使用的訪客ID。

* [Cookie名稱：s_ ecid](../cookies-overview/cookies-mc.md#section-32fd753c3fa54452acd62b021434919a)
* [Cookie 名稱: AMCV_###@AdobeOrg](../cookies-overview/cookies-mc.md#section-a12aa2a9296940ae82d8921b381b8fb0)

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

## Cookie 名稱: AMCV_###@AdobeOrg {#section-a12aa2a9296940ae82d8921b381b8fb0}

[訪客ID服務](https://marketing.adobe.com/resources/help/en_US/mcvid/) 使用JavaScript將獨特訪客ID儲存在目前網站之網域的 `AMCV_###@AdobeOrg` Cookie中，其中 `###` 代表隨機字元字串。例如, `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg`. 也請參閱 [Cookie 和 ID 服務](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html)。

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
   <td colname="col2"> <p> 該 Cookie 用於識別獨特訪客 </p> </td> 
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

>[!MORE_LIKE_THIS]
>
>* [Cookie 與 ID 服務](https://marketing.adobe.com/resources/help/en_US/mcvid/mcvid_cookies.html)

