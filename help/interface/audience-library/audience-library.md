---
description: 可管理將訪客資料轉換為受眾區隔的過程。
seo-description: 可管理將訪客資料轉換為受眾區隔的過程。
seo-title: 受眾
solution: Experience Cloud
title: 受眾
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
translation-type: tm+mt
source-git-commit: f8b48077d936e289d66c1a93a96fe9ebaa4f0136

---


# 受眾 {#topic_679810123CAA4E0CA4FA3417FB0100C7}

受眾是訪客的集合 (訪客 ID 的清單)。Adobe 的受眾服務可管理將訪客資料轉換為受眾區隔的過程。因此，建立和管理受眾類似於建立和使用區隔，再加上可與 [!DNL Experience Cloud] 共用受眾區隔的能力。

![](assets/audiences.png)

您可以建立受眾，或從各種來源衍生出受眾，例如:

* 在 [!DNL Experience Cloud] 中建立新的受眾
* 從發佈至 [!DNL Analytics] 的 [!DNL Experience Cloud] 區隔
* 開始日期 [!DNL Audience Manager]

**即時受眾 vs. 歷史受眾**

即時鎖定使用案例可以存取所有受眾，無論受眾來源為何。不過，即時鎖定目標無法存取從 Analytics 共用到 Audience Manager 的受眾。系統以兩種方式評估受眾:

* 每 12 小時評估一次源自分析的歷史受眾。歷史受眾一律包含回訪訪客。
* 即時受眾源自於 Experience Cloud 受眾，且為即時評估。


## 解決方案如何使用受眾 {#concept_01EB9345C5344597BC94A864EDD38EE1}

下表說明 Experience Cloud 解決方案如何使用受眾:

| 解決方法 | 說明 |
|--- |--- |
| Experience Cloud 受眾 | 使用[受眾程式庫](../audience-library/audience-library.md) 介面以原生方式建立、管理和共用受眾。您可以:<ul><li>使用原始分析屬性以使用即時受眾</li><li>結合受眾以建立複合受眾，加入即時和歷史資料</li><li>請參閱估計之受眾規模的圖形檢視</li></ul><br>如需有關要建立的受眾類型建議，請參閱 [Experience Cloud 受眾](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| Analytics | 在區隔中，您可以建立區隔，組合區隔與報表套裝，然後[發佈區段至 Experience Cloud](../audience-library/audience-library.md)。發佈區隔會顯示在[受眾](../audience-library/audience-library.md)頁面上。受眾也可作為 Adobe Target 提供之促銷活動體驗以及 Audience Manager 中的目標受眾。從 Analytics 中共用受眾後，且選擇在啟用的行銷活動中使用時，會將過去 90 天符合區隔定義準則的所有訪客設定檔傳送至 Experience Cloud 受眾服務平台。重要: 您必須將透過 Analytics 共用的對象數量限制為 20，以避免額外的程序延誤。透過 Analytics 與 Experience Cloud 共用的受眾不能超過 2,000 萬個不重複的成員。另外，由於快取關係，Experience Cloud 會在 12 小時之後才顯示 Analytics 中刪除的報表套裝資訊。 |
| Mobile Services | Analyze mobile traffic using the sunburst visualization in the [Device Types](https://marketing.adobe.com/resources/help/en_US/mobile/?f=reports_devices). |
| Target | [ID 服務](https://marketing.adobe.com/resources/help/en_US/mcvid/)會將訪客 ID 和資料統一至單一、可運作的設定檔以供各解決方案使用。[發佈至 Experience Cloud](../audience-library/audience-library.md) 核取方塊會在 Adobe Analytics 區隔建立程序期間顯示，勾選後該區隔將可供 Adobe Target 的自訂受眾程式庫使用。在 Analytics 或 Audience Manager 中建立的區隔皆適用於 Target 中的活動。例如，您可以根據 Analytics 中建立的 Analytics 轉換度量和受眾區隔來建立行銷活動。 |
| Audience Manager | 可在 Audience Manager 區隔中使用共用受眾。Audience Manager 原本就可使用所有的 Experience Cloud 受眾，提供:<ul><li>內建自動化，不論解決方案工作流程如何共用和使用受眾</li><li>離站目的地</li><li>外觀類似塑型</li></ul> |
| 促銷活動 | <ul><li>從不同的 Adobe Experience Cloud 解決方案匯入共用受眾至 Adobe Campaign。</li><li>以共用受眾的形式匯出接收者清單。這些共用受眾可用於您有使用的其他 Adobe Experience Cloud 解決方案。</li></ul> |
| Media Optimizer | 使用受眾做為目標。 |


>[!IMPORTANT]
>
>訪客符合從 Analytics 共用的受眾資格後，此項資訊會延遲 24 至 48 小時，然後才能在 Target、Media Optimizer 和 Campaign 中操作。

## 更多說明 - 問題、指南和使用個案 {#section_C7F151644D8A45F7B6FC54F58845635D}


| 說明 | 資源 |
|--- |--- |
| 找不到受眾嗎? | 請確認您已完成佈建。請參閱[快速入門 - 啟用核心服務的解決方案](../core-services/core-services.md)。<br>按一下[此處](https://www.adobe.com/go/audiences)，申請存取「設定檔與受眾」(整合佈建表單)。 |
| 使用個案 | 如需更多有關使用解決方案的指南，請前往知識庫中的[受眾建立選項](https://helpx.adobe.com/marketing-cloud-core/kb/People/Audience-Creation-Options.html)。 |
| 論壇 | [受眾論壇](https://forums.adobe.com/community/experience-cloud/platform/core-services/people-service/audiences)是取得有關受眾說明的額外資源。 |


## 受眾程式庫介面元素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] 提供一個資料庫，能讓您利用原始的即時受眾識別來建立和管理受眾。

**[!UICONTROL Experience Cloud]** &gt; **[!UICONTROL Experience Platform]** &gt; **[!UICONTROL People]** &gt; **[!UICONTROL Audience Library]**

![](assets/audience_library.png)

| 元素 | 說明 |
|--- |--- |
| 新增 | [建立受眾](../audience-library/audience-library.md)。 |
| 標題與說明 | 用來識別和說明受眾的欄標題。 |
| 作者 | 受眾區隔的建立者。 |
| 來源 | 識別建立受眾的位置。<ul><li>**Analytics:** 在 Reports &amp; Analytics 或 Ad Hoc Analysis 中建立的區隔，然後[發佈至 Experience Cloud](../audience-library/audience-library.md)。</li><li>**Experience Cloud:**&#x200B;在 Experience Cloud Audiences 中[建立](../audience-library/audience-library.md)新的受眾。</li><li>**Audience Manager:** 在 Audience Manager 中建立的受眾會自動顯示在 Experience Cloud「受眾」中。</li></ul> |
| 目前規模 | 目前的受眾規模。 |
| 啟用 | 區隔的啟用狀態。 |
