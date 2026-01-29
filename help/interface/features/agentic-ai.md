---
title: Experience Cloud應用程式中的Agentic AI
description: 瞭解Experience Cloud應用程式中可在何處使用Agentic AI。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
hidefromtoc: true
index: false
exl-id: c1a8f9a7-4752-4040-b5f0-dc775417f536
source-git-commit: da7a2a9e9aa8365288fa6e05afb6485e4c33ccb2
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 2%

---

# Adobe Experience Cloud中的Agentic AI

更新日期： **2026年1月29日**

Adobe Experience Platform代理程式使用Experience Platform [Agent Orchestrator](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/home)將代理程式功能新增至Experience Cloud應用程式。

這些代理程式有助於自動化工作、更快地提供見解並簡化工作流程。 因此，團隊可以更有效率地工作，並從Experience Cloud中獲得更多價值。

您可透過下列任一方式存取Experience Cloud中的AI代理程式：

* [現有的Experience Cloud應用程式](#existing-apps)
* [AI優先的Experience Cloud應用程式](#ai-first-apps)

以下各節說明如何在Experience Cloud中啟用代理程式人工智慧。

## 現有的Experience Cloud應用程式 {#existing-apps}

在現有應用程式中，您可以使用自然語言，透過[AI助理](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/home)交談介面來指示Adobe Experience Platform代理程式。 AI助理同時適用於全熒幕和右側邊欄檢視。

您可以在現有的Experience Cloud應用程式中，為具有以下類別之一的客戶啟用代理程式：

* 已購買Adobe Experience Platform Agents AI信用授權
* 包含在使用範圍內的試用版中（提供有限的AI積分）
* 已交易Agent Orchestrator促銷SKU （限時試用授權）

當您使用AI代理程式執行&#x200B;_代理程式工作_&#x200B;時，您就會使用AI積分。 在[代理程式工作和AI信用消耗](/help/interface/features/ai-credit-consumption.md)中瞭解它。

AI代理程式會遵循&#x200B;_您的_&#x200B;輸入、監督，並遵守產品層級的存取控制。 您只能執行您獲授權用於基礎Experience Cloud產品的工作或存取資料。

### 現有Experience Cloud應用程式中的AI代理程式 {#existing-apps-table}

下表列出現有Experience Platform應用程式中可用的Experience Cloud代理程式。

| 代理程式名稱 | 功能 | 支援的應用程式 |
|---|----------|----------|
| [Audience Agent](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/audience) | 讓您的團隊能夠使用自然語言提示來建立、管理和最佳化對象，以獲得更容易、更高效率和更快的市場上市速度。 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> |
| **內容顧問代理程式** | <ul><li>[內容探索](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/discovery/overview)：透過簡化的自然語言提示，加速撰寫並加速探索，以立即在影像、視訊、文字型檔案、內容片段及表單中尋找並顯示Experience Manager內容。</li><li>[內容最佳化](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/content-optimization/overview)：使用自然語言提示簡化從來源資產建立視覺內容變體的程式。</li><li>[體驗生產](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/production/overview)：在CMS中自動執行大量工作和大量工作。 此代理程式將手動、冗長的流程轉換為快速的AI輔助工作流程，讓每個體驗保持最新且一致，協助您的企業達成目標。</li></ul> | <ul><li>Adobe Experience Manager （內容探索）</li></ul><ul><li>Adobe Experience Manager搭配動態媒體與OpenAPI （內容最佳化）</li></ul><ul><li>Adobe Experience Manager Cloud Services與Edge Delivery Services （體驗生產） </li></ul> |
| [Data Insights Agent](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-b2c-overview/data-analysis-ai) | 快速解答有關您資料的問題。 它會使用您資料檢視中的元件，並使用您的實際資料，在Analysis Workspace中建置相關的視覺效果。 | <ul><li>Customer Journey Analytics （B2B和B2C版本）</li></ul> |
| **品牌體驗代理程式** | [部署支援](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/development/overview)：透過分析根本原因並提出修正建議，協助AEM CS開發人員和技術管理員疑難排解Cloud Manager管道中的建置步驟失敗。 | <ul><li>AEM Cloud Service和Adobe Managed Services中的AI助理</li></ul> |
| **品牌治理代理程式*** | [品牌治理](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/governance/overview)：透過在Experience Manager中強制實行安全性、法規及品牌政策，以維護品牌完整性和法規遵循。 此代理程式會套用品牌控管來維護視覺和訊息標準。 它使用細微的許可權來管理存取和內容變更，並整合DRM以維護授權和使用限制。 | <ul><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Assets</li><li>Adobe Experience Manager Forms</li></ul> |
| [Journey Agent](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze) | 讓您的團隊快速建立、分析和最佳化大規模的多點觸控客戶歷程。 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> |
| [產品支援代理程式](https://experienceleague.adobe.com/en/docs/experience-platform/ai-assistant/new-features/customer-support) | 在不離開工作流程的情況下疑難排解支援問題、建立客戶支援票證，並使用AI Assistant追蹤案例進度。 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2B和B2C版本）</li><li>Adobe Journey Optimizer B2B edition</li><li>Customer Journey Analytics</li><li>Adobe Experience Manager</li></ul> |

星號(*)：此代理程式可由瀏覽器程式中的客戶存取。 Explorer程式是僅供邀請使用的程式，可讓您提早存取Adobe的最新代理程式功能。 如需詳細資訊，請洽詢您的客戶代表。

## AI優先的Experience Cloud應用程式 {#ai-first-apps}

AI優先應用程式是以產生式或無代理式Al為核心所建置。 它們使用產生式或無代理式Al來執行關鍵任務，而無代理式功能已包含在Al-first應用程式授權中。 因此，它們不需要Experience Platform Agent Orchestrator授權。

下表列出可作為所有優先應用程式使用的Experience Platform代理程式。 透過授權這些優先應用程式來啟用這些功能：

| 代理程式名稱 | 功能 | 支援的應用程式 |
|---|----------|----------|
| [Experimentation Agent](https://experienceleague.adobe.com/en/docs/journey-optimizer/using/content-management/content-experiment/experiment/experiment-accelerator-security) | 自動化、分析和綜合深入分析，讓您從集中式工作區中快速找出高影響力的實驗和發展機會，同時減少手動程式。 | <ul><li>AJO Experimentation Accelerator</li></ul> |
| [LLM最佳化代理程式](https://experienceleague.adobe.com/zh-hant/docs/llm-optimizer/using/home) | 增強AI導向搜尋環境中的可見度、準確性和影響力，在AI產生的回答中提供品牌存在的深入分析，提供規範性的內容建議，並自動化最佳化修正。 | <ul><li>Adobe LLM Optimizer</li></ul> |
| [Site Optimization Agent](https://experienceleague.adobe.com/zh-hant/docs/experience-manager-sites-optimizer/content/home) | 透過自動偵測和部署網站增強功能，將業務影響最大化。 使用創作AI和多種監控技術，您可以增加網站流量的獲得、參與度等 | <ul><li>AEM Sites Optimizer</li></ul> |
| [Product Advisor Agent](https://experienceleague.adobe.com/en/docs/brand-concierge/content/documentation/overview) | 透過根據個人偏好和行為量身打造的智慧型內容感知產品探索，促進轉換和參與。 | <ul><li>Adobe Brand Concierge</li></ul> |

## 有關此主題的更多說明

* Experience Cloud中的[AI](https://experienceleague.adobe.com/zh-hant/docs/ai)檔案首頁
* [AEM代理程式概觀](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/ai-in-aem/agents/overview)

[!BADGE 進一步瞭解Adobe for Business]{type=Informative url="https://business.adobe.com/products/experience-platform/agent-orchestrator.html" tooltip="前往Business.adobe.com"}
