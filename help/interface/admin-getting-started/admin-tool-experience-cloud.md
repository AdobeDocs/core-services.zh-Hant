---
description: 瞭解 Experience Cloud 管理工具，用於檢視所有 Experience Cloud 使用者的可排序和可篩選清單。
keywords: core services
seo-description: 瞭解 Experience Cloud 管理工具，用於檢視所有 Experience Cloud 使用者的可排序和可篩選清單。
seo-title: 檢視 Experience Cloud 使用者和使用者詳細資訊
solution: Experience Cloud
title: '檢視 Experience Cloud 使用者和使用者詳細資訊 '
index: true
translation-type: ht
source-git-commit: 43de353155c640b3ddc519147c94d7e9ffcafe4e
workflow-type: ht
source-wordcount: '693'
ht-degree: 100%

---


# 在管理工具中檢視 Experience Cloud 使用者

管理員可以在管理工具中，檢視所有 Experience Cloud 使用者及其詳細資訊，且可將清單加以排序及篩選。使用者詳細資訊包括使用者的產品存取情形、角色，以及上次存取的資訊。(**注意：**&#x200B;使用者和產品管理需在 [Admin Console](admin-getting-started.md) 中設定。)

1. 登入 `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. 在 Experience Cloud 首頁上，按一下&#x200B;**[!UICONTROL 管理工具]**。

   (或者，您可以將首頁 URL 中的 _home_ 取代為 _admin_。)

   [!UICONTROL 使用者]頁面隨即顯示。

## 「使用者」頁面

此頁面顯示貴組織中可存取 Experience Cloud 的使用者完整清單。它提供解決方案權限和上次登入的相關資訊。您可以搜尋、排序和篩選使用者清單以取得自訂檢視。

![](assets/admin-tool-users.png)

| 元素 | 說明 |
|---|---|
| [!UICONTROL 名稱] | 使用者的名字和姓氏。您可以將此欄由 A 到 Z 和 Z 到 A 排序。按一下使用者名稱即可查看有關該使用者的詳細資訊。 |
| [!UICONTROL 電子郵件] | 與使用者相關聯的電子郵件地址。欄可以按 A->Z、Z->A 排序。 |
| [!UICONTROL ID 類型] | 使用者帳戶的身分類型。可套用篩選器以檢視特定 ID 類型。如需詳細資訊，請參閱[管理身分類型](https://helpx.adobe.com/tw/enterprise/using/identity.html)。 |
| [!UICONTROL 解決方案] | 使用者可存取的 Experience Cloud 解決方案摘要。您可以套用篩選器，依特定解決方案存取權縮小使用者清單的範圍。 |
| [!UICONTROL 上次登入] | 使用者上次登入 Experience Cloud 的時間和日期。此欄可依遞增或遞減日期排序。<br> **重要：**&#x200B;自 2020 年 1 月 13 日起，使用者的上次登入資料會保留 365 天。這項資訊的用途是顯示 Experience Cloud 中的目前登入活動，而不是建議在 2020 年 1 月 13 日之前對非作用中帳戶採取行動。 |

## 自訂使用者清單檢視

您可以搜尋、排序或篩選欄以自訂使用者清單。

* 依名稱或電子郵件搜尋使用者。搜尋會比對您輸入的文字字串。
* 依遞增或遞減值排序欄。這會套用至[!UICONTROL 名稱]、[!UICONTROL 電子郵件]和[!UICONTROL 上次登入]欄。
* 按一下&#x200B;**[!UICONTROL 篩選條件]**&#x200B;圖示，套用多個篩選器以列出具有特定條件的使用者。套用多個篩選器類別時，搜尋會包含「電子郵件網域」`AND`「ID 類型」`AND`「解決方案」。

| 元素 | 說明 |
|---------|----------|
| [!UICONTROL 電子郵件網域]篩選器 | 在「電子郵件」欄中搜尋字元字串，將結果縮小至一或多個網域。在每個搜尋詞後按 Enter 鍵即可新增多個篩選器 |
| [!UICONTROL ID 類型]篩選器。 | 從可用的 ID 類型中選擇。多個 ID 類型均可作為篩選器使用。 |
| [!UICONTROL 解決方案]篩選器 | 從可用的解決方案中選擇。多個解決方案篩選器搜尋包含「解決方案1」`OR`「解決方案 2」的結果。 |

## 檢視使用者詳細資訊

在[!UICONTROL 使用者]頁面上，若要檢視使用者的詳細資訊，請按一下使用者的電子郵件。

![](assets/admin-tool-user-details.png)

每位使用者的詳細檢視中，會顯示有關使用者解決方案存取權、管理員和產品角色以及上次存取資訊的重要詳細資訊。

## 關於區段

本區段顯示使用者帳戶的摘要，包括：

* 使用者顯示圖片和系統管理員徽章 (如果適用)
* 名稱
* 電子郵件
* 使用者名稱 (Federated ID 帳戶的使用者名稱可能與電子郵件地址不同)
* [ID 類型](https://helpx.adobe.com/tw/enterprise/using/identity.html)
* 國家/地區
* 上次登入

## 解決方案摘要

本區段顯示使用者可存取的 Experience Cloud 解決方案摘要。包含產品管理角色 (如果適用)。

## 詳細的產品存取清單

本區段顯示使用者所有產品設定檔成員資格的完整清單。

| 元素 | 說明 |
|---------|----------|
| [!UICONTROL 產品] | 與產品設定檔相關聯的產品名稱。 |
| [!UICONTROL 例項] | 與產品和產品設定檔相關聯的例項名稱 (例如登入公司或租用戶)。 |
| [!UICONTROL 產品設定檔] | 產品設定檔的不重複名稱。 |
| [!UICONTROL 依群組指派] | 為使用者與產品設定檔建立關聯的使用者群組名稱。空白結果表示使用者是直接指派給產品設定檔，而非透過群組。 |
| [!UICONTROL 產品角色] | 產品設定檔中的使用者角色指派。目前此資訊僅適用於 Adobe Target 產品設定檔。 |
