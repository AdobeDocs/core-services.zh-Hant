---
description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
keywords: customer attributes
seo-description: Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。
seo-title: 常見問題、限制和最佳作法
solution: Experience Cloud
title: 常見問題、限制和最佳作法
uuid: e93eb531-23c7-4d75-92e8-75699f58546a
translation-type: tm+mt
source-git-commit: 12c3ac8bfa64b7c8708312576ac6dc4036c1b7d8

---


# 常見問題、限制和最佳作法

Analytics 和 Target 中的客戶屬性常見問題集和最佳作法。

## 最佳作法和限制 {#section_7F5189B3DAA84EE6865B91D2026EE05A}

客戶屬性使用指南和限制。

| 問題 | 說明 |
|--- |--- |
| 客戶屬性訂閱限制 | 升級至 Analytics Premium 後，您必須等待 24 小時才可使用其他屬性。在這段期間，您可能會看到已達到屬性訂閱上限錯誤。 |
| 同一裝置上多次登入 | 當使用客戶屬性將客戶個人檔案上傳至資料來源時，Adobe建議使用共用相同裝置的使用者（亦即相同的Experience Cloud ID）。 這麼做可能會導致ECID服務（此服務在裝置上持續存在）在相同的Experience Cloud ID下連結多個使用者，造成非預期的結果 [!DNL Target]。 **** 注意：對於Mobile,ECID在安裝Mobile應用程式後是永久的，您必須重新安裝應用程式才能產生新的ECID。 若是網頁，則會在清除瀏覽器Cookie後產生新的ECID。 |
| 每日頻率上傳限制 | Adobe建議您每天只更新一次客戶屬性。 您至少必須等待24小時，才能為同一組個人檔案上傳另一個客戶個人檔案資料檔案。 |
| Custom Analytics ID (`s.visitorID`) | 在 Analytics 中，使用 `s.visitorID` 來設定客戶 ID 是辨識使用者的方法。不過，當使用 `s.visitorID.`<br>This includes（但不限於）共用觀眾、Analytics for Target(A4T)和客戶屬性來識別訪客時，使用ID服務匯出或匯入Analytics資料的整合將無法運作。<br>對於這類整合內容，設定自訂 Analytics ID 的方法便不受支援。 |
| Analytics 的字元長度限制 | 建立 Analytics 訂閱時，已上傳檔案的欄位長度會遭到截斷，僅能顯示 255 個字元。 |

## 客戶屬性常見問題 {#section_E47866EEA83348E09FE43CEC5E44C461}

<table id="table_88631069013B408EBB0A810657662B36"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 問題 </th> 
   <th colname="col2" class="entry"> 回答 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>我能夠收到客戶屬性上傳狀態的相關通知嗎? </p> </td> 
   <td colname="col2"> <p>是。請參閱<a href="../admin-getting-started/organizations.md#concept_0105453AD71847B8BFCAF4A40915F157" format="dita" scope="local">管理通知</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 剛開始使用客戶屬性時該做什麼? </p> </td> 
   <td colname="col2"> 
    <ol id="ol_1FACEF0990B6486B8DE86245D17695A8"> 
     <li id="li_F0C1542853684F8591FDC1B441D31A56"> <p>取得佈建。 </p> <p>如果您是 <b>Analytics</b> 客戶，Adobe 會為您佈建客戶屬性。如果您只使用 <b>Target</b> 而且沒有 Analytics，則須聯絡客戶服務，請他們幫您佈建核心服務。 </p> </li> 
     <li id="li_444FEDEE4B7244F79BA847662F5B17CB"> <p>與您的 CRM 團隊討論。找出適用於 Analytics 和整個 Experience Cloud 中所需的客戶資料種類。 </p> </li> 
     <li id="li_32D4AAF8C29748A78801A0E1BFB37AF5"> <p>實作核心服務。 </p> <p>請參閱<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> 快速入門 - 啟用核心服務的解決方案</a>，瞭解為核心服務導入最新實作方式的相關步驟。(請參閱同步客戶 ID 做為重要資訊一節) </p> </li> 
    </ol> <p> <b>附註:</b> 有關實作核心服務的管理員常見問題集可在<a href="../admin-getting-started/faq.md#concept_13219B4E51784577B6FF78AAA203DE91" format="dita" scope="local">此處</a>取得。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 我可以使用多少個客戶屬性? </p> </td> 
   <td colname="col2"> <p>您可以上傳數百欄 <span class="filepath">.csv</span> 至客戶屬性服務。不過，在設定訂閱和選取屬性時，會根據您擁有的解決方案，套用下列限制（每個報表套裝）:</p> <p> 
     <ul>
     <li>Foundation: 0 個</li>
     <li>Select: 3 個</li>
     <li>Prime: 15 個</li>
     <li>Ultimate: 200 個</li>
     <li>Standard 版: 共 3 個</li>
     <li>Premium:200</li>
     <li>Target Standard: 5 個</li>
     <li>Target Premium: 200 個</li></ul>
     </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>一定要移轉至 Experience Cloud ID 服務嗎? </p> </td> 
   <td colname="col2"> <p>是否移轉取決於您使用的解決方案。 </p> <p> 
     <ul id="ul_9C473434B5DA4C6299AAB209DEDFCDE7"> 
      <li id="li_8BC10EB2825F4ADF8CA61F71D4994A28"> <b>Adobe Analytics</b>: 強烈建議 </li> 
      <li id="li_56F518E3F3DF4C93B6F7EF3B40ACC52F"> <b>Adobe Target:</b> 必要。 </li> 
     </ul> </p> <p>使用 ID 服務可提升功能，開啟一道使用最新 Experience Cloud 功能的方便之門，包括即時受眾、Target 最新化、Analytics 整合、視訊心率追蹤。 </p> <p>如需詳細資訊，請參閱<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">核心服務 - 如何啟用解決方案</a>。 </p> <p> <b>附註</b>: <span class="term">Experience Cloud ID 服務</span>是前身為 <span class="term">Analytics 訪客 ID 服務</span>的最新化實作。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>客戶屬性功能與 Adobe Audience Manager 有何關係? </p> </td> 
   <td colname="col2"> <p>Audience Manager 可以接收資料以執行受眾識別，但不能執行將屬性聯結至歷史行為資料的分析功能，也不能提供 Adobe Analytics 中的報告、分析及區隔功能。「People」核心服務將來自各解決方案的豐富資料串連起來，並與單一 ID 建立關聯，以便在整個 Experience Cloud 之中使用。 </p> <p> 在 Adobe Target 中，客戶屬性顯示為個別屬性，可與其他規則結合以建立受眾。「People」核心服務中共用的受眾是無法修改的完整受眾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(僅限 Analytics) </b>這項功能與 Analytics Premium 提供的有何差異? </p> </td> 
   <td colname="col2"> <p>在過去，有意結合客戶屬性資料與 Analytics 資料的客戶，十分依賴此功能的資料工作台工具。客戶屬性提供客戶屬性做為 Reports &amp; Analytics、Ad Hoc Analysis 和 Report Builder 中的維度和度量，將此功能開放給更廣大的受眾。Analytics Standard 的客戶將可存取客戶屬性，但可使用的功能有限。Analytics Premium 的客戶則可使用完整功能。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(僅限 Target)</b> 我是否能為客戶預先載入或上傳 Target 中不曾出現的資料嗎? </p> </td> 
   <td colname="col2"> <p> 是。訪客第一次向 Taget 提出要求時，系統會從「客戶屬性」擷取現有的相關資料，並使用此資料進行鎖定。 </p> <p> <p>附註: 如果訪客是第一次與 Target 互動，則擷取此資料可能需花費 20 分鐘。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(僅限 Target)</b> 我是否能結合客戶屬性資料和共用的受眾資料來建立超級受眾? </p> </td> 
   <td colname="col2"> <p>不會。共用的受眾資料已經是建立完畢的受眾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(僅限 Target) </b>客戶屬性功能與 Target 大量設定檔 API 有何差異? </p> </td> 
   <td colname="col2"> <p> <a href="https://www.adobe.io/apis/experiencecloud/target.html" format="https" scope="external">大量設定檔 API</a> 可以透過 API 以個別或大量的方式直接更新 Target 設定檔。其功能類似於客戶屬性，但有下列幾點重要差異: </p> 
    <ul id="ul_5AAA4A8497C04F50A8AAA9F776BB868E"> 
     <li id="li_B20AEA397F3B4C86A1140CDA61ABD575">設定檔 API 是 REST API 呼叫，而客戶屬性使用 FTP。 </li> 
     <li id="li_7FBE428EF5D34B6AA09B6368E8210344">Target 的設定檔 API 只會傳送資料給 Target，而非整個 Experience Cloud。 </li> 
     <li id="li_CBB4D3FAF53944E0A066A4AD9F9C8760">客戶屬性提供簡單介面，用於建立和管理此外部資料。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>(僅限 Target)</b> 從客戶屬性上傳資料至 Adobe Target 是否能延長 Target 訪客設定檔期限? </p> </td> 
   <td colname="col2"> <p>是。請參閱 Adobe Target 說明中的<a href="https://docs.adobe.com/content/help/en/target/using/audiences/visitor-profiles/visitor-profile.html" format="https" scope="external">訪客設定檔期限</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b> (僅限 Target)</b> 從客戶 ID 辨別出訪客後，我可以立即鎖定上傳至客戶屬性中的資料嗎? </p> </td> 
   <td colname="col2"> <p>是. </p> <p>在對 Target 進行的伺服器呼叫後，由於此呼叫包含 mbox 第三方 ID，因此所有客戶屬性資料都可供使用。 </p> </td> 
  </tr> 
 </tbody> 
</table>
