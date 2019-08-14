---
description: Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。
keywords: Cookie;隱私
seo-description: Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。
seo-title: Scene7 Cookie
solution: Marketing Cloud, Analytics, Target, Social
title: Scene7 Cookie
uuid: f9b9d13a-17e5-4139-8c84-6fe5d22c4196
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 426c1fecf16e1cf83cd28971e4de6fdb66b0e10d

---


# Scene7 Cookie{#scene-cookies}

Scene7 使用 Cookie 來儲存用於將動態媒體傳送給瀏覽器的有用資訊。

Scene7 將資訊儲存在本機，以供部分舊版 AS2 Flash 檢視器使用。

針對 AS2 檢視器，Cookie:

* 追蹤使用者的工作階段狀態，例如目前頁面和檢視影像、目前縮放程度等等。
* 確定從使用者前一工作階段至今經歷了多久時間。檢視器使用此資訊決定是否要繼續前一工作階段，或是開始新的工作階段。此項資訊也同樣傳送至 Scene7 伺服器，但未受到使用。

對於 AS2 Flash eCatalog 檢視器，Cookie:

* 儲存使用者產生的內容 (最顯眼的內容由使用者輸入在 ecatalog 檢視器的「自黏便箋」功能中)。此內容在使用者重新開始一個工作階段時會重新儲存。
* 當使用者發送電子郵件與另一名使用者共用 ecatalog 時，第二 AS2 檢視器項目符號內的自黏便箋內容即被複製到我們的伺服器以提供給收件者。當收件者開始檢視器工作階段時，自黏便箋內容即從伺服器被擷取並複製到 Cookie。此功能極少用到，所以不會到期，而過舊的內容也不會被移除。此時，它會無限期持續存留在伺服器上。

較新的 AS3 檢視器並未執行工作階段持續性。

* [Cookie 名稱: VatLogin.jsp](../cookies-overview/cookies-s7.md#section-03aa90aa7e36427b8cb12dc4a0f0291e)
* [Cookie 名稱: s7js.flyout.InfoMessage.displayed.state](../cookies-overview/cookies-s7.md#section-14ad50dfcd7342f9ac80283b1f0d3400)
* [Cookie 名稱: s7js.flyout.InfoMessage.displayed_idx.ant](../cookies-overview/cookies-s7.md#section-05d1c52c478541609f4a18a9c1eb032f)

## Cookie 名稱: VatLogin.jsp {#section-03aa90aa7e36427b8cb12dc4a0f0291e}

| 屬性 | 說明 |
|---|---|
| 儲存資訊 | 設定作業 Cookie。內嵌於 IPS ImageServer (IS、IR 及 SWF/外觀和視訊內容) 的 AuthFilter 使用 Cookie 來取得存取授權。如果 Cookie 存在的話，它便會允許 HTTP 請求通過，否則會傳回未經授權。 |
| 過期 | 此 Cookie 為作業 Cookie。Scene7 IPS [!DNL web.xml] 將目前的作業過期時間設定為 45 分鐘。 |

## Cookie 名稱: s7js.flyout.InfoMessage.displayed<assetId>.state {#section-14ad50dfcd7342f9ac80283b1f0d3400}

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
   <td colname="col2"> <p>&lt;assetId&gt; 是檢視器使用之資產的名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期。 </td> 
  </tr> 
 </tbody> 
</table>

## Cookie 名稱: s7js.flyout.InfoMessage.displayed<assetId>_idx<id>.ant {#section-05d1c52c478541609f4a18a9c1eb032f}

舊式 DHTML 檢視器使用瀏覽器 Cookie 來儲存狀態資訊和自黏便箋資料。多重畫面 DHTML 彈出式視窗亦會使用這些 Cookie 來使訊息指標隸屬於特定作業。

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
   <td colname="col2"> <p> </p> <p> &lt;assetId&gt; 是檢視器使用之資產的名稱，而 &lt;id&gt; 則是以 0 為基礎的自黏便箋索引。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 過期 </td> 
   <td colname="col2"> 該 Cookie 是作業 Cookie，關閉瀏覽器後即過期。 </td> 
  </tr> 
 </tbody> 
</table>

