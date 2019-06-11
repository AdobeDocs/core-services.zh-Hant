---
description: 建立客戶屬性來源及上傳資料。
keywords: 客戶屬性；核心服務
seo-description: 建立客戶屬性來源及上傳資料。
seo-title: 建立客戶屬性來源及上傳資料檔案
solution: Experience Cloud
title: 建立客戶屬性來源及上傳資料檔案
uuid: 53dca 7899-a91-4385-839d-c9 d1 aa36 b9
translation-type: tm+mt
source-git-commit: b6058194725c3ad50d280a3daad737cd53416204

---


# 建立客戶屬性來源及上傳資料檔案

建立客戶屬性來源及上傳資料。您可以在準備好時啓動資料來源。資料來源生效後，將屬性資料共用給 Analytics 和 Target。

## 客戶屬性工作流程 {#concept_BF0AF88E9EF841219ED4D10754CD7154}

![](assets/crs.png)

1. [建立資料檔案](../attributes/t-crs-usecase.md#task_B5FB8C0649374C7A94C45DCF2878EA1A)
1. [建立屬性來源及上傳資料檔案](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [驗證結構](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)
1. [設定訂閱及啟動屬性來源](../attributes/t-crs-usecase.md#task_1ACA21198F0E46A897A320C244DFF6EA)


啟動資料來源後，您可以:

* [在 Adobe Analytics 中使用客戶屬性](../attributes/t-crs-usecase.md#task_7EB0680540CE4B65911B2C779210915D)
* [在 Adobe Target 中使用客戶屬性](../attributes/t-crs-usecase.md#task_FC5F9D9059114027B62DB9B1C7D9E257)



>[!IMPORTANT]
>
>若要存取此功能，使用者必須指派給客戶屬性產品設定檔(客戶屬性-預設存取權)。( **[!UICONTROL 管理]** &gt; **[!UICONTROL 管理控制台]** &gt; **[!UICONTROL 使用者]** &gt;)。加入客戶屬性群組的使用者可在 Experience Cloud 介面左側的[!UICONTROL 「受眾」]中，看到[!UICONTROL 「客戶屬性」]功能表項目。
>
>另外也需要解決方案群組成員資格。

若要使用「客戶屬性」功能，使用者必須在使用者管理中隸屬於「Adobe 客戶屬性」群組以及解決方案等級的群組 (Analytics 或 Target)。

請參閱[使用者和群組](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。

## 建立資料檔案 {#task_B5FB8C0649374C7A94C45DCF2878EA1A}

此資料是自您的 CRM 那裡取得的企業客戶資料。資料可能包含產品的訂閱者資料，包括成員 ID、有權限的產品、最常啟動的產品等等。


1. 建立 [!DNL .csv].


   >[!NOTE]
   >
   >在此程序稍後，您將拖放以 [!DNL .csv] 上傳檔案。不過，如果您 [透過FTP](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)上傳，則您也需要同名 [!DNL .fin] 的檔案 [!DNL .csv]。



   企業客戶資料檔案範例:

   ![](assets/01_crs_usecase.png)

1. 繼續之前，請先檢閱 [「資料檔案需求」](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)中的重要資訊，然後再上傳檔案。
1. [建立客戶屬性來源並上傳資料](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)，如下所述。

## 建立屬性來源及上傳資料檔案 {#task_09DAC0F2B76141E491721C1E679AABC8}

在 Experience Cloud 的「建立新客戶屬性來源」頁面執行這些步驟。


>[!IMPORTANT]
>
>建立、修改或刪除客戶屬性來源時，會延遲一小時，ID開始與新資料來源同步。您必須擁有Audience Manager中的管理權限才能建立或修改客戶屬性來源。聯絡Audience Manager客戶服務或諮詢以取得管理權限。


1. 在此 [!DNL Experience Cloud]中，按一下「功能表 ![](assets/menu-icon.png) 」圖示。
1. 按一下 **[!UICONTROL 「人員]**」，然後按一下 **[!UICONTROL 「客戶屬性]**」。

   您可以在[!UICONTROL 「客戶屬性」]頁面管理及編輯現有屬性資料來源。

   ![步驟結果](assets/03_crs_usecase.png)
1. 按一下 **[!UICONTROL 「新增]**」。

   ![步驟結果](assets/04_crs_usecase.png)
1. 在[!UICONTROL 「編輯客戶屬性來源」]頁面，設定以下欄位:


   * **[!UICONTROL 名稱：]** 資料屬性來源的好記名稱。對於 [!DNL Adobe Target]，屬性名稱不能包含空格。如果傳遞含有空格的屬性，請 [!DNL Target] 忽略它。其他不支援的字元包括: `< , >, ', "`.

   * **[!UICONTROL 說明：]** (可選)資料屬性來源的說明。

   * **[!UICONTROL 別名ID：]** 代表客戶屬性資料的來源，例如特定CRM系統。唯一 ID 用於客戶屬性來源代碼。此 ID 應是唯一、小寫、無空格。在 Experience Cloud 使用者介面的「別名 ID」欄位輸入的客戶屬性來源值，應與從實作傳入的值 (不論是透過動態標籤管理或行動 SDK 的 JavaScript 傳入) 相符。

      別名 ID 要符合您設定額外客戶 ID 值的特定區域。例如:

      * **動態標籤管理：** 別名ID與「客戶設定」下的 ** 「 [!UICONTROL 客戶設定]」下的「整合 [代碼」值相符](https://marketing.adobe.com/resources/help/en_US/dtm/?f=macid) 。

      * **訪客 API:** 別名 ID 要符合可用來與每位訪客關聯的額外[客戶 ID](https://marketing.adobe.com/resources/help/en_US/mcvid/?f=mcvid_customer_ids)。

         例如， *「crm_ id」* in：


         ```
         "crm_id":"67312378756723456"
         ```


      * **iOS：** 別名ID對應至visitorSyncIdentifiers中的 *「idType」*[：識別碼](https://marketing.adobe.com/resources/help/en_US/mobile/ios/?f=methods)。

         例如:

         `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`


      * **Android:** 別名 ID 要符合*SyncIdentifiers* 中的「 [idType」](https://marketing.adobe.com/resources/help/en_US/mobile/android/?f=methods)。

         例如:

         `identifiers.put(`**`"idType"`**`, "idValue");`

         有關「別名ID」欄位和客戶ID的資料處理相關資訊，請參閱 [運用多個資料來源](../attributes/crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB) 。
   * **[!UICONTROL 檔案上傳：]** 您可以拖放 [!DNL .csv] 資料檔案，或透過FTP上傳資料。(使用FTP也需要 [!DNL .fin] 檔案)。請參閱 [透過FTP上傳資料](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。


      >[!IMPORTANT]
      >
      >特定資料檔案需求存在。如需詳細資訊，請參閱 [資料檔案需求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) 。


      上傳檔案後，會在此頁面的[!UICONTROL 「檔案上傳」]標題下顯示表格資料。您可以驗證結構、設定訂閱或設定 FTP。



      **檔案上傳圖形**

      ![](assets/file_upload_attributes.png)

   * **[!UICONTROL 唯一客戶ID：]** 顯示您上傳至此屬性來源的唯一ID。

   * **[!UICONTROL 別名為Experience Cloud訪客ID別名的客戶提供ID：]** 顯示有多少ID已別名至Experience Cloud訪客ID。

   * **[!UICONTROL 具有高別名數的客戶提供ID：]** 顯示客戶提供ID的計數(超過500個或更多別名Cloud訪客ID)。這些客戶提供的 ID 很可能不代表個人，而是某種共用的登入。系統會將與這些 ID 關聯的屬性發送給 500 個最近設別名的 Experience Cloud 訪客，直到別名數到達 10,000。到時候，系統會令客戶提供的 ID 失效，並不再發送關聯的屬性。










## 驗證結構 {#task_404AAC411B0D4E129AB3AC8B7BE85859}

驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。您也可以更新結構，以刪除屬性。

請參閱 [驗證結構](../attributes/validate-schema.md#concept_B3A01A15D04E4F998118E09B3A9B5043)。

若要刪除屬性，請參閱 [(選擇性)更新結構(刪除屬性)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

## (可選)更新結構(刪除屬性) {#task_6568898BB7C44A42ABFB86532B89063C}

如何在結構中刪除屬性並取代屬性。


1. 在 [!UICONTROL 「編輯客戶屬性來源」] 頁面上，移除 **[!UICONTROL Target]** 或 **[!UICONTROL Analytics]** 訂閱( [!UICONTROL 在「設定訂閱]」下)。
1. [上傳含有更新欄位](../attributes/t-crs-usecase.md#task_09DAC0F2B76141E491721C1E679AABC8)的新資料檔案。

## 設定訂閱及啟動屬性來源 {#task_1ACA21198F0E46A897A320C244DFF6EA}

設定訂閱可使得資料在 Experience Cloud 和解決方案之間流通。啟動屬性來源可讓資料流向訂閱的解決方案。您上傳的客戶記錄將與從您的網站或應用程式傳入的 ID 訊號比對。

請參閱 [設定訂閱](../attributes/subscription.md#concept_ECA3C44FA6D540C89CC04BA3C49E63BF)。

**啟動屬性來源**

在[！UICCOHTROL建立新 [或編輯] 客戶屬性來源]頁面、找出 [!UICONTROL 啓動] 標題，然後按一下 **[!UICONTROL 「活動]**」。

![步驟結果](assets/activate_attribute_source.png)

## 在 Adobe Analytics 中使用客戶屬性 {#task_7EB0680540CE4B65911B2C779210915D}

現在，您可以使用
<keyword>
Adobe Analytics
</keyword>您可以報告資料、分析資料，並在行銷活動中採取適當的動作。

以下範例示範以上傳屬性為依據的 [!DNL Analytics] 區隔。此區隔顯示 Photoshop Lightroom 的訂閱者中最常啟動 Photoshop 產品的人。

![](assets/08_crs_usecase.png)

當您將區段發佈至Experience Cloud時，它會在Experience Cloud觀眾和Audience Manager中提供。

如需詳細資訊，請參閱 Analytics 說明中的[客戶屬性報告](https://marketing.adobe.com/resources/help/en_US/reference/?f=reports_customer_attributes)。

## 在 Adobe Target 中使用客戶屬性 {#task_FC5F9D9059114027B62DB9B1C7D9E257}

在 Target 中，您可在建立受眾時，從「訪客資料」區段選取客戶屬性。所有客戶屬性都將包含清單 [!DNL crs.] 中的首碼。視需要將這些屬性與其他資料屬性結合，以建立受眾。

![](assets/crs-add-attribute-target.png)

請參閱 Target 說明中的[建立新受眾](https://marketing.adobe.com/resources/help/en_US/target/target/?f=t_creating_a_new_audience)。
