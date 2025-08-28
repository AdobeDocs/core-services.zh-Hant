---
title: 關於 [!DNL Customer Attributes]
description: 了解 Experience Cloud 中的  [!DNL Customer Attributes] 。了解如何上傳客戶屬性資料，以便在 Adobe Analytics 和 Adobe Target 使用。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: bd718358c6db1ea4a6150d019773072418b629f9
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 80%

---

# Experience Cloud 中的 [!DNL Customer Attributes]

**[!UICONTROL 應用程式]** ![功能表](assets/menu-icon.png) > **[!DNL Customer Attributes]**

Experience Cloud 中的 [!DNL Customer Attributes] 可讓您上傳從客戶關係管理 (CRM) 資料庫擷取的企業資料。您可以[將資料](t-crs-usecase.md)上傳到Experience Cloud中的[!DNL Customer Attributes]資料來源，然後在[!DNL Adobe Analytics]和[!DNL Adobe Target]中使用資料。

![客戶屬性概觀](assets/custom_reports.png)

## 什麼是企業客戶資料？ {#enterprise_data}

企業資料位於其他系統中。這些資料可能很複雜，而且對不同的人來說有不同的意義。此資料可包含成員資格、忠誠度、年齡、性別、擁有的產品、興趣和終身價值等資訊。

下圖是資料檔案的範例，顯示產品的訂閱者資料，包括成員 ID、已授權產品、最常啟動的產品等。

![什麼是企業客戶資料？](assets/01_crs_usecase.png)

建立資料檔案後，可將其上傳至您在&#x200B;**[!UICONTROL Experience Cloud]** > **[!UICONTROL 客戶屬性]**&#x200B;中建立的客戶屬性來源。

請參閱[上傳客戶屬性資料](t-crs-usecase.md)以瞭解此工作流程。

## Analytics和Target中的客戶屬性範例 {#examples}

資料傳入 Experience Cloud 後，您就可以自訂資料，並共用至解決方案以用於報表、細分、活動和行銷活動。

例如：

| 解決方法 | 優點和使用案例 |
|--- |--- |
| Adobe Analytics  | 行銷人員和分析師可以了解：<ul><li>對金級客戶最有效的線上行銷活動。</li><li>金級客戶所搜尋的產品與白金級客戶所搜尋的產品比較。</li><li>網站重新設計是否對舊客戶的轉換率帶來正面影響。</li><li>終身價值低的客戶會在我的網站上研究哪些產品。</li></ul> |
| Adobe Target | 屬性資料可讓 Adobe Target 使用者：<ul><li>顯示忠誠俱樂部會員的特別折扣和產品建議。</li><li>向您的高消費力客戶推薦更昂貴的產品。</li><li>針對已收到電子郵件的客戶，在通常保留給電子郵件註冊的空間顯示追加銷售產品建議</li></ul> |

{style="table-layout:auto"}
