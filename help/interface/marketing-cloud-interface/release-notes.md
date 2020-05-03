---
description: Experience Cloud 介面的功能、發行說明和已知問題。
keywords: core services
seo-description: Experience Cloud 介面的功能、發行說明和已知問題。
seo-title: 歷來的發行說明
solution: Experience Cloud
title: 歷來的發行說明
uuid: fcff8cc6-e587-4bf2-9a75-261d4eabc7d4
translation-type: tm+mt
source-git-commit: 31811e718be130612c8688e80084cb7579e94f47

---


# 歷來的發行說明

Experience Cloud 介面的功能、發行說明和已知問題。

如需文件更新的清單，請參閱 [Experience Cloud](../doc-updates.md#concept_4C8983FCD23848A4B1E4C2D99ED82784)。

如需所有解決方案的發行說明，請參 [閱Experience Cloud發行說明](https://docs.adobe.com/content/help/zh-Hant/release-notes/experience-cloud/current.html)。

## 2020年1月至1月

* 「動態消息」頁面已於2019年12月過時。 請參閱產品中的淘汰通知。(MCUI-10039)

## 2019 年 8 月版

* 修正 Experience Cloud 登入時的重大問題，這會導致部分使用者從工作階段登出。(MCUI-6908)
* 更新 Experience Cloud 登入機制，以改善效能並減少延遲。(MCUI-6854、MCUI-6869、MCUI-6883)
* 更新介面外觀。(MCUI-6861、MCUI-6911、MCUI-6862)
* 修正 Experience Cloud [!UICONTROL Triggers] 的問題，此問題會導致錯誤詮釋 _Like_ 子句 (位於 [!UICONTROL Trigger] 定義中)。(MCUI-6611)

## 2019 年 4 月版

* 已更新應用程式切換器，將Marketo納入Experience Cloud解決方案套件，並更新Experience Platform的品牌。 (MCUI-6529)
* 更新Experience Cloud首頁，加入動態消息和管理頁面的導覽連結。 (MCUI-6682)
* 修正正確使用「like」子句的[!UICONTROL 「觸發」]定義問題。(MCUI-6611)
* 客戶屬性的改進功能，以更好地登入訂閱服務。 (MCUI-6519)

## 發行版本 19.1.1 - 2019 年 1 月 17 日

**注意:** 自 2019 年 3 月起，Experience Cloud 介面將不再支援 Internet Explorer 11。

* 修正幫助搜尋無法傳回結果的問題。 (MCUI-1670)
* 已修正並改善觸發器中的eVar管理。 (MCUI-6400)

## 發行版本 16.5.1 - 2016 年 5 月 26 日 {#section_3785F182BC13493F84903CA69EB6D0A8}

**功能和改進項目**

<table id="table_ABBCE1A66F534059BD728BC2B9AEFA80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>在Admin Console中預先設定的產品設定 </p> </td> 
   <td colname="col2"> <p>Experience Cloud客戶管理員可運用預先建立並對應至Analytics和動態標籤管理之預設權限群組的產品設定。 </p> <p>此最佳化適用於新布建的組織，並可縮短組織在管理控制台中管理使用者所需的時間。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>飼料改良 </p> </td> 
   <td colname="col2"> <p> 在Experience Cloud動態消息中建立新貼文時，「收件者」行現在會依預設使用目前作用中的主題，而改用組織。</p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 修正無法顯示從「隨選資產」共用至Experience Cloud動態消息的資產縮圖的問題。 (MAC-29955)


## 發行版本 16.2 - 2016 年 2 月 18 日 {#section_D9610373116C4D77A38F67815C725EA3}

<table id="table_C9B288CF42034F329C3C72D95D22E515"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud資產改進 </p> </td> 
   <td colname="col2"> <p>在Experience Cloud資產中，您可以從一個集中位置儲存、共用及同步您的數位資產。 Experience Cloud 資產運用 <span class="keyword">Adobe Experience Manager</span> (AEM) 提供的部分功能。 </p> <p>請參閱 <a href="../experience-cloud-assets/experience-cloud-assets.md#concept_DDA5224C907D4A4F817D795DA0ED64D0" format="dita" scope="local">Experience Cloud</a></p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>帳戶連結改進 </p> </td> 
   <td colname="col2"> <p>已改善將解決方案帳戶連結至Experience Cloud(Adobe ID)的介面工作流程。 此新工作流程會找出與組織相關聯的所有使用者帳戶，並讓您選擇要連結的帳戶。 我們也簡化了帳戶連結體驗，因此您不再需要存取「管理組織」頁面來手動連結帳戶。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 修正Analytics無法連結和SSO的問題。 此問題會顯示「通知： 錯誤訊息： 錯誤IMS SSO失敗： 找不到連結的公司。」

**已知問題**

If you access Dynamic Tag Management via the **[!UICONTROL Experience Cloud]** > **[!UICONTROL Activation]** interface, but your Dynamic Tag Management account is not linked to the Experience Cloud (Adobe ID), you will not be able to log in to Dynamic Tag Management. 請在新的瀏覽器分頁中直接導覽至 [!DNL dtm.adobe.com]，即可避免此問題。

## 發行版本 16.1 - 2016 年 1 月 21 日 {#section_33B3F7DF6CA347E3AA93801BAC6232CE}

<table id="table_4223658257DA41C999AC710A10D26771"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 觀眾程式庫訊息 </td> 
   <td colname="col2"> <p> 我們改善了「受眾程式庫」，在建立受眾和發生逾時問題時提供實用資訊。 </p> <p>例如，新增超過5個規則時，會顯示訊息，指出您已超出允許的最大規則。 (MAC-27376、MAC-27375) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Microsoft 即將[停止支援](https://www.microsoft.com/en-us/WindowsForBusiness/End-of-IE-support) Internet Explorer 8、9 和 10。有鑑於此，我們將不修正針對這些特定版本 Internet Explorer 所回報的問題。

## 發行版本15.10 - 2015年10月14日 {#section_68123833D3634BD3A473C12862BF9606}

**已知問題**

* 如果客戶透過Experience Cloud以單一登入方式登入Analytics，就無法登入報告建立工具。 此問題不會影響使用舊版Analytics認證的客戶。
* Analytics中「連結至報表」功能的已知問題。 透過Experience Cloud登入Analytics的客戶嘗試共用報表時，會導向至Analytics的非SSO登入頁面。

## 發行版本 15.9 - 2015 年 9 月 10 日 {#section_BCCE3E7DF62A4FF5A57B9C8FE2A5F37B}

* 修正Audience Manager API效能問題，此問題會在上傳客戶屬性資料時造成間歇性逾時。 (MAC-26305)
* 修正使用者無法將多達200個客戶屬性新增至訂閱的問題。 (MAC-26188)
* 修正無法從Analytics區段共用觀眾的「觀眾程式庫」問題。 此問題會顯示「收集資料」（0個觀眾）。 為避免此問題，Adobe建議將區段大小保持在每個區段50,000名受眾成員以下。 (MAC-25788)
* 修正「客戶屬性——編輯結構」頁面上，在變更顯示名稱時造成內容感知錯誤的先前已知問題。 (MAC-25589、AN-103834)

## Release 15.7 - July 22 2015 {#section_2683A152176944E48EF6C943892975B7}

* 修正Analytics報表中無法更新在「檢視／編輯結構描述」頁面（在客戶屬性中）上指定的屬性說明的問題。 (MAC-25985)
* 已修正無法為已上傳資產呈現縮圖的問題。 (MAC-25863)
* 修正在報告與分析中建立的新區段無法在Experience Cloud觀眾中使用的問題。 (MAC-25817)
* 已修正讓適用受眾無法在使用訪客 ID 服務時從 Analytic 共用的問題。(MAC-25788、MAC-25747)
* 新增對客戶屬性中多位元組字元的支援。 (MAC-25552)

**已知問題**

已知問題會導致在Audience Manager中建立重複的自動產生帳戶，並自動將其連結至使用者的Experience Cloud身分識別。 如果您嘗試在連結帳戶前導覽至Audience Manager，就會發生此問題。 Adobe建議您先將Audience Manager帳戶連結至Experience Cloud，然後再導覽至Audience Manager。 (MAC-25640)


## 發行版本15.6.1 - 2015年6月11日 {#section_AD2019F8D2F84C9EB2B0533FAACF7043}

無可用的資訊

## 發行版本 15.5.1 - 2015 年 5 月 13 日 {#section_EF197410964E40D294D0D8024738CFBA}

<table id="table_14E7B35E06C84A258A21D09691B58354"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>左側導覽功能表已更新並排程，以提供所有核心服務和解決方案的存取權。 顯著變更包括： </p> 
    <ul id="ul_5BEBAB86B9234A239C4E2DAF8826D8E3"> 
     <li id="li_7FA9F64CE69144B8A8A92746BF40E5A1">The <span class="term"> Audience Library</span> and <span class="term"> Customer Attributes</span> menu selections are now located under <span class="term"> Audiences</span>. </li> 
     <li id="li_95D62A43AE6243DBB2A65EDB830D05C4">此 <span class="term">Exchange</span> 功能表選取項目從「說明」下拉式功能表移動至左側導覽邊欄。 </li> 
     <li id="li_0443FD50C78446CD8AA27A4F272CAD31"> <span class="term">解決方案</span>已移除。您可以從導覽邊欄的下半部啟動所有解決方案。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

* 已修正妨礙客戶屬性與某些客戶同步的問題。
* Fixed an issue preventing [Adobe Target Product Documentation](https://docs.adobe.com/content/help/zh-Hant/target/using/integrate/a4t/a4t.html) page from displaying in Japanese.
* 已修正無法在 [!DNL Creative Cloud] 和 [!DNL Experience Cloud] 的評論中使用日文字的問題。

## 發行版本 15.4.1 - 2015 年 4 月 8 日 {#section_75634120CC934B3381EDEA7F6F976F0A}

<table id="table_3A6FBAE36558425A803B078150862C92"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>管理改進： </p> 
    <ul id="ul_7D5FCBEFA262435D865CA1018BFB792E"> 
     <li id="li_6E98974CCB094ABBAB57C51ED56C3F00"> <span class="wintitle"> 管理控制台</span> </li> 
     <li id="li_8CDAB6301FD44C3999EE4EEB1A0A2FD6">企業與同盟ID支援 </li> 
    </ul> </td> 
   <td colname="col2"> <p>使用者和群組管理功能已移至管理控制台。 新的導覽路徑是： </p> <p> <span class="uicontrol">「Experience Cloud</span> &gt; <span class="uicontrol">管理</span> &gt; <span class="uicontrol">啟動 Admin Console」</span></p> <p> 此外，也新增了對企業ID和同盟ID的支援。 您可以在相同的企業部署中使用企業ID、同盟ID和Adobe ID。 例如，對於可能使用其他Adobe產品和服務的使用者，請使用Adobe ID。 針對您想要嚴格管理其帳戶的使用者，使用企業或同盟ID。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 已修正無法在 [!DNL Experience Cloud] 和 [!DNL Media Optimizer] 使用單一登入功能的問題。

**已知問題**

* 將動態標籤管理組織與Experience Cloud連結及取消連結，不適用於新建立的Experience Cloud組織。 我們正致力於修正此問題，並在5月發行版本中恢復正常功能。 如果您在嘗試透過 Experience Cloud 以單一登入的方式登入動態標籤管理時發生問題，請在 [!DNL dtm.adobe.com] 使用舊版登入。
* 一個已知問題是受眾無法分享不屬於已連結 Analytics 帳號的報表套裝。我們積極修正

## 發行版本 15.3.2 - 2015 年 3 月 19 日 {#section_07760FD9CA43497FA8BDCCA990A24BFD}

<table id="table_54025DBE2D094FF1BE837BA60816C6DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>客戶屬性 </p> </td> 
   <td colname="col2"> <p>如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳資料後，您可以在 Analytics 中執行<span class="uicontrol">「訪客設定檔</span> &gt;<span class="uicontrol"> 客戶屬性」</span>報告。 </p> <p>也可以使用上傳的資料做為 <span class="keyword">Adobe Target</span> 中的受眾區隔。 </p> <p>請參閱<a href="../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1" format="dita" scope="local">客戶屬性</a>產品文件。 </p> <p> 如需最新化核心服務解決方案的相關資訊，請參閱<a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local">啟用核心服務的解決方案</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 發行版本 15.3.1 - 2015 年 3 月 4 日 {#section_57CB69C044DD47BDBC1A1BEC38957551}

<table id="table_EB3FFBA2DF904546A5185EC9A63BBA98"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>群組對應 </p> </td> 
   <td colname="col2"> <p>「群組管理」頁面已重新設計為管理介面，可讓您建立群組、新增使用者至群組，以及跨Experience Cloud解決方案套用權限。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>一對多對應 </p> </td> 
   <td colname="col2"> <p>在Experience Cloud中連結解決方案帳戶時，如果您有多個解決方案和組織，現在可以將多個產品和服務對應至單一組織。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>啟用 </p> </td> 
   <td colname="col2"> <p> <a href="../activation/activation.md#concept_EE756B6B0A0643DAB8CA3A00E665406C" format="dita" scope="local">「啟用」</a>現在顯示在 <span class="keyword">Experience Cloud</span> 的左側導覽器中。<span class="wintitle"> 啟動</span> 是 <span class="keyword"></span> Experience Cloud服務，目前包含動態標籤管理技術，在點按時會指引您前往。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>檔案更新——核心服務 </p> </td> 
   <td colname="col2"> <p>Added the topic <a href="../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C" format="dita" scope="local"> Enable your solutions for core services</a> to assist you with implementing core services. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 發行版本 15.2.1 - 2015 年 2 月 19 日 {#section_BC694D5AE16A4E16B44B353ED67947F3}

修正:

* 已改善帳戶布建的使用者電子郵件邀請工作流程。
* 修正 [!DNL Experience Cloud] 和 [!DNL Adobe Campaign] 資產無法顯示相同資料夾階層的資產資料夾問題。
* 修正無法刪除隸屬於已停用 [!DNL Target] 活動之受眾的問題。
* 修正「[!UICONTROL 建立新受眾]」頁面的「[!UICONTROL 規則]」下方無法顯示「新增」(加號) 圖示的問題。
* 已改善Internet Explorer 9的Experience Cloud介面支援。

## Release 15.1.1 - January 15 2015 {#section_F1A352E928AF432E94CC0A289C345184}

[!DNL Adobe Experience Cloud] 共同作業和共用介面中的新功能和修正。

<table id="table_AD0A8CA760E64227BB04BA6B0E425E80"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>唯讀存取。 </p> </td> 
   <td colname="col2"> <p>管理員現在可授予非管理使用者唯讀存取權。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 已修正此問題：無法在資訊卡上呈現PNG檔案。
* 修正透過拖放將檔案上傳至Experience Cloud資產的問題。

**已知問題**

* 使用者無法在展示板上共用PowerPoint檔案。
* 在「使用者管理」中所做的群組和權益變更，只有在新登入後才會生效。
* 有些使用者無法上傳大型檔案類型至 Experience Cloud 資產。
* 使用者的 Experience Cloud 卡片上未顯示來自 Media Optimizer 的連結。
* 有些管理員使用者在接受加入 Experience Cloud 的邀請後，無法順利連結帳戶。
* 多名使用者同時使用 Experience Cloud 介面時，會導致介面效能下滑。
* 有些使用者可以刪除過時資產，而不會收到錯誤通知。
* 有些使用者在同時使用相同Adobe ID登入兩個瀏覽器時可能會遇到問題。
* 刪除 Creative Cloud 使用者後，有些使用者無法重新新增該 Creative Cloud 使用者至共用資料夾。
* 從 Experience Cloud 共用資料夾至 Creative Cloud 時，有些使用者會遇到通知延遲的問題。
* 有些使用者在 Experience Cloud 和 Creative Cloud 之間共用資料夾時遇到問題。
* 共用的受眾已啟用後，有些使用者無法在 Analytics 報表套裝中建立受眾。
* 有些使用者無法將資產上傳至展示板。

## 發行版本14.11.1 - 2014年11月13日 {#section_A6CF1D4F27B9496892A89C983EB39102}

已知問題:

* 有些使用者可以刪除過時資產，而不會收到錯誤通知。
* 有些 [!DNL .png] 檔案無法呈現在資訊卡上。
* 有些使用者無法將資產上傳至展示板。
* 在使用者管理中所做的群組和權限變更，只有在重新登入後才會生效。
* 管理員必須登出並登入，才能查看「帳戶設定」中所做的變更。
* 使用者無法在展示板上共用 PowerPoint 檔案。
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，會導致介面效能下滑。
* Adobe Experience Manager與Creative Cloud同步無法運作。

## 發行版本14.10.1 - 2014年10月16日 {#section_E3A0F4423B814707AA3745E083500835}

[!DNL Adobe Experience Cloud] 共同作業和共用介面中的新功能和修正。

<table id="table_7C1ACE8108D54782AE128ACD35069DF5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>編輯使用者權限 </p> </td> 
   <td colname="col2"> <p>展示板的擁有者現在可以編輯特定展示板的使用者權限。 </p> <p> 
     <ol id="ol_B12251C510744538AF9BCE60ACB04016"> 
      <li id="li_87B3EDE9542B47CEBE0BE7F2D1DE844D">在展示板上，按一下<span class="uicontrol">「設定」</span>。 </li> 
      <li id="li_0F4786B0E1E743069D082E7DC488A031">在每一個擁有者旁，指定<span class="uicontrol">「擁有者」</span>、<span class="uicontrol">「檢視者」</span>或<span class="uicontrol">「編輯者」</span>。 </li> 
     </ol> </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 從PDF建立資訊卡並共用至展示板時，會傳回錯誤訊息。

**已知問題**

* 有些使用者無法將資產上傳至展示板。
* 有些 [!DNL .png] 檔案無法呈現在資訊卡上。
* 在使用者管理中所做的群組和權限變更，只有在重新登入後才會生效。
* 有些使用者可能無法從PDF建立資訊卡並將資訊卡分享至展示板。
* 有些使用者可以刪除過時資產，而不會收到錯誤通知。
* 使用者無法在展示板上共用 PowerPoint 檔案。
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，會導致介面效能下滑。
* 無法從「[!DNL Search&Promote]組織及產品存取」頁面使用  連結。

## 發行版本 14.9.1 - 2014 年 9 月 18 日 {#section_20F156A9CC2F4FC59C4970075C181D3A}

**修正和改良**

* 現在，當您導覽至 [!DNL experiencecloud.adobe.com] 時，您感受到的登入體驗將會與 Adobe Creative Cloud 的登入一致。
* 現在，在「管理組織」頁面上，每個解決方案的連結體驗（收到邀請後）都是一致的。

**已知問題**

* 在使用者管理中所做的群組和權限變更，只有在重新登入後才會生效。
* 有些使用者可能無法從PDF建立資訊卡並將資訊卡分享至展示板。
* 有些使用者無法將資產上傳至展示板。
* 有些使用者可以刪除過時資產，而不會收到錯誤通知。
* 使用者無法在展示板上共用 PowerPoint 檔案。
* 有些 [!DNL .png] 檔案無法呈現在資訊卡上。
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，會導致介面效能下滑。
* 無法從「[!DNL Search&Promote]組織及產品存取」頁面使用  連結。
* 如果在 [!DNL Creative Cloud] 中將 [!DNL Experience Cloud] 內容取消共用，該內容也可能會從某些使用者的資料夾中移除。

## 發行版本 14.8.1 - 2014 年 8 月 21 日 {#section_03BF00F6A95A490C91BCC0A1988FA7AA}

[!DNL Adobe Experience Cloud] 共同作業和共用介面中的新功能和修正。

<table id="table_1E7DBEB5E83B4E4285B6FD1D718CD16D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>您現在可從左側導覽存取 <span class="keyword">Adobe Mobile Services</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**已知問題**

* 在使用者管理中所做的群組和權限變更，只有在重新登入後才會生效。
* 有些使用者可能無法從PDF建立資訊卡並將資訊卡分享至展示板。
* 有些使用者無法將資產上傳至展示板。
* 有些使用者可能無法從 [!DNL Target] 登入 [!DNL Experience Cloud]。
* 有些 Audience Manager 的使用者無法登入 [!DNL Experience Cloud]。
* 有些使用者可以刪除過時資產，而不會收到錯誤通知。
* 從 [!DNL Experience Cloud] 中刪除的檔案並不會從 [!DNL Digital Asset Management] 中刪除。
* 使用者無法在展示板上共用 PowerPoint 檔案。
* 有些 [!DNL .png] 檔案無法呈現在資訊卡上。
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，會導致介面效能下滑。
* 無法從「[!DNL Search&Promote]組織及產品存取」頁面使用  連結。
* 如果在 [!DNL Creative Cloud] 中將 [!DNL Experience Cloud] 內容取消共用，該內容也可能會從某些使用者的資料夾中移除。

## 發行版本 14.7.1 - 2014 年 7 月 24 日 {#section_B22D4F830756463DB27BB4D508D9ADD5}

[!DNL Adobe Experience Cloud] 共同作業和共用介面中的新功能和修正。

**已知問題**

* 從 [!DNL Experience Cloud] 中刪除的檔案並不會從 [!DNL Digital Asset Management] 中刪除。
* 有些 [!UICONTROL Exchange] 使用者顯示在評論中的名稱是長字串 ID，而非其名稱
* 有些 [!DNL .png] 檔案無法呈現在資訊卡上
* 上傳檔案比拖放方法允許更多檔案類型。 為獲得最佳效果，請使用 [!UICONTROL Assets上傳]。
* 無法從「[!DNL Search&Promote]組織及產品存取」頁面使用  連結。
* [!DNL Exchange] 使用者必須清除 Cookie 才能獲得更好的使用體驗。
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，可能會導致介面速度變慢。
* 如果在 [!DNL Creative Cloud] 中將 [!DNL Experience Cloud] 內容取消共用，該內容也可能會從某些使用者的資料夾中移除。
* 15 分鐘無活動，系統就會將您登出。此外，您從某個位置登出後，系統會將您登出 [!DNL Experience Cloud].
* 有些使用者無法將其 Audience Manager 帳戶連結至 [!DNL Experience Cloud]。
* [!UICONTROL Exchange] 使用者在語言選擇器中只能看到英文。

**修正**

無可報告。

## 發行版本14.6.1 - 2014年6月19日 {#marketing_cloud_interface}

[!DNL Adobe Experience Cloud] 共同作業和共用介面中的新功能和修正。

**改進**

<table id="table_C9BD63436BF0414B97B8D07387D1993B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 「受眾」中的<span class="wintitle">「儲存」</span>按鈕 </p> </td> 
   <td colname="col2"> <p>現在，當您建立受眾時，<span class="wintitle">建立新受眾</span>頁面上的<span class="wintitle">儲存</span>按鈕要在您填妥所有必要欄位之後才會停用。 
      
     <!--MAC-19712 --></p> </td> 
  </tr> 
 </tbody> 
</table>

**已知問題**

* 從 [!DNL Experience Cloud] 中刪除的檔案並不會從 [!DNL Digital Asset Management] 中刪除。
* 上傳檔案比拖放方法允許更多檔案類型。 為獲得最佳效果，請使用「資產」上傳。
* 無法從「[!DNL Search&Promote]組織及產品存取」頁面使用  連結。
* 套用至 [!DNL Analytics] 趨勢報表的篩選器沒有套用至 [!DNL Experience Cloud] 中的卡片。
* 某些使用者無法將其受眾管理帳戶與 [!DNL Experience Cloud] 帳戶建立連結。
* 15 分鐘無活動，系統就會將您登出。此外，登出一個位置會將您登出Experience Cloud。
* 有些 Exchange 使用者顯示在評論中的名稱是長字串 ID，而非其名稱

**修正**

* 修正無法將視訊上傳至應用程式的問題。

## 發行版本 14.5.1 - 2014 年 5 月 22 日 {#section_7E22B2CB3ABA4D6EAED8CA8EFDE5433E}

<table id="table_4E4B34EEE3D94D78BA1A1FBC62950559"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud Exchange </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol">「Experience Cloud</span> &gt; <span class="uicontrol">說明</span> &gt; <span class="uicontrol">Exchange」</span></p> <p><span class="keyword">Experience Cloud</span><span class="wintitle">Exchange</span> 是可讓您透過應用程式來搜尋、瀏覽、選擇、支付及下載數位行銷擴展元件的多合一路徑。 </p> <p>應用程式包括 Data Connectors、Adobe 核心產品的設定自訂功能、第三方應用程式、報表，以及 <span class="keyword">Experience Cloud</span> 資訊卡。 </p> <p>請參閱 <a href="../exchange.md#concept_E07F16F070544B82B56527A845C41D59" format="dita" scope="local"> Exchange Marketplace</a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Experience Cloud 受眾 </p> </td> 
   <td colname="col2"> <p> <span class="uicontrol">「Experience Cloud</span> &gt; <span class="uicontrol">受眾」</span></p> <p> 您可以使用類似於處理區隔的方式，在<span class="wintitle">「受眾」</span>建立、編輯及管理受眾。例如，您可以在報表與分析中建立區隔，然後共用至 <span class="wintitle">「Experience Cloud </span><span class="wintitle">受眾」</span>。共用後，您便可將受眾用於 <span class="keyword">Adobe Target</span> 中的促銷活動以及 Adobe Audience Manager 中的區隔。 </p> <p> <p>附註: 若要提出 Target 啟用請求，請造訪 <a href="https://www.adobe.com/go/audiences" format="http" scope="external"> https://www.adobe.com/go/audiences</a>。 </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p><span class="keyword">Experience Cloud</span> 資訊卡上提及的使用者現在擁有該資訊卡的權限。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>新的Adobe使用者可將其Scene7帳戶連結至Adobe ID及其團隊成員。 管理員也可以將使用者與Scene7帳戶取消連結。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>資產同步。 </p> </td> 
   <td colname="col2"> <p> 您可以與Adobe Experience Cloud和Adobe Creative Cloud共用Adobe Experience Manager(AEM)Assets中的資產，如此對這些資產所做的任何變更都會反映在Adobe Experience Cloud和Adobe Creative Cloud中資產的共用副本中。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* [!DNL Experience Cloud] 未連結至 [!DNL Adobe Target]。如果可在多個 [!DNL Adobe Target] 伺服器上使用 [!DNL Target] 登入，則會發生此問題。
* 在 [!DNL Adobe Media Optimizer] 中建立使用者後，[!DNL Experience Cloud] 不會自動建立使用者。
* 在輸入時，組合方塊中用來新增使用者的選項會暫時消失。
* 無法點按資產卡片檢視上的「留言」連結。
* 將自訂標籤新增至資產後，不會有其他中繼資料變更持續存在。
* 刪除影像時，如果該影像用於 Adobe Target Essentials，則資產不會發出警告。
* 多名使用者同時使用 [!UICONTROL Experience Cloud] 介面時，會導致介面效能下降。
* 刪除 [!UICONTROL Experience Cloud 資產]中的影像時，如果該影像用於 [!DNL Adobe Target Essentials]，則系統不會發出警告。
* 登入期間未選取&#x200B;**[!UICONTROL 記住我]**&#x200B;時，使用者將在 15 分鐘後登出。
* 使用者必須先登出再登入，才能讓所有權限變更生效。
* 登入 [!DNL Experience Cloud] 的時間超過一秒鐘。
* 針對某些使用者，從 [!DNL Experience Cloud] 刪除檔案並不會與 [!DNL Digital Asset Management] 同步。
* 在瀏覽器未活動僅15分鐘後，使用者就被登出。
* 使用者無法在展示板上共用PowerPoint檔案。
* 有些使用者在Internet Explorer 10中的視覺版面配置比其他瀏覽器差。

## 發行版本 14.4.1 - 2014 年 4 月 22 日 {#section_E2A699764E744D2E8D418E9A3D40AF6B}

<table id="table_D95C0DC64F2A4B47BAC83E504CFD6825"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>從說明主題建立卡片 </p> </td> 
   <td colname="col2"> <p>在瀏覽器的「書籤」工具列中啟用「共用至Adobe Experience Cloud」功能後，您現在可以從微網站URL共用說明頁面。 </p> <p> <b>要共用幫助主題</b> </p> 
    <ol id="ol_F94B816121494B0FA16CC07B0E96AED8"> 
     <li id="li_F47187D4B5FE46D3A51D257DD569B4D6"> <p>在 <span class="keyword">Experience Cloud</span> 中，按一下<span class="uicontrol">「管理」</span>。 </p> </li> 
     <li id="li_94EF58E7A4974B63951E14F72A710183"> <p>將<span class="uicontrol">「共用至 Adobe Experience Cloud」</span>按鈕拖曳至「書籤」工具列。 </p> </li> 
     <li id="li_69EEC4F25D8F4AD7AA106A10B7F50FF6"> <p>導覽至說明頁面 (或停留在此頁面)，然後按一下瀏覽器「書籤」工具列的<span class="uicontrol">「共用至 Adobe Experience Cloud」</span>。 </p> <p>此步驟會建立一張卡片，供您在 <span class="wintitle">Experience Cloud</span> 中檢視。 </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 將自訂標籤新增至資產後，就不會保留其他中繼資料變更。
* 使用者必須重新整理展示板，才能讓已刪除的資訊卡從檢視中消失。
* 登入期間未選取&#x200B;**[!UICONTROL 記住我]**&#x200B;時，使用者將在 15 分鐘後登出
* [!DNL Analytics] 解決方案登陸頁面會顯示格式設定錯誤。
* 使用者必須先登出再登入，才能讓所有權限變更生效。
* 刪除影像時，如果該影像用於 [!UICONTROL ，則]資產[!DNL Adobe Target Essentials]不會發出警告。
* 無法點按資產卡片檢視上的「留言」連結。
* 在輸入時，組合方塊中用於新增使用者的選項會暫時消失。
* 登入 [!DNL Experience Cloud] 所需的時間超過一秒。
* 自 [!DNL Media Optimizer] 共用的資料在 [!DNL Experience Cloud] 中的呈現方式有誤。
* 在 [!DNL Media Optimizer] 中建立使用者後，Adobe [!DNL Experience Cloud] 不會自動建立使用者。
* 如果 [!DNL Experience Cloud] 登入資訊可用於多個 [!DNL Adobe Target] 伺服器，則無法將 [!DNL Adobe Target] 連結到 [!DNL Target]
* 多名使用者同時使用 [!DNL Experience Cloud] 介面時，可能會導致介面速度變慢。
* 無法從[!UICONTROL 組織及產品存取]頁面使用 [!DNL Search&Promote] 連結。
* [!DNL Adobe Media Optimizer] 模擬卡片未正確呈現。
* 套用至 [!DNL Analytics] 趨勢報表的篩選器沒有套用至 [!DNL Experience Cloud] 中的卡片。
* 套用至 Analytics 趨勢報表的篩選器沒有套用至 Experience Cloud 中的卡片。
* 無法將某些 Excel 或 CSV 檔案上傳到留言板。
* 某些使用者可能無法將其受眾管理帳戶與 [!DNL Experience Cloud] 帳戶建立連結。
* 有些使用者在 [!DNL Analytics] 中共用 [!DNL Experience Cloud] 區段時遇到錯誤。
* 有些使用者無法深入檢視 [!UICONTROL Asset Selector] 的子資料夾。
* 某些使用者無法分享 [!DNL Experience Cloud] 中的 AdLens 小工具。

## 發行版本 14.3.1 - 2014 年 3 月 13 日 {#section_5D142E3225E3477A84DC01B8197D39BC}

14.3.1版是維護髮行，主要針對速度、穩定性和安全性。 它不包含主要的新功能。

**修正**

* 新增移除頭像影像的功能。
* 修正讓您無法取消連結 [!DNL Adobe Media Optimizer] 帳戶的問題。

**已知問題**

* 如果Adobe Target Essentials使用Experience Cloud資產中的影像，刪除影像不會發出警告。
* 從 [!DNL Analytics] 重新整理卡片有時會導致擴充卡片出現空白圖表。
* 使用者必須先登出再登入，才能讓所有權限變更生效。
* 若未於登入期間選取 *`Remember me`*，系統會在 15 分鐘後將使用者登出。
* [!DNL Analytics] 解決方案登陸頁面會顯示格式設定錯誤。
* 無法點按資產卡片檢視上的「註解」連結。
* 當許多使用者同時使用Experience Cloud介面時，其速度可能會變慢
* 如果 [!DNL Adobe Target] 登入資訊可用於多個 Target 伺服器，則無法將 Experience Cloud 連結到 [!DNL Adobe Target]
* 登入Experience Cloud需要超過一秒的時間。
* 將自訂標籤新增至資產後，就不會保留其他中繼資料變更。
* 在 Experience Cloud 中建立使用者後，[!DNL Adobe Media Optimizer] 不會自動建立使用者。
* 在輸入時，組合方塊中用於新增使用者的選項會暫時消失。
* 自 [!DNL Media Optimizer] 共用的資料在 Experience Cloud 中的呈現方式有誤。
* 無法分享 Flickr 影像。
* 套用至 [!DNL Analytics] 趨勢報表的篩選器沒有套用至 Experience Cloud 中的卡片。
* 在使用者管理中所做的群組和權限變更，只有在重新登入後才會生效。
* 無法從[!DNL Search&Promote]「組織和產品存取」[!UICONTROL 使用 ] 連結。
* 使用者必須重新整理展示板，才能讓已刪除的資訊卡從檢視中消失。
* 無法將某些 Excel 或 CSV 檔案上傳到留言板。
* [!DNL Adobe Media Optimizer] 模擬卡片未正確呈現。
* 某些PNG檔案無法轉譯在卡片上。
* 無法提交測試版意見回應。

## Release 14.2.1 - February 24 2014 {#section_5AD81B0737C843AFB4BE9C4420D70EB3}

<table id="table_DFAB002358C94A17A7F91DAB323A488F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 功能 </th> 
   <th colname="col2" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>OEmbed </p> </td> 
   <td colname="col2"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>重新整理資料 </p> </td> 
   <td colname="col2"> <p> 
     <!--MAC-18174-->如果解決方案不允許重新整理資料，現在會隱藏卡片上圖形的<span class="uicontrol">「重新整理資料」</span>圖示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**修正**

* 修正分享的 [!DNL Analytics] 報表無法套用區隔篩選器的問題。
* 修正在並未連結解決方案帳戶的情況下，解決方案在[!UICONTROL 「Experience Cloud 解決方案」]頁面上卻顯示為已連結的問題。
* 修正 [!DNL Adobe Target] 亞洲客戶無法點按連結頁面上&#x200B;**[!UICONTROL 「繼續前往 Experience Cloud」]**&#x200B;按鈕的問題。
* 修正無法分享 Youtube 影片的問題。
