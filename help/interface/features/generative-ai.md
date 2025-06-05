---
title: Experience Cloud應用程式中的Generative AI
description: 瞭解generative AI (GenAI)以及Experience Cloud應用程式如何使用GenAI和[!UICONTROL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 1b7b2479159c93e186d975b14a75fc6e5152d72e
workflow-type: tm+mt
source-wordcount: '1768'
ht-degree: 3%

---

# Experience Cloud產品中的Generative AI

Experience Cloud中的Generative AI (genAI)可幫助您自動化創意和認知任務並提高生產力。 本頁說明Experience Cloud應用程式支援genAI和AI Assistant的位置，並提供深入瞭解這些功能的連結。

**什麼是genAI？**

Generative AI是可建立原始內容的AI型別。 例如，它可以建立文字、影像、視訊、音訊或軟體程式碼，以回應使用者的提示或要求。

* **建立：**&#x200B;根據訓練和輸入提示從頭開始產生內容（文字、影像、音樂或視訊）的能力。 此功能是generative AI的&#x200B;_generative_&#x200B;方面。

* **產生回應：** AI會針對提示提供回應或回應，通常會利用其可用的資料和知識存放庫。

**什麼是[!UICONTROL AI小幫手]？**

[!UICONTROL AI小幫手]是Experience Platform和相關應用程式支援的對話工具。 使用它可快速取得支援產品中的&#x200B;_產品知識_&#x200B;和&#x200B;_營運深入分析_。

* **產品知識：**&#x200B;產品知識是指以Experience League檔案為根據的概念和主題。 瞭解如何建立有效的[目標型提示](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)，以充分利用[!UICONTROL AI小幫手]。 來自Experience League的所有回應都是可驗證的，並會透過連結引用。

* **營運分析：** [營運分析](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions#objects-questions)參考中繼資料物件（屬性、對象、資料流、資料集等）的相關回應。 透過[!UICONTROL AI小幫手]，您可以在數秒內完成其他可能需要數小時或數天的作業。

* **產品支援：** [產品支援代理程式](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support)是[!UICONTROL AI小幫手]的自助式偵錯和疑難排解功能，可用於Experience Platform功能和應用程式。 在不離開工作流程的情況下疑難排解支援問題、建立客戶支援票證，並使用AI Assistant追蹤案例進度。

* **Data Insights Agent：** [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)，可在[!DNL Customer Journey Analytics]中從AI助理存取，是產生式AI交談代理程式，可快速並有效率地回答有關您資料的問題。 它會使用您資料檢視中的元件並使用實際資料，在[!UICONTROL Analysis Workspace]中建置相關的視覺效果。

[瞭解AI助理](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

## Experience Cloud產品中的GenAI可用性 {#products}

下列Experience Cloud應用程式支援產生AI或[!UICONTROL AI助理]。 也依產品說明支援Adobe Firefly。

更新日期： 2025年6月5日&#x200B;**&#x200B;**

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign]受管理的雲端服務](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是創作AI應用程式，旨在協助企業行銷團隊建立、啟用和最佳化跨管道（例如付費媒體、電子郵件和顯示廣告）的品牌上行銷活動內容。

效能行銷人員可使用自然語言提示來產生個人化、符合品牌規範的資產。 GenStudio for Performance Marketing可加快行銷活動的執行速度、在不影響品牌完整性的情況下擴展內容生產，並提供效能分析以提高整體投資報酬率。

[了解更多](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Firefly相容性： **是**

## [!DNL Experience Manager] {#aem}

以下章節簡要說明AEM應用程式中的創作AI。

### Experience Manager Sites

在AEM Sites中，您可以使用&#x200B;_[!UICONTROL 產生變數]_。 此功能會使用產生式人工智慧，根據您的輸入提示建立內容變異。 提示是由Adobe提供，或由您建立及管理。

建立變化後，您可以在網站上使用該內容，並使用Edge Delivery Services中的[Experimentation](https://www.aem.live/docs/experimentation)功能來測量其成功。 您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。

**輸入和輸出範例**

輸入欄位包括：

* 要產生的變數數量
* 對象Source
* 對象目標
* 其他內容
* 客戶導向提示

輸出是產生的內容或市場副本。

Adobe Firefly相容性： **是**

[了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Sites Optimizer {#sites-optimizer}

AEM Sites Optimizer使用創作AI來分析和改進網頁體驗的效能和有效性。 這些見解將分組為關鍵機會領域：參與、流量取得、安全性狀態以及網站健康狀態。 每個類別都會反白標示增強網站的特定方式，包括增加訪客互動、改善可發現性、增強安全性，或維持網站穩定性。 [了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/opportunity-types/overview)

### Experience Manager Assets {#aem-assets}

在AEM Assets中，您可以在&#x200B;**Content Hub**&#x200B;和&#x200B;**AI產生的智慧標籤**&#x200B;中使用產生式AI。

Adobe Firefly相容性： **是**

**Content Hub**

[!UICONTROL Content Hub]是[!DNL Experience Manager Assets as a Cloud Service]的一部分，可讓組織及其業務夥伴對品牌上內容的存取權進行民主化。 其著重於大規模散發資產以供啟用，以及建立品牌內內容變體，以提升行銷靈敏度。

在Content Hub中，您可以使用Adobe Express建立內容(如果您有Adobe Express許可權)。 您可以使用簡單的工具編輯現有內容、使用範本和品牌元素產生品牌上的變化，以及使用[!DNL Adobe Firefly]的最新GenAI功能建立內容。 [了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

**智慧標籤**

AI可以自動將描述性標籤指派給數位資產，而不依賴手動輸入。 這些AI產生的標籤可增強中繼資料品質，讓資產更容易搜尋、分類和推薦。

例如，如果資產是影像，AI就可識別物件、場景、情感，甚至品牌標誌。 它可以產生相關標籤，例如&#x200B;_sunset_、_beach_、_vacation_&#x200B;或&#x200B;_微笑_。 [了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags)

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer] (AJO)中，您可以使用[AI助理](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)來取得&#x200B;_產品知識_&#x200B;和&#x200B;_營運深入分析_ （測試版）。

### 在AJO中使用AI助理的範例

以下是產品知識的輸入範例：

* _一個Journey Optimizer沙箱中可以有多少個已上線活動？_

  輸出是從Experience League和其他Adobe資料存放區產生。

以下是運算深入分析的輸入範例：

* _過去七天已建立多少歷程？_

  對於輸出，AI Assistant查詢客戶特定的資料存放區。 資料存放區包含有關[!UICONTROL 歷程]的集中操作資料。 此功能與客戶無關，只會從商業物件提取中繼資料。 它不會存取您沙箱中的資料。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)

Adobe Firefly相容性： **否**

### 用於產生內容的AI助理(AJO Prime和Ultimate) {#ajo-prime}

在AJO _Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;中，您可以使用[內容產生](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)來產生內容，為文字和影像提供主動式內容變數建議。

此功能適用於電子郵件、推播通知、網頁、內容和SMS頻道。 它提供提示式文字和影像產生。 AJO Prime和Ultimate中內容產生的輸出不會受到任何影響。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Firefly相容性： **是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!UICONTROL AI助理]協助您瞭解產品知識。

範例輸入：

* _如何在帳戶歷程中傳送電子郵件？_

  產品知識輸出是從Experience League提取。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Firefly相容性： **否**

## [!DNL Campaign]受管理的雲端服務 {#campaign-cs}

Campaign Managed Cloud Services使用[!UICONTROL AI助理]來產生內容。 此功能可讓您根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對品牌概述的樣式、版面、色調等最佳化。 您可以在電子郵件、簡訊和推播等管道間使用它。

**注意：**&#x200B;在Campaign Managed Cloud Services中產生內容的輸出不會有任何損失。

[了解更多](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Firefly相容性： **是**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics可讓您透過以下方式使用創作AI或AI助理：

* 產品知識的[AI助理](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)
* AI助理中的[產品支援代理程式](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support)
* AI助理中的[Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai)
* Workspace視覺效果中的[智慧型字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)
* [Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/report#template)自動指派每個資產中繼資料

Adobe Firefly相容性： **否**

**AI 助理**

探索Experience League的產品知識。 如果您是新使用者，請快速瞭解Customer Journey Analytics概念，並熟悉產品和功能。 例如：

* _如何在帳戶歷程中傳送電子郵件？_

經驗豐富的使用者可獲得進階使用案例或學習策略，以更快的速度執行任務。 您可以快速瞭解概念、疑難排解問題或搜尋資訊。

[了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

**智慧型字幕**

您可以在[!DNL Customer Journey Analytics]中使用&#x200B;_智慧型字幕_&#x200B;來取得最常用Workspace視覺效果的自然語言深入分析。 智慧型字幕是需要敘述和上下文以與其他使用者分享的分析師的理想選擇。 商務使用者可以利用它來快速探索高階收穫。

例如：

* **輸入：**&#x200B;在CJA中，執行支援的視覺效果（包括線條、區域、長條圖、流量或流失），然後按一下&#x200B;**[!UICONTROL 智慧型字幕]**。

* **輸出：**&#x200B;檢視自動產生的自然語言註解，顯示內容與主要內容。 接著，您可對產生的資料執行動作，例如檢閱、複製資料並與組織共用。 [檢視方式](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

**Content Analytics**

Content Analytics使用AI和GenAI自動指派每個資產中繼資料，例如主題、場景、前景顏色等。 屬性是AI指派的中繼資料標籤，說明資產或體驗中的內容。

例如：前景`color: red`是自動指派的屬性。 視覺效果可協助您識別哪些資產屬性對轉換的貢獻最大。 [了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/report#template)

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP使用[!UICONTROL AI助理]協助您瞭解Experience League的產品知識。 此外，還提供營運深入分析（測試版）。 [!UICONTROL AI小幫手]查詢客戶特定的營運分析資料存放區，該資料存放區包含已分割到AEP沙箱的集中營運資料。 系統只會從屬性、受眾、資料流程、資料集、目的地、結構描述和來源提取中繼資料，不會存取沙箱中的資料。

例如，如果您查詢對象，[!UICONTROL AI助理]可以存取對象名稱和其他關聯的中繼資料，但無法存取該對象內的設定檔。

[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)

Adobe Firefly相容性： **否**

## [!DNL Marketo] {#marketo}

在Marketo中，互動式網路研討會和Dynamic Chat提供generative AI。

**互動式網路研討會**

為您錄製的網路研討會自動產生章節和摘要，讓對象更容易存取和導覽。 功能包括：

* 自動產生章節
* AI產生的文字摘要
* 可編輯的內容 — 修改產生的章節和摘要
* 輕鬆整合 — 將HTML程式碼複製到您選取的網頁編輯器，以將章節和摘要新增至您的登陸頁面

[了解更多](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai)

**Dynamic Chat**

Adobe Dynamic Chat中由創作AI支援的功能可讓您最佳化銷售代理的生產力、深入瞭解網站的訪客意圖，並以安全的方式回應訪客問題。 您可以預先核准問題、答案和交談摘要。 Dynamic Chat包含免費和付費版本。

[了解更多](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Firefly相容性： **否**

## [!DNL Workfront] {#workfront}

[!DNL Workfront]中的[!UICONTROL AI小幫手]提供應用程式內資訊和建議，協助您完成工作。 您可以：

* 取得某些物件的摘要，讓您以高層級檢視物件的意圖或詳細資訊。
* 提出問題並讓[!UICONTROL AI小幫手]在Experience League上尋找答案。
* 根據您的提示取得產生的公式。 您也可以解決計算欄位中無效自訂運算式的錯誤。
* 尋找專案、任務和問題。

[了解更多](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Firefly相容性： **否**

## 其他資源

* [信任中心上的AI資源](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**免責宣告：**&#x200B;此頁面上的資訊僅供一般參考。 我們的目標是要保持其正確性和最新狀態，但軟體和AI功能可能會經常變更。 我們並不保證資訊的完整或可靠性。 在根據此內容做出決定之前，請仔細檢查任何重要細節。
