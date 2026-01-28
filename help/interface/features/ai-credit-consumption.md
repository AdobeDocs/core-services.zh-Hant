---
title: 代理程式工作與AI信用沖銷
description: 瞭解Experience Cloud應用程式中的代理程式工作和AI點數消耗。
solution: Experience Cloud
landing-page-name: ai
landing-page-breadcrumb-title: AI Documentation
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: 623bb6e240987cb2ff76bce3488b827b901b84db
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 9%

---


# 代理程式工作與AI信用沖銷

## 代理程式工作

**代理程式工作**&#x200B;是「代理程式」根據客戶輸入的指示，為達成特定結果而執行的一系列工作與動作。

透過AI Assistant使用自然語言提示，客戶可以要求Agent執行特定工作。 Agent Orchestrator會根據這些輸入協調適當的代理程式，以在相關的Experience Cloud應用程式中執行每個步驟。

## AI積分

**AI評分**&#x200B;是以使用量為基礎的量度，可量化代理程式工作的執行。 AI積分不適用於AI優先的應用程式。

## AI信用沖銷

AI評分的使用方式可能會因所執行工作的複雜性和價值而異：

* 簡單（通常是單步）工作消耗的積分較少
* 複雜（通常為多步驟）的工作會消耗更多積分
* 涉及進階推理、驗證、多代理程式協調或整合的工作會消耗更多評分

### 預估的AI信用消耗率

| 代理程式 | 工作 | 支援的應用程式 | 預估的AI積分 |
|------|-----|------------------------|----------------------|
| Audience 代理 | 對象/帳戶構思 | Real-Time CDP； Adobe Journey Optimizer | 50 |
| Audience 代理 | 以知識為基礎的對象/帳戶建立 | Real-Time CDP； Adobe Journey Optimizer | 150 |
| Audience 代理 | 對象/帳戶管理 | Real-Time CDP； Adobe Journey Optimizer | 25 |
| Audience 代理 | 對象/帳戶分析 | Real-Time CDP； Adobe Journey Optimizer | 25 |
| Audience 代理 | 購買團體創意 | Adobe Journey Optimizer (B2B) | 25 |
| Data Insights Agent | 資料分析和視覺效果 | Customer Journey Analytics | 25 |
| Data Insights Agent | 資料storytelling和共用 | Customer Journey Analytics | 100 |
| Journey Agent | 歷程構想 | Adobe Journey Optimizer (B2B) | 25 |
| Journey Agent | 歷程建立 | Adobe Journey Optimizer (B2B， B2C) | 30 |
| Journey Agent | 歷程分析 | Adobe Journey Optimizer (B2B， B2C) | 50 |
| Journey Agent | 歷程管理 | Adobe Journey Optimizer (B2B， B2C) | 25 |
| 產品支援代理 | 知識型疑難排解 | 多個Experience Cloud應用程式 | 0 |
| 產品支援代理 | 支援案例建立和追蹤 | 多個Experience Cloud應用程式 | 10 |
| 內容建議程式代理程式 | 內容探索 | Adobe Experience Manager雲端服務 | 5 |
| 內容建議程式代理程式 | 內容更新和最佳化 | Adobe Experience Manager雲端服務 | 10 |
| Brand Experience Agent | 部署支援 | Adobe Experience Manager雲端服務 | 5 |
| Brand Experience Agent | 網站現代化 | Adobe Experience Manager雲端服務 | 100 |

**注意：**&#x200B;實際AI點數消耗可能會因執行的步驟數以及每個步驟的反複專案而有所不同。

