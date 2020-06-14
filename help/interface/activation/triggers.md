---
description: 如何設定 Experience Cloud Triggers。
keywords: integrations;Triggers
seo-description: 如何設定 Experience Cloud Triggers。
seo-title: Triggers
solution: Marketing Cloud
title: Triggers
uuid: dab536e3-1969-4661-919e-5b15f423fecd
translation-type: tm+mt
source-git-commit: fb03bf89bcc6ed4438daf18c8415de3052ba8fa4
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 96%

---


# Triggers

## Triggers 概述 {#topic_4F21FCE9A64E46E8B6D51F494FA652A7}

Triggers 能讓您識別、定義及監控重要的客戶行為，然後產生跨解決方案的交流，重新與訪客互動。您可以在進行即時決策和個人化時使用觸發器。

* 針對放棄購物車或透過移除產品放棄購物車設定快速再行銷
* 不完整的表單和應用程式
* 網站上的任何動作或動作順序

![](assets/trigger-abandonment-2.png)

### 觸發器的類型

一般而言，觸發器可能需要花 15 到 90 分鐘的時間來啟動行銷活動。所需時間會根據資料收集實作、管道上的負載、已定義觸發器的自訂設定，以及 Adobe Campaign 中的工作流程而有所不同。

* **丟棄：**&#x200B;您可以建立觸發器，在訪客檢視產品但未新增任何項目至購物車時引發。
* **動作：**&#x200B;您可以建立觸發器，在電子報註冊、電子郵件訂閱或信用卡申請 (確認) 等動作後引發。如果您是零售商，可針對註冊忠誠度計畫的訪客建立觸發器。若為媒體和娛樂產業，可針對觀看特定節目的訪客建立觸發器，而您可能會想透過意見調查給予回應。
* **工作階段開始和工作階段結束：**&#x200B;針對工作階段開始和工作階段結束事件建立觸發器。

## 建立 Experience Cloud 觸發器 {#task_821F37183AC045E5AC8EED20317598FE}

建立觸發器並設定觸發器的條件。 例如，您可以指定造訪期間觸發器規則的條件，例如「購物車放棄」等量度，或產品名稱等維度。符合規則時，觸發器就會執行。

>[!NOTE]
>
>目前存在 100 個觸發器的技術限制。

1. In the Experience Cloud, click ![](assets/menu-icon.png), then click **[!UICONTROL Launch]**.
2. Locate the [!UICONTROL Triggers] card, then click **[!UICONTROL Manage Triggers]**.
3. 按一下&#x200B;**[!UICONTROL 新增觸發器]**，然後指定觸發器的類型:

   ![步驟結果](assets/add-trigger.png)

4. 完成下列欄位，並將量度與維度項目拖曳至規則的容器來設定觸發器：

   | 元素 | 說明 |
   |--- |--- |
   | 名稱 | 此觸發器的易記名稱。 |
   | 說明 | 此觸發器的說明、使用方式等資訊。 |
   | 報表套裝 | 用於此觸發器的 Analytics [報表套裝](https://docs.adobe.com/content/help/zh-Hant/analytics/admin/manage-report-suites/report-suites-admin.translate.html)。此設定可識別要使用的報表資料。 |
   | 造訪必須包括<br>造訪不得包括<br>在無動作後觸發<br>包括中繼資料 | 您可以定義準則或您要發生的訪客行為，以及您不要發生的訪客行為。例如，簡單的購物車丟棄觸發器的規則可能是:<ul><li>造訪必須包括:  新增購物車 (量度) 和存在。(您可以進一步調整具有特定產品檢視或具有瀏覽器類型之類維度的規則。)</li><li>造訪不得包括:  結帳。</li><li>無動作達下列時間後觸發: 10 分鐘。</li><li>包括中繼資料: 可讓您新增與訪客的行為相關的特定行銷活動維度或變數。此欄位有助於 Adobe Campaign 建置正確的再行銷電子郵件。</li></ul><br>您可以根據您判斷對規則來說很重要的準則，在容器內或容器之間指定 Any、And 或 Or 邏輯。 |
   | 容器 | 容器是設定和儲存定義觸發器的規則、條件或篩選器的位置。如果您想讓事件同時發生，請將事件放在相同的容器中。這表示每個容器是在點擊層級獨立處理。例如，如果您有兩個以和運算子聯結的容器，您可預期規則在兩個點擊符合要求時符合資格。 |
   | 發生後開始新工作階段 | 為工作階段開始和工作階段結束事件建立觸發器。 |

5. 按一下&#x200B;**[!UICONTROL 儲存]**。
6. 在 [!DNL Adobe Campaign] 中使用這些觸發器進行[即時再行銷](https://helpx.adobe.com/tw/support/campaign/standard.html)。

### 範例觸發器

Experience Cloud Triggers 範例：

#### 購物車放棄觸發器

例如，下列頁面會根據造訪期間檢視的產品，顯示您可用於「購物車放棄」觸發器的規則。

![](assets/abandonment-trigger.png)

#### 反向連結觸發器

當點擊隨「男靴」產品和 Facebook 的反向連結傳入時，便會引發下列觸發器。為了在同一個點擊中評估這兩個條件 (*產品*&#x200B;和&#x200B;*反向連結*)，應該將它們新增至相同的容器中。

![](assets/fb-boots-promo.png)
