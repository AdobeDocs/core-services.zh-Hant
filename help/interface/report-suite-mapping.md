---
description: 了解如何在 Experience Cloud 中將一個或多個報表套裝對應至組織。
title: '將報表套裝對應至組織 '
uuid: b983d5a6-b3d0-4137-ac53-bc5681d3e58b
feature: Admin Console
topic: 管理
role: Administrator
level: Experienced
exl-id: 4e9f0f7a-8e16-4473-af4a-3e74ad50c044
source-git-commit: 11b999ef0c0d4f258e8665eb9c5bf427f5d618c4
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 68%

---

# 將報表套裝對應至組織 {#topic_7C4740559EAC4E0FA5F8DEF886B580DA}

>[!NOTE]
>
>報表套裝對應功能已於 2020 年 11 月終止支援。如有任何疑問，請聯絡客戶支援。

Experience Cloud 服務 (例如 Experience Cloud ID Service 和 [!UICONTROL People]) 與組織相關聯而非個別報表套裝。為確保這些服務正常運作，每個 Analytics 報表套裝都必須對應至一個組織。對應程序：

* 將Experience Cloud組織設為報表套裝的主要組織。
* 不會變更可以存取報表套裝的人員 (存取權仍由每個使用者的 Adobe Analytics 登入帳戶決定)

## 需求

您必須是登入公司的 Analytics 管理員，才能存取您要對應的報表套裝。此外，此帳戶必須連結至Experience Cloud組織](organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)，才能將報表套裝對應至該組織。[

如果您沒有可存取特定報表套件組織的登入公司之 Analytics 管理員權限，組織一區則會顯示灰色。

## 將報表套裝對應至組織 {#task_23993FE78DF6455FA8D7BE60686EA16C}

1. 依序前往「[!DNL Analytics] > **[!UICONTROL 管理]** > **[!UICONTROL 資料管理]**」，導覽至「資料管理報表套裝」(請參閱[檢視/管理報表套裝的管理設定](https://experienceleague.adobe.com/docs/analytics/admin/data-governance/gdpr-view-settings.html?lang=en))。

1. 若要查看可存取每個報表套裝的登入公司資訊，請按一下&#x200B;**[!UICONTROL 只有登入公司能看見]**。

   此檢視模式的目的在於協助您在對應上做出明智的決策。

1. 按一下報表套裝旁邊&#x200B;**[!UICONTROL 「已對應組織」]**&#x200B;欄中的下拉式清單，並選取您要對應的組織。

   如需選取 Experience Cloud 組織的相關秘訣，請參閱下一節。

## 將多個報表套裝對應至組織 {#task_94955B0D8ABA4CB1A38746ECF8E32711}

1. 按一下 **[!UICONTROL Experience Cloud]** > **[!UICONTROL 管理]** > **[!UICONTROL 報表套裝對應]**。

1. 選取您要對應的報表套裝。

   ![](assets/rs-mapping-multiple.png)

1. 選取組織 (在此範例中為 Outdoors Inc)，然後按一下&#x200B;**[!UICONTROL 選取]**。

   如需選取 Experience Cloud 組織的相關秘訣，請參閱下一節。

1. 按一下&#x200B;**[!UICONTROL 儲存對應]**。

## 選取 Experience Cloud 組織的秘訣 {#mapping-tips}

本節提供的秘訣可協助您選擇應將報表套裝對應到哪個 Experience Cloud 組織。

### 我應選擇哪個組織？

如果報表套裝上已部署Experience CloudID服務，請確認您在報表套裝對應工具中選取的組織與網站上[!DNL visitorAPI.js]檔案中指定的組織相同。 您可以透過[測試及驗證 Experience Cloud ID 服務](https://experienceleague.adobe.com/docs/id-service/using/implementation/test-verify.html)中的指示，尋找訪客 ID 服務所使用的組織 ID。

請確定您的部署符合您在報表套裝對應工具中選擇的組織。

### 為什麼有些組織會變灰色？

淘汰組織表示您沒有足夠的權限對應至反灰的報表套裝。 考量下列範例：

![](assets/rs-mapping.png)

此圖表中，藍色圖例表示管理權限，灰線表示可見度。

此使用者可存取兩個 Experience Cloud 組織。他們已執行下列作業：

* 將其[!UICONTROL chapek] Analytics登入公司中的管理員帳戶連結至其[!UICONTROL Chapek] CorpExperience Cloud組織帳戶。
* 將其[!UICONTROL doohan] Analytics登入公司中的非管理員帳戶連結至其[!UICONTROL Chapek] CorpExperience Cloud組織帳戶。
* 將其Analytics登入公司nigel的非管理員帳戶連結至Nigel IncExperience Cloud組織帳戶。

以下幾點列出此使用者可以和無法針對這些報表套裝執行的的對應動作：

* [!UICONTROL Chapek-prod] 報表套裝可以對應至 [!UICONTROL Chapek] Corp org，因為此使用者是連結 Analytics 登入公司 ([!UICONTROL chapek]) 的管理員，且其帳戶已連結至此組織。
* [!UICONTROL 此使用] 者無法連結Nigel-prodreport套裝，因為他們並非任何可看到此報表套裝的登入公司的管理員。
* [!UICONTROL Doohan-prod] 報表套裝可對應至 [!UICONTROL Chapek Corp]，因為此使用者是連結至 Experience Cloud 組織的登入公司 ([!UICONTROL chapek]) 之管理員 (請注意，他並非 doohan Analytics 登入公司的管理員)。請務必了解，即使此使用者無法執行該對應，[!UICONTROL doohan-prod]報表套裝也有資格對應至Nigel IncExperience Cloud組織。 在這種情況下，兩個 Experience Cloud 組織都會顯示在清單中，但 [!UICONTROL Nigel Inc] 會呈現灰色。進行對應之前，此使用者應洽詢 nigel 登入公司的管理員，判斷最適合對應的組織。如果您選取的組織與報表套裝最初建立時所在的組織不同，UI會顯示「可能衝突」警告。

## 常見問答 {#section_099E485805994C929FF9C9F75219BEE1}

### 為何我看不到所有報表套裝？

您的某些報表套裝可能會顯示在不同的登入公司底下。您可以使用畫面上方的下拉式清單，變更目前的登入公司。

### 如果我不認識其中一個報表套裝的下拉式清單中列出的某些組織，該怎麼辦？

清單會顯示您的報表套裝可對應的所有&#x200B;*可能*&#x200B;組織，即使您並未擁有這些報表套裝的權限。如果您不確定報表套裝是否應對應至清單中其中一個灰色的報表套裝，請洽詢貴組織的Experience Cloud管理員以決定最佳選擇。

### 如果我不認識「只有登入公司能看見」欄中針對某個報表套裝列出的登入公司，該怎麼辦？

某時，此報表套裝會與其他登入公司共用，而後者可能屬於不同的Experience Cloud組織。

### 其他組織所產生有關報表套裝的這個「可能衝突」錯誤是什麼？其重要性為何？

此通知可協助您針對報表套裝對應做出明智的決策。 目的是要提醒您，此報表套裝原本是建立在不同組織底下，以防該組織更適合用於此報表套裝。

### 如何知道報表套裝是否已對應？

對應的報表套裝會以不可編輯的格式顯示。 如果您必須變更對應，請連絡客戶服務。

### 如果我只知道 Experience Cloud 組織的組織 ID 該怎麼辦？如何查詢組織 ID 的名稱？

您可以在[組織和帳戶設定](organizations.md)中找到您的組織名稱。

### 我在「已對應日期」欄中看到日期。該對應是誰執行的？

您可以參閱 Analytics 介面中的報表套裝變更記錄檔，查看進行變更的使用者 ID。尋找「與 IMS 組織相關聯的套裝」事件。