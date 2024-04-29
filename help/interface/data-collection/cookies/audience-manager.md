---
description: 了解 Adobe Experience Cloud 中的 Audience Manager Cookie。
keywords: Cookie
solution: Experience Cloud, Audience Manager
title: Audience Manager Cookie
uuid: 8b384c38-b85a-4e93-b00e-41a9d3ae2b21
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: ab6de845-99ea-4cd8-b7cd-012fb641403f
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 99%

---

# Audience Manager Cookie{#audience-manager-cookies}

Audience Manager 仰賴一些簡單的 Cookie 執行不同功能。這些功能包括指派 ID、記錄資料呼叫、追蹤錯誤和進行測試以瞭解 Cookie 是否可以設定。本節列出並說明 Audience Manager 所設定的各種 Cookie。

**demdex Cookie**

<table id="table_1CCF7EA2BC9E421F8DEECA5F611E33F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> 設定此 Cookie 以指派唯一 ID 至網站訪客。<span class="wintitle"> demdex</span> Cookie 可協助 <span class="keyword">Audience Manger</span> 執行基本功能，例如︰訪客身分識別、ID 同步化、分割、模型、報告等。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>內容</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">demdex</span> Cookie 包含「唯一使用者 ID」(UUID)，如下列範例所示: </p> <p> <span class="codeph"> 06151304227769720433039235178204449977 </span> </p> <p>也請參閱 <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/ids-in-aam.html" format="https" scope="external">Audience Manager 內的 ID 索引</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他屬性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_11291DA87C5045E880034E06C863BCDA"> 
      <li id="li_40C30A06A12449A4A8748621223CA71B">存留期︰<span class="wintitle">demdex</span> Cookie 具有 180 天的存留時間 (TTL) 間隔。每位使用者與合作夥伴網站互動時，TTL 都會重設為 180天。如果使用者沒有在 TTL 間隔內回訪您的網站，Cookie 便會過期。 </li> 
      <li id="li_A589EDA2198249829207A183872EF1FF">選擇退出：如果使用者許選擇退出資料收集，則 <span class="keyword">Audience Manager</span> 會重新設定附有 <span class="codeph">Do Not Adobe Target</span> 字串的 Cookie。在此情況下，Cookie TTL 會設定為 10 年。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**dextp Cookie**

<table id="table_7343C9C9ADD24D3FA693ECC76E4A4045"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> 設定此 Cookie 以記錄其最後一次進行資料同步呼叫的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>內容</b> </p> </td> 
   <td colname="col2"> <p><span class="wintitle">dextp</span> Cookie 包含資料提供者的名稱或 ID，以及直立線符號分隔字串格式的 UNIX UTC 時間戳記。在這些範例中，<i>斜體字</i>代表變數預留位置。 </p> <p> 
     <ul id="ul_80D0BC3FCF06470991E12712401D784A"> 
      <li id="li_03747A433CEB4756A26CD866E716B89D">舊樣式：<span class="codeph"> <span class="varname"> 資料提供者名稱 </span>-1490307822097| <span class="varname"> 資料提供者名稱 </span>-1490307822038 </span> </li> 
      <li id="li_79E7000E82DB4ADA9E9887B017343B2D">新樣式：<span class="codeph">21-1-1490307821616|544-1-1490307821793|3-1-1490307821852|420-1-1490307822038| </span> </li> 
     </ul> </p> <p>另請參閱下文的 dextp 資料語法一節。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他屬性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_4922AC2CD55D4C888A6FBEB22F8B889B"> 
      <li id="li_91A68C44E53840379C2ACDED25468735">存留期：<span class="wintitle">dextp</span> Cookie 具有 180 天的存留時間 (TTL) 間隔。 </li> 
      <li id="li_6B8C674EFAAC4DABA0A640CF29247F99">選擇退出：如果使用者許選擇退出資料收集，則 <span class="keyword">Audience Manager</span> 會重新設定附有 <span class="codeph">Do Not Adobe Target</span> 字串的 Cookie。在此情況下，Cookie TTL 會設定為 10 年。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

dextp Cookie 資料語法：

下表列出並定義 `dextp` Cookie 內的元素，依其在資料字串內的位置而定。

<table id="table_BE00604B97F24F5A94AA4F566063D785"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 變數位置 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>第一或第二</b> </p> </td> 
   <td colname="col2"> <p>資料提供者名稱或 ID 的位置，會因 Cookie 使用新樣式或舊樣式格式設定而異。 </p> <p> <b>舊樣式格式設定：</b> </p> <p> 
     <ul id="ul_5BFBF40E3FE849CA859030F2D070FDF6"> 
      <li id="li_E8F4DC0CB15B472ABE9892B3A61D7F77">語法：<span class="codeph"> <span class="varname"> 資料提供者名稱 </span> - <span class="varname"> UNIX UTC 時間戳記 </span> </span> </li> 
      <li id="li_7CD8B101156140F49EA97B18E9591402">範例：<span class="codeph"> dataProvider1 - 1490307822038 </span> </li> 
     </ul> </p> <p>舊樣式 Cookie 會以可讀名稱識別資料提供者。 </p> <p> <b>新樣式格式設定：</b> </p> <p> 
     <ul id="ul_AC6225CA781746148C125F21DFED1ED9"> 
      <li id="li_29C4B52E398B4EA28944980A15B05A57">語法：<span class="codeph"> <span class="varname"> 資料提供者 ID </span> - 1|2 - <span class="varname"> UNIX UTC 時間戳記 </span> </span> </li> 
      <li id="li_3BF30CA5FED242DF96E0B54AFC64B06F">範例：<span class="codeph"> 123345 - 1 - 1490307822038 </span> </li> 
     </ul> </p> <p>新樣式 Cookie： </p> <p> 
     <ul id="ul_F05A91A455FA44C7A71186C0C9E31630"> 
      <li id="li_A8C9638173684359BABC4207845A4F48">以數值 ID 取代可讀資料提供者名稱。 </li> 
      <li id="li_28F1E2DB24904E53BE9718AD788CE61E">使用 ID 1 或 ID 2 識別呼叫類型。ID 1 代表 ID 同步呼叫。ID 2 代表已不再使用的過時呼叫。您應該不會看到多個 (或任何) 使用 ID 2 的 dextp Cookie。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>上次</b> </p> </td> 
   <td colname="col2"> <p>上次位置包含 UNIX UTC 時間戳記。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**dst Cookie**

<table id="table_83AE9B6350C6408BAECD9FCF33022B98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 屬性 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>用途</b> </p> </td> 
   <td colname="col2"> <p> <span class="keyword">Audience Manager</span> 在有傳送資料至<a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/destinations.html" format="https" scope="external">目的地</a>的錯誤發生時設定此 Cookie。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>內容</b> </p> </td> 
   <td colname="col2"> <p> <span class="wintitle">DST</span> Cookie 包含目的地 ID 集合和直立線符號分隔字串格式的 UNIX 時間戳記。在這些範例中，<i>斜體字</i>代表變數預留位置。 </p> <p> 
     <ul id="ul_CE98076A02DA413486C1D341E9806889"> 
      <li id="li_850209D956644749B98C7A208C825C15">語法：<span class="codeph"> <span class="varname"> 目的地 ID </span> - <span class="varname"> UNIX UTC 時間戳記 </span> </span> </li> 
      <li id="li_4A22152C70844733982230EBF7B9EB78">範例：<span class="codeph">067797-1490349684|1010788-1490349692|1067797-1490349692 </span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>其他屬性</b> </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_5D13DD701B484B51BF2808A69A919106"> 
      <li id="li_4E665114C63246FBA32A4E19984D2693">存留期：<span class="wintitle">dst</span> Cookie 具有 180 天的存留時間 (TTL) 間隔。 </li> 
      <li id="li_A682B566704F43D2AB72487EFF212474">選擇退出：如果使用者許選擇退出資料收集，則 <span class="keyword">Audience Manager</span> 會重新設定附有 <span class="codeph">Do Not Adobe Target</span> 字串的 Cookie。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**_dp Cookie**

此 cookie 為暫時性。[!DNL Audience Manager] 嘗試設定 `_dp` Cookie，以確定其是否可以在協力廠商內容的 demdex.net 網域設定其他 Cookie。`_dp` 設定完成後，其內包含 1 的值。[!DNL Audience Manager] 讀取此值並立即移除該 Cookie。如果 `_dp` Cookie 不存在，則 [!DNL Audience Manager] 會知道不能設定 Cookie。
