---
description: 瞭解如何在 [!DNL Customer Attributes] 中設定Analytics和Target的訂閱，以及啟用資料來源。
solution: Experience Cloud
title: 如何在 [!DNL Customer Attributes]中設定訂閱
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: cfa2aa5c-337f-401e-80eb-cbe36cb1d41e
TQID: https://experienceleague.adobe.com/I--LZ-Nqu0VdVAAs8qvv88pZTcaRQ97XiHWXd15WQcE
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 421
ht-degree: 46%

---

# 設定客戶屬性訂閱

[!DNL Customer Attributes]訂閱可讓客戶屬性資料在CX Enterprise和應用程式（[!DNL Analytics]和[!DNL Target]）之間流動。

例如，Adobe Analytics 訂閱可啟用報表中的屬性資料。 如果您使用[!DNL Adobe Target]，則可上傳客戶屬性以用於目標定位和細分。

**若要設定訂閱及啟用資料來源**

1. 在[!DNL Customer Attributes]中找到您的資料來源以進行編輯：

   在[!DNL CX Enterprise]中，按一下&#x200B;**[!UICONTROL 應用程式]** ![功能表](assets/menu-icon.png) > **[!DNL Customer Attributes]**。

1. 在[!UICONTROL 編輯客戶屬性Source]上，按一下&#x200B;**[!UICONTROL 檔案上傳]**。

1. 按一下&#x200B;**[!UICONTROL 設定訂閱]**。

   ![在CX Enterprise中設定訂閱](assets/configure-subscriptions.png)

1. 若要啟用客戶屬性來源，請按一下[啟用] **&#x200B;**，然後按一下[儲存] **&#x200B;**。

1. 若要設定[!DNL Analytics]或[!DNL Target]的訂閱，請按一下[設定]。**&#x200B;**

   下列範例顯示[!DNL Target]訂閱：

   ![步驟結果](assets/subscription-target.png)

   | 元素 | 說明 |
   | --- | --- |
   | 解決方法 | **Adobe Analytics**<br>&#x200B;選取「[!DNL Analytics]」，指定您要用來接收屬性資料的報表套裝，以及要包含的屬性。<br>**Adobe Target**<br>&#x200B;您可上傳客戶屬性以用於鎖定和區隔。 若要根據屬性資料鎖定測試，或在Analytics中讓資料可用於分段，此功能相當實用。<br>訪客的已上傳客戶屬性資料在登入時即可使用，位於&#x200B;**[!DNL Target]** > **受眾**&#x200B;中。<br>支援多個資料來源。 您在網站上設定客戶ID時，請確定至少有一個別名訂閱了[!DNL Target]。 |
   | 報表套裝(Adobe Analytics) | 報表套裝來自Analytics。<br>在單一屬性來源的Analytics訂閱中，不可加入超過10個報表套裝。 選擇要包含哪些報表套裝時，請考慮下列建議事項：<ul><li>選擇具有同一組已驗證客戶的報表套裝。 如果一個報表套裝中的已驗證客戶與另一個報表套裝中的已驗證客戶沒有重疊，請將這些報表套裝區分至不同的屬性來源中。</li><li>如果可行，屬性來源中包含的報表套裝應具有類似的流量。</li></ul><br>如果超過 10 個報表套裝有同一組已驗證客戶，可以設定額外的客戶屬性來源，每個各有最多 10 個報表套裝。 |
   | 要包含的屬性 (Analytics 和 [!DNL Target]) | 您要傳送給應用程式的屬性。 <br>設定訂閱及選取屬性時，系統會根據您擁有的應用程式，_針對每個報表套裝_&#x200B;套用以下限制：<ul><li>Foundation：0 個</li><li>Select：3 個</li><li>Prime：15 個</li><li>Ultimate：200 個</li><li>Standard：共 3 個</li><li>Premium：每一報表套裝 200 個</li><li>[!DNL Target] Standard：5 個</li><li>[!DNL Target] Premium：200 個</li></ul><br>**注意：**&#x200B;升級至 Analytics Premium 後，您必須等待 24 小時才可使用其他屬性。 在這段延遲期間，您可能會看到已核發的屬性訂閱上限錯誤。 |

1. 按一下「**[!UICONTROL 儲存]**」。
