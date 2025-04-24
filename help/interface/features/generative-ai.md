---
title: Experience Cloud 應用程式中的 AI
description: 瞭解generative AI以及Experience Cloud應用程式如何使用genAI和 [!DNL AI Assistant]。
solution: Experience Cloud
feature: AI Assistant, Generative AI
topic: Administration
role: Admin
level: Intermediate
exl-id: bdc51956-82aa-4aae-b627-a2018f80b5f5
source-git-commit: 835bcd684384d1c8809fba062c9e9d8edd4de535
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 3%

---

# Experience Cloud產品中的AI

此頁面可協助您瞭解哪些產品支援創作AI、[!DNL AI Assistant]，以及Adobe Firefly是否相容。 您也可以找到產品特定說明資源的連結，瞭解如何在Experience Cloud中使用AI。

**關於產生AI**

創作AI是一種人工智慧，其作用不僅僅是回答問題。 它可以&#x200B;_建立_&#x200B;內容，並&#x200B;_產生您問題或陳述式的回應_ （稱為&#x200B;_提示_）。

* **建立：** AI根據其訓練和輸入提示從頭開始產生內容（文字、影像、音樂或視訊）的能力。 此功能是generative AI的&#x200B;_generative_&#x200B;方面。

* **產生回應：** AI正在提供提示的回應或回應，通常會利用其可用的資料和知識存放庫。

如果您是初次使用Experience Cloud，則可透過創作AI快速獲得產品知識。 經驗豐富的使用者可在數秒內發現營運深入分析，而非數小時。

**什麼是 [!DNL AI Assistant]？**

[!DNL AI Assistant]是Experience Platform和相關應用程式支援的對話工具。 這些應用程式使用方式類似，但具有產品特定優勢。 使用它可以加速您的工作流程、改善您的產品知識、疑難排解問題，或搜尋資訊並尋找營運深入分析。 在某些應用程式中，[!DNL AI Assistant]可讓您立即探索運作分析。

**產品知識：**&#x200B;產品知識是以Experience League檔案為根據的概念和主題。 來自Experience League的回應是可驗證的，並可透過連結引用。 瞭解[目標型提示](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)的型別，以充分利用[!DNL AI Assistant]。

**營運分析：**&#x200B;營運分析參考回答AI助理產生的中繼資料物件（屬性、對象、資料流、資料集、目的地、歷程、結構描述和來源），包括計數、查閱和歷程影響。

[了解更多](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/landing)

<!-- **Your data remains yours**

In AI Assistant, security is the priority:

* Customer data is not used to train language models.
* AI Assistant looks at only the documents that you tell it to. You are in control.
* Your people can use AI Assistant only on documents they can access.
* It's audit-ready: Responses are attributable to source documents.
* Enterprise controls are in place to manage who has AI access in the company. -->

## Experience Cloud產品中的AI可用性

瞭解對Experience Cloud產品中generative AI或[!DNL AI Assistant]的支援，以及是否支援Adobe Firefly。

* [[!DNL GenStudio for Performance Marketing]](#gspm)
* [[!DNL Experience Manager Sites]](#aem-sites)
* [[!DNL Journey Optimizer]](#journey-optimizer)
* [[!DNL Journey Optimizer] Prime和Ultimate](#ajo-prime-ultimate)
* [[!DNL Journey Optimizer] B2B edition](#ajo-b2b)
* [[!DNL Campaign] v8網頁使用者介面](#campaign-cs)
* [[!DNL Customer Journey Analytics]](#cja)
* [[!DNL Customer Journey Analytics]](#cja-captions)
* [[!DNL Real-Time CDP]](#rtcdp)
* [[!DNL Marketo]](#marketo)
* [[!DNL Workfront]](#workfront)

## GenStudio for Performance Marketing {#gspm}

[!DNL GenStudio for Performance Marketing]是AI導向的平台，可讓您產生和管理行銷內容，以遵循您的品牌標準並符合您的企業政策。 產生電子郵件、中繼廣告、LinkedIn廣告、顯示廣告和橫幅的內容。

您也可以使用範例、客戶角色和產品的說明以及品牌指引，針對您的品牌訓練GenStudio for Performance Marketing。

[了解更多](https://experienceleague.adobe.com/zh-hant/docs/genstudio-for-performance-marketing/user-guide/home)

與Adobe Firefly的相容性： **是**

## [!DNL Experience Manager Sites] {#aem-sites}

在AEM Sites中，您可以使用[!UICONTROL 產生變數]來根據提示建立內容變數。 這些提示是由Adobe提供，或由您建立及管理。

建立變化後，您可以在網站上使用內容，並使用Edge Delivery Services中的Experimentation功能來衡量其成功與否。 您也可以選擇使用Firefly的產生AI功能，在Adobe Express中產生影像。

[了解更多](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/generative-ai/generate-variations-integrated-editor)

與Adobe Firefly的相容性： **是**

## [!DNL Journey Optimizer] {#journey-optimizer}

在[!DNL Journey Optimizer]中，使用[!DNL AI Assistant]來取得產品知識和營運見解。 例如，詢問&#x200B;_一個Journey Optimizer沙箱中可以有多少個已上線的活動？_&#x200B;您會立即從Experience League和其他Adobe資料存放區取得答案。

[!DNL AI Assistant]也有助於營運分析（測試版）。 例如，您可以快速瞭解過去七天內已建立多少歷程。

如需營運分析，[!DNL AI Assistant]會查詢客戶特定的資料存放區。 資料存放區包含有關[!UICONTROL 歷程]的集中操作資料。 此功能與客戶無關，只會從商業物件提取中繼資料。 它不會存取您沙箱中的資料。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/get-started/ai-assistant)。

與Adobe Firefly的相容性： **否**

## [!DNL Journey Optimizer] Prime和Ultimate {#ajo-prime-ultimate}

[!DNL Journey Optimizer] Prime和Ultimate使用[!DNL AI Assistant]產生內容，為文字和影像提供主動式內容變數建議。

此功能適用於電子郵件、推播通知、網頁、內容和SMS頻道。 它提供提示式文字和影像產生。 AJO Prime和Ultimate中內容產生的輸出不會受到任何影響。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/ai-assistant/gs-generative)

與Adobe Firefly的相容性： **是**

## [!DNL Journey Optimizer B2B Edition] {#ajo-b2b}

Journey Optimizer B2B edition使用[!DNL AI Assistant]來協助您瞭解產品知識。

[了解更多](https://experienceleague.adobe.com/en/docs/journey-optimizer-b2b/user/ai-assistant/ai-assistant-overview)

與Adobe Firefly的相容性： **否**

## [!DNL Campaign] v8 Web UI {#campaign-cs}

Campaign Managed Cloud Services使用[!DNL AI Assistant]來產生內容。 此功能可讓您根據行銷目標自動產生個人化、吸引人且有效的內容，其內容已針對品牌概述的樣式、版面、色調等最佳化。 您可以在電子郵件、簡訊和推播等管道間使用它。

**注意：**&#x200B;在Campaign Managed Cloud Services中產生內容的輸出不會有任何損失。

[了解更多](https://experienceleague.adobe.com/en/docs/campaign-web/v8/content/ai-assistant/generative-gs)

與Adobe Firefly的相容性： **是**

## [!DNL Customer Journey Analytics] {#cja}

Customer Journey Analytics使用[!DNL AI Assistant]協助您探索Experience League的產品知識和深入分析。 如果您是新使用者，請快速瞭解Customer Journey Analytics概念，並熟悉產品和功能。

經驗豐富的使用者可獲得進階使用案例或學習策略，以更快的速度執行任務。 瞭解概念、疑難排解問題或搜尋資訊。

[了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/ai-assistant)

與Adobe Firefly的相容性： **否**

## [!DNL Customer Journey Analytics] {#cja-captions}

[!DNL Customer Journey Analytics]中的智慧型字幕可提供最常用Workspace視覺效果的自然語言深入分析。 智慧型字幕是需要敘述和上下文以與其他使用者分享的分析師的理想選擇。 商務使用者可以利用它來快速探索高階收穫。

[了解更多](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/visualizations/intelligent-captions)

與Adobe Firefly的相容性： **否**

## [!DNL Real-Time CDP] {#rtcdp}

Real-Time CDP使用[!DNL AI Assistant]協助您瞭解Experience League的產品知識。 此外，還提供營運深入分析（測試版）。 [!DNL AI Assistant]查詢客戶特定的營運分析資料存放區，該存放區包含已分割至AEP沙箱的集中營運資料。 系統只會從屬性、受眾、資料流程、資料集、目的地、結構描述和來源提取中繼資料，不會存取沙箱中的資料。

例如，如果您查詢對象，[!DNL AI Assistant]可以存取對象名稱和其他關聯的中繼資料，但無法存取該對象內的設定檔。

[了解更多](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ai-assistant/home)

與Adobe Firefly的相容性： **否**

## [!DNL Marketo] {#marketo}

Adobe Dynamic Chat中由創作AI支援的功能可讓您最佳化銷售代理的生產力、深入瞭解網站的訪客意圖，並以安全的方式回應訪客問題。 您可以預先核准問題、答案和交談摘要。

[了解更多](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/demand-generation/dynamic-chat/generative-ai/overview)

與Adobe Firefly的相容性： **否**

## [!DNL Workfront] {#workfront}

[!DNL Workfront]中的[!DNL AI Assistant]會提供應用程式內資訊和建議，協助您完成工作。 您可以：

* 取得某些物件的摘要，讓您以高層級檢視物件的意圖或詳細資訊。
* 提出問題並讓[!DNL AI Assistant]在Experience League上尋找答案。
* 根據您的提示取得產生的公式。 您也可以解決計算欄位中無效自訂運算式的錯誤。
* 尋找專案、任務和問題。

[了解更多](https://experienceleague.adobe.com/en/docs/workfront/using/basics/ai-assistant/ai-assistant-overview)

與Adobe Firefly的相容性： **否**
