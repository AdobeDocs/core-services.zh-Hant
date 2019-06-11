---
description: 管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。
keywords: 升級
seo-description: 管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。
seo-title: 升級至 Analytics Premium 和 Experience Cloud
solution: Experience Cloud
title: 升級至 Analytics Premium 和 Experience Cloud
topic: Premium
uuid: 450a601c-d199-4e90-b525-19bd9 f9576 d
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 升級至 Analytics Premium 和 Experience Cloud

管理員可瞭解升級至 Analytics Premium 的需求以及期望，以及何處提供 Experience Cloud 管理員的相關說明。


## Analytics Premium {#section_7F50AD7906544F899B844BE31D3BB507}

升級至 Adobe Analytics Premium 可以取得 Analytics Standard 提供的完整功能或產品，包括資料倉庫、臨機分析、報告建立工具和 Data Connectors。(這些產品單獨出售給使用單點解決方案 SiteCatalyst 的客戶。)

Analytics Premium 可讓您:

* 存取 250 個轉換變數 (eVar)
* [行動應用程式分析](https://marketing.adobe.com/resources/help/en_US/mobile/)
* 資料工作台 (視覺資料查詢、規則型歸因、跨頻道分析)



>[!NOTE]
>
>升級無須進行移轉，但需注意以下幾點:
>
>* eVar 76-250 (SiteCatalyst) 和 100-250 (Standard) 會顯示在管理工具中，但尚未啟用。&gt;
>* Adobe 會開啟貢獻分析。不會變更位置 (仍可從「異常偵測」頁面使用)，但現在會自動開始分析所有資料點。&gt;


以下章節說明如何根據您購買的功能尋找說明:

* [Analytics Premium 完整版](../admin-getting-started/upgrade-to-analytics-premium.md#section_BFAD815EDF364845A52B340B2FD5B64C)
* [Predictive Intelligence](../admin-getting-started/upgrade-to-analytics-premium.md#section_B407932C07A7476F83FB0275C3FB63DC)
* [Customer 360](../admin-getting-started/upgrade-to-analytics-premium.md#section_3B2AC245388248688067DC9A48957AFB)
* [進階歸因](../admin-getting-started/upgrade-to-analytics-premium.md#section_9E4986A8389946CCAA7D003268343296)
* [資料工作台需求](../admin-getting-started/upgrade-to-analytics-premium.md#section_D959CA68D6DB42C38707F8E0CA3654CC)
* [Experience Cloud](../admin-getting-started/upgrade-to-analytics-premium.md#section_6471C54454024301B2E0B687F79F6738)



## Analytics Premium 完整版 {#section_BFAD815EDF364845A52B340B2FD5B64C}

在 Analytics Premium 完整版中，您可取得 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的所有功能，再加上下列升級項目:

| 產品 | 升級 |
|--- |--- |
| Reports &amp; Analytics | <ul><li>[貢獻分析](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/)</li><li>[客戶屬性](../attributes/attributes.md#concept_ACFEE7C8B8E94875BA0825CDF4913AF1) (高達 200 個)</li></ul> |
| Data Workbench | <ul><li>演算法歸因</li><li>預先建立工作區</li></ul> |
| Analytics 平台 | [即時資料流](https://marketing.adobe.com/developer/documentation/analytics-live-stream/overview-1) (原始資料、控制面板、觸發器) |


## Predictive Intelligence {#section_B407932C07A7476F83FB0275C3FB63DC}

升級至 Predictive Intelligence 可啟用 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，再加上:

| 產品 | 升級 |
|---|---|
| Reports &amp; Analytics | [貢獻分析](https://marketing.adobe.com/resources/help/en_US/analytics/contribution/) |
| Data Workbench | 受眾資格和預測行銷的預先建立工作區。 |
| Analytics 平台 | 即時資料流 (控制面板和觸發器) |


## Customer 360 {#section_3B2AC245388248688067DC9A48957AFB}

升級至 Customer 360 可提供 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507)，再加上:

| 產品 | 升級 |
|--- |--- |
| [客戶屬性](../attributes/attributes.md) | 客戶屬性 (分析和區隔共用) |
| Data Workbench | <ul><li>衍生客戶屬性</li><li>受眾探索的預先建立工作區</li></ul> |
| Analytics 平台 | [客戶屬性](../attributes/attributes.md) |


## 進階歸因 {#section_9E4986A8389946CCAA7D003268343296}

進階歸因提供 [Analytics Premium](../admin-getting-started/upgrade-to-analytics-premium.md#section_7F50AD7906544F899B844BE31D3BB507) 的存取，再加上資料工作台中的演算法歸因 (25% 伺服器呼叫容量)。

## 資料工作台需求 {#section_D959CA68D6DB42C38707F8E0CA3654CC}

獲支援的使用者可以寄送電子郵件至 `dwb@adobe.com`，要求更新所有用戶端授權以符合 Premium。這可啟用演算法歸因等功能。

TechOps 會審查您的合約保證，判斷適合的受管理基礎結構、增加或減少功能，然後透過客戶經理或顧問與您合作，以便部署變更。

內部部署執行的所有軟體都必須停用。其中包括感應器，這表示您必須確保能透過 Analytics 標記進行適當追蹤。

**Premium 完整版** 和 **進階歸因**

對於預先建立範本中的規則型歸因，請參閱: [規則型歸因](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_rules_attrib)。

對於演算法歸因，請參閱: [最適歸因](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_attrib_algorithmic)

**Predictive Intelligence**

資料工作台中的 Predictive intelligence 包括下列視覺效果:

* [受眾傾向得分](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_visitor_propensity)
* [訪客叢集](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_visitor_cluster)
* [關聯分析](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_correlation_analysis)


**Customer 360** 和 **進階歸因**

請參閱[規則型歸因](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_rules_attrib)中，預先建立範本的 Analytics 規則型歸因。

請參閱[最適歸因](https://marketing.adobe.com/resources/help/en_US/insight/client/?f=c_attrib_algorithmic)中的演算法歸因。。

## Experience Cloud - 管理使用者和產品 {#section_6471C54454024301B2E0B687F79F6738}

Experience Cloud和核心服務可供Analytics Standard和Premium使用者使用，前提是您已遵循快速入門中 [所述的實作現代化-啓用核心服務的解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)。(該程序可協助您導入最新的實作方式，並可讓您成為 Experience Cloud 的管理員)。

加入 Experience Cloud 後，您就能在 [!DNL marketing.adobe.com] 透過 Experience Cloud 登入，並開始使用核心服務 (包括客戶屬性、受眾和行動應用程式分析)。

**管理使用者和群組**

您可以在 [Adobe Admin Console](https://helpx.adobe.com/enterprise/help/aedash.html) (產品連結) 中管理使用者。

您可以在 Adobe Admin Console 中建立的群組和解決方案群組 (例如 Adobe Analytics) 之間設定 1:1 對應。之後，新增至已對應 Admin Console 群組的使用者都會自動建立 Analytics 解決方案帳戶，並連結至該使用者的 Adobe ID。(現有使用者必須手動連結自己的解決方案帳戶憑證，才能透過 Experience Cloud 登入存取解決方案)。


>[!NOTE]
>
>您可以將數個解決方案群組對應至一個管理控制台群組。但是 Adobe 建議 1:1 對應。事先對應群組可讓您透過上傳 CSV 邀請、建立、授予權限和新增多個使用者。

