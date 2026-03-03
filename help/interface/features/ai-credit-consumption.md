---
title: 代理程式工作與AI信用沖銷
description: 瞭解Experience Cloud應用程式中的代理程式工作和AI信用消費率。
solution: Experience Cloud
topic: Artificial Intelligence
feature: Agentic AI, AI Tools
role: Admin, User
level: Intermediate
source-git-commit: d9d9eb0b3bad1abd517e4c6b0bd5ecaa45a7930d
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 4%

---

# Adobe Experience Platform代理程式工作和AI點數消耗

更新日期： 2026年3月3日&#x200B;**&#x200B;**

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
| ------ | ----- | ------------------------ | ----------------------- | ----------------- |
| Audience 代理 | 對象/帳戶概念 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 50 | <ul><li>_為我顯示富裕買家的欄位_</li><li>_尋找與客戶偏好設定相關的所有欄位_</li></ul> |
| Audience 代理 | 以知識為基礎的對象/帳戶建立 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 150 | <ul><li>_建立由住在加州的人組成的對象_</li><li>_產生本季花費超過$1000的VIP成員對象_</li><li>_建立已購買服裝但過去60天內未購買的使用者對象_</li></ul> |
| Audience 代理 | 對象/帳戶管理 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_我有任何重複的對象嗎？_</li><li>_顯示我的5大對象。_</li><li>_顯示未啟用至任何目的地的對象_</li><li>_列出即時歷程中使用的所有對象_</li></ul> |
| Audience 代理 | 對象/帳戶分析 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer (B2C Edition)</li></ul> | 25 | <ul><li>_哪些對象在上星期增加了超過20%？_</li><li>_與30天前的值相比，對象「忠誠白金」有多少變化？_</li><li>_我增長最快的對象是哪個？_</li></ul> |
| Audience 代理 | 購買團體創意 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_哪些帳戶顯示這些產品的目的？_</li><li>_依產品意向顯示XYZ排名最前的人員。_</li><li>_哪些購買群組擁有超過5名成員？_</li></ul> |
| Data Insights Agent | 資料分析和視覺效果 | <ul><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 25 | <ul><li>_7月趨勢訂單_</li><li>_依地區顯示收入。_</li><li>_依性別顯示從3月到6月的訂單。_</li><li>_我在6月獲利的前10大SKU為何_</li><li>_按月份計算的購買比例_</li><li>_依產品類別劃分的收入份額_</li></ul> |
| Journey Agent | 歷程構想 | <ul><li>Adobe Journey Optimizer (B2B edition)</li></ul> | 25 | <ul><li>_為想要用於我的解決方案的空白帳戶建立歷程，著重於參與網站內容的人員_</li></ul> |
| Journey Agent | 歷程建立 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 30 | <ul><li>_產生歷程以傳送提醒給過去7天內未完成首次購買的使用者_</li><li>_當使用者完成首次購買時，請在3天後透過電子郵件傳送簡訊確認及後續權益說明_</li></ul> |
| Journey Agent | 歷程分析 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 50 | <ul><li>_我想針對7月4日的行銷活動歷程依節點分析流失。_</li><li>_歷程X_&#x200B;是否有任何排程衝突</li><li>_顯示歷程X_&#x200B;的對象重疊衝突</li></ul> |
| Journey Agent | 歷程管理 | <ul><li>Adobe Journey Optimizer （B2B和B2C版本）</li></ul> | 25 | <ul><li>_我有多少個即時歷程？_</li><li>_列出使用對象X的所有歷程。_</li><li>_列出目前處於測試模式的所有歷程_</li></ul> |
| 產品支援代理 | 知識型疑難排解 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li><li>Adobe Journey Optimizer （B2C和B2B版本）</li><li>Customer Journey Analytics （B2C和B2B版本）</li></ul> | 0 | <ul><li>_為什麼我的設定檔計數在[授權使用儀表板]和Experience Platform首頁上不同？_</li><li>_歷程未觸發的原因是什麼？_</li><li>_Adobe Experience Platform如何建立即時體驗？_</li><li>_如何在Adobe Experience Platform中設定和使用警示？_</li><li>_在Adobe Experience Platform Activation中的平均設定檔豐富度限制是多少？_</li></ul> |
| 產品支援代理 | 支援案例建立和追蹤 | <ul><li>Real-Time CDP （B2B、B2C和B2P版本）</li>Adobe Journey Optimizer （B2C和B2B版本）<li>Customer Journey Analytics （B2C和B2B版本）</li><li>Adobe Experience Manager</li></ul> | 10 | <ul><li>_為我失敗的分段工作建立新的支援票證_</li><li>_票證E-001772068的狀態為何？_</li></ul> |
| 內容建議程式代理程式 | 內容探索 | <ul><li>Adobe Experience Manager Assets</li></ul> | 5 | <ul><li>_顯示建立WKND選件行銷活動的內容片段。_</li><li>_尋找產品封裝PNG影像。_</li><li>_在資料夾WKND中顯示已標籤的Office影像。_</li><li>_資料夾WKND中是否有任何svg？_</li><li>_顯示所有貸款申請表單。_</li><li>_我正在尋找員工入職表格。_</li></ul> |
| 內容建議程式代理程式 | <ul><li>內容最佳化</li></ul> | <ul><li>Adobe Experience Manager Assets</li></ul> | 10 | <ul><li>_以80%品質建立2000px轉譯為JPEG。_</li><li>_建立Instagram劇本的轉譯。_</li><li>_將影像以30%折扣的圖形覆蓋在促銷橫幅上，從中心放置100px。_</li><li>_將PNG的背景顏色變更為#ff8932。_</li></ul> |
| Brand Governance Agent | <ul><li>內容更新</li><li>Forms建立</li><li>管道疑難排解</li></ul> | <ul><li>Adobe Experience Manager雲端服務</li><li>Adobe Experience Manager Sites</li><li>Adobe Experience Manager Forms</li></ul> | 50 | <ul><li>_疑難排解我失敗的管道_</li><li>_列出主要方案的失敗管道。_</li><li>_分析我的失敗管道，稱為「開發管道」。_</li><li>_疑難排解管道執行1234567_</li></ul> |
| Brand Experience Agent | 網站現代化 | Adobe Experience Manager雲端服務 | 100 | <ul><li>_移轉頁面`https://wknd-trendsetters.site`_</li></ul> |

>[!NOTE]
>
>實際的AI點數消耗可能會因執行的步驟數以及每個步驟的反複專案而異。

## 有關此主題的更多說明

* [Experience Cloud中的Agentic AI](/help/interface/features/agentic-ai.md)
* [Adobe Experience Platform代理程式使用量繫結試用版](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-ai/experience-cloud-ai/agents/trial)
