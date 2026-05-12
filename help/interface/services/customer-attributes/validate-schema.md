---
description: 瞭解如何驗證Adobe CX Enterprise中的 [!DNL Customer Attributes] 結構描述。
solution: Experience Cloud
title: 如何驗證 [!DNL Customer Attributes] 結構描述
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 776d1fd3-c733-4970-a76b-4c3c0119ee77
TQID: https://experienceleague.adobe.com/J-AaDn4HtD1bS-VCPn2XiPLVBbTnYyl5o1NpJ9HFj1g
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 43%

---

# 驗證結構描述

驗證程序可讓您將顯示名稱和說明對應至已上傳的屬性 (字串、整數、數字等)。

系統會根據這些設定來建立結構。 此結構用於驗證將來上傳至此資料來源的所有資料。 這個對應程序不會更改原始資料。

>[!NOTE]
>
>在驗證後更新結構會刪除客戶屬性。 請參閱[更新結構 (也會刪除屬性)](t-crs-usecase.md)。

**驗證結構描述**

1. 在[!DNL Customer Attributes]中，按一下要編輯的屬性來源。

1. 在&#x200B;**[!UICONTROL Edit Customer Attribute Source]**&#x200B;上，按一下&#x200B;**[!UICONTROL File Upload]**。

1. 在[!UICONTROL File Upload and Schema Validation]頁面上，按一下&#x200B;**[!UICONTROL Actions]** > **[!UICONTROL View/Edit Schema]**

   ![編輯結構](assets/actions.png)

   在[!UICONTROL Edit Schema]頁面上，結構描述的每一列代表上傳之CSV檔案的一欄。

   在CX Enterprise中![編輯結構描述頁面](assets/schema-edit.png)

**動作**

* **[!UICONTROL Add Data:]**&#x200B;上傳新的屬性資料到此資料來源。

* **[!UICONTROL View/Edit Schema:]**&#x200B;將顯示名稱對應至屬性資料，如下一個步驟所述。

* **[!UICONTROL FTP Setup:]**&#x200B;建立您的FTP帳戶以[透過FTP上傳您的資料](t-upload-attributes-ftp.md) （選擇性）。

* **[!UICONTROL ID Lookup:]**&#x200B;輸入您`.csv`中的客戶ID (CID)以查詢該ID的CX Enterprise資訊。 在疑難排解訪客的屬性資料為何沒有顯示時，此功能很實用：

   * **[!UICONTROL ECID (CX Enterprise ID):]**&#x200B;在您使用最新的CX Enterprise ID服務時顯示。 如果您使用MCID服務，但此處未列出ID，表示CX Enterprise尚未收到該CID的別名。 這表示訪客還沒登入，或您的實作沒有傳遞該 ID。

   * **[!UICONTROL CID (customer ID):]**&#x200B;與此CID關聯的屬性。 如果您使用 prop 或 eVar 上傳 CID (AVID)，有看到屬性顯示但沒有 AVID，這表示訪客尚未登入您的網路。

   * **[!UICONTROL AVID (Analytics visitor ID):]**&#x200B;在您使用prop或eVar上傳CID時顯示。 如果這些ID正傳遞至CX Enterprise，則此處會顯示與您輸入的CID相關聯的任何訪客ID。
