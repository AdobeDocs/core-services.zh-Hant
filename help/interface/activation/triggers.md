---
description: 如何設定 Experience Cloud 觸發器。
keywords: integrations;Triggers
seo-description: 如何設定 Experience Cloud 觸發器。
seo-title: 觸發器
solution: Marketing Cloud
title: 觸發器
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 觸發器

## 觸發器概述 {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

*觸發程式* 可讓您識別、定義和監控關鍵消費者行為，然後產生跨解決方案的通訊，以重新吸引訪客。 您可以在即時決策和個人化中使用觸發器。

* 設定放棄購物車或放棄購物車且移除產品的快速重新行銷
* 表單和應用程式不完整
* 網站上的任何動作或動作順序

![](assets/trigger-abandonment-2.png)

### 觸發器的類型

一般而言，觸發器可能需要花 15 到 90 分鐘的時間來啟動行銷活動。所需時間會根據資料收集實作、管道上的負載、已定義觸發器的自訂設定，以及 Adobe Campaign 中的工作流程而有所不同。

* **丟棄:** 您可以建立觸發器，在訪客檢視產品但未新增任何項目至購物車時發動。設定[傾向分數](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334)以瞭解客戶在丟棄購物車之後不回訪的傾向。
* **動作：** 例如，您可以建立觸發器，以便在電子報註冊、電子郵件訂閱或信用卡申請（確認）後觸發。 如果您是零售商，您可以為註冊忠誠度方案的訪客建立觸發器。 在媒體和娛樂業中，為觀看特定節目的訪客建立觸發器，而您可能想要以調查回應。
* **會話開始和會話結束：** 為會話開始和會話結束事件建立觸發器。

## 建立 Experience Cloud 觸發器 {#task_821F37183AC045E5AC8EED20317598FE}

建立放棄觸發並設定觸發和傾向分數的條件。 例如，您可以指定在瀏覽期間觸發器規則的條件，例如「購物車放棄」等量度，或產品名稱等維度。 當符合規則時，觸發器就會執行。

>[!NOTE]
>
>目前存在 100 個觸發器的技術限制。

1. 在 Experience Cloud 中，按一下 ![](assets/menu-icon.png)，然後按一下&#x200B;**[!UICONTROL 啟用]**。
1. 尋找[!UICONTROL 觸發器]卡片，然後按一下&#x200B;**[!UICONTROL 啟動]**。

   ![步驟結果](assets/activation-triggers.png)

1. 按一下&#x200B;**[!UICONTROL 新增觸發器]**，然後指定觸發器的類型:

   ![步驟結果](assets/add-trigger.png)

1. 完成下列欄位，並將度量與維度項目拖曳至規則的容器來設定觸發器:

   | 元素 | 說明 |
   |--- |--- |
   | 名稱 | 此觸發器的好記名稱。 |
   | 說明 | 此觸發器的說明、如何使用它等。 |
   | 報表套裝 | 用於此 [觸發器](https://docs.adobe.com/content/help/en/analytics/implementation/analytics-basics/ref-reports-report-suites.html) 的Analytics報表套裝。 此設定可識別要使用的報表資料。 |
   | Visit must include<br>Visit must not include<br>Trigger after no action<br>Include meta data | 您可以定義準則或您要發生的訪客行為，以及您不要發生的訪客行為。例如，簡單的購物車丟棄觸發器的規則可能是:<ul><li>造訪必須包括:  新增購物車 (量度) 和存在。(您可以進一步調整具有特定產品檢視或具有瀏覽器類型之類維度的規則。)</li><li>造訪不得包括:  結帳。</li><li>無動作達下列時間後觸發: 10 分鐘。</li><li>包括中繼資料: 可讓您新增與訪客的行為相關的特定行銷活動維度或變數。此欄位有助於 Adobe Campaign 建置正確的再行銷電子郵件。</li></ul><br>您可以根據您判斷對規則來說很重要的準則，在容器內或容器之間指定 Any、And 或 Or 邏輯。 |
   | 容器 | 容器是您設定和儲存定義觸發器的規則、條件或篩選器的位置。 如果您想要同時發生事件，請將事件放在相同的容器中。 這表示每個容器是在點擊層級獨立處理。例如，如果您有兩個以和運算子聯結的容器，您可預期規則在兩個點擊符合要求時符合資格。 |
   | 之後開始新作業 | 為會話開始和會話結束事件建立觸發器。 |

1. (Optional) In [!UICONTROL Abandonment triggers], you can apply [Propensity Scoring](../activation/triggers.md#concept_A506150674AD45DB98D3CC07E560D334).

   ![步驟結果](assets/propensity-scoring.png)

1. 按一下&#x200B;**[!UICONTROL 「儲存」]**。
1. Use triggers for [real-time remarketing](https://docs.campaign.adobe.com/doc/standard/en/EMA_Transactional_messaging_Marketing_Cloud_Triggers.html) in [!DNL Adobe Campaign].

### 範例觸發器

Experience Cloud觸發器範例：

#### 購物車放棄觸發器

例如，下列頁面會根據瀏覽期間檢視的產品，顯示您可能用於「購物車放棄」觸發器的規則。

![](assets/abandonment-trigger.png)

#### 反向連結觸發器

當點擊隨Facebook的「男性靴子」和反向連結產品傳入時，會觸發下列觸發器。 For the two criteria (*products* and *referrer*) to be evaluated in the same hit, they should be added to the same container.

![](assets/fb-boots-promo.png)

## 傾向得分 {#concept_A506150674AD45DB98D3CC07E560D334}

瞭解客戶在丟棄購物車之後回訪的傾向。傾向得分內建在 Experience Cloud 觸發器中，並且可用於丟棄觸發器。

![步驟結果](assets/propensity-scoring.png)

例如，有些客戶會放棄購物車，以利用電子郵件獎勵來返回購物車。 為了減少收入損失，「傾向評分」演算法可協助識別在沒有獎勵的情況下可能無法返回的相關購物車放棄者。

您可以：

* 避免讓客戶過度暴露於再行銷。
* 識別適當的購物車放棄客戶，並將其活動對應至適當的訊息。
* 透過瞭解哪些客戶會回訪，以及哪些客戶不會回訪，以增加收入。

### 傾向評分的價值 {#section_CA99874A25434CC0BF01D0DA61608889}

您可以執行資料探索，以識別資料中存在的隱藏行為或模式。 特別是，傾向分數可協助您使用更專注和客觀的方式，來識別類似客戶的群組，而不是使用簡單的細分或篩選。 此外，傾向分數可讓您設定預測性功能，以識別公司高價值客戶的行為。

一旦您識別出高價值受眾，您就可以吸引他們發揮最大效果。 例如，如果您是企業對企業的公司，您可能會有銷售電話銷售機會，讓您對銷售機會評分並識別其離線轉換的可能性。 由於每個銷售機會都會增加成本，因此建立獎勵來識別最有可能轉換銷售的潛在客戶，是最有效、成本最低的方式來集中資源。

傾向分數可讓您識別最能預測特定分數的因素，或增加發生事件的可能性，但也可套用至回答特定問題：

* 客戶是否會轉換？
* 客戶是否會回覆電子郵件？
* 客戶會回購嗎？

傾向分數可讓您回答這些問題，並識別有傾向採取動作的訪客，然後設定並計分。
