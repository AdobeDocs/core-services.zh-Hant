---
title: 創成式人工智慧在Experience Cloud中的應用
description: 從高級別瞭解您在Experience Cloud應用程式中可以利用AI支援的功能的位置。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
feature: AI Assistant, Generative AI
topic: Artificial Intelligence
role: Admin, User
level: Beginner, Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
TQID: https://experienceleague.adobe.com/7mRkCgAhCWLxUZHj6zGC698TZPEPeetFChWoRfx5iac
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8cid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d095671a-1355-40aa-8b5f-06c33c68080bid: e1e0219c-f879-479f-8427-888ed2a6e9c2id: e4bd5f48-22a4-465d-a046-5ffb52e27856id: e9001ce2-5245-4a8e-8601-dd958009072fid: eddd9b14-83bd-4ff4-9072-54a4a484abb7id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 06923be2a98a9301a3d3e16c47c50cd34f7a05e9
workflow-type: tm+mt
source-wordcount: 2476
ht-degree: 8%

---

# 生成型人工智慧在Experience Cloud中的應用

Experience Cloud中的創成性人工智慧(genAI)可幫助您自動執行創造性和認知任務，並提高生產力。 本頁可幫助您瞭解Experience Cloud應用程式支援genAI和AI Assistant的位置，並提供連結以瞭解有關這些功能的詳細資訊。

>[!IMPORTANT]
>
>在使用Experience Cloud生成AI功能之前，必須瞭解並遵循[Adobe Experience Cloud生成AI使用手冊](https://www.adobe.com/tw/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html)。

**什麼是genAI？**

Generative AI是可建立原始內容的AI型別。 例如，它可以建立文字、影像、視訊、音訊或軟體程式碼，以回應使用者的提示或要求。

* **建立：**&#x200B;根據訓練和輸入提示從頭開始產生內容（文字、影像、音樂或視訊）的能力。 此能力是生成AI的&#x200B;_生成_&#x200B;方面。

* **生成響應：** AI提供對提示的回答或反應，通常使用其可用資料和知識儲存庫。

[!BADGE 了解更多]{type=Informative url="https://business.adobe.com/ai/adobe-genai.html" tooltip="Adobe的GenAI"}

**什麼是 [!UICONTROL AI Assistant]？**

[!UICONTROL AI Assistant]是許多Experience Cloud應用程式都支援的對話式genAI工具。 根據您使用的應用程式，使用它來快速取得&#x200B;_產品知識_&#x200B;和&#x200B;_營運深入分析_。

* **產品知識：**&#x200B;產品知識是指以Experience League上的Experience Cloud產品檔案為基礎的概念和主題。 例如，使用[目標型提示](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)來快速瞭解Experience Platform。 來自Experience League的所有回應都是可驗證的，並會透過連結引用。

* **Operational insights:**&#x200B;例如，Experience Platform中的[Operational insights](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/questions#objects-questions)引用了有關元資料對象（屬性、受眾、資料流、資料集等）的生成響應。 使用[!UICONTROL AI Assistant]，您可以在幾秒鐘內完成否則可能需要數小時或數天的時間。

>[!NOTE]
>
>許多Experience Cloud應用程式使用&#x200B;_AI Assistant_&#x200B;作為功能名稱（如下所述）。 但是，此功能只會獲取您使用的特定應用程式的資訊。 例如，中的AI Assistant提AEM供了相關的有益信AEM息。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing" tooltip="前往AI助理"}

[!BADGE 隱私、安全和治理]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/privacy" tooltip="Adobe的GenAI"}

## 支援哪些genAI功能？

以下是使用generative AI功能和AI Assistant的[!DNL Experience Cloud]應用程式彙總。 已指出產生AI功能與[Adobe Firefly](https://business.adobe.com/products/firefly-business/firefly-ai-approach.html)的相容性。

### 生成式 AI

<!--
| Product | Key AI features | Firefly Compatibility |
| ----------------| -----------------| ---------|
| GenStudio for Performance Marketing | Create personalized, on-brand content | Yes |
| Adobe Experience Manager (AEM CS) | Generate Variations, Sites Optimizer GenAI, Content Hub, Smart Tags | Yes |
| Adobe Experience Manager 6.5 | AI Assistant support | Yes |
| Adobe Experience Manager 6.5 LTS | AI Assistant support | Yes |
| Adobe Experience Platform | AI Assistant for product knowledge and operational insights | No |
| Adobe Journey Optimizer | AI Assistant, content generation (Prime/Ultimate) | Yes |
| Adobe Journey Optimizer B2B Edition | AI Assistant for product knowledge | No |
| Campaign Managed Cloud Services | Content Accelerator for cross-channel personalization | Yes |
| Customer Journey Analytics | AI Assistant, Intelligent Captions, Content Analytics | No |
| Real-Time CDP | AI Assistant for product knowledge and operational insights | No |
| Marketo | Email Designer, Dynamic Chat, Interactive Webinars | Yes |
| Workfront | AI Assistant for work management and recommendations | Yes |
-->

| **產品名稱** | **重要GenAI功能** | **Firefly相容性** |
| ------------------| -------------------------| -------------------|
| [Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home) | 使用genAI建立個人化的品牌內內容。 | 是 |
| [Adobe Experience Manager as a Cloud Service(AEMCS)](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/overview) | GenAI提供於： <ul><li>在&#x200B;**AEM Sites**&#x200B;中生成變體（[瞭解更多資訊](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)）</li><li>**站點優化程式**&#x200B;中的GenAI（[瞭解更多資訊](https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/opportunity-types/overview)）</li><li>[AEM Assets](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview?lang=en)中的[Content Hub](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/smart-tags?lang=en#ai-smart-tags)和&#x200B;**智慧標籤**</li></ul> AI助理用於： <ul><li>Experience Hub概觀頁面</li><li>Edge Delivery Services</li><li>網站</li><li>資產</li><li>表單</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | 是 |
| [Adobe Experience Manager 6.5](https://experienceleague.adobe.com/en/docs/experience-manager-65/content/ai-assistant/ai-assistant-in-aem) | AI助理用於： <ul><li>Experience Hub概觀頁面</li><li>Edge Delivery Services</li><li>網站</li><li>資產</li><li>表單</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | 是 |
| [Adobe Experience Manager6.5 LTS](https://experienceleague.adobe.com/en/docs/experience-manager-65-lts/content/ai-assistant/ai-assistant-in-aem) | AI助理用於： <ul><li>Experience Hub概觀頁面</li><li>Edge Delivery Services</li><li>網站</li><li>資產</li><li>表單</li><li>Dynamic Media</li><li>Cloud Manager</li></ul> | 是 |
| [LLM Optimizer](https://experienceleague.adobe.com/zh-hant/docs/llm-optimizer/using/home) | 創作、AI優先的應用程式，使用AI代理程式來自動識別可見度差距、自動建議改善專案，並在特定情況下自動最佳化您的網站體驗。 | 無 |
| [Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing) | 用於產品知識和操作見解的AI助理。 | 無 |
| [Adobe Journey Optimizer](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-assistant) | 用於產品知識和操作見解的AI助理。 | 無 |
| | _AJO Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;提供[產生內容](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative?lang=en)的功能，針對文字和影像提供主動式內容變數建議。 | 是 |
| [Adobe Journey Optimizer B2B edition](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview) | AI產品知識助理。 | 無 |
| [[!DNL Campaign] 托管Cloud Service](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs) | AI Assistant for Content Accelerator，可根據跨渠道（如電子郵件、SMS和推送）的營銷目標自動生成個性化、吸引人且有效的內容。 | 是 |
| **[!DNL Customer Journey Analytics]** | GenAI用於：<ul><li> [智慧型字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions?lang=en)：深入瞭解最常用的Workspace視覺效果。</li><li>[Content Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/report?lang=en#template)：自動指派資產中繼資料。</li></ul> AI助理用於：<ul><li>[產品知識](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant?lang=en) </li><li>[產品支援代理](agentic-ai.md) </li><li>[Data Insights代理](agentic-ai.md)</li></ul> | 無 |
| [REAL-TIME CDP](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home) | Experience League產品知識的AI助理。 它也能提供營運深入分析。 | 無 |
| **[!DNL Marketo]** | GenAI可在電子郵件Designer(帶Firefly)、[Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview?lang=en)和[互動式網路研討會](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai?lang=en)中找到。 Marketo Engage的<br> AI小幫手[電子郵件Designer](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/ai-assistant) | 是 |
| [Adobe Target](https://experienceleague.adobe.com/en/docs/target/using/introduction/assistant-ai/ai-assistant) | 產品知識的AI助理。 | 無 |
| [Workfront](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) | AI助理以提供應用程式內資訊和建議。 | 是 |

**注意：** [!DNL Experience Platform Agents]已在Experience Cloud中的[AI代理程式中說明](agentic-ai.md)。

## 如何在Experience Cloud中使用創作AI？

以下各節將更詳細地說明如何在特定應用程式中使用genAI或AI Assistant。 提供進一步瞭解的連結。

### GenStudio for Performance Marketing

+++詳細資料

[!DNL GenStudio for Performance Marketing]是創作AI應用程式，旨在協助企業行銷團隊建立、啟用和最佳化跨管道（例如付費媒體、電子郵件和顯示廣告）的品牌上行銷活動內容。

效能行銷人員可使用自然語言提示來產生個人化、符合品牌規範的資產。 GenStudio for Performance Marketing可加快行銷活動的執行速度、在不影響品牌完整性的情況下擴展內容生產，並提供效能分析以提高整體投資報酬率。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home" tooltip="前往GenStudio for Performance Marketing"}

+++

### [!DNL Experience Manager]

+++詳細資料

以下幾節簡要描述了在應用中產生式人工AEM智慧。

#### 雲服務在AEM中的生成人工智慧

AdobeAdobe Experience Manager(AEM)as a Cloud Service的創成式人工智慧使品牌能夠在編輯介面中通過複製和影像生成創造高效能體驗。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generative-ai-in-aem" tooltip="前往AEM CS中的GenAI"}

#### AEM CS中的AI助理

[!DNL Experience Manager as a Cloud Service]中的AI Assistant可協助您即時取得AEM產品相關問題的答案（適用於所有使用者），並自動建立支援票證（適用於支援管理員）。

AI助理在下列位置支援AEM as a Cloud Service：

* Experience Hub概觀頁面
* Edge Delivery Services
* 網站
* 資產
* 表單
* Dynamic Media
* Cloud Manager

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-assistant/ai-assistant-in-aem" tooltip="轉到中的AI助AEM理"}

#### Experience Manager Sites

在AEM Sites中，您可以使用&#x200B;_[!UICONTROL Generate Variations]_。 此功能會使用產生式人工智慧，根據您的輸入提示建立內容變異。 提示是由Adobe提供，或由您建立及管理。

建立變化後，您可以在網站上使用該內容，並使用Edge Delivery Services中的[Experimentation](https://www.aem.live/docs/experimentation)功能來測量其成功。 您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。

**輸入和輸出範例**

輸入欄位包括：

* 要產生的變數數量
* 對象Source
* 對象目標
* 其他內容
* 客戶驅動的提示

輸出是生成的內容或市場拷貝。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor" tooltip="前往在Experience League上產生變數"}

#### 站點優化程式

AEM Sites Optimizer使用生成式AI來分析和改進Web體驗的效能和有效性。 這些洞見將分為關鍵機會領域：參與、流量獲取、安全態勢和站點健康。 每個類別都會反白標示增強網站的特定方式，包括增加訪客互動、改善可發現性、增強安全性，或維持網站穩定性。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-sites-optimizer/content/opportunity-types/overview" tooltip="前往Experience League上的Sites Optimizer"}

#### Experience Manager Assets

在AEM Assets中，您可以在&#x200B;**Content Hub**&#x200B;和&#x200B;**AI產生的智慧標籤**&#x200B;中使用產生式AI。

**內容中心**

[!UICONTROL Content Hub]可作為[!DNL Experience Manager Assets as a Cloud Service]的一部分用於使組織及其業務合作夥伴對品牌內容的訪問民主化。 其著重於大規模散發資產以供啟用，以及建立品牌內內容變體，以提升行銷靈敏度。

在Content Hub中，您可以使用Adobe Express建立內容（如果您有Adobe Express許可權）。 您可以使用簡單的工具編輯現有內容、使用範本和品牌元素產生品牌上的變化，以及使用[!DNL Adobe Firefly]的最新GenAI功能建立內容。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/content-hub/product-overview" tooltip="前往Experience League上的Content Hub"}

**智慧標籤**

AI可以自動將描述性標籤指派給數位資產，而不依賴手動輸入。 這些AI產生的標籤可增強中繼資料品質，讓資產更容易搜尋、分類和推薦。

例如，如果資產是影像，AI可以識別對象、場景、情緒甚至品牌標識。 它可以產生相關標籤，例如&#x200B;_sunset_、_beach_、_vacation_&#x200B;或&#x200B;_微笑_。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/smart-tags#ai-smart-tags" tooltip="瞭解智慧標籤"}

+++

### LLM Optimizer

+++詳細資料

Adobe LLM Optimizer是創作AI優先的應用程式，適用於Generative Engine Optimization，旨在協助品牌在AI驅動的搜尋環境中提升可見度、準確性和影響力。 它提供AI產生之答案中品牌存在感的深入分析、提供規範性內容建議，並自動化最佳化修正。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/llm-optimizer/using/home" tooltip="瞭解LLM Optimizer"}

+++

### Experience Platform

+++詳細資料

Adobe Experience Platform中的AI助理是聊天工具，可幫助您在Adobe應用程式中更快速地工作。 您可以使用它來：

* 瞭解產品如何運作
* 取得協助解決問題
* 搜尋有關您的資料和設定的資訊和見解

AI助理可在Experience Platform、Real-Time Customer Data Platform、Adobe Journey Optimizer和Customer Journey Analytics中使用。 （如下所述）

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing" tooltip="Adobe Experience Platform中的AI助理"}

+++

### Adobe [!DNL Journey Optimizer]

+++詳細資料

在[!DNL Journey Optimizer] (AJO)中，您可以使用[AI助理](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-assistant)來取得&#x200B;_產品知識_&#x200B;和&#x200B;_營運深入分析_ （測試版）。

#### 在AJO中使用AI助理的範例

以下是產品知識的輸入範例：

* _一個Journey Optimizer沙箱中可以有多少個已上線活動？_

  輸出是從Experience League和其他Adobe資料存放區產生。

以下是運算深入分析的輸入範例：

* _過去七天已建立多少歷程？_

  對於輸出，AI Assistant查詢客戶特定的資料存放區。 資料存放區包含有關[!UICONTROL Journeys]的集中式作業資料。 此功能與客戶無關，只會從商業物件提取中繼資料。 它不會存取您沙箱中的資料。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer/using/get-started/ai-assistant" tooltip="瞭解AJO中的AI助理"}

#### 用於產生內容的AI助理（AJO Prime和Ultimate）

在AJO _Prime_&#x200B;和&#x200B;_Ultimate_&#x200B;中，您可以使用[內容產生](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)來產生內容，為文字和影像提供主動式內容變數建議。

此功能適用於電子郵件、推播通知、網頁、內容和SMS頻道。 它提供提示式文字和影像產生。 AJO Prime和Ultimate中內容產生的輸出不會受到任何影響。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative" tooltip="瞭解AJO中的AI助理"}

+++

### [!DNL Journey Optimizer B2B Edition]

+++詳細資料

Journey Optimizer B2B edition使用[!UICONTROL AI Assistant]來協助您瞭解產品知識。

範例輸入：

* _如何在帳戶歷程中傳送電子郵件？_

  產品知識輸出是從Experience League提取。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview" tooltip="瞭解AJO中的AI助理"}

+++

### [!DNL Customer Journey Analytics]

+++詳細資料

Customer Journey Analytics可讓您透過以下方式使用創作AI或AI助理：

* 產品知識的[AI助理](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)。
* [智慧型字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)可提供自然語言中最常用Workspace視覺效果的關鍵深入分析。
* [內容分析](https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/report#template)，自動分配每個資產元資料。

**AI 助理**

從Experience League中發現產品知識。 如果您是新用戶，請快速學習Customer Journey Analytics概念，並隨身瞭解產品和功能。 例如：

* _如何在帳戶旅程中發送電子郵件？_

經驗豐富的用戶可以獲得高級使用案例或學習快速執行任務的策略。 您可以快速瞭解概念、疑難排解問題或搜尋資訊。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant" tooltip="瞭解CJA中的AI助理"}

**智慧型字幕**

您可以在&#x200B;_中使用_&#x200B;智慧型字幕[!DNL Customer Journey Analytics]來取得最常用Workspace視覺效果的自然語言深入分析。 智慧型字幕是需要敘述和上下文以與其他使用者分享的分析師的理想選擇。 業務用戶可以利用它快速發現高級別的收穫。

例如：

* **輸入：**&#x200B;在CJA中，執行支援的視覺效果（包括折線圖、面積圖、長條圖、流量或流失），然後按一下&#x200B;**[!UICONTROL Intelligent captions]**。

* **輸出：**&#x200B;檢視自動產生的自然語言註解，顯示內容與主要內容。 接著，您可對產生的資料執行動作，例如檢閱、複製資料並與組織共用。 [檢視方式](https://video.tv.adobe.com/v/3420131/?quality=12&learn=on#_blank)

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions" tooltip="瞭解智慧型字幕"}

**內容分析**

內容分析使用AI和GenAI自動分配每個資產元資料，如主題、場景、前景顏色等。 屬性是AI分配的元資料標籤，描述資產或體驗中的內容。

例如：前景`color: red`是自動指派的屬性。 視覺效果可協助您識別哪些資產屬性對轉換的貢獻最大。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/analytics-platform/using/content-analytics/report/report#template" tooltip="瞭解Content Analytics"}

+++

### [!DNL Real-Time CDP]

+++詳細資料

Real-Time CDP使用[!UICONTROL AI Assistant]來幫助您瞭解來自Experience League的產品知識。 它還提供運營洞察力（測試版）。 [!UICONTROL AI Assistant]查詢包含集中化操作資料的特定於客戶的操作洞察資料儲存，該資料儲存在您的AEP沙箱中分區。 系統僅從屬性、訪問群體、資料流、資料集、目標、架構和源中提取元資料，並且不訪問沙箱中的資料。

例如，如果您查詢某個受眾，則[!UICONTROL AI Assistant]可以訪問該受眾的名稱和其他關聯元資料，但無法訪問該受眾中的配置檔案。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home" tooltip="瞭解Real-Time CDP"}

+++

### [!DNL Campaign]受管理的雲端服務

+++詳細資料

Campaign Managed Cloud Services使用[!UICONTROL AI Assistant]來產生內容。 此功能可讓您根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對品牌概述的樣式、版面、色調等最佳化。 您可以在電子郵件、簡訊和推播等管道間使用它。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs" tooltip="瞭解AJO中的AI助理"}

+++

### [!DNL Marketo]

+++詳細資料

在Marketo中，互動式網路研討會和Dynamic Chat提供generative AI。 AI助理可在電子郵件Designer中使用。

**互動式網路研討會**

為您錄製的網路研討會自動產生章節和摘要，讓對象更容易存取和導覽。 功能包括：

* 自動產生章節
* AI產生的文字摘要
* 可編輯的內容 — 修改產生的章節和摘要
* 輕鬆整合 — 將HTML程式碼複製到您選取的網頁編輯器，以將章節和摘要新增至您的登陸頁面

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/events/interactive-webinars/gen-ai" tooltip="瞭解互動式網路研討會"}

**DYNAMIC CHAT**

Adobe Dynamic Chat中由創作AI支援的功能可讓您最佳化銷售代理的生產力、深入瞭解網站的訪客意圖，並以安全的方式回應訪客問題。 您可以預先核准問題、答案和交談摘要。 Dynamic Chat包含免費和付費版本。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview" tooltip="瞭解Dynamic Chat"}

**電子郵件設計工具**

Marketo Engage [!UICONTROL AI Assistant]中的[!UICONTROL Email Designer]可協助您建立現代、高效且直覺式的電子郵件。 透過 Adobe 的生成式 AI 技術和提示資料庫，並搭配 Firefly 來產生影像，協助針對特定的人物誌/購買群組、行銷歷程階段、溝通策略、語調等建立適當的內容，便能打造出這樣的電子郵件。也可以使用特定品牌資產來建立內容。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/email-marketing/email-designer/ai-assistant" tooltip="瞭解Dynamic Chat"}

**GenStudio for Performance Marketing**

Marketo與GenStudio for Performance Marketing整合

+++

### [!DNL Workfront]

+++詳細資料

[!UICONTROL AI Assistant]中的[!DNL Workfront]會提供應用程式內資訊和建議，協助您完成工作。 您可以：

* 取得某些物件的摘要，讓您以高層級檢視物件的意圖或詳細資訊。
* 提出問題並讓[!UICONTROL AI Assistant]在Experience League上尋找答案。
* 根據您的提示取得產生的公式。 您也可以解決計算欄位中無效自訂運算式的錯誤。
* 尋找專案、任務和問題。

[!BADGE 了解更多]{type=Informative url="https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview" tooltip="瞭解Workfront中的AI助理"}

+++

## 其他資源

+++詳細資料

* [信任中心上負責的AI資源](https://www.adobe.com/tw/trust/responsible-ai.html)<!-- * [Customer AI Propensity Scoring Model Card](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/model-cards/ai-model-cards/customer-ai) -->

+++

<!--
## More help on this topic

* [AI in Experience Cloud](https://experienceleague.adobe.com/en/docs/ai) documentation home
-->

**免責聲明：**&#x200B;此頁上的資訊僅供參考。 儘管我們努力確保資訊保持準確和最新，但軟體和生成的人工智慧特徵可能經常變化。 因此，Adobe並不保證資訊在任何時候的完整性、準確性或可靠性。 在根據此內容做出決策之前，請驗證任何重要詳細資訊。
