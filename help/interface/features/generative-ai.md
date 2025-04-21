---
title: Experience Cloud 應用程式中的 AI
description: 瞭解Experience Cloud應用程式如何使用generative AI和AI Assistant。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
hide: false
hidefromtoc: true
index: n
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 4c0e9ef974ab31a7d82a61c3a69f7d76389774f9
workflow-type: tm+mt
source-wordcount: '1314'
ht-degree: 4%

---

# Experience Cloud 應用程式中的 AI

本頁可協助您瞭解創作AI，以及如何在Experience Cloud應用程式中使用它。 瞭解哪些產品功能使用Generative AI、AI Assistant，以及是否支援Adobe Firefly。

## 關於產生AI和AI助理

創作AI是一種人工智慧，其作用不僅僅是回答問題。 它&#x200B;_建立_&#x200B;內容，並&#x200B;_回應_&#x200B;您的&#x200B;_提示_ （問題和陳述式）。

* **建立：**&#x200B;參考AI根據其訓練和輸入提示從頭開始產生新內容（文字、影像、音樂或視訊）的能力。 此功能是generative AI的&#x200B;_generative_&#x200B;方面。

* **回應：**&#x200B;是指對特定提示提供回應或回應的AI，通常會利用其知識或推理能力。

如果您是Experience Cloud的新手，則可以使用創作AI來快速獲得產品知識。 身為經驗豐富的使用者，您可以在數秒內發現營運深入分析，而非數小時。

### AI 助理

[AI小幫手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)是Experience Platform和相關應用程式支援的對話工具。 使用它可以加速您的工作流程、改善您的產品知識、疑難排解問題，或搜尋資訊。 在某些應用程式中，AI Assistant可讓您立即探索營運深入分析。

來自Experience League的產品知識回應是可驗證的，並透過連結引用。 瞭解[目標型提示](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)的型別，以充分利用AI Assistant。

## 具備支援AI之功能的應用程式

* [GenStudio for Performance Marketing](#gspm)
* [在AEM Sites (Cloud Service)中產生變數](#aem-sites)
* [Journey Optimizer 的 AI 助理](#journey-optimizer)
* [Adobe Journey Optimizer Prime和Ultimate](#ajo-prime-ultimate)
* [Journey Optimizer B2B 版](#ajo-b2b)
* [Journey Optimizer Prime和Ultimate中的AI助理](#ajo-prime-ultimate)
* [Journey Optimizer B2B edition中的AI助理](#ajo-b2b)
* [Campaign Managed Cloud Services中的AI助理](#campaign-cs)
* [Customer Journey Analytics中的AI助理](#cja)
* [Customer Journey Analytics中的智慧型字幕](#cja-captions)
* [Real-Time CDP中的AI助理](#rtcdp)
* [Marketo中的Dynamic Chat](#marketo)
* [Workfront中的AI助理](#workfront)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)不是功能，而是產生式AI導向的平台。 其創造性AI功能可改變行銷內容的建立、稽核、共用及分析方式。

在[建立](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)首頁上，您可以建立高效能且符合品牌標準的體驗。 產生以下專案的內容：

* 電子郵件
* 中繼廣告
* LinkedIn廣告
* 顯示廣告
* 橫幅

您也可以使用範例、客戶角色和產品的說明以及品牌指引，針對您的品牌訓練GenStudio for Performance Marketing。 [了解更多...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**與Adobe Firefly相容：**&#x200B;已規劃

### 在Experience Manager Sites中產生變數 {#aem-sites}

在AEM Sites中[產生變數](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)使用產生AI根據提示建立內容變數。 這些提示是由[Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)提供，或由[使用者](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)建立及管理。

建立變化後，您可以在網站上使用內容，並使用Edge Delivery Services中的Experimentation功能來衡量其成功與否。

### 輸入和輸出欄位

輸入欄位包括：

* 要產生的變數數量
* 對象Source
* 對象目標
* 其他內容
* 客戶導向提示

輸出是產生的內容或市場副本。

您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。 [了解更多...](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)

**與Adobe Firefly相容：**&#x200B;是

## Journey Optimizer 的 AI 助理 {#journey-optimizer}

在Journey Optimizer中，AI助理可以協助您取得產品知識和營運見解。

**產品知識：** AI助理查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 輸出不受客戶限制。

範例：

* _一個Adobe Journey Optimizer沙箱中可以有多少個已上線活動？_

**Operational Insights (Beta)** - AI Assistant會查詢客戶特定的營運分析資料存放區，該資料存放區包含有關歷程的集中營運資料，依客戶的沙箱分割。 此功能只會從商業物件提取中繼資料，不會存取沙箱中的資料。

範例提示：

* _過去七天已建立多少歷程？_

「營運分析」輸出取決於從客戶的業務物件中提取的中繼資料。 此輸出不受客戶限制。

_Journeys_&#x200B;是Journey Optimizer中唯一可用於AI助理的物件，而中繼資料是從目前沙箱中提取。 [深入了解...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

**與Adobe Firefly相容：**&#x200B;否

## Journey Optimizer Prime和Ultimate中的AI助理 {#ajo-prime-ultimate}

Journey Optimizer Prime和Ultimate使用Content Accelerator的[AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)為文字和影像提供主動式內容變數建議。

此功能適用於[電子郵件](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)、[推播通知](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)、[網頁](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)、[內容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)及[簡訊](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms)頻道。 它提供提示式文字和影像產生。

**注意：** AJO Prime和Ultimate中內容加速器的輸出不會受到任何影響。

**與Adobe Firefly相容：**&#x200B;是

## Journey Optimizer B2B edition中的AI助理 {#ajo-b2b}

Journey Optimizer B2B edition會根據您的產品知識提示，使用[AI助理](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)來協助您瞭解產品知識。

**產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。

* **輸入：**&#x200B;如何在帳戶歷程中傳送電子郵件？

* **輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/question-guidance)

**與Adobe Firefly相容：**&#x200B;否

## Campaign Managed Cloud Services中的AI助理 {#campaign-cs}

Campaign Managed Cloud Services使用[內容加速器](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)的AI助理。 此功能可讓您根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對品牌概述的樣式、版面、色調等最佳化。 您可以跨如[電子郵件](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content)、[簡訊](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms)和[推播](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push)等管道使用它。

**注意：**&#x200B;來自Campaign Managed Cloud Services中內容加速器的輸出不會有任何損失。

**與Adobe Firefly相容：**&#x200B;是

## Customer Journey Analytics中的AI助理 {#cja}

Customer Journey Analytics使用[AI助理](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)協助您探索Experience League的產品知識和深入分析。

**範例提示：**&#x200B;如何建立計算量度？

新使用者可以使用此指南來瞭解Customer Journey Analytics概念，並且瞭解您不熟悉的產品和功能。

經驗豐富的使用者可以使用AI Assistant來呈現更進階的使用案例或提示和技巧，並以更快的速度執行任務。 瞭解概念、疑難排解問題或搜尋資訊。 [了解更多...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge)

**與Adobe Firefly相容：**&#x200B;否

## Customer Journey Analytics中的智慧型字幕 {#cja-captions}

Customer Journey Analytics中的[智慧型字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)提供最常使用的Workspace視覺效果的自然語言深入分析。

**與Adobe Firefly相容：**&#x200B;否

## Real-Time CDP中的AI助理 {#rtcdp}

Real-Time CDP使用[AI助理](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)協助您探索Experience League的產品知識和深入分析。 [取得提問提示](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions)。

此外，還提供營運深入分析（測試版）。 AI Assistant會查詢客戶特定的營運見解資料存放區，該存放區包含集中式營運資料，由客戶的AEP沙箱分割。 它只會從屬性、受眾、資料流程、資料集、目的地、結構描述和來源提取中繼資料，不會存取沙箱中的資料。

例如，針對有關對象的查詢，[!DNL AI Assistant]可以存取對象名稱和其他關聯的中繼資料，但無法存取該對象內的設定檔。

例如：

* 輸入： _我有多少資料集？_

* 回應： Operational Insights輸出取決於從客戶的業務物件（屬性、受眾、資料流程、資料集、目的地、結構描述和來源）提取的中繼資料，並包括指向包含查詢資料的特定UI頁面的連結。

如需更多範例，請參閱Experience Platform中[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)中的&#x200B;_產品知識_&#x200B;和&#x200B;_營運分析_&#x200B;輸入表格

**與Firefly相容：**&#x200B;否

## Marketo中的Dynamic Chat {#marketo}

Adobe Dynamic Chat中由創作AI支援的功能可讓您最佳化銷售代理的生產力、深入瞭解網站的訪客意圖，並以安全的方式回應訪客問題。 您可以預先核准問題、答案和交談摘要。 [了解更多...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

**與Firefly相容：**&#x200B;否

## Workfront中的AI助理 {#workfront}

Workfront中的AI助理可提供應用程式內資訊和建議，協助您完成工作。 您可以：

* 取得某些物件的摘要，讓您以高層級檢視物件的意圖或詳細資訊。
* 提出問題並讓[!DNL AI Assistant]在Experience League上尋找答案。
* 根據您的提示取得產生的公式。 您也可以解決計算欄位中無效自訂運算式的錯誤。
* 尋找專案、任務和問題。

[了解更多...](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

**與Firefly相容：**&#x200B;否

<!-- ## Experience Cloud applications that use AI

Learn how Experience Cloud applications use generative AI or AI Assistant, and whether Adobe Firefly is supported. 

| Application | How Generative AI Is Used | Examples | Adobe Firefly? |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/home) is a generative AI-driven platform. It infuses the content creation lifecycle with generative AI capabilities that transform how marketing content is created, reviewed, shared, and analyzed.<br>You can train GenStudio for Performance Marketing on your brand using examples, descriptions of customer personas and products, and brand guidelines. |_GenStudio for Performance Marketing Create_ lets you generate content for emails, Meta ads, LinkedIn ads, display ads, and banners. <br>**Inputs:** <ul><li>Use templates to start the content creation process. </li><li>Add parameters like Brands, Products, and Personas (guidelines) and Content (assets) to shape the generated experience. </li><li>Enter descriptive prompts that describe the context or experience you intend to generate. [Learn more...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> |Yes |
|Adobe Experience Manager Sites (Cloud Service)  | AEM Sites uses [Generate Variations](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations). <br>Generate Variations uses generative AI to create content variations based on prompts. These prompts are either provided by Adobe or created and managed by users. |After creating variations, you can use the content on your website and measure its success using the Experimentation functionality of Edge Delivery Services. <br>**Input:** Input fields include Number of Variations to generate; Audience Source / Audience Target; Additional Context, and customer-driven prompts. <ul><li>[Adobe prompt template](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[User generated prompt](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **Output:** Generated Content / Market Copy. You also have the option to generate images in Adobe Express using the generative AI capabilities of Firefly. See [Generate Image](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image). | Yes|
| Adobe Journey Optimizer |Journey Optimizer uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) with two classes of questions:<ul><li>**Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. </li><li>**Operational Insights (Beta)** - queries a customer-specific operational insights data store that contains centralized operational data about Journeys, partitioned by the customer's sandbox. Pulls metadata only from business objects and does not access data within the sandbox.</li></ul>|<ul><li>**Product Knowledge Input:** How many live activities can I have in one Adobe Journey Optimizer sandbox?</li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li>**Operational Insights Input:** How many Journeys have been created in the last seven days? </li><li>**Operational Insights Output:** Operational Insights output depends on metadata pulled from customer's business objects. Journeys is the only object available in AJO, and metadata is pulled from the current sandbox. </li></ul> See [Work with the AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) and [Field Readiness](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | No |
| Journey Optimizer: _Prime_ and _Ultimate_  | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) brings proactive content variation suggestions for text and images. It is available for email, push, web and SMS channels. This new capability provides prompt-based text and image generation. |<ul><li> **Email** - generate a full email, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **Push Notification** - Generate a full push notification, text only or image only. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **SMS** - Generate a full SMS, or text only. [Learn more](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **Webpage** - Generate web page images or web page text. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **Content** - Generate content for various messaging campaigns. [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **Note:** Output from Content Accelerator in AJO Prime and Ultimate is indemnified. | Yes   |
| Journey Optimizer B2B Edition  | Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant) with one class of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. | <ul><li>**Input:** How do I send an email in an account journey?</li><li>**Output:** Product Knowledge pulls from Experience League (public documentation). [Learn more...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | No   |
| Campaign Managed Cloud Services | [AI Assistant for Content Accelerator](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) auto-generates personalized, engaging, and effective content based on the marketing objective with content optimized for brand outlined styles, layouts, tone, and more across channels like Email, SMS, Push. |<ul><li> **Email** - Generate a full email, text only or image only. [Learn more](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **SMS** - Generate full SMS or text only. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **Push** - Craft compelling messaging and generate content. [Learn more...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **Note:** Output from Content Accelerator in Campaign Managed Cloud Services is indemnified. | Yes  |
| Customer Journey Analytics   | CJA uses [AI Assistant](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant) to help you discover product knowledge and insights from Experience League. <br>For example, new users can use it to learn Customer Journey Analytics concepts and onboard yourself to products and features that you are unfamiliar with. <br>Experienced users can use AI Assistant to present more advanced use cases or tips and tricks and perform tasks at a fast pace. Understand concepts, troubleshoot problems, or search for information. [Learn more...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**Product Knowledge Input:** How do I build a calculated metric? </li><li> **Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li></ul> | No |
| Customer Journey Analytics    | [Intelligent Captions](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions) provides natural-language insights for line visualizations in Workspace visualizations.| <ul><li>**Input:** Line visualizations. Captions are auto-generated based on such line visualizations when you click **Intelligent captions**. </li><li> **Output:** Auto-generated natural-language captions.</li></ul>  | No             |
| Real-Time CDP |Uses [AI Assistant](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home) to help you discover product knowledge and insights from Experience League. It queries a database and translates data from the database into a human-readable answer. Two classes of questions: <br> **Product knowledge** - Queries Adobe data stores (such as Experience League product documentation) for product insight. This output is customer agnostic. <br> **Operational Insights (Beta)** - Queries a customer-specific operational insights data store that contains centralized operational data, partitioned by the customer's AEP sandbox. Pulls metadata only from Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources, and does not access data within the sandbox. <br>For example, for a query about an audience [!DNL AI Assistant] can access the name of the audience and other associated metadata but cannot access the profiles within that audience. | <ul><li>**Product Knowledge Input:** How is profile richness calculated? </li><li>**Product Knowledge Output:** Product Knowledge pulls from Experience League (public documentation). </li><li> **Operational Insights Input:** How many datasets do I have? </li><li> **Operational Insights Output:** Operational Insights output depends on metadata pulled from Customer's business objects (Attributes, Audiences, Dataflows, Datasets, Destinations, Schemas, and Sources), and includes a link to specific UI page containing queried data. </li></ul>For examples, see the _Product Knowledge_ and _Operational Insights_ input tables in [AI Assistant in Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/home)  | No |
| Marketo  | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview) creates AI-assisted conversations with customized and pre-approved questions and answers, as well as conversation summary |<ul><li> **Generate Questions:** Provide URLs from which content is extracted and used to generate questions / responses. </li><li> **Conversation Summary:** Generates a summary of a chat conversation. </li></ul> [Learn more...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library)  | No |
| Workfront | [AI Assistant](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) in Workfront helps you accomplish your work by offering in-app information and suggestions in a natural-language conversation. AI Assistant offers the following functionality: Summarizes projects/tasks/issues/documents, provides instructions or reference information pulled from the Workfront documentation on Experience League, generates or refines formulas for calculated custom fields.  | <ul><li>**Summarize Project Input:** Summarize this project </li><li> **Summarize Project Output:** Returns brief descriptions of the project's purpose and status, gives examples of tasks that are completed and that are still pending, and provides some additional details and notes.</li><li> **Generate/Refine Formula Input:** "Rewrite this formula to remove the invalid expression error." </li><li> **Generate/Refine Formula Output:** Generated or refined formula. </li></ul>**Note:** AI Assistant may take a few moments to generate the revised formula, depending on the size and complexity of the formula. | No  | -->
