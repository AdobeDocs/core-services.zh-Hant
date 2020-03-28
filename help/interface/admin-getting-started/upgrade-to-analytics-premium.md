---
description: 管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。
keywords: upgrading
seo-description: 管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。
seo-title: 升級至 Analytics Premium 和 Experience Cloud
solution: Experience Cloud
title: 升級至 Analytics Premium 和 Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9f9576d2
translation-type: tm+mt
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e

---


# 升級至 Analytics Premium 和 Experience Cloud

管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。

## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升級至Adobe Analytics Premium可為您提供Analytics Standard的所有功能或產品，包括資料倉庫、臨機分析、報告建立工具和資料連接器。 （這些產品是單獨銷售給使用點式解決方案SiteCatalyst的客戶。）

Analytics Premium提供您：

* 存取250個轉換變數(eVar)
* [行動應用程式分析](https://docs.adobe.com/content/help/en/mobile-services/using/home.html)
* 資料工作台 (視覺資料查詢、規則型歸因、跨頻道分析)

>[!NOTE]
>
>升級時不需要進行遷移，但需注意以下幾點：
>
>* eVar 76-250(SiteCatalyst)和100-250（標準）將會顯示在「管理工具」中，但尚未啟用。>
>* 貢獻分析由Adobe開啟。 它不會變更位置（仍可在「異常偵測」頁面上使用），但現在會自動開始分析所有資料點。>


## Analytics Premium 完整版 {#section_BFAD815EDF364845A52B340B2FD5B64C}

在Analytics Premium Complete中，您可取得 [Analytics Premium的所有功能](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，以及下列升級：

| 產品 | 升級 |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢獻分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html)</li><li>[客戶屬性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (高達 200 個)</li></ul> |
| Data Workbench | <ul><li>演算法歸因</li><li>預先建立的工作區</li></ul> |
| Analytics平台 | [即時串流](https://helpx.adobe.com/analytics/kb/getting-started-with-livestream-api.html) （原始資料、控制面板、觸發器） |

## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升級至Predictive Intelligence可讓 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 加上：

| 產品 | 升級 |
|---|---|
| Reports &amp; Analytics | [貢獻分析](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/virtual-analyst/contribution-analysis/ca-tokens.html) |
| Data Workbench | 受眾資格和預測性行銷的預先建立工作區。 |
| Analytics平台 | 即時串流（控制面板和觸發器） |

## 客戶360 {#section_3B2AC245388248688067DC9A48957AFB}

升級至Customer 360提供 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) ，另外：

| 產品 | 升級 |
|--- |--- |
| [客戶屬性](../attributes/attributes.md) | 客戶屬性 (分析和區隔共用) |
| Data Workbench | <ul><li>衍生客戶屬性</li><li>預先建立的受眾探索工作區</li></ul> |
| Analytics平台 | [客戶屬性](../attributes/attributes.md) |

## 進階歸因 {#section_9E4986A8389946CCAA7D003268343296}

進階歸因提供 [Analytics Premium的存取權](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，以及資料工作台中的演算法歸因（25%伺服器呼叫量）。

## 資料工作台需求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

獲支援的使用者可以寄送電子郵件至 `dwb@adobe.com`，要求更新所有用戶端授權以符合 Premium。這可啟用演算歸因等功能。

TechOps將審查您的合約承諾，並確定適當的受管理基礎架構、增加或減少容量，然後他們將通過客戶經理或咨詢與您協調，以部署任何更改。

任何內部部署執行的軟體都必須停用。 這包括感測器，這表示您需要確保透過Analytics標籤進行正確追蹤。

## Experience Cloud - 管理使用者和產品 {#section_6471C54454024301B2E0B687F79F6738}

假設您已按照[快速入門 - 啟用核心服務的解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)中的實作最新化進行作業，Analytics Standard 和 Premium 使用者即可使用 Experience Cloud 和核心服務。(該程序可協助您導入最新的實作方式，並可讓您成為 Experience Cloud 的管理員)。

加入 Experience Cloud 後，您就能在 [!DNL experiencecloud.adobe.com] 透過 Experience Cloud 登入，並開始使用核心服務 (包括客戶屬性、受眾和行動應用程式分析)。

### 管理使用者和群組

使用者管理是在 [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) （產品連結）中執行。

您可以在Adobe Admin Console中建立的群組和解決方案群組（例如Adobe Analytics）之間設定1:1對應。 之後，新增至映射「管理控制台」群組的新使用者將會自動建立Analytics解決方案帳戶並連結至使用者的Adobe ID。 （現有使用者必須手動連結其解決方案帳戶認證，才能透過Experience Cloud登入存取解決方案。）

>[!NOTE]
>
>您可將數個解決方案群組對應至一個 Admin Console 群組。不過，Adobe建議使用1:1對應。 提前對應群組可讓您透過上傳CSV來邀請、建立、權限和新增多個使用者。
