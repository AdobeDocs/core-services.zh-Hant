---
description: 上傳客戶屬性至 Experience Cloud 的概述和先決條件。
keywords: 核心服務;客戶屬性
seo-description: 上傳客戶屬性至 Experience Cloud 的概述和先決條件。
seo-title: 客戶屬性
solution: Experience Cloud
title: 客戶屬性
uuid: 1621402d-990f-46f9-981a-473280559069
translation-type: ht
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# 客戶屬性

## 概述

若要找到[!UICONTROL 客戶屬性]，請導覽至&#x200B;**「[!DNL Experience Platform]** &gt; **[!UICONTROL 人物]** &gt; **[!UICONTROL 客戶屬性」]**

如果您在客戶關係管理 (CRM) 資料庫中擷取企業客戶資料，您可將該資料上傳至 Experience Cloud 的客戶屬性資料來源。上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

![](assets/custom_reports.png)

## 上傳客戶屬性的先決條件 {#section_BD38693AFBF34926BA28E964963B4EA0}


* **解決方案啟用:** [啟用核心服務的解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。

* **群組成員資格:** 若要上傳客戶屬性資料，使用者必須成為以下群組成員:   [客戶屬性群組](../admin-getting-started/admin-getting-started.md#task_3295A85536BF48899A1AB40D207E77E9)。您也必須屬於 Adobe Analytics 群組或 Adobe Target 群組。

   若想知道您的公司是否有客戶屬性的存取權，您的 [!DNL Experience Cloud] 管理員應該登入 [!DNL Experience Cloud]。導覽至&#x200B;**[!UICONTROL 管理]** &gt; **[!UICONTROL Launch Admin Console]** &gt; **[!UICONTROL 群組]**。如果&#x200B;*客戶屬性*&#x200B;顯示為其中一個群組，您就可以開始了。

   加入客戶屬性群組的使用者可在 Experience Cloud 介面的左邊看到[!UICONTROL 「客戶屬性」]選單項目.

* **目標 mbox:**&#x200B;必須有 mbox.js 58 版或以上版本才能使用客戶屬性。


   請參閱 [Mbox.js 實作](https://marketing.adobe.com/resources/help/zh_TW/target/ov/t_mbox_download.html)。

* **at.js:** 任何版本。




## 什麼是企業客戶資料? {#section_6F34C29F11414842AA57D2B1248FA3C6}

企業客戶資料位於其他系統。它可以很複雜，而且對不同人有不同意義。這項資料包含各種資訊，如成員資格、忠誠程度、年齡、性別、擁有的產品、興趣和存留值。

下圖為資料檔案的範例，其中顯示產品的訂閱者資料，包括成員 ID、有權限的產品、最常啟動的產品等等。

![](assets/01_crs_usecase.png)

建立資料檔案後，可將其上傳至您在 **[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL 客戶屬性]**&#x200B;中建立的客戶屬性來源。

請參閱[上傳客戶屬性資料](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78)以瞭解此工作流程。

## 解決方案使用個案 {#section_4E77650F6CEE4C4ABCD0B3221A5AE5D9}

資料放在 Experience Cloud 中後，您可以自訂資料、在解決方案間共用資料，並用於報告、區隔、活動與促銷活動。

例如:

| 解決方法 | 優勢和使用個案 |
|--- |--- |
| Adobe Analytics  | 行銷人員和分析人員可以瞭解:<ul><li>對黃金等級客戶最有效的線上促銷活動。</li><li>黃金等級客戶搜尋的產品，和白金等級客戶搜尋的產品的比較。</li><li>我的網站重新設計對舊客戶的轉換率是否有正面影響。</li><li>低存留值的客戶在我的網站上傾向搜尋哪些產品。</li></ul> |
| Adobe Target | 屬性資料可讓 Target 使用者:<ul><li>顯示忠心客戶會員的特別折扣和優惠。</li><li>推薦更昂貴的產品給豪華客戶。</li><li>對於已接收電子郵件的客戶，顯示通常保留給電子郵件註冊的向上銷售優惠</li></ul> |
