---
description: 瞭解如何使用屬性規則來建立受眾與定義 Experience Cloud 中的複合受眾。
keywords: 核心服務
seo-description: 瞭解如何使用屬性規則來建立受眾與定義 Experience Cloud 中的複合受眾。
seo-title: 建立對象
solution: Experience Cloud
title: 建立對象
uuid: 7e622539-296e-4ff3-93b0-ec1 c08 b35429
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 建立對象

瞭解如何使用屬性規則來建立受眾與定義 Experience Cloud 中的複合受眾。

本文幫助您瞭解如何:

* 建立對象
* 建立規則
* 使用規則定義複合受眾


下圖解說複合受眾的兩條規則。

![](assets/audience_sharing.png)

每一個圓圈代表定義受眾成員資格的一條規則。兩條受眾規則皆符合的訪客重疊形成定義的複合受眾。

>[!NOTE]
>
>在指定時段的資料收集完成後，就會完全定義觀眾。
以下範例解說如何建立複合受眾的規則。此受眾的組成成員:

* 「家庭與花園」區隔，從頁面資料、或原始分析資料衍生而來。
* Chrome和Safari使用者是從 [!DNL Adobe Analytics][發佈](../audience-library/audience-library.md#task_32FEEFE0B32E4E388CD4D892D727282A) 到的區段衍生 [!DNL Experience Cloud]而來。


   ![](assets/audience_create.png)

1. 在此 [!DNL Experience Cloud]中，按一下 **[!UICONTROL 「人物]** &gt; **[!UICONTROL 對象庫]**」。
1. 在 [!UICONTROL 「對象] 」頁面上按一下 **[!UICONTROL 「新增]**」。 ![](assets/add_icon_small.png)

![步驟結果](assets/audience_create_new.png)

1. 在[!UICONTROL 建立新受眾]頁面上，指定標題和說明。
1. 在[!UICONTROL 規則]下，選擇屬性來源:

* **[!UICONTROL 即時分析資料:]** (或原始資料) 這是從即時 Analytics 影像請求衍生的屬性資料，並包含 eVars 和事件等資料。使用此屬性來源時必須選擇報表套裝，和定義要加入的維度或事件。此報表套裝選擇提供報表套裝所使用的變數結構。

   >[!NOTE]
   >
   >由於快取，Analytics中已刪除的報表套裝需要12小時的時間，Experience Cloud才會顯示刪除。

* **[!UICONTROL Experience Cloud：]** 來源資料衍生自 [!DNL Experience Cloud] 來源。例如，這可以是您在 [!DNL Analytics] 中建立的受眾區段資料，或是 [!DNL Audience Manager] 中的資料。

1. 定義受眾規則:

>[!NOTE]
>
>定義觀眾規則時，您應瞭解實施變數。

在 [!UICONTROL 規則]下，定義 *`Home & Garden`* 屬性選擇：

* **[!UICONTROL 屬性來源:]** 原始 Analytics 資料
* **[!UICONTROL 報表套裝:]** 報表套裝 31
* Dimension= **[!UICONTROL Store(Merch)(v6)]** &gt; **[!UICONTROL 等於]** &gt; **[!UICONTROL 家庭與花園]**

   ![](assets/home_garden.png)

   *Chrome和Safari訪客* 是從Analytics共用的觀眾區隔：

* **[!UICONTROL 屬性來源:]** Experience Cloud
* **[!UICONTROL 維度:]** Chrome 與 Safari 訪客

   ![](assets/chrome_safari.png)

   為了比較，您可以新增 *OR* 規則來查看網站區域的所有訪客，例如「中庭與家俱」。

   ![](assets/audiences_rule_patio.png)

1. 檢視結果。

導出的規則是定義的受眾，包含造訪「家庭與花園」的 Chrome 與 Safari 使用者。「中庭與傢俱」區隔對造訪該網站區段的所有訪客提供更深入的資訊。

![](assets/defined_audience.png)

**歷史預估:** (虛圓形) 代表根據 [!DNL Analytics] 資料建立的規則。

**實際受眾:**(實心圓形) 建立之任何具備 30 天 Audience Manager 資料的規則。當 Audience Manager 資料達到 30 天時，會變成實心並代表實際的數字。

完成指定期間的資料收集後，圓圈會結合以顯示定義的受眾。

1. 定義規則後，按一下 **[!UICONTROL 「儲存]**」。

儲存受眾後，即可供其他解決方案使用。例如，您可以在 Target 活動中加入共用受眾。
