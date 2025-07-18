---
description: 了解解決方案資料來源及設定訂閱。 訂閱可讓客戶屬性資料在Experience Cloud和應用程式（Analytics和Target）之間流動。
solution: Experience Cloud
title: 如何設定訂閱
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
source-git-commit: 2f126877f6a5f090884ebe093f35e4f6d90b4df6
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 75%

---

# 如何在 Experience Cloud 中設定訂閱

了解應用程式資料來源及設定訂閱。 訂閱可啟用Experience Cloud和應用程式（[!DNL Analytics]和[!DNL Target]）之間的[!DNL customer attribute]資料流。

例如，Adobe Analytics 訂閱可啟用報表中的屬性資料。若您使用 Adobe Target，則可以上傳客戶屬性以用於目標鎖定和細分。

**[!UICONTROL 客戶屬性Source]** > **[!UICONTROL 建立新的客戶屬性Source]** > **[!UICONTROL 新增]**

![在 Experience Cloud 中設定訂閱](assets/configure_subscription_page.png)

| 元素 | 說明 |
|--- |--- |
| 解決方法 | **Adobe Analytics**<br>&#x200B;選取「[!DNL Analytics]」，指定您要用來接收屬性資料的報表套裝，以及要包含的屬性。<br>**Adobe Target**<br>&#x200B;您可上傳客戶屬性以用於鎖定和區隔。如果想根據屬性資料鎖定測試，或想在 Analytics 中將資料用於分段，這個功能會很好用。<br>訪客的已上傳客戶屬性資料在登入時即可使用，位於 **[!DNL Target]** > **客群**&#x200B;中。<br>支援多個資料來源您在網站上設定客戶ID時，請確定至少有一個別名訂閱了[!DNL Target]。 |
| 報表套裝(Adobe Analytics) | 來自 Analytics 的報表套裝。<br>在單一屬性來源的 Analytics 訂閱中，不可加入超過 10 個報表套裝。選擇要包含哪些報表套裝時，請考慮下列建議事項：<ul><li>選擇具有同一組已驗證客戶的報表套裝。如果一個報表套裝中的已驗證客戶與另一個報表套裝中的已驗證客戶沒有重疊，請將這些報表套裝區分至不同的屬性來源中。</li><li>如果可行，屬性來源中包含的報表套裝應具有類似的流量。</li></ul><br>如果超過 10 個報表套裝有同一組已驗證客戶，可以設定額外的客戶屬性來源，每個各有最多 10 個報表套裝。 |
| 要包含的屬性（Analytics和[!DNL Target]） | 您要傳送給應用程式的屬性。 <br>設定訂閱及選取屬性時，系統會根據您擁有的應用程式，_針對每個報表套裝_&#x200B;套用以下限制：<ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：每一報表套裝 200 個</li><li>[!DNL Target] Standard：5 個</li><li>[!DNL Target] Premium：200 個</li></ul><br>**注意：**&#x200B;升級至 Analytics Premium 後，您必須等待 24 小時才可使用其他屬性。在這段延遲期間，您可能會看到已核發的屬性訂閱上限錯誤。 |

{style="table-layout:auto"}
