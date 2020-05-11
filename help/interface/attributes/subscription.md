---
description: 瞭解解決方案資料來源和設定訂閱。 訂閱可讓客戶屬性資料在Experience Cloud和解決方案（Analytics和Target）之間流動。
keywords: Customer Attributes;core services
seo-description: 瞭解解決方案資料來源和設定訂閱。 訂閱可讓客戶屬性資料在Experience Cloud和解決方案（Analytics和Target）之間流動。
seo-title: 設定訂閱
solution: Experience Cloud
title: 設定訂閱
uuid: f74a8155-0a21-46b3-9b1e-4c838f72f24f
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 43%

---


# 設定訂閱

瞭解解決方案資料來源和設定訂閱。 訂閱可讓客戶屬性資料在Experience Cloud和解決方案(Analytics和 [!DNL Target])之間流動。

例如，Adobe Analytics訂閱可啟用報表中的屬性資料。 如果您使用Adobe Target，可以上傳客戶屬性以進行定位和劃分。

**[!UICONTROL 客戶屬性來源]** >建 **[!UICONTROL 立新客戶屬性來源]** >新 **[!UICONTROL 增]**

![](assets/configure_subscription_page.png)

| 元素 | 說明 |
|--- |--- |
| 解決方法 | **Adobe Analytics **<br>選取 Analytics，指定您要用來接收屬性資料的報表套裝，以及要包含的屬性。<br>**Adobe**<br>Target您可以上傳客戶屬性以進行定位和區隔。 如果想根據屬性資料鎖定測試，或想在 Analytics 中將資料用於分段，這個功能會很好用。<br>已上傳的訪客客戶屬性資料可在登入時使用，位&#x200B;**[!DNL Target]**於>**&#x200B;觀眾&#x200B;**。<br>支援多個資料來源您在網站上[設定客戶 ID](../core-services/core-services.md)時，請確定至少有一個別名訂閱了[!DNL Target]. |
| 報表套裝 (Analytics) | 來自 Analytics 的報表套裝。<br>在單一屬性來源的 Analytics 訂閱中，不可加入超過 10 個報表套裝。選擇要包含的報表套裝時，請考慮下列建議：<ul><li>選擇具有一組共同驗證客戶的報表套裝。 如果一個報表套裝中的已驗證客戶與另一個報表套裝中的已驗證客戶沒有重疊，請將這些報表套裝分隔為不同的屬性來源。</li><li>如果可能，屬性來源中包含的報表套裝應具有類似的流量。</li></ul><br>如果超過 10 個報表套裝有同一組已驗證客戶，可以設定額外的客戶屬性來源，每個各有最多 10 個報表套裝。 |
| 要包含的屬性 (Analytics 和 [!DNL Target]) | 您要傳送至解決方案的屬性。 <br>設定訂閱和選取屬性時，會根據您擁有的 _解決方案_ ，針對每個報表套裝套用下列限制：<ul><li>Foundation: 0 個</li><li>Select: 3 個</li><li>Prime: 15 個</li><li>Ultimate: 200 個</li><li>Standard 版: 共 3 個</li><li>Premium 版: 每一報表套裝 200 個</li><li>[!DNL Target] 標準： 5</li><li>[!DNL Target] Premium: 200</li></ul><br>**注意:**升級至 Analytics Premium 後，您必須等待 24 小時才可使用其他屬性。在這段期間，您可能會看到已達到屬性訂閱上限錯誤。 |
