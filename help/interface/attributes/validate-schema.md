---
description: 驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。會根據這些設定來建立結構。 此架構用於驗證將來上傳至此資料來源的所有資料。 此映射過程不會更改原始資料。
keywords: customer attributes;core services
seo-description: 驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。會根據這些設定來建立結構。 此架構用於驗證將來上傳至此資料來源的所有資料。 此映射過程不會更改原始資料。
seo-title: 驗證結構
solution: Experience Cloud
title: 驗證結構
uuid: 163a4dbe-d60b-4089-8ff8-65f7461fbdf7
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 驗證結構

驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。會根據這些設定來建立結構。 此架構用於驗證將來上傳至此資料來源的所有資料。 此映射過程不會更改原始資料。

>[!NOTE]
>
>在驗證後更新結構會刪除客戶屬性。請參閱[更新結構 (也會刪除屬性)](../attributes/t-crs-usecase.md#task_6568898BB7C44A42ABFB86532B89063C)。

**[!UICONTROL 客戶屬性來源]** >建 **[!UICONTROL 立新客戶屬性來源]** >檢 **[!UICONTROL 視／編輯結構]**

![](assets/view_edit_schema.png)

在[!UICONTROL 「驗證結構」]頁面，結構的每一列代表上傳之 CSV 檔案的一欄。

![](assets/06_crs_usecase.png)

* **[!UICONTROL 新增資料:]** 可讓您上傳新的屬性資料至此資料來源。

* **[!UICONTROL 檢視/編輯結構:]** 將顯示名稱對應至屬性資料，如下一個步驟所述。

* **[!UICONTROL FTP 設定:]**[ 透過 FTP 上傳資料](../attributes/t-upload-attributes-ftp.md#task_591C3B6733424718A62453D2F8ADF73B)。

* **[!UICONTROL ID 查閱:]** 輸入您的 `.csv` 中的客戶 ID (CID) 以查閱該 ID 的 Experience Cloud 資訊。在疑難排解訪客的屬性資料為何沒有顯示時，此功能很實用:

   * **[!UICONTROL ECID(Experience Cloud ID):]** 顯示您是否使用最新的Experience Cloud ID服務。 如果您在MCID服務上，但此處未列出ID，則Experience Cloud尚未收到該CID的別名。 這表示訪客還沒登入，或您的實作沒有傳遞該 ID。

   * **[!UICONTROL CID (客戶 ID):]** 與此 CID 關聯的屬性。如果您使用 prop 或 eVar 上傳 CID (AVID)，有看到屬性顯示但沒有 AVID，這表示訪客尚未登入您的網路。

   * **[!UICONTROL AVID (Analytics 訪客 ID):]** 顯示您是否使用 prop 或 eVar 上傳 CID。如果這些ID正傳遞至Experience Cloud，則此處會顯示與您輸入的CID相關的任何訪客ID。

在Experience Cloud中建立客戶屬性來源和FTP帳戶後，您也可以透過FTP上傳資料。 您會為每個屬性來源建立一個FTP帳戶。 上傳的檔案會儲存在該帳戶的根資料夾中。 資料必須為。csv格式，並有第二個。fin檔案，以指出上傳完成

您套用至字串、整數、數字的名稱是用於建立 [!DNL Analytics] 度量。如需詳 [細資訊，請參閱說](https://docs.adobe.com/help/en/analytics/components/variables/dimensions-reports/reports-customer-attributes.html)[!DNL Analytics] 明中的客戶屬性報表。

* **[!UICONTROL 屬性:]** 從上傳之 `.csv` 檔案讀取的屬性資料。

* **[!UICONTROL 類型:]** 資料類型，例如:

   * **字串：** 字元順序。

   * **整數：** 全數。

   * **數字：** 最多可以有兩位小數。

* **[!UICONTROL 顯示名稱:]** 好記的屬性名稱。例如，您可能會將&#x200B;*客戶年齡*&#x200B;屬性變更為&#x200B;*客戶加入時間*。

* **[!UICONTROL 說明:]** 好記的屬性說明。
