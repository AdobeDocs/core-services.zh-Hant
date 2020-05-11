---
description: 將客戶屬性上傳至Experience Cloud的概述和必要條件。
keywords: core services;Customer Attributes
seo-description: 將客戶屬性上傳至Experience Cloud的概述和必要條件。
seo-title: 客戶屬性
solution: Experience Cloud
title: 客戶屬性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: tm+mt
source-git-commit: 75d3d045964aa42f7ac6b32b25cfd77aa7f663a9
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 16%

---


# 客戶屬性

導覽至 **[!DNL Experience Platform]** >人 **[!UICONTROL 員]** >客 **[!UICONTROL 戶屬性]**

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

![](assets/custom_reports.png)

## 上傳客戶屬性的先決條件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **解決方案啟用：** [啟用您的Experience Platform服務解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **群組成員資格：** 要上載客戶屬性資料，用戶必須是「客戶屬性」組 [的成員](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。 您也必須屬於Adobe Analytics群組或Adobe Target群組。

   To know whether your company has access to Customer Attributes, your [!DNL Experience Cloud] administrator should log into the [Experience Cloud](https://experience.adobe.com). 導覽至「 **[!UICONTROL 管理]** >管 **[!UICONTROL 理控制台]** > **[!UICONTROL 產品]**」。 If *Customer Attributes* displays as one of the [!UICONTROL Product Profiles], you are ready to begin.

   Users that are added to the Customer Attributes will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

* **客戶屬性** 需要Adobe Target [!DNL at.js] （任何版本）或 [!DNL mbox.js] 58版或更新版本。

   請參 [閱如何部署at.js](https://docs.adobe.com/content/help/en/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.html) 或 [Mbox.js實施](https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

## What is enterprise customer data? {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業資料位於其他系統。 它可以是複雜的，對不同的人來說，有不同的意義。 此資料可包含會籍、忠誠度、年齡、性別、擁有的產品、興趣和期限值等資訊。

下圖是資料檔案的範例，顯示產品的訂閱者資料，包括成員ID、已授權的產品、最常啟動的產品等。

![](assets/01_crs_usecase.png)

After you create the data file, you can upload it to the customer attribute source that you create in **[!UICONTROL Experience Cloud]** > **[!UICONTROL Customer Attributes]**.

請參閱[上傳客戶屬性資料](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)以瞭解此工作流程。

## 解決方案使用個案 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

資料駐留在Experience Cloud中後，您就可以自訂資料，並將它共用給報告、細分、活動和促銷活動的解決方案。

例如:

| 解決方法 | 優點和使用案例 |
|--- |--- |
| Adobe Analytics  | 行銷人員和分析師可以瞭解：<ul><li>對金級客戶最有效的線上促銷活動。</li><li>金級客戶所搜尋的產品與白金級客戶所搜尋的產品。</li><li>網站重新設計是否對舊客戶的轉換率有正面影響。</li><li>低存留值的客戶會在我的網站上研究哪些產品。</li></ul> |
| Adobe Target | 屬性資料可讓Adobe Target使用者：<ul><li>顯示忠誠會籍會員的特別折扣和優惠。</li><li>向您的奢侈品客戶推薦更昂貴的產品。</li><li>對於已收到電子郵件的客戶，請在通常保留給電子郵件註冊的空間顯示向上銷售優惠</li></ul> |
