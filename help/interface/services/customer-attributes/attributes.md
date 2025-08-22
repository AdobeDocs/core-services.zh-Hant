---
title: '[!DNL Customer attributes]'
description: 了解 Experience Cloud 中的  [!DNL customer attributes] 。了解如何上傳客戶屬性資料，以便在 Adobe Analytics 和 Adobe Target 使用。
solution: Experience Cloud,Target,Analytics
feature: Customer Attributes
role: Admin
topic: Administration
level: Experienced
exl-id: fe8ad013-76da-49f8-aa51-dc5f6c1b1d79
source-git-commit: 3043cd913d5165c58fb84f3342b05a00a690d6a6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 78%

---

# Experience Cloud 中的 [!DNL Customer attributes]

Experience Cloud 中的 [!DNL Customer attributes] 可讓您上傳從客戶關係管理 (CRM) 資料庫擷取的企業資料。您可以將資料上傳至 Experience Cloud 中的客戶屬性資料來源，然後將資料用於 [!DNL Adobe Analytics] 和 [!DNL Adobe Target]。

## 找到 [!DNL customer attributes] 功能

1. 登入[!DNL Experience Cloud]並選取功能表![功能表](assets/menu-icon.png)圖示。

1. 選取&#x200B;**[!UICONTROL 客戶屬性]**。

![客戶屬性概觀](assets/custom_reports.png)

## 上傳 [!DNL customer attributes] 的先決條件 {#prerequisites}

* **群組成員資格：**&#x200B;若要上傳客戶屬性資料，使用者必須是客戶屬性群組的成員。 您也必須先加入 Adobe Analytics 群組或 Adobe Target 群組。

  若要知道您的公司是否具有客戶屬性的存取權，您的[!DNL Experience Cloud]管理員應登入[Experience Cloud](https://experience.adobe.com)。 導覽至&#x200B;**[!UICONTROL Admin Console]** > **[!UICONTROL 產品]**。 如果 *[!DNL Customer Attributes]* 以其中一個[!UICONTROL 產品設定檔]顯示，表示您可以開始使用了。

  若是加入 [!DNL Customer Attributes] 的使用者，可在 Experience Cloud 介面的左側看到[!UICONTROL 客戶屬性]功能表項目。

* 客戶屬性需要 **Adobe Target** `at.js` (任何版本) 或 `mbox.js` 58 版或更新版本。

  參閱「[如何部署 at.js](https://experienceleague.adobe.com/docs/target-dev/developer/client-side/overview.html)」。

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
