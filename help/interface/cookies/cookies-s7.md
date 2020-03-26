---
description: Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。
keywords: cookies;privacy
seo-description: Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。
seo-title: Scene7 Cookie
solution: Marketing Cloud,Analytics,Adobe Target,Adobe Social
title: Scene7 Cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。

Scene7會將資訊儲存在本機，以供某些舊版AS2 Flash檢視器使用。

對於AS2檢視器，Cookie:

* 追蹤使用者的工作階段狀態，例如目前檢視的頁面和影像、目前的縮放等級。
* 確定自使用者上一個作業開始至今的時間。 檢視器會使用這項資訊來決定是否繼續先前的作業或啟動新的作業。 這項資訊也會傳送至Scene7伺服器，但不會使用。

對於AS2 Flash eCatalog檢視器，Cookie:

* 儲存使用者產生的內容（最引人注意的是使用者在Ecatalog檢視器的「註解」功能中輸入的內容）。 當使用者繼續作業時，會還原此內容。
* 當使用者發出電子郵件以與其他使用者共用對話方塊時，第二個AS2檢視器項目符號的便條紙內容會複製到我們的伺服器，以提供給收件者。 當收件者啟動檢視器工作階段時，便條紙內容會從伺服器擷取並複製至Cookie。 此功能很少使用，因此不會過期，且不會移除過時內容。 此時，它會無限期地在伺服器上持續存在。

較新的AS3檢視器不會實作作業持續性。

**Cookie 名稱: VatLogin.jsp**

| 屬性 | 說明 |
|---|---|
| 儲存的資訊 | 設定工作階段Cookie。 內嵌在IPS ImageServer（IS、IR以及SWF/外觀和視訊內容）中的AuthFilter會使用Cookie進行存取授權。 如果存在，則允許HTTP請求通過。 否則，它會傳回未授權內容。 |
| 過期 | 此Cookie是作業Cookie。 Scene7 IPS [!DNL web.xml] 將目前的作業過期時間設定為 45 分鐘。 |

**Cookie 名稱: s7js.flyout.InfoMessage.displayed`assetId`.state**

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
   <td colname="col2"> <p>&lt;assetId&gt;是檢視器使用的資產名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 此Cookie是作業Cookie，在瀏覽器關閉時過期。 </td> 
  </tr> 
 </tbody> 
</table>

**Cookie 名稱: s7js.flyout.InfoMessage.displayed`assetId`_idx`id`.ant**

舊版DHTML檢視器會使用瀏覽器Cookie來儲存狀態資訊和註解資料。 多螢幕DHTML彈出畫面也會使用它們，讓訊息指示器作業特定。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt;是檢視器使用的資產名稱，而&lt;id&gt;是以0為基礎的嚴格附註索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 此Cookie是作業Cookie，在瀏覽器關閉時過期。 </td> 
  </tr> 
 </tbody> 
</table>

