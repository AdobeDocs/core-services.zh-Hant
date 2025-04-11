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
source-git-commit: 4d784762d7d533b672e0cfa6944a3f26ebca0eaa
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 5%

---

# Experience Cloud 應用程式中的 AI

本頁可協助您瞭解Experience Cloud應用程式如何使用創作AI，以及在何處尋找應用程式專屬資訊。 瞭解問題、提示以及輸入和輸出模型的類別。

## 關於產生AI和AI助理

Generative AI是一種人工智慧，可以&#x200B;_建立_&#x200B;新內容和&#x200B;_回應_&#x200B;您的陳述和問題（提示）：

* **建立：** 指 AI 根據其培訓和輸入提示從頭開始生成新內容（文本、圖像、音樂或視頻）的能力。 此功能是generative AI的&#x200B;_generative_&#x200B;方面。

* **回應：**&#x200B;是指提供特定問題、陳述式或提示的答案或回應的AI，通常會利用其知識或推理能力。

某些Experience Cloud應用程式會利用創作AI，協助新使用者快速取得產品知識，而經驗豐富的使用者只需幾秒鐘就能發現營運深入分析，而非數小時。

### AI 助理

[AI小幫手](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)是Experience Platform和相關應用程式支援的對話工具。 使用它可以加速您的工作流程、改善您的產品知識、疑難排解問題，或搜尋資訊。 AI Assistant可讓您在數秒內發現營運深入分析，而非數小時。

所有產品知識答案都可驗證，並附有Experience League中產品檔案的連結加以引用。 [瞭解AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)以及目標提示型別，以便充分利用AI小幫手。

## 使用AI的Experience Cloud應用計畫

>[!TIP]
>
>Subhead版本（只是個開始）。..


* [Adobe GenStudio for Performance Marketing](#gspm)
* [Adobe Experience Manager Sites (Cloud Service)](#aem-sites)
* [Adobe Journey Optimizer](#journey-optimizer)
* [Adobe Journey Optimizer Prime和Ultimate](#ajo-prime-ultimate)

### GenStudio for Performance Marketing {#gspm}

[GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)是創作AI導向的平台。 它透過創作AI功能注入內容建立生命週期，轉變行銷內容的建立、檢閱、共用及分析方式。

_GenStudio for Performance Marketing Create_&#x200B;運用Adobe GenAI的強大功能，讓行銷人員和分散的團隊能夠建立高效能且符合品牌的體驗。 產生以下專案的內容：

* 電子郵件
* 中繼廣告
* LinkedIn廣告
* 顯示廣告
* 橫幅

您可以使用範例、客戶角色和產品的說明以及品牌指引，針對您的品牌訓練GenStudio for Performance Marketing。 [了解更多。](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)

**與Adobe Firefly的相容性：**&#x200B;已規劃

### Experience Manager Sites {#aem-sites}

AEM Sites使用[產生變數](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)。 生成變體使用生成式 AI 根據提示創建內容變體。 這些提示是由[Adobe](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started)提供，或由[使用者](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)建立及管理。

创建变体后，您可以在網站上使用該內容，並使用邊緣交付服務的實驗功能測量其成功。

**輸入：** 輸入欄位包括：

* 要產生的變數數
* 物件來源
* 對象目標
* 其他內容
* 客戶導向提示

**輸出：**&#x200B;產生的內容/市場副本。 您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。

請參閱[產生影像](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)。

**與Adobe Firefly的相容性：**&#x200B;是

## Journey Optimizer {#journey-optimizer}

Journey Optimizer使用[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)來回答兩類問題：

**產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。 範例：

* 一個Adobe Journey Optimizer沙箱中可以有多少個已上線活動？

**Operational Insights (Beta)** — 查詢客戶特定的營運分析資料存放區，該資料存放區包含有關歷程的集中營運資料，依客戶的沙箱分割。 僅從業務物件提取中繼資料，不訪問沙箱中的數據。

* 在過去七天內建立了多少個歷程？

作Insights輸出取決於從客戶的業務物件中提取中繼資料。

Journeys 是 Journey Optimizer 中唯一可用於 AI Assistant 的物件，中繼資料是從當前沙盒中提取的。

有關詳細資訊，請參閱 [使用 AI 助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) 和 [現場準備](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) 。

**與Adobe Firefly的相容性：**&#x200B;否

## Journey Optimizer Prime和Ultimate {#ajo-prime-ultimate}

Journey Optimizer Prime和Ultimate使用Content Accelerator的[AI Assistant](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)為文字和影像提供主動式內容變數建議。

此功能適用於電子郵件、推播、網頁和簡訊頻道。 它提供提示式文字和影像產生。

**電子郵件** — 產生完整電子郵件、僅限文字或僅限影像。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email)

**推播通知** — 產生完整推播通知、僅限文字或僅限影像。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push)

**簡訊** — 產生完整簡訊或僅傳送文字。 [了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms)

**網頁** — 產生網頁影像或網頁文字。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web)

**內容** — 產生各種傳訊行銷活動的內容。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)

**注意：** AJO Prime和Ultimate中內容加速器的輸出不會受到任何影響。

**與Adobe Firefly的相容性：**&#x200B;是

## Journey Optimizer B2B 版 {#ajo-b2b}

使用[AI助理](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)進行產品知識提示。

**產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。 | <ul><li>**輸入：**&#x200B;如何在帳戶歷程中傳送電子郵件？</li><li>**輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul>   | 否   |

## 使用AI的Experience Cloud應用計畫

>[!TIP]
>
>表格版本……


瞭解Experience Cloud應用程式如何使用Generative AI或AI Assistant，以及是否支援Adobe Firefly。

| 應用程式 | 如何使用創作AI | 範例 | Adobe Firefly？ |
|----------|------------|-----------|----------------|
| GenStudio for Performance Marketing | [GenStudio for Performance Marketing](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)是創作AI導向的平台。 它透過創作AI功能注入內容建立生命週期，轉變行銷內容的建立、檢閱、共用及分析方式。<br>您可以使用範例、客戶角色和產品的說明，以及品牌准則，來訓練您品牌的GenStudio for Performance Marketing。 | _GenStudio for Performance Marketing建立_&#x200B;可讓您產生電子郵件、中繼廣告、LinkedIn廣告、顯示廣告和橫幅的內容。 <br>**輸入：** <ul><li>使用範本開始內容建立流程。 </li><li>新增品牌、產品和角色（指引）和內容（資產）等引數來塑造產生的體驗。 </li><li>輸入描述性提示，說明您要產生的內容或體驗。 [了解更多...](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/overview)</li></ul> | 是 |
| Adobe Experience Manager Sites (Cloud Service) | AEM Sites使用 [產生變數](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations)。 <br>產生變數使用產生AI根據提示建立內容變數。 這些提示要麼由Adobe Systems提供，要麼由使用者創建和管理。 | 创建变体后，您可以在網站上使用該內容，並使用邊緣交付服務的實驗功能測量其成功。 <br>**輸入：** 輸入欄位包括要生成的變數數;物件來源/Target;其他上下文和客戶驅動的提示。 <ul><li>[Adobe Systems提示範本](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#get-started) </li><li>[用戶產生的提示](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#create-prompt)</li></ul> **輸出：**&#x200B;產生的內容/市場副本。 您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。 請參閱[產生影像](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations#generate-image)。 | 是 |
| Adobe Journey Optimizer | Journey Optimizer使用[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)來回答兩類問題：<ul><li>**產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。 </li><li>**Operational Insights (Beta)** — 查詢客戶特定的營運分析資料存放區，該資料存放區包含有關歷程的集中營運資料，依客戶的沙箱分割。 只會從商業物件提取中繼資料，不會存取沙箱中的資料。</li></ul> | <ul><li>**產品知識輸入：**&#x200B;一個Adobe Journey Optimizer沙箱中可以有多少上線活動？</li><li>**產品知識輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 </li><li>**營運見解輸入：**&#x200B;過去七天內已建立多少歷程？ </li><li>**營運見解輸出：**&#x200B;營運見解輸出取決於從客戶的業務物件提取的中繼資料。 歷程是 AJO 中唯一可用的物件，中繼資料是從當前沙盒中提取的。 </li></ul> 請參閱 [使用 AI 助手](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant) 和 [現場準備](https://fieldreadiness-adobe.highspot.com/items/6661f1c132683fd5e6a8adf4?lfrm=srp.1#11) | 無 |
| 歷程優化器： _Prime_ 和 _Ultimate_ | [内容加速器](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative) 的 AI 助手為文本和圖像提供主動內容變體建議。 它可用於電子郵件、推送、Web 和 SMS 通道。 這項新功能提供提示式文字和影像產生功能。 | <ul><li> **電子郵件** — 產生完整電子郵件、僅限文字或僅限影像。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-email) </li><li> **推播通知** — 產生完整推播通知、僅限文字或僅限影像。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-push) </li><li> **簡訊** — 產生完整簡訊或僅傳送文字。 [了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-sms) </li><li> **網頁** — 產生網頁影像或網頁文字。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-web) </li><li> **內容** — 產生各種傳訊行銷活動的內容。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/generative-experimentation)</li></ul> **注意：** AJO Prime和Ultimate中內容加速器的輸出不會受到任何影響。 | 是 |
| Journey Optimizer B2B 版 | 使用[AI小幫手](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)並有一個問題類別： <br> **產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。 | <ul><li>**輸入：**&#x200B;如何在帳戶歷程中傳送電子郵件？</li><li>**輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 [了解更多...](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/get-started/ai-assistant)</li></ul> | 無 |
| Campaign Managed Cloud Services | [內容加速器的AI Assistant](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)會根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對跨管道（例如電子郵件、簡訊、推播）的品牌簡介樣式、版面配置、色調等最佳化。 | <ul><li> **電子郵件** — 產生完整電子郵件、僅限文字或僅限影像。 [了解更多](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-content) </li><li> **簡訊** — 僅產生完整簡訊或文字。 [了解更多...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-sms) </li><li> **推播** — 製作吸引人的訊息並產生內容。 [了解更多...](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-push) </li></ul> **注意：**&#x200B;來自Campaign Managed Cloud Services中內容加速器的輸出不會有任何損失。 | 是 |
| Customer Journey Analytics | CJA使用[AI助理](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant)協助您探索Experience League的產品知識和深入分析。 <br>例如，新使用者可以利用它來瞭解Customer Journey Analytics概念，並且將自己帶入你不熟悉的產品和功能。 <br>經驗豐富的使用者可以使用AI助理來呈現更進階的使用案例或提示與技巧，並以快速的速度執行工作。 瞭解概念、疑難排解問題或搜尋資訊。 [了解更多...](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/ai-assistant#knowledge) | <ul><li>**產品知識輸入：**&#x200B;如何建立計算量度？ </li><li> **產品知識輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 </li></ul> | 無 |
| Customer Journey Analytics | [智慧型字幕](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)可為Workspace視覺效果中的線條視覺效果提供自然語言深入分析。 | <ul><li>**輸入：**&#x200B;線條視覺效果。 當您按一下&#x200B;**智慧型字幕**&#x200B;時，字幕會根據這類線條視覺效果自動產生。 </li><li> **輸出：**&#x200B;自動產生的自然語言字幕。</li></ul> | 無 |
| Real-Time CDP | 使用[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)協助您探索Experience League的產品知識和深入分析。 它會查詢資料庫，並將資料庫中的資料轉譯成人類看得懂的答案。 兩個問題類別： <br> **產品知識** — 查詢Adobe資料存放區(例如Experience League產品檔案)以取得產品insight。 此輸出不受客戶限制。<br> **Operational Insights (Beta)** — 查詢包含集中式營運資料(依客戶的AEP沙箱分割)的客戶特定營運分析資料存放區。 僅從屬性、受眾、資料流、資料集、目的地、結構描述和來源提取中繼資料，不會存取沙箱中的資料。 <br>例如，針對有關對象的查詢，[!DNL AI Assistant]可以存取對象名稱和其他關聯的中繼資料，但無法存取該對象內的設定檔。 | <ul><li>**產品知識輸入：**&#x200B;如何計算設定檔豐富度？ </li><li>**產品知識輸出：**&#x200B;來自Experience League的產品知識提取（公開檔案）。 </li><li> **操作深入分析輸入：**&#x200B;我有多少資料集？ </li><li> **Operational Insights輸出：** Operational Insights輸出取決於從客戶的業務物件（屬性、受眾、資料流、資料集、目的地、結構描述和來源）提取的中繼資料，並包括指向包含查詢資料的特定UI頁面的連結。 </li></ul>如需範例，請參閱Experience Platform中[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)中的&#x200B;_產品知識_&#x200B;和&#x200B;_營運分析_&#x200B;輸入表格 | 無 |
| Marketo | [Dynamic Chat](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/dynamic-chat-overview)使用自訂和預先核准的問題與答案，以及交談摘要，建立AI輔助交談 | <ul><li> **產生問題：**&#x200B;提供URL，內容會從中擷取並用於產生問題/回應。 </li><li> **交談摘要：**&#x200B;產生交談摘要。 </li></ul> [了解更多...](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/response-library) | 無 |
| Workfront | [Workfront 中的 AI 助手](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview) 通過在自然語言對話中提供應用內資訊和建議來説明您完成工作。 AI 助手提供以下功能：匯總專案/任務/問題/檔，提供從Experience League上的 Workfront 文檔中提取的說明或參考資訊，生成或優化計算自定義欄位的公式。 | <ul><li>**匯總專案輸入：** 匯總此專案 </li><li> **摘要專案輸出：**&#x200B;傳回專案用途和狀態的簡短描述，提供已完成和仍在擱置中的任務範例，並提供一些其他詳細資訊和附註。</li><li> **產生/調整公式輸入：** 「重寫此公式以移除無效的運算式錯誤。」 </li><li> **產生/調整公式輸出：**&#x200B;產生或調整的公式。 </li></ul>**注意：** AI助理可能需要一些時間才能產生修訂後的公式，視公式的大小和複雜度而定。 | 無 |
