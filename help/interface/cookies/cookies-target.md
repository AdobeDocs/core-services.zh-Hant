---
description: Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和促銷活動與訪客的關聯性較強。
keywords: cookies;privacy
seo-description: Target 使用 Cookie 來讓網站營運人員測試哪些線上內容和促銷活動與訪客的關聯性較強。
seo-title: Target Cookie
solution: Marketing Cloud,Analytics,Target,Social
title: Target Cookie
uuid: 44f7e32e-8d99-4682-8b54-8364d001b403
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Adobe Target Cookies{#target-cookies}

Adobe Target使用Cookie讓網站營運商能夠測試哪些線上內容和優惠與訪客更相關。

您可以視需要變更這些設定，但Cookie持續時間除外。 變更Cookie設定時，請洽詢您的帳戶代表。

>[!NOTE]
>
>Adobe Target使用者也可以建立自訂的第三方Cookie。

<table id="table_54B402C6E19C4A70B1E27BC9DFF776EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 設定 </th> 
   <th colname="col2" class="entry"> 資訊 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie名稱 </p> </td> 
   <td colname="col2"> <p>mbox。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie網域 </p> </td> 
   <td colname="col2"> <p>您從中提供mbox的網域的第二層和頂層。 因為是使用公司所提供的網域，所以這些會是第一方 Cookie。範例: <span class="filepath">mycompany.com</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>伺服器網域 </p> </td> 
   <td colname="col2"> <p> <span class="filepath"> clientcode.tt.omtrdc.net</span>，使用Adobe Target帳戶的用戶端代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cookie持續時間 </p> </td> 
   <td colname="col2"> <p>自訪客上次登入後兩年，Cookie仍會留在訪客的瀏覽器上。 您無法變更Cookie持續時間。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>如果您的網域名稱包含國碼 (例如 [!DNL mycompany.co.uk])，請和您的客戶服務代表合作設定您的 [!DNL mbox.js] 以支援此作業。

Cookie會保留一些值，以管理訪客體驗Adobe Target促銷活動的方式：

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
   <td colname="col2"> <p>使用者工作階段的唯一ID。 依預設，這會持續30分鐘。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pc ID</span> </p> </td> 
   <td colname="col2"> <p>訪客瀏覽器的半永久ID。 持續直到手動刪除Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> check</span> </p> </td> 
   <td colname="col2"> <p>用來判斷訪客是否支援Cookie的簡單測試值。 每次訪客請求頁面時，都會進行設定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> disable</span> </p> </td> 
   <td colname="col2"> <p>如果訪客的載入時間超過 <span class="filepath">mbox.js</span> 檔案中所設定的逾時時間，則設定此選項。依預設，這會持續 1 個小時。 </p> </td> 
  </tr> 
 </tbody> 
</table>

