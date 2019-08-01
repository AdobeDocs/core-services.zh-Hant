---
description: Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和促銷活動與訪客的關聯性較強。
keywords: Cookie；隱私權
seo-description: Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和促銷活動與訪客的關聯性較強。
seo-title: Target Cookie
solution: Marketing Cloud、Analytics、Target、Social
title: Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: c1630f5de61e410eaf10cf940faa9adc6017fb6b

---


# Target Cookie{#target-cookies}

Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和促銷活動與訪客的關聯性較強。

您可以視需要變更這些設定，但不包括 Cookie 持續時間。變更 Cookie 設定時，請洽詢您的帳戶代表。

>[!NOTE]
>
>Target使用者也可以建立自訂第三方Cookie。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 設定 </th> 
   <th colname="col2" class="entry"> 資訊 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie 名稱 </p> </td> 
   <td colname="col2"> <p>mbox。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie 網域 </p> </td> 
   <td colname="col2"> <p>是指您提供給此 mbox 的第一層與第二層網域。因為是使用公司所提供的網域，所以這些會是第一方 Cookie。範例: <span class="filepath">mycompany.com</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>伺服器網域 </p> </td> 
   <td colname="col2"> <p> <span class="filepath">clientcode.tt.omtrdc.net</span>，使用您 Target 帳戶的用戶端代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie 持續時間 </p> </td> 
   <td colname="col2"> <p>Cookie 會從訪客上一次登入開始，在訪客的瀏覽器中繼續存在兩個星期。您無法變更 Cookie 持續時間。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>If any of your domain names include a country code, such as [!DNL mycompany.co.uk], work with your Client Services to configure your [!DNL mbox.js] to support this.

此 Cookie 會保留一些值，以管理您訪客體驗 Target 促銷活動的方式:

<table id="table_5245F72A2D5A4322B40ABB10B7DFB338"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 值 </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> session ID</span> </p> </td> 
   <td colname="col2"> <p>每個使用者作業會有一個唯一 ID。依預設，這會持續 30 分鐘。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>每位訪客瀏覽器的半永久性 ID。會持續直到手動刪除此 Cookie 為止。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>用來決定訪客是否支援 Cookie 的簡單測試值。每次訪客請求頁面時都會進行設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>如果訪客的載入時間超過 <span class="filepath">mbox.js</span> 檔案中所設定的逾時時間，則設定此選項。依預設，這會持續 1 個小時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

