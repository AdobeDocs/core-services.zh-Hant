---
title: 代理程式工作與AI信用沖銷
description: 瞭解 CX Enterprise 應用程式中的 AI 代理工作和 AI 點數消耗率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
last-update: '2026-05-21T00:00:00.000Z'
source-git-commit: e88ba99174bf84de9b58a61ae8c22c0bbd7ed9bf
workflow-type: tm+mt
source-wordcount: '993'
ht-degree: 6%

---

# Adobe Experience Platform代理程式工作和AI點數消耗

瞭解CX Enterprise應用程式中的Agential AI工作和AI信用消耗。 如需有關在現有CX Enterprise應用程式中啟用代理程式人工智慧功能的資訊，請參閱[CX Enterprise中的代理程式人工智慧](agentic-ai.md#existing-apps)。

## 新增功能

| 功能 | 說明 |
| --- | --- |
| [CX Enterprise Agentic AI功能目錄](https://agentic-capability-explorer.entapp.adproto.com/) | 探索您的授權CX Enterprise應用程式中有哪些代理程式AI工作。 |

## 代理程式工作

_代理程式工作_&#x200B;是代理程式根據客戶輸入的指示，為達成特定結果所執行的一系列工作與動作。

透過AI助理使用自然語言提示，您可以要求代理程式執行特定工作。 根據這些輸入，Agent Orchestrator會協調適當的代理程式，以便在相關的CX Enterprise應用程式中執行每個步驟。

## AI 點數

_AI評分_&#x200B;是以使用量為基礎的量度，可量化代理程式工作的執行。 AI積分不適用於[AI優先應用程式](/help/interface/features/agentic-ai.md)。

## AI信用消耗

AI評分使用方式可能會因所執行工作的複雜性和價值而異：

* 簡單（通常是單步）工作消耗的積分較少
* 複雜（通常為多步驟）的工作會消耗更多積分
* 涉及進階推理、驗證、多代理程式協調或整合的工作會消耗更多評分

**注意：** [CX Enterprise Agentic AI Capability Catalog](https://agentic-capability-explorer.entapp.adproto.com/)也可協助您探索您的授權CX Enterprise應用程式中有哪些代理AI工作。

### 預估的AI信用消耗率

| 代理程式 | 工作 | 支援的應用程式 | 預估的AI積分 | 範例提示 |
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience 代理 | 對象/帳戶概念 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li><em>為我顯示富裕買家的欄位</em></li><li><em>尋找與客戶偏好設定相關的所有欄位</em></li></ul> |
| Audience 代理 | 對象/帳戶管理 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>我有任何重複的對象嗎？</em></li><li><em>顯示我的5大對象。</em></li><li><em>顯示未啟用至任何目的地的對象</em></li><li><em>列出即時歷程中使用的所有對象</em></li></ul> |
| Audience 代理 | 對象/帳戶分析 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li><em>哪些對象在上星期增加了超過20%？</em></li><li><em>與30天前的值相比，對象「忠誠白金」有多少變化？</em></li><li><em>我增長最快的對象是哪個？</em></li></ul> |
| Audience 代理 | 購買團體創意 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>哪些帳戶顯示這些產品的目的？</em></li><li><em>依產品意向顯示XYZ排名最前的人員。</em></li><li><em>哪些購買群組擁有超過5名成員？</em></li></ul> |
| Data Insights Agent | 資料分析和視覺效果 | <ul><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 25 | <ul><li><em>7月趨勢訂單</em></li><li><em>依地區顯示收入。</em></li><li><em>依性別顯示從3月到6月的訂單。</em></li><li><em>我在6月獲利的前10大SKU為何</em></li><li><em>按月份計算的購買比例</em></li><li><em>依產品類別劃分的收入份額</em></li></ul> |
| Journey Agent | 歷程構想 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li><em>為想要用於我的解決方案的空白帳戶建立歷程，著重於參與網站內容的人員</em></li></ul> |
| Journey Agent | 歷程分析 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 50 | <ul><li><em>我想針對7月4日的行銷活動歷程依節點分析流失。</em></li><li><em>歷程X</em>是否有任何排程衝突</li><li><em>顯示歷程X</em>的對象重疊衝突</li></ul> |
| Journey Agent | 歷程管理 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 25 | <ul><li><em>我有多少個即時歷程？</em></li><li><em>列出使用對象X的所有歷程。</em></li><li><em>列出目前處於測試模式的所有歷程</em></li></ul> |
| 產品支援代理 | 知識型疑難排解 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2C和B2B版本）</li><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 0 | <ul><li><em>為什麼我的設定檔計數在[授權使用儀表板]和Experience Platform首頁上不同？</em></li><li><em>歷程未觸發的原因是什麼？</em></li><li><em>Adobe Experience Platform如何建立即時體驗？</em></li><li><em>如何在Adobe Experience Platform中設定和使用警示？</em></li><li><em>在Adobe Experience Platform Activation中的平均設定檔豐富度限制是多少？</em></li></ul> |
| 產品支援代理 | 支援案例建立和追蹤 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2C和B2B版本）</li><li>Customer Journey Analytics （B2C和B2B版本）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li><em>為我失敗的分段工作建立新的支援票證</em></li><li><em>票證E-001772068的狀態為何？</em></li></ul> |
| 內容建議程式代理程式 | 內容探索 | <ul><li>Adobe Experience Manager</li></ul> | 5 | <ul><li><em>顯示建立WKND選件行銷活動的內容片段。</em></li><li><em>尋找產品封裝PNG影像。</em></li><li><em>在資料夾WKND中顯示已標籤的Office影像。</em></li><li><em>資料夾WKND中是否有任何svg？</em></li><li><em>顯示所有貸款申請表單。</em></li><li><em>我正在尋找員工入職表格。</em></li></ul> |
| 內容建議程式代理程式 | <ul><li>內容最佳化</li></ul> | <ul><li>Adobe Experience Manager Assets與Dynamic Media</li></ul> | 10 | <ul><li><em>以80%品質建立2000px轉譯為JPEG。</em></li><li><em>建立Instagram劇本的轉譯。</em></li><li><em>將影像以30%折扣的圖形覆蓋在促銷橫幅上，從中心放置100px。</em></li><li><em>將PNG的背景顏色變更為#ff8932。</em></li></ul> |
| Brand Governance Agent | <ul><li>品牌原則檢查</li></ul><ul><li>Content Hub的許可權</li></ul><ul><li>資產有效期</li></ul> | <ul><li>Adobe Experience Manager Sites （品牌政策）</li></ul><ul><li>Adobe Experience Manager Assets</li></ul> | 25 | <ul><li><em>此頁面是否符合我的品牌？`https://www.website/en.html`</em></li><li><em>顯示所有現有的Content Hub ABAC規則</em></li><li><em>我的任何資產是否即將到期？</em></li></ul> |
| Brand Experience Agent | <ul><li>內容更新</li><li>Forms建立</li><li>管道疑難排解</li></ul> | <ul><li>Adobe Experience Manager雲端服務</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li><em>在`URL`，將標題更新為Hello world</em></li><li><em>建立包含名稱、電子郵件和訊息欄位的連絡人表單</em></li><li><em>疑難排解我失敗的管道</em></li><li><em>列出主要方案的失敗管道。</em></li></ul> |
| Brand Experience Agent | 網站現代化 | Adobe Experience Manager雲端服務 | 100 | <ul><li><em>移轉頁面`https://wknd-trendsetters.site`</em></li></ul> |

>[!NOTE]
>
>實際的AI點數消耗可能會因執行的步驟數以及每個步驟的反複專案而異。

## 有關此主題的更多說明

* [CX Enterprise中的GenAI](/help/interface/features/generative-ai.md)
* [CX Enterprise中的Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理程式使用範圍試用版](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
