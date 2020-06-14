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
ht-degree: 71%

---


# 客戶屬性

導覽至 **[!DNL Experience Platform]** >人 **[!UICONTROL 員]** >客 **[!UICONTROL 戶屬性]**

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

![](assets/custom_reports.png)

## 上傳客戶屬性的先決條件 {#section_BD38693AFBF34926BA28E964963B4EA0}

* **解決方案啟用：** [啟用您的Experience Platform服務解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **群組成員資格：** 要上載客戶屬性資料，用戶必須是「客戶屬性」組 [的成員](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。 您也必須屬於 Adobe Analytics 群組或 Adobe Target 群組。

   To know whether your company has access to Customer Attributes, your [!DNL Experience Cloud] administrator should log into the [Experience Cloud](https://experience.adobe.com). Navigate to **[!UICONTROL Administration]** > **[!UICONTROL Admin Console]** > **[!UICONTROL Products]**. If *Customer Attributes* displays as one of the [!UICONTROL Product Profiles], you are ready to begin.

   Users that are added to the Customer Attributes will see the [!UICONTROL Customer Attributes] menu item on the left side of the Experience Cloud interface.

* **客戶屬性** 需要Adobe Target [!DNL at.js] （任何版本）或 [!DNL mbox.js] 58版或更新版本。

   請參閱[如何部署at.js](https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/client-side/deploy-at-js/how-to-deployatjs.translate.html) 或 [Mbox.js 實作](https://docs.adobe.com/content/help/zh-Hant/target/using/implement-target/client-side/mbox-implement/mbox-download.html)。

## 什麼是企業客戶資料？ {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業資料位於其他系統中。這些資料可能很複雜，而且對不同的人來說有不同的意義。此資料可包含成員資格、忠誠度、年齡、性別、擁有的產品、興趣和終身價值等資訊。

下圖是資料檔案的範例，顯示產品的訂閱者資料，包括成員 ID、已授權產品、最常啟動的產品等。

![](assets/01_crs_usecase.png)

建立資料檔案後，可將其上傳至您在 **[!UICONTROL Experience Cloud]** > **[!UICONTROL 客戶屬性]**&#x200B;中建立的客戶屬性來源。

請參閱[上傳客戶屬性資料](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)以瞭解此工作流程。

## 解決方案使用個案 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

資料傳入 Experience Cloud 後，您就可以自訂資料，並共用至解決方案以用於報表、細分、活動和行銷活動。

例如：

| 解決方法 | 優點和使用案例 |
|--- |--- |
| Adobe Analytics  | 行銷人員和分析師可以瞭解：<ul><li>對金級客戶最有效的線上行銷活動。</li><li>金級客戶所搜尋的產品與白金級客戶所搜尋的產品比較。</li><li>網站重新設計是否對舊客戶的轉換率帶來正面影響。</li><li>終身價值低的客戶會在我的網站上研究哪些產品。</li></ul> |
| Adobe Target | 屬性資料可讓 Adobe Target 使用者：<ul><li>顯示忠誠俱樂部會員的特別折扣和優惠方案。</li><li>向您的高消費力客戶推薦更昂貴的產品。</li><li>針對已收到電子郵件的客戶，在通常保留給電子郵件註冊的空間顯示追加銷售優惠方案</li></ul> |
