---
description: 可管理將訪客資料轉換為受眾區隔的過程。
seo-description: 可管理將訪客資料轉換為受眾區隔的過程。
seo-title: 受眾
solution: Experience Cloud
title: 受眾
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: 14d6e0ae15b023ad4dd3f8aca0606f26b39a21e9

---


# 受眾 {#topic_679810123CAA4E0CA4FA3417FB0100C7}

對象是訪客的集合（訪客ID的清單）。 Adobe的觀眾服務可管理將訪客資料轉譯為觀眾區隔。 因此，建立和管理受眾類似於建立和使用區隔，再加上可與 [!DNL Experience Cloud] 共用受眾區隔的能力。

![](assets/audiences.png)

您可以建立受眾，或從各種來源衍生出受眾，例如:

* 在 [!DNL Experience Cloud] 中建立新的受眾
* 從發佈至 [!DNL Analytics] 的 [!DNL Experience Cloud] 區隔
* 從 [!DNL Audience Manager]

**即時受眾 vs. 歷史受眾**

即時鎖定使用案例可以存取所有受眾，無論受眾來源為何。不過，即時鎖定目標無法存取從 Analytics 共用到 Audience Manager 的受眾。系統會以兩種方式評估觀眾：

* 每4小時評估一次Analytics的歷史觀眾。 處理和分享的總時間可能需要8小時。  歷史觀眾一律會包含回訪訪客。
* 即時受眾源自於 Experience Cloud 受眾，且為即時評估。

## 解決方案如何使用受眾 {#concept_01EB9345C5344597BC94A864EDD38EE1}

下表說明如何在Experience Cloud解決方案中使用觀眾：

| 解決方法 | 說明 |
|--- |--- |
| Experience Cloud 受眾 | 使用[受眾程式庫](../audience-library/audience-library.md) 介面以原生方式建立、管理和共用受眾。您可以：<ul><li>使用原始分析屬性使用即時觀眾</li><li>結合觀眾以建立複合觀眾，加入即時和歷史資料</li><li>檢視預計觀眾大小的圖形檢視</li></ul><br>如需您要建立何種對象類型的建議，請參閱： [Experience Cloud觀眾](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| Analytics | 在區段中，您可以建立區段、將其與報表套裝結合，然 [後將區段發佈至Experience Cloud](../audience-library/audience-library.md)。 發佈區隔會顯示在[受眾](../audience-library/audience-library.md)頁面上。受眾也可作為 Adobe Target 提供之促銷活動體驗以及 Audience Manager 中的目標受眾。Once an audience is shared from Analytics, and selected for use in an active campaign, all the visitor profiles who met the segment definition criteria for the past 90 days are sent to the Experience Cloud [!UICONTROL Audience Services] platform. 共用觀眾的限制已提高至75個。 從Analytics分享給Experience Cloud的觀眾不能超過2000萬個獨特成員。 此外，由於快取，Analytics中刪除的報表套裝需要12小時才能在Experience Cloud中顯示刪除。 |
| Mobile Services | 使用「裝置類型」報表中的散射環視覺化 [!UICONTROL 分析行動流量] 。 |
| Target | The [ID service](https://docs.adobe.com/content/help/en/id-service/using/home.html) unifies visitor IDs and data into a single, actionable profile for use across solutions. [發佈至 Experience Cloud](../audience-library/audience-library.md) 核取方塊會在 Adobe Analytics 區隔建立程序期間顯示，勾選後該區隔將可供 Adobe Target 的自訂受眾程式庫使用。在 Analytics 或 Audience Manager 中建立的區隔皆適用於 Target 中的活動。例如，您可以根據 Analytics 中建立的 Analytics 轉換度量和受眾區隔來建立行銷活動。 |
| Audience Manager | Audience Manager區段中提供共用的觀眾。 Audience Manager 原本就可使用所有的 Experience Cloud 受眾，提供:<ul><li>內建自動化功能，瞭解解決方案工作流程中共用和使用這些功能的方式</li><li>離站目的地</li><li>相似模型</li></ul> |
| 促銷活動 | <ul><li>從不同的 Adobe Experience Cloud 解決方案匯入共用受眾至 Adobe Campaign。</li><li>以共用觀眾的形式匯出收件者清單。 這些共用觀眾可用於您使用的不同Adobe Experience Cloud解決方案。</li></ul> |
| Media Optimizer | 使用對象做為目標。 |

>[!IMPORTANT]
>
>一旦訪客符合從Analytics共用的觀眾資格，該資訊在Target、Ad Cloud和Campaign Standard中可操作之前會有4-8小時的延遲。

## 更多說明 - 問題、指南和使用個案 {#section_C7F151644D8A45F7B6FC54F58845635D}

| 協助 | 資源 |
|--- |--- |
| 找不到對象？ | 請確定您已布建。 See [Getting started - enable your solutions for core services](../core-services/core-services.md).<br>按一 [下這裡](https://www.adobe.com/go/audiences) ，以要求存取「設定檔與對象」（整合布建表單）。 |
| 使用個案 | 如需使用何種解決方案的詳細指引，請前往「知 [識庫」中的「觀眾建立選項](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html) 」。 |
| 論壇 | The [Audiences forum](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences) is an additional resource to get help with audiences. |

## 受眾程式庫介面元素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] 提供一個資料庫，能讓您利用原始的即時受眾識別來建立和管理受眾。

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** >人 **[!UICONTROL 員]** >觀 **[!UICONTROL 眾庫]**

![](assets/audience_library.png)

| 元素 | 說明 |
|--- |--- |
| 新增 | [建立受眾](../audience-library/audience-library.md)。 |
| 標題與說明 | 用來識別和說明受眾的欄標題。 |
| 作者 | 建立觀眾區隔的人員。 |
| 來源 | 識別建立對象的位置。<ul><li>**Analytics:** 在 Reports &amp; Analytics 或 Ad Hoc Analysis 中建立的區隔，然後[發佈至 Experience Cloud](../audience-library/audience-library.md)。</li><li>**Experience Cloud:**&#x200B;在 Experience Cloud Audiences 中[建立](../audience-library/audience-library.md)新的受眾。</li><li>**Audience Manager:** 在 Audience Manager 中建立的受眾會自動顯示在 Experience Cloud「受眾」中。</li></ul> |
| 目前大小 | 目前的受眾規模。 |
| 作用中 | 區段的作用中狀態。 |
