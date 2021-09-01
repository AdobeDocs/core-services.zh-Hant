---
description: 了解升級至 Analytics Premium 時的需求和期望。
keywords: Adobe Analytics Premium 升級
solution: Experience Cloud
title: '升級至 Analytics Premium 和 Experience Cloud '
topic: Administration
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
feature: Admin Console
role: Admin
level: Experienced
exl-id: 746d396d-9629-42db-8c55-07d2d24e4611
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 100%

---

# 升級至 Analytics Premium 和 Experience Cloud

管理員可了解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升級至 Adobe Analytics Premium 即可使用 Analytics Standard 的所有功能或產品，包括 Data Warehouse、Ad Hoc Analysis、Report Builder 和 Data Connectors。

Analytics Premium 提供您：

* 存取 250 個轉換變數 (eVar)
* [行動應用程式分析](https://experienceleague.adobe.com/docs/mobile-services/using/home.html?lang=zh-Hant)
* Data Workbench (視覺資料查詢、規則型歸因、跨管道分析)

>[!NOTE]
>
>升級時不需要進行移轉，但需注意以下幾點：
>
>* eVars 76-250 和 100-250 (標準) 會出現在管理工具中，但未啟用。
>* 貢獻分析由 Adobe 開啟。這不會變更位置 (仍可在「異常偵測」頁面上使用)，但會自動開始分析所有資料點。


## Analytics Premium 完整版 {#section_BFAD815EDF364845A52B340B2FD5B64C}

在 Analytics Premium 完整版中，您可取得 [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的所有功能及下列升級項目：

| 產品 | 升級 |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢獻分析](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=zh-Hant)</li><li>[客戶屬性](attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (高達 200 個)</li></ul> |
| Data Workbench | <ul><li>演算法歸因</li><li>預先建立的 Workspace</li></ul> |
| Analytics Platform | [Live Stream](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/index.md) (原始資料、控制面板、觸發器) |

{style=&quot;table-layout:auto&quot;}

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升級至 Predictive Intelligence可讓 [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 加上：

| 產品 | 升級 |
|---|---|
| Reports &amp; Analytics | [貢獻分析](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html?lang=en) |
| Data Workbench | 預先建立的 Workspace，用於決定對象資格和預測性行銷。 |
| Analytics平台 | Live Stream (控制面板和觸發器) |

{style=&quot;table-layout:auto&quot;}

## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

升級至 Customer 360 可提供 [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 加上：

| 產品 | 升級 |
|--- |--- |
| [客戶屬性](attributes.md) | 客戶屬性 (分析和區隔共用) |
| Data Workbench | <ul><li>衍生客戶屬性</li><li>預先建立的 Workspace，用於進行對象探索</li></ul> |
| Analytics平台 | [客戶屬性](attributes.md) |

{style=&quot;table-layout:auto&quot;}

## 進階歸因 {#section_9E4986A8389946CCAA7D003268343296}

進階歸因提供 [Analytics Premium](upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的存取權，加上 Data Workbench 中的演算法歸因功能 (25% 伺服器呼叫量)。

## Data Workbench 需求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

獲支援的使用者可以寄送電子郵件至 `dwb@adobe.com`，要求更新所有用戶端授權以符合 Premium。此更新可啟用演算法歸因等功能。

TechOps 將會審核您的合約承諾，並決定適當的受託基礎架構、增加或減少容量，然後會透過客戶經理或咨詢與您協調以部署任何變更。

任何內部部署的執行中軟體都必須停用。此軟體包含 Sensors，表示您必須確保透過 [!DNL Analytics] 標記進行適當追蹤。

## Experience Cloud - 管理使用者和產品 {#section_6471C54454024301B2E0B687F79F6738}

假設您已按照[快速入門 - 啟用核心服務的解決方案](core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)中的實作最新化進行作業，Analytics Standard 和 Premium 使用者即可使用 Experience Cloud 和核心服務。(該程序可協助您導入最新的實作方式，並可讓您成為 Experience Cloud 的管理員)。

加入 Experience Cloud 後，您就能在 [!DNL experience.adobe.com] 透過 Experience Cloud 登入，並開始使用核心服務 (包括客戶屬性、Audiences 和行動應用程式分析)。

### 管理使用者和群組

您可以在 [Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/using/admin-console.html) (產品連結) 中管理使用者。

您可以在 Adobe Admin Console 中建立的群組和解決方案群組 (例如 Adobe Analytics) 之間設定 1 對 1 的對應。此後，將新使用者新增至對應 Admin Console 群組時，系統會自動建立 Analytics 解決方案帳戶並連結至該使用者的 Adobe ID。(現有使用者必須手動連結其解決方案帳戶憑證，才能透過 Experience Cloud 登入存取解決方案。)

>[!NOTE]
>
>您可將數個解決方案群組對應至一個 Admin Console 群組。不過 Adobe 建議使用 1 對 1 的對應。提前對應群組可讓您透過上傳 CSV 來邀請、建立、和新增多個使用者，以及為其提供權限。
