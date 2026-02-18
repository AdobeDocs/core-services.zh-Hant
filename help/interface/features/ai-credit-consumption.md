---
title: 代理程式工作與AI信用沖銷
description: 瞭解Experience Cloud應用程式中的代理程式工作和AI信用消費率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: bb6adf13bed37d4a885b5baec28199efade592e1
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 3%

---

# Adobe Experience Platform代理程式工作和AI點數消耗

瞭解Experience Cloud應用程式中的代理式AI工作和AI點數消耗。 如需有關在現有Experience Cloud應用程式中啟用代理程式人工智慧功能的資訊，請參閱[Experience Cloud中的代理程式人工智慧](agentic-ai.md#existing-apps)。

## 代理程式工作

_代理程式工作_&#x200B;是代理程式根據客戶輸入的指示，為達成特定結果所執行的一系列工作與動作。

透過AI助理使用自然語言提示，您可以要求代理程式執行特定工作。 Agent Orchestrator會根據這些輸入協調適當的代理程式，以在相關的Experience Cloud應用程式中執行每個步驟。

## AI 點數

_AI評分_&#x200B;是以使用量為基礎的量度，可量化代理程式工作的執行。 AI積分不適用於[AI優先應用程式](/help/interface/features/agentic-ai.md)。

## AI信用消耗

AI評分使用方式可能會因所執行工作的複雜性和價值而異：

* 簡單（通常是單步）工作消耗的積分較少
* 複雜（通常為多步驟）的工作會消耗更多積分
* 涉及進階推理、驗證、多代理程式協調或整合的工作會消耗更多評分

### 預估的AI信用消耗率

| 代理程式 | 工作 | 支援的應用程式 | 預估的AI積分 | 範例提示 |
| ------ |-----|------------------------|----------------------|----------------|
| Audience 代理 | 對象/帳戶概念 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>為我顯示富裕買家的欄位</li><li>尋找與客戶偏好設定相關的所有欄位</li></ul> |
| Audience 代理 | 以知識為基礎的對象/帳戶建立 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>建立由住在加州的人組成的對象</li><li>產生本季花費超過$1000的VIP成員對象</li><li>建立已購買服裝但過去60天內未購買的使用者受眾</li></ul> |
| Audience 代理 | 對象/帳戶管理 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>我有任何重複的對象嗎？</li><li>顯示我的5個最大對象。</li><li>顯示未啟用至任何目的地的對象</li><li>列出即時歷程中使用的所有對象</li></ul> |
| Audience 代理 | 對象/帳戶分析 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>上週哪些對象的大小增加超過20%？</li><li>與30天前的值相比，對象「忠誠白金」有哪些變更？</li><li>我增長最快的對象是哪個？</li></ul> |
| Audience 代理 | 購買團體創意 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>哪些帳戶顯示這些產品的意圖？</li><li>顯示XYZ產品意圖的排名最前的人員。</li><li>哪些購買群組擁有超過5名成員？</li></ul> |
| Data Insights Agent | 資料分析和視覺效果 | <ul><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 25 | <ul><li>7月趨勢訂單</li><li>依地區顯示收入。</li><li>依性別顯示從3月到6月的訂單。</li><li>我在6月獲利的前10大SKU為何？</li><li>按月份和年份的購買比例</li><li>依產品類別劃分的收入份額</li></ul> |
| Journey Agent | 歷程構想 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>為意圖用於我的解決方案的空白帳戶建立歷程，著重於參與網站內容的人員</li></ul> |
| Journey Agent | 歷程建立 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 30 | <ul><li>產生歷程，以傳送提醒給過去7天內未完成首次購買的使用者</li><li>使用者完成首次購買後，在3天後透過電子郵件傳送簡訊確認及後續權益說明</li></ul> |
| Journey Agent | 歷程分析 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 50 | <ul><li>我想針對7月4日的行銷活動歷程依節點分析流失。</li><li>歷程X是否有任何排程衝突</li><li>顯示歷程X的對象重疊衝突</li></ul> |
| Journey Agent | 歷程管理 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 25 | <ul><li>我有多少個即時歷程？</li><li>列出使用對象X的所有歷程。</li><li>列出目前處於測試模式的所有歷程</li></ul> |
| 產品支援代理 | 知識型疑難排解 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2C和B2B版本）</li><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 0 | <ul><li>為什麼我的設定檔計數在「授權使用儀表板」和Experience Platform首頁上會不同？</li><li>歷程未觸發的原因是什麼？</li><li>Adobe Experience Platform如何建立即時體驗？</li><li>如何在Adobe Experience Platform中設定和使用警報？</li><li>Adobe Experience Platform啟用的平均設定檔豐富度限制是多少？</li></ul> |
| 產品支援代理 | 支援案例建立和追蹤 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li>Adobe Journey Optimizer （B2C和B2B版本）<li>Customer Journey Analytics （B2C和B2B版本）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>為我失敗的細分工作建立新的支援票證</li><li>票證E-001772068的狀態為何？</li></ul> |
| 內容建議程式代理程式 | 內容探索 | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 5 | <ul><li>顯示建立WKND選件行銷活動的內容片段。</li><li>尋找產品封裝PNG影像。</li><li>在資料夾WKND中顯示已標籤辦公室影像。</li><li>WKND資料夾中是否有任何svg？</li><li>顯示所有貸款申請表單。</li><li>我正在尋找員工入職表格。</li></ul> |
| 內容建議程式代理程式 | <ul><li>內容更新</li><li>內容最佳化</li><li>Forms建立</li></ul> | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 10 | <ul><li>以80%品質建立2000px轉譯為JPEG。</li><li>建立Instagram故事的轉譯。</li><li>將影像以30%折扣的圖形覆蓋在促銷橫幅上，從中心放置100px。</li><li>將PNG的背景顏色變更為#ff8932。</li></ul> |
| Brand Experience Agent | <ul><li>體驗支援</li><li>部署支援</li></ul> | <ul><li>Adobe Experience Manager雲端服務</li></ul> | 5 | <ul><li>疑難排解我的失敗管道</li><li>列出主要方案的失敗管道。</li><li>分析我名為「開發管道」的失敗管道。</li><li>疑難排解管道執行1234567</li></ul> |
| Brand Experience Agent | 網站現代化 | Adobe Experience Manager雲端服務 | 100 | <ul><li>移轉頁面https://wknd-trendsetters.site</li></ul> |

>[!NOTE]
>
>實際的AI點數消耗可能會因執行的步驟數以及每個步驟的反複專案而異。

## 有關此主題的更多說明

* [Experience Cloud中的Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理程式使用量繫結試用版](https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)