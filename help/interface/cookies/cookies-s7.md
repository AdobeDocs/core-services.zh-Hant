---
description: Adobe Scene7 如何使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。
keywords: Cookie;隱私
solution: Experience Cloud,Analytics,Target
title: 'Scene7 Cookie '
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
feature: Cookies
topic: Administration
role: Administrator
level: Experienced
translation-type: ht
source-git-commit: 61d60273e933c637dfe4400da78257e1c80015b3
workflow-type: ht
source-wordcount: '417'
ht-degree: 100%

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。

Scene7 會將資訊儲存在本機，以供某些舊版 AS2 Flash 檢視器使用。

針對 AS2 檢視器，Cookie 會：

* 追蹤使用者的工作階段狀態，例如目前檢視的頁面和影像、目前的縮放等級等等。
* 確定自使用者上一個工作階段開始至今的時間。檢視器會使用這項資訊來決定是否繼續先前的工作階段或開始新的工作階段。這項資訊也會傳送至 Scene7 伺服器，但不會使用。

針對 AS2 Flash eCatalog 檢視器，Cookie 會：

* 儲存使用者產生的內容 (最明顯的是使用者在 eCatalog 檢視器的「註解」功能中輸入的內容)。當使用者繼續工作階段，此內容會還原。
* 使用者起始電子郵件以與其他使用者共用 eCatalog 時，第二個 AS2 檢視器項目符號的註解內容會複製到我們的伺服器並以提供給收件者。收件者起始檢視器工作階段時，系統會從伺服器擷取註解內容並複製到 Cookie 中。此功能很少使用，因此不會過期，且不會移除過時內容。目前無限期地在伺服器上持續存在。

較新的 AS3 檢視器不會實作工作階段持續性。

**Cookie 名稱：VatLogin.jsp**

| 屬性 | 說明 |
|---|---|
| 儲存的資訊 | 設定工作階段 Cookie。內嵌在 IPS ImageServer (IS、IR 及 SWF/面板和視訊內容) 中的 AuthFilter 會使用 Cookie 進行存取授權。如果存在，它會允許 HTTP 請求通過。若不存在，則會以未授權狀態傳回。 |
| 過期 | 此 Cookie 是工作階段 Cookie。Scene7 IPS [!DNL web.xml] 將目前的作業過期時間設定為 45 分鐘。 |

**Cookie 名稱：s7js.flyout.InfoMessage.displayed `assetId`.state**

<table id="table_6835D64C5D464A049F576621F2BE3FAD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 儲存的資訊 </td> 
   <td colname="col2"> <p>&lt;assetId&gt; 是檢視器使用中的資產名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 此 Cookie 是工作階段 Cookie，會在瀏覽器關閉時過期。 </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名稱：s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

舊版 DHTML 檢視器會使用瀏覽器 Cookie 來儲存狀態資訊和註解資料。多螢幕 DHTML 彈出式視窗也會使用這些 Cookie 來讓訊息指示器屬於特定工作階段。

<table id="table_8F6CC83D32D54BEE99884318AD126C98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 儲存的資訊 </td> 
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; 是檢視器使用中的資產名稱，而 &lt;id&gt; 是以 0 為基礎的註解索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 此 Cookie 是工作階段 Cookie，會在瀏覽器關閉時過期。 </td> 
  </tr> 
 </tbody> 
</table>

