---
description: 瞭解用於將廣告參與事件對應至轉換事件的Adobe AdvertisingCookie，並可能使用該資訊來最佳化廣告競標。
title: Adobe AdvertisingCookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 5d0e02713ec4b233e06ecd3ac0234d1526b947f1
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 75%

---

# Adobe AdvertisingCookie{#advertising-cloud-cookies}

Adobe Advertising (前身為Adobe Advertising Cloud)會使用Cookie將廣告參與事件對應至轉換事件，並可能使用該資訊來最佳化廣告競標。

>[!NOTE]
>
>Beta版Adobe AdvertisingJavascript標籤，此標籤使用 [Adobe Experience Cloud ID (ECID)服務](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant) 建立 [第一方Experience Clouds_ecid Cookie](cookies-first-party.md)，而非Adobe AdvertisingCookie。

## Cookie 名稱：_lcc

<table id="table_821F8EBE91F244CBA72B0975B961B908"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>顯示廣告點擊的 ID 和時間戳記 (格式為 yyyymdd)</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>15 分鐘</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>協力廠商 Cookie，用於判斷顯示廣告上的點擊事件是否適用於 Adobe Analytics 點擊 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>52 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：_tmae

<table id="table_28C2B62595E240D5A3C3E0BE147748C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>使用Adobe Advertising DSP追蹤的廣告參與編碼ID和時間戳記 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>1 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>此第三方 Cookie 會一併儲存使用者參與和廣告，例如「最近一次於 2016 年 6 月 30 日觀看廣告 xyz123」 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>變數；資料經過編碼，通常少於 1 KB </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：adcloud

<table id="table_D7CD238736BC4571883F92F47673F57C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>瀏覽者上次造訪廣告商網站的時間戳記、瀏覽者上次的搜尋點擊，以及使用者點擊廣告時建立的 ef_id</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>1 年</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>將瀏覽者 ID 與相關對象區段和轉換建立關聯的第一方 Cookie </p> <p> 上次造訪的相關資訊可避免向傳送不必要的請求，進而最佳化頁面載入時間。 [!DNL Adobe] 伺服器。 </p> <p>上次搜尋點擊的相關資訊有助於判斷轉換事件是由點擊還是觀看率 (因曝光但無點擊所產生的轉換) 所產生。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>廣告商的頂層網域 (例如 example.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>變數，但通常為 50-150 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：ev_sync_&#42;

(Ev_sync_ax、ev_sync_bk、ev_sync_dd、ev_sync_fs、ev_sync_ix、ev_sync_nx、ev_sync_ox、ev_sync_pm、ev_sync_rc、ev_sync_tm、ev_sync_yh)

<table id="table_A05C02AB261946E0AABAD78259392D81"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>要執行同步的日期，格式為 yyyymmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>要執行同步的日期，格式為 yyyymmdd </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>協力廠商廣告交易特定Cookie，可將Adobe Advertising瀏覽者ID與合作夥伴廣告交易同步。 系統會為新瀏覽者建立此 Cookie，並在過期時傳送同步請求。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>8 個字元 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：everest_g_v2

<table id="table_04043292A43B41B69EAF17AF4E217C69"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>瀏覽器和瀏覽者 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>1 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>在使用者首次點擊用戶端廣告後建立，可將目前和後續點擊對應至用戶端網站上的其他事件。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~27 個字元 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：everest_session_v2

<table id="table_1A3AE4CA71304ADB943CB1F64BE695F5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>工作階段 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>瀏覽器關閉時 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>協力廠商瀏覽器工作階段 Cookie；同一 Cookie 可用於所有帳戶 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~16 個字元 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：ev_tm

<table id="table_6C4D9DCFA4BF4FB2BD445E027550955F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>Adobe Advertising DSP(Demand Side Platform) ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>2 年 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>此第三方 Cookie 儲存的 DSP ID 會對應至 everest_g_v2 Cookie 中的瀏覽者 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>everesttech.net </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>~20 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱：id_adcloud

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p>瀏覽者 ID </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>有效期限 </p> </td> 
   <td colname="col2"> <p>91 天 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>使用方式 </p> </td> 
   <td colname="col2"> <p>第一方網域已設定 Cookie，但尚未使用 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>位置 </p> </td> 
   <td colname="col2"> <p>廣告商的頂層網域 (例如 example.com) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>大小 </p> </td> 
   <td colname="col2"> <p>16 位元組 </p> </td> 
  </tr> 
 </tbody> 
</table>
