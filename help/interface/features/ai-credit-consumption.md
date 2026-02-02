---
title: 代理程式工作與AI信用沖銷
description: 瞭解Experience Cloud應用程式中的代理程式工作和AI信用消費率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 7eb6c6e463102ca445093c69797619202202b35e
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 12%

---

# 代理程式工作和AI信用消耗

瞭解Experience Cloud應用程式中的代理式AI工作和AI點數消耗。 如需有關在現有Experience Cloud應用程式中啟用代理程式人工智慧功能的資訊，請參閱[Experience Cloud中的代理程式人工智慧](agentic-ai.md#existing-apps)。

## 代理程式工作

_代理程式工作_&#x200B;是「代理程式」根據客戶輸入的指示，為達成特定結果而執行的一系列工作與動作。

透過AI助理使用自然語言提示，您可以要求代理程式執行特定工作。 Agent Orchestrator會根據這些輸入協調適當的代理程式，以在相關的Experience Cloud應用程式中執行每個步驟。

## AI積分

_AI評分_&#x200B;是以使用量為基礎的量度，可量化代理程式工作的執行。 AI積分不適用於[AI優先應用程式](/help/interface/features/agentic-ai.md)。

## AI信用消耗

AI評分使用方式可能會因所執行工作的複雜性和價值而異：

* 簡單（通常是單步）工作消耗的積分較少
* 複雜（通常為多步驟）的工作會消耗更多積分
* 涉及進階推理、驗證、多代理程式協調或整合的工作會消耗更多評分

### 預估的AI信用消耗率

| 代理程式 | 工作 | 支援的應用程式 | 預估的AI積分 |
|------|-----|------------------------|----------------------|
| Audience 代理 | 對象/帳戶構思 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 50 |
| Audience 代理 | 以知識為基礎的對象/帳戶建立 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 150 |
| Audience 代理 | 對象/帳戶管理 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 25 |
| Audience 代理 | 對象/帳戶分析 | <ul><li>Real-Time CDP</li><li>Adobe Journey Optimizer</li></ul> | 25 |
| Audience 代理 | 購買團體創意 | <ul><li>Adobe Journey Optimizer (B2B)</li></ul> | 25 |
| Data Insights Agent | 資料分析和視覺效果 | <ul><li>Customer Journey Analytics</li></ul> | 25 |
| Journey Agent | 歷程構想 | <ul><li>Adobe Journey Optimizer (B2B)</li></ul> | 25 |
| Journey Agent | 歷程建立 | <ul><li>Adobe Journey Optimizer (B2B， B2C)</li></ul> | 30 |
| Journey Agent | 歷程分析 | <ul><li>Adobe Journey Optimizer (B2B， B2C)</li></ul> | 50 |
| Journey Agent | 歷程管理 | <ul><li>Adobe Journey Optimizer (B2B， B2C)</li></ul> | 25 |
| 產品支援代理 | 知識型疑難排解 | <ul><li>多個Experience Cloud應用程式</li></ul> | 0 |
| 產品支援代理 | 支援案例建立和追蹤 | <ul><li>多個Experience Cloud應用程式</li></ul> | 10 |
| 內容建議程式代理程式 | 內容探索 | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 5 |
| 內容建議程式代理程式 | 內容更新和最佳化 | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 10 |
| Brand Experience Agent | 部署支援 | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 5 |
| Brand Experience Agent | 網站現代化 | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 100 |

>[!NOTE]
>
>實際的AI點數消耗可能會因執行的步驟數以及每個步驟的反複專案而異。

## 有關此主題的更多說明

* [Experience Cloud中的Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理程式使用量繫結試用版](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)