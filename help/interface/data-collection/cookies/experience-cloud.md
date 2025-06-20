---
description: 了解 ID 服務如何在 Experience Cloud 應用程式間儲存和使用。
solution: Experience Cloud,Analytics,Target
title: Experience Cloud Cookie
uuid: a4788c1c-0402-4fc8-b894-cd24fa794f4f
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: bd9bea58-9987-40d6-84e0-da185388bbbb
source-git-commit: 2073400a04933226bd036c1fcd729df70f101df3
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 88%

---

# Experience Cloud Cookie

Adobe Experience Cloud使用Cookie來儲存不同Experience Cloud應用程式所使用的訪客ID。 這些Cookie特別適用於在[experience.adobe.com](https://experience.adobe.com)上存取Adobe Experience Cloud應用程式。

**Cookie 名稱：s_ecid**

<table id="table_FF4C70D3D4CC425BA65162D5A9504F7D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p> 包含 Experience Cloud ID (ECID) 或 MID 副本。MID 儲存在遵循此語法 (s_ecid=MCMID|&lt;ECID&gt;) 的機碼值組中 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p>2年，不過大部分的現代瀏覽器都會截斷為13個月</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用方式 </p> </td> 
   <td colname="col2"> <p>此 Cookie 是在用戶端設定 AMCV Cookie 後，由客戶的網域所設定。此 Cookie 的目的是允許以第一方狀態進行永久性 ID 追蹤，並在 AMCV Cookie 過期時作為參考 ID 使用。請在此查看 AMCV Cookie，以瞭解詳細資訊。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p>僅限 CNAME 客戶。不適用於協力廠商情況。Cookie 會儲存在您的網域中，此網域與 CNAME 和 Analytics 影像要求所使用的網域相同。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p>45 位元組 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> SameSite=Lax </p> </td> 
   <td colname="col2"> <p>唯有瀏覽器 URL 中顯示的網域符合 Cookie 的網域時，系統才會傳送具有此設定的 Cookie。此設定是 Chrome 中的 Cookie 新預設值。</p> </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名稱：AMCV_###@AdobeOrg**

[Experience Platform ID Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant) 會使用 JavaScript 將不重複訪客 ID 儲存在現行網站網域的 `AMCV_###@AdobeOrg` Cookie 中，其中 `###` 代表隨機的字元字串，例如 `AMCV_1FD6776A524453CC0A490D44%40AdobeOrg.`

另請參閱 [Cookie 和 ID Service](https://experienceleague.adobe.com/docs/id-service/using/intro/cookies.html?lang=zh-Hant)。

<table id="table_1883C0836C1E4AF5A262FBF5000C1B11"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>儲存的資訊 </p> </td> 
   <td colname="col2"> <p> Experience Cloud 解決方案使用的不重複訪客 ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 過期 </p> </td> 
   <td colname="col2"> <p> 13 個月 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 使用方式 </p> </td> 
   <td colname="col2"> <p> 該 Cookie 用於識別不重複訪客 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 位置 </p> </td> 
   <td colname="col2"> <p> 此 Cookie 會儲存在網站的網域中 (而非影像請求的網域)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 大小 </p> </td> 
   <td colname="col2"> <p> 視情況而異，大部分客戶可預期此 Cookie 的長度約為 200 位元組。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>未增加值。Chrome 預設為 Lax。 </p> </td> 
   <td colname="col2"> <p> 唯有瀏覽器 URL 中顯示的網域符合 Cookie 的網域時，系統才會傳送具有此設定的 Cookie。此設定是 Chrome 對 Cookie 的新預設值。 </p> </td> 
  </tr> 
 </tbody> 
</table>
