---
title: Experience Cloud應用程式中的Agentic AI
description: 瞭解CX Enterprise應用程式中可在何處使用Agentic AI。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
feature_v2:
  - id: f84b2906-3ce9-4ef0-86f6-cda249273937
source-git-commit: 5b2b81c029b81b9f0689a012cb2a9ca8714c0b40
workflow-type: tm+mt
source-wordcount: 1130
ht-degree: 11%

---

# Adobe CX Enterprise中的Agentic AI

Adobe Experience Platform代理程式由[Experience Platform Agent Orchestrator](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/home)提供技術支援，可在CX Enterprise應用程式中啟用代理程式人工智慧功能。

這些代理程式有助於自動化工作、更快地提供見解並簡化工作流程。 因此，團隊可以更有效率地工作，並從CX Enterprise中獲得更多價值。

CX Enterprise中的AI代理程式可透過以下任一方式存取：

* [現有的CX企業應用程式](#existing-apps)
* [AI優先的CX企業應用程式](#ai-first-apps)

以下各節將說明在CX Enterprise中啟用代理程式人工智慧的兩種方式。

## 現有的CX企業應用程式 {#existing-apps}

在現有應用程式中，您可以使用自然語言，透過[AI小幫手](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/home)交談介面來指示Adobe Experience Platform代理程式。 AI Assistant可用於全熒幕和右邊欄檢視。

您可以在現有的CX Enterprise應用程式中，為具有下列其中一種類別的客戶啟用代理程式：

* 您已購買Adobe Experience Platform Agents AI信用授權
* 您被包含在符合使用規定的試用中（提供的有限AI積分）
* 您已交易Agent Orchestrator促銷SKU （限定時間試用授權）

使用AI代理程式執行&#x200B;_代理程式工作_&#x200B;會使用AI積分。 深入瞭解&#x200B;_[代理程式工作和AI信用消耗](/help/interface/features/ai-credit-consumption.md)_&#x200B;中的代理程式工作和AI信用消耗。

AI代理程式會遵循&#x200B;_您的_&#x200B;輸入、監督，並遵守產品層級的存取控制。 您只能執行工作或存取您授權在底層CX Enterprise應用程式中使用的資料。

### 現有CX Enterprise應用程式中的AI代理程式 {#existing-apps-table}

下表列出現有CX Enterprise應用程式中可用的Experience Platform Agent。

| 代理程式名稱 | 功能 | 支援的應用程式 | 健康情況資料/符合HIPAA標準 |
|---|----------|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 讓您的團隊能夠使用自然語言提示來管理和最佳化受眾，以獲得更容易、更高效率和更快的上市速度。 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | |
| [內容顧問代理程式](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-advisor/overview) | <ul><li>協助團隊使用自然語言，在整個企業中快速找到最相關的內容，減少搜尋所花費的時間，並加快決策和執行的速度。</li><li>使用自然語言提示簡化從來源資產建立視覺內容變體的過程。</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul><ul><li>Dynamic Media （雲端服務）</li></ul> | |
| [Data Insights Agent](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 快速解答有關您資料的問題。 此代理會使用來自您資料視圖的元件以及您的實際資料，在 Analysis Workspace 中建置相關的視覺效果。 | <ul><li>Customer Journey Analytics （B2B和B2C版本）</li></ul> | 是 |
| [Brand Experience Agent](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/brand-experience/overview) | <ul><li>自動重新建構、豐富和驗證現有網站，以加速數位體驗的移轉和現代化，讓團隊能夠以更低的風險和手動作業，更快速地體驗現代、AI就緒的體驗。</li><li>進行大量體驗建立和更新，大幅減少手動工作量和週期時間，讓團隊能夠在不犧牲品質或一致性的情況下更快速地移動。</li><li>藉由自動產生、建構和驗證表單體驗，加速建立最佳化、符合品牌的表單，讓團隊能夠更快速地啟動，並擷取更高品質的資料，而只需最少的手動工作。</li><li>透過分析根本原因並提出修正建議，協助AEM CS開發人員和技術管理員疑難排解Cloud Manager管道中的建置步驟失敗。</li></ul> | <ul><li>Adobe Experience Manager Sites雲端服務（體驗現代化）</li></ul><ul><li>Adobe Experience Manager Sites （體驗生產）</li></ul><ul><li>Adobe Experience Manager Forms （建立表單）</li></ul><ul><li>所有雲端型Adobe Experience Manager應用程式（開發支援）</li></ul> | |
| [品牌治理代理程式](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview) | 透過自動化品牌政策檢查、許可權和智慧來保障品牌完整性和合規性，以透過即時控管支援DRM。 | <ul><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Sites （品牌政策）</li></ul> | |
| [Journey Agent](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent) | 讓您的團隊快速分析和最佳化大規模的多點觸控客戶歷程。 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | |
| [產品支援代理程式](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/product-support) | 在不離開工作流程的情況下疑難排解支援問題、建立客戶支援票證，並使用AI Assistant追蹤案例進度。 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2B和B2C版本）</li><li>Customer Journey Analytics （B2B和B2C版本）</li><li>Adobe Experience Manager</li></ul> | |
| [Adobe Marketing Agent for Microsoft 365 Copilot](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/ama-ms) | 將Experience Platform直接連線至Microsoft 365 Copilot。 您可以在Microsoft 365應用程式（例如Teams、Word、Powerpoint和Excel）中詢問自然語言問題，以便立即從Experience Platform擷取行銷深入分析，而不會中斷您的工作流程。 | <ul><li> Adobe Agent Orchestrator支援Audience Agent、Journey Agent、Customer Journey Analytics Data Insights、Experience Platform Operational Insights</li></ul> | |

## AI優先的CX企業應用程式 {#ai-first-apps}

AI優先應用程式是以產生式或無代理式Al為核心所建置。 它們使用產生式或無代理式Al來執行關鍵任務，而無代理式功能已包含在Al-first應用程式授權中。 因此，它們不需要Experience Platform Agent Orchestrator授權。

下表列出可作為所有優先應用程式使用的Experience Platform代理程式。 透過授權這些優先應用程式來啟用這些功能：

| 代理程式名稱 | 功能 | 支援的應用程式 |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 自動化、分析和綜合深入分析，讓您從集中式工作區中快速找出高影響力的實驗和發展機會，同時減少手動程式。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM最佳化代理程式](https://experienceleague.adobe.com/zh-hant/docs/llm-optimizer/using/home) | 增強AI驅動搜尋環境的可見度、準確性和影響力、在AI產生的回答中提供品牌存在感的深入分析、提供規範性的內容建議，以及自動化最佳化修正。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-sites-optimizer/content/home) | 透過自動偵測和部署網站增強功能，將業務影響最大化。 使用創作AI和多種監控技術，您可以增加網站流量的獲得、參與度等 | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | 透過根據個人偏好和行為量身打造的智慧型內容感知產品探索，促進轉換和參與。 | <ul><li>Adobe Brand Concierge</li></ul> |

## 有關此主題的更多說明

* [代理程式工作和AI信用消耗](/help/interface/features/ai-credit-consumption.md)
* CX Enterprise[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/ai)檔案首頁中的AI
* [AEM代理程式概觀](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE 進一步瞭解Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="前往Business.adobe.com"}
