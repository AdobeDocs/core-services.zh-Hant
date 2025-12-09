---
description: 瞭解如何建立 [!DNL Customer Attributes] 資料來源並將其上傳至Experience Cloud。
solution: Experience Cloud
title: 建立及上傳 [!DNL Customer Attributes] 資料Source檔案
uuid: 53dca789-9a91-4385-839d-c9d1aa36b9be
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 21ed7c35-aac9-46f1-a50c-84e7c075209c
source-git-commit: 63d5c080a7282c78eb7a66c5a54c69b5597545ab
workflow-type: tm+mt
source-wordcount: '1063'
ht-degree: 45%

---

# 建立及上傳客戶屬性資料

建立客戶屬性來源（`.csv`和`.fin`個檔案）並上傳資料。 您可以在準備就緒後啟動資料來源。資料來源使用中後，將屬性資料共用至[!DNL Analytics]和[!DNL Target]。

**[!DNL Customer Attributes]工作流程**

![客戶屬性工作流程](assets/crs.png)

## 尋找[!DNL Customer Attributes]

在[!DNL Experience Cloud]中，按一下&#x200B;**[!UICONTROL Apps]** ![功能表](assets/menu-icon.png) > **[!DNL Customer Attributes]**。

## 使用[!DNL Customer Attributes]的必要條件

* **群組成員資格：**&#x200B;若要上傳資料，使用者必須是[!DNL Customer Attributes]群組的成員。 您也必須先加入 Adobe Analytics 群組或 Adobe Target 群組。

  若要知道您的公司是否具有客戶屬性的存取權，您的[!DNL Experience Cloud]管理員應登入[Experience Cloud](https://experience.adobe.com)。 導覽至&#x200B;**[!UICONTROL Admin Console]** > **[!UICONTROL Products]**。 如果&#x200B;*[!DNL Customer Attributes]*&#x200B;顯示為其中一個[!UICONTROL product profiles]，表示您已準備開始。

  新增至[!DNL Customer Attributes]的使用者可在Experience Cloud介面的左側看到[!DNL Customer Attributes]功能表專案。

* 客戶屬性需要 **Adobe Target** `at.js` (任何版本) 或 `mbox.js` 58 版或更新版本。

  參閱「[如何部署 at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html)」。

## 建立資料檔案

此資料是來自您 CRM 的企業客戶資料。資料可能包含產品的訂閱者資料，包括成員 ID、已授權產品、最常啟動的產品等。

1. 建立`.csv`檔案。

   >[!NOTE]
   >
   >在程式後面的步驟中，您需拖放`.csv`檔案以上傳檔案。 不過，如果您[透過 FTP 上傳](t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)，則另外還需要一個與 `.csv` 同名的 `.fin` 檔案。

   企業客戶資料檔案範例：

   ![企業客戶資料檔案範例](assets/01_crs_usecase.png)

1. 繼續進行之前，請先檢閱[資料檔案需求](crs-data-file.md)中的重要資訊，然後再上傳檔案。
1. [建立客戶屬性來源及上傳資料](t-crs-usecase.md#create-source)，如下所述。

## 建立屬性來源及上傳資料檔案

在Experience Cloud的[!UICONTROL Create Customer Attribute Source]頁面上執行這些步驟。

>[!IMPORTANT]
>
>建立、修改或刪除客戶屬性來源時，會有最長達一小時的延遲，之後 ID 就會開始與新資料來源同步。您在 Audience Manager 中必須有管理權限，才能建立或修改客戶屬性來源。聯絡Audience Manager客戶服務或洽詢如何取得管理許可權。

1. 在[!DNL Experience Cloud]中，按一下&#x200B;**[!UICONTROL Apps]** ![功能表](assets/menu-icon.png) > **[!DNL Customer Attributes]**。

   ![客戶屬性頁面](assets/cust-attr.png)

1. 按一下「**[!UICONTROL New]**」。

   ![步驟結果](assets/new-customer-attribute-source.png)

1. 在[!UICONTROL Create Customer Attribute Source]頁面上，設定下列欄位：

   * **[!UICONTROL Name:]**&#x200B;好記的資料屬性來源名稱。 若為 [!DNL Adobe Target]，屬性名稱不得包含空格。如果傳遞了包含空格的屬性，[!DNL Target] 會忽略該屬性。其他不支援的字元包括：`< , >, ', "`.

   * **[!UICONTROL Description:]** （選用）資料屬性來源的說明。

   * **[!UICONTROL Alias ID:]**&#x200B;代表客戶屬性資料的來源，例如特定的CRM系統。 [!UICONTROL Alias ID]是在您的[!UICONTROL customer attribute Source]程式碼中使用的唯一識別碼。 此 ID 應是唯一、小寫、無空格。在Experience Cloud中，針對客戶屬性來源在[!UICONTROL Alias ID]欄位中輸入的值，應與從實作傳入的值相符(不論是透過Platform Data Collection還是Mobile SDK的JavaScript)。

     >[!IMPORTANT]
     >
     >刪除與別名ID相關聯的資料來源時，別名ID將無法使用，因為別名ID會儲存在多個服務中，並用於在多個服務之間對應設定檔。

     別名ID會對應至您設定其他客戶ID值的特定區域。 例如：

      * **標籤：**&#x200B;別名ID對應至&#x200B;*Experience Cloud ID服務*&#x200B;工具中[!UICONTROL customer Settings]底下的[整合代碼](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)值。

      * **訪客API：**&#x200B;別名ID對應至您可與每個訪客建立關聯的其他[客戶ID](https://experienceleague.adobe.com/docs/id-service/using/reference/authenticated-state.html)。

        例如，下列位置中的&#x200B;*「crm_id」*：

        ```
        "crm_id":"67312378756723456"
        ```

      * **iOS：**&#x200B;別名識別碼對應至&#x200B;*visitorSyncIdentifiers*[中的:identifiers&quot;idType&quot;](https://experienceleague.adobe.com/docs/mobile-services/ios/overview.html?lang=zh-Hant)。

        例如：

        `[ADBMobile visitorSyncIdentifiers:@{@<`**`"idType"`**`:@"idValue"}];`

      * **Android™：** 別名 ID 對應至 [syncIdentifiers](https://experienceleague.adobe.com/docs/mobile-services/android/overview.html?lang=zh-Hant) 中的 *&quot;idType&quot;*。

        例如：

        `identifiers.put(`**`"idType"`**`, "idValue");`

        請參閱[運用多個資料來源](crs-data-file.md#section_76DEB6001C614F4DB8BCC3E5D05088CB)，以瞭解別名ID欄位和客戶ID的資料處理相關資訊。

   * **[!UICONTROL Namespace Code:]**&#x200B;在AEP WebSDK實作中使用[IdentityMap](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/identity/overview)時，使用此值來識別客戶屬性來源。

1. 按一下「**[!UICONTROL Save]**」。

## 上傳檔案

客戶屬性記錄已建立，您可以編輯客戶屬性來上傳檔案。

1. 在[!DNL Customer Attributes]頁面上，按一下屬性來源。

1. 在[!UICONTROL Edit Customer Data Source]頁面上，按一下&#x200B;**[!UICONTROL File Upload]**。

   ![檔案上傳和結構描述驗證](assets/file-upload-schema-validation.png)

1. 將`.csv`或`.zip`或`.gzip`資料檔案拖放至拖放視窗中。

>[!IMPORTANT]
>
>需符合特定的資料檔案需求。如需詳細資訊，請參閱[資料檔案需求](crs-data-file.md)。

上傳檔案後，表格資料會顯示在此頁面的[!UICONTROL File Upload]標題下。 您可以驗證結構、設定訂閱或設定 FTP。

![屬性](assets/file_upload_attributes.png)

* **[!UICONTROL Unique customer ID:]**&#x200B;顯示您上傳多少個唯一ID至此屬性來源。

* **[!UICONTROL customer-Provided IDs Aliased to Experience Cloud Visitor IDs:]**&#x200B;顯示有多少個ID已將別名傳送至Experience Cloud訪客ID。

* **[!UICONTROL customer-Provided IDs with High Alias Counts:]**&#x200B;顯示已將500個或更多別名傳送至Experience Cloud訪客ID之客戶提供的ID計數。 這些客戶提供的 ID 很可能不代表個人，而代表某種共用登入名稱。系統會將與這些 ID 相關的屬性分配給最近設定別名的 500 個 Experience Cloud 訪客 ID，直到別名數達到 10,000 個。到時候，系統會令客戶提供的ID失效，並不再傳送關聯的屬性。—>

## 驗證結構

驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。您也可以更新結構以刪除屬性。

請參閱[驗證結構](validate-schema.md)。

若要刪除屬性，請參閱 [(選用) 更新結構 (刪除屬性)](t-crs-usecase.md)。

## (選用) 更新結構 (刪除屬性)

如何在結構中刪除屬性及取代屬性。

1. 在[!UICONTROL Edit Customer Attribute Source]頁面上，移除&#x200B;**[!UICONTROL Target]**&#x200B;或&#x200B;**[!UICONTROL Analytics]**&#x200B;訂閱（在&#x200B;**[!UICONTROL Configure Subscriptions]**&#x200B;底下）。

1. [上傳含有更新欄位的新資料檔案](t-crs-usecase.md)。

## 設定訂閱及啟動屬性來源

設定訂閱可設定Experience Cloud和應用程式之間的資料流。 啟用屬性來源可讓資料流向已訂閱的應用程式。 您上傳的客戶記錄會與您網站或應用程式傳入的 ID 訊號相符。

請參閱[設定訂閱及啟用資料來源](subscription.md)。

## 在Adobe Analytics中使用[!DNL Customer Attributes]資料

現在有了 Adobe Analytics 等應用程式所提供的資料，您就可以彙整資料報表、分析資料，並在行銷活動中採取適當的行動。

以下範例示範以上傳屬性為依據的 [!DNL Analytics] 區隔。此區段顯示最常啟動 Photoshop 產品的 [!DNL Photoshop Lightroom] 訂閱者。

![根據上傳的屬性的 Analytics 區段](assets/08_crs_usecase.png)

您將區段發佈至Experience Cloud後，Experience Cloud Audiences和Audience Manager可隨即使用該區段。

## 在Adobe Target中使用[!DNL Customer Attributes]資料

在[!DNL Target]中，您可在建立對象時，從[!UICONTROL Visitor Profile]區段選取客戶屬性。 清單中的所有客戶屬性都有前置詞`crs.`。 您可視需求將這些屬性與其他資料屬性結合，以建立客群。

![在 Adobe Target 中使用客戶屬性](assets/crs-add-attribute-target.png)

請參閱[說明中的](https://experienceleague.adobe.com/docs/target/using/audiences/create-audiences/audiences.html??lang=zh-Hant)建立對象[!DNL Target]。
