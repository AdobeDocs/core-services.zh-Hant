---
title: Experience Cloud應用程式中的Generative AI
description: 瞭解generative AI (GenAI)以及Experience Cloud應用程式如何使用GenAI和 [!DNL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: f1954b7137bcd492a289969e005293b6857824ec
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 3%

---

# Experience Cloud產品中的Generative AI

本頁可協助您瞭解哪些產品支援generative AI (GenAI)、[!DNL AI Assistant]，以及Adobe Firefly是否相容。 您也可以找到在Experience Cloud應用程式中使用AI各種方式相關資訊的連結。

**關於產生AI**

Generative AI是可建立原始內容的AI型別。 例如，它可以建立文字、影像、視訊、音訊或軟體程式碼，以回應使用者的提示或要求。

* **建立：**&#x200B;根據訓練和輸入提示從頭開始產生內容（文字、影像、音樂或視訊）的能力。 此功能是generative AI的&#x200B;_generative_&#x200B;方面。

* **產生回應：** AI會針對提示提供回應或回應，通常會利用其可用的資料和知識存放庫。

**什麼是 [!DNL AI Assistant]？**

[!DNL AI Assistant]是Experience Platform和相關應用程式支援的對話工具。 使用它來快速取得&#x200B;_產品知識_，並且在支援的產品中幾乎立即取得&#x200B;_營運分析_。

* **產品知識：**&#x200B;產品知識是指以Experience League檔案為根據的概念和主題。 瞭解如何建立有效的[目標型提示](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)，以充份運用[!DNL AI Assistant]。 來自Experience League的所有回應都是可驗證的，並會透過連結引用。

* **營運分析：** [營運分析](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions#objects-questions)參考中繼資料物件（屬性、對象、資料流、資料集等）的相關回應。 透過[!DNL AI Assistant]，您可以在數秒內完成其他可能需要數小時或數天的作業。

[瞭解AI助理](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!--## Adobe Marketing Agent for Microsoft 365 Copilot 

The Adobe Marketing Agent for Microsoft 365 Copilot is a generative AI-powered assistant designed to enhance marketing workflows by integrating Adobe's marketing capabilities directly into Microsoft 365 applications such as Word, PowerPoint, Teams, and Outlook. This collaboration between Adobe and Microsoft aims to streamline marketing processes, allowing marketers to access insights and tools within their existing work environments.
Adobe for Business

Key features and capabilities:

**Audience Refinement:** Marketers can use natural language prompts within Microsoft 365 to access data and insights from Adobe Experience Platform, enabling quick audience analysis and segmentation for personalized campaigns. 

**Insight Discovery:** The agent can retrieve meaningful insights from Adobe Customer Journey Analytics, facilitating the creation of campaign performance reports directly within Microsoft apps, thus supporting informed decision-making. 

**Content Creation:** Through integration with Adobe Express, users can generate high-quality images and assets within Microsoft 365 applications, aiding in the development of presentations, documents, and social media content. 
Adobe Newsroom

**Workflow Optimization:** The agent can automate tasks in Adobe Workfront, manage content approvals, and provide real-time alerts in Microsoft Teams based on analytics data, enhancing operational efficiency. 

**Campaign Performance Monitoring:** Users can query the agent for campaign performance metrics, which can be visualized and incorporated into PowerPoint presentations for easy sharing and analysis. 
Adobe for Business

Currently in private preview, the Adobe Marketing Agent for Microsoft 365 Copilot is expected to be generally available later in 2025. This integration represents a significant step in unifying marketing tools and data, aiming to improve productivity and collaboration for marketing teams.
 -->

## Experience Cloud產品中的GenAI可用性

瞭解下列Experience Cloud應用程式如何支援產生AI或[!DNL AI Assistant]。 也指出支援Adobe Firefly。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager]](#aem)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign]受管理的雲端服務](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## Adobe GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是AI導向的平台，可讓您產生和管理行銷內容，以遵循您的品牌標準並符合您的企業政策。 產生電子郵件、中繼廣告、LinkedIn廣告、顯示廣告和橫幅的內容。

您也可以使用範例、客戶角色和產品的說明以及品牌指引，針對您的品牌訓練GenStudio for Performance Marketing。

[了解更多](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)

Adobe Firefly相容性： **是**

## Adobe [!DNL Experience Manager] {#aem}

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

[深入瞭解產生變數](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

### Experience Manager Assets

[!UICONTROL Content Hub]是[!DNL Experience Manager Assets as a Cloud Service]的一部分，可讓組織及其業務夥伴對品牌上內容的存取權進行民主化。 其著重於大規模散發資產以供啟用，以及建立品牌內內容變體，以提升行銷靈敏度。

在Content Hub中，您可以使用Adobe Express建立內容(如果您有Adobe Express許可權)。 您可以使用簡單的工具編輯現有內容、使用範本和品牌元素產生品牌上的變化，以及使用[!DNL Adobe Firefly]的最新GenAI功能建立內容。

[了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview)

Adobe Firefly相容性： **是**

## Adobe [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer] (AJO)中，您可以使用[AI助理](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)來取得&#x200B;_產品知識_&#x200B;和&#x200B;_營運深入分析_ （測試版）。

### 在AJO中使用AI助理的範例

以下是產品知識的輸入範例：

* _一個Journey Optimizer沙箱中可以有多少個已上線活動？_

  輸出是從Experience League和其他Adobe資料存放區產生。

以下是運算深入分析的輸入範例：

* _過去七天已建立多少歷程？_

  對於輸出，AI Assistant查詢客戶特定的資料存放區。 資料存放區包含有關[!UICONTROL 歷程]的集中操作資料。 此功能與客戶無關，只會從商業物件提取中繼資料。 它不會存取您沙箱中的資料。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

Adobe Firefly相容性： **否**

### 用於產生內容的AI助理(AJO Prime和Ultimate) {#ajo-prime}

在AJO _Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;中，您可以使用[內容產生](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)來產生內容，為文字和影像提供主動式內容變數建議。

此功能適用於電子郵件、推播通知、網頁、內容和SMS頻道。 它提供提示式文字和影像產生。 AJO Prime和Ultimate中內容產生的輸出不會受到任何影響。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

Adobe Firefly相容性： **是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!DNL AI Assistant]來協助您瞭解產品知識。

範例輸入：

* _如何在帳戶歷程中傳送電子郵件？_

  產品知識輸出是從Experience League提取。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

Adobe Firefly相容性： **否**

## [!DNL Campaign]受管理的雲端服務 {#campaign-cs}

Campaign Managed Cloud Services使用[!DNL AI Assistant]來產生內容。 此功能可讓您根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對品牌概述的樣式、版面、色調等最佳化。 您可以在電子郵件、簡訊和推播等管道間使用它。

**注意：**&#x200B;在Campaign Managed Cloud Services中產生內容的輸出不會有任何損失。

[了解更多](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

Adobe Firefly相容性： **是**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics可讓您透過以下方式使用創作AI：

* [!DNL AI Assistant]產品知識與深入分析
* Workspace視覺效果中的[!UICONTROL 智慧型字幕]
* AI和GenAI會自動在[!DNL Content Analytics]中指派每個資產中繼資料

**AI 助理**

探索Experience League的產品知識和深入分析。 如果您是新使用者，請快速瞭解Customer Journey Analytics概念，並熟悉產品和功能。 例如：

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

Adobe Firefly相容性： **否**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP使用[!DNL AI Assistant]協助您瞭解Experience League的產品知識。 此外，還提供營運深入分析（測試版）。 [!DNL AI Assistant]查詢客戶特定的營運分析資料存放區，該存放區包含已分割至AEP沙箱的集中營運資料。 系統只會從屬性、受眾、資料流程、資料集、目的地、結構描述和來源提取中繼資料，不會存取沙箱中的資料。

例如，如果您查詢對象，[!DNL AI Assistant]可以存取對象名稱和其他關聯的中繼資料，但無法存取該對象內的設定檔。

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

Adobe Dynamic Chat中由創作AI支援的功能可讓您最佳化銷售代理的生產力、深入瞭解網站的訪客意圖，並以安全的方式回應訪客問題。 您可以預先核准問題、答案和交談摘要。

[了解更多](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

Adobe Firefly相容性： **否**

## [!DNL Workfront] {#workfront}

[!DNL Workfront]中的[!DNL AI Assistant]會提供應用程式內資訊和建議，協助您完成工作。 您可以：

* 取得某些物件的摘要，讓您以高層級檢視物件的意圖或詳細資訊。
* 提出問題並讓[!DNL AI Assistant]在Experience League上尋找答案。
* 根據您的提示取得產生的公式。 您也可以解決計算欄位中無效自訂運算式的錯誤。
* 尋找專案、任務和問題。

[了解更多](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

Adobe Firefly相容性： **否**

## 其他資源

* [信任中心上的AI資源](https://www.adobe.com/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

**免責宣告：**&#x200B;此頁面上的資訊僅供一般參考。 我們的目標是要保持其正確性和最新狀態，但軟體和AI功能可能會經常變更。 我們並不保證資訊的完整或可靠性。 在根據此內容做出決定之前，請仔細檢查任何重要細節。
