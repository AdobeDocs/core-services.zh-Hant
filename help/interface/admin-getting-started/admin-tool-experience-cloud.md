---
description: 瞭解Experience Cloud管理工具，以檢視所有Experience Cloud使用者和原則的可排序和可篩選清單。
keywords: core services
seo-description: 瞭解Experience Cloud管理工具，以檢視所有Experience Cloud使用者和原則的可排序和可篩選清單。
seo-title: 檢視 Experience Cloud 使用者和使用者詳細資訊
solution: Experience Cloud
title: '檢視 Experience Cloud 使用者和使用者詳細資訊 '
index: true
translation-type: tm+mt
source-git-commit: fa03e384d1dc878d45ef4b8d1f6fe269734ea891
workflow-type: tm+mt
source-wordcount: '1271'
ht-degree: 52%

---


# 在管理工具中檢視Experience Cloud使用者和原則

管理員可以使用管理工具的詳細資訊，檢視所有Experience Cloud使用者和原則的可排序和可篩選清單。 使用者詳細資訊包括使用者的產品存取情形、角色，以及上次存取的資訊。 原則詳細資訊包括原則的（產品設定檔）使用者、群組、開發人員、整合與管理清單，以及原則的詳細權限與資源資訊。

>[!NOTE]
>
>User and product management is configured in the [Admin Console](admin-getting-started.md).

1. 登入 `https://experience.adobe.com/.`

   ![](assets/admin-tool.png)

1. 在「快 [!UICONTROL 速存取]」下，按一 **[!UICONTROL 下「管理工具」。]**

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

## 「策略」頁

此頁面會顯示您組織中的Experience Cloud原則完整清單。 它提供產品、例項、使用者和開發人員的相關資訊。 您可以搜尋、排序和篩選原則清單的自訂檢視。

![](assets/admin-tool-policies.png)

| 元素 | 說明 |
|---|---|
| [!UICONTROL 產品設定檔] | 產品設定檔的名稱。 列可以排序A->Z、Z->A。按一下產品描述檔的名稱，以檢視有關原則的詳細資訊。 |
| [!UICONTROL 產品] | 與產品設定檔相關聯的產品。 欄可以按 A->Z、Z->A 排序。 |
| [!UICONTROL 例項] | 與產品設定檔相關聯的例項（例如租用戶或登入公司）。 沒有唯一例項或租戶的產品會顯示&quot; - &quot;作為值。 欄可以按 A->Z、Z->A 排序。 |
| [!UICONTROL 使用者人數] | 與產品設定檔相關聯的使用者獨特計數，包括直接指派和群組指派。 列可以從最小到最大或從最大到最小。 |
| [!UICONTROL 開發人員人數] | 與產品設定檔相關聯的開發人員角色計數。 列可以從最小到最大或從最大到最小。 |

## 自定義策略清單視圖

您可以搜尋、排序或篩選欄以自訂原則清單。

* 依名稱搜尋產品設定檔。 搜尋會比對您輸入的文字字串。
* 依遞增或遞減值排序欄。這適用於產品配置檔案、產 [!UICONTROL 品、] 實 [!UICONTROL 例] 、用 [!UICONTROL 戶數、開發] 人員數、列數。
* Click the **[!UICONTROL Filter By]** icon to apply multiple filters to list product profiles with specific criteria. 套用多個篩選類別時，搜尋會包含與例項解決方案相 `AND` 關的 `AND` 群組。

| 元素 | 說明 |
|---------|----------|
| [!UICONTROL 例項篩選] (Instance Filter) | 在例項欄中搜尋字元字串，將結果縮小為一或多個例項。 在每個搜尋詞後按 Enter 鍵即可新增多個篩選器. |
| [!UICONTROL 解決方案]篩選器 | 從可用的解決方案中選擇。多個解決方案篩選器搜尋包含「解決方案1」`OR`「解決方案 2」的結果。 |

## 檢視原則詳細資訊

在「策 [!UICONTROL 略] 」頁上，要查看策略的詳細資訊，請按一下產品配置檔案名稱。

![](assets/admin-tool-policy-detail.png)

每個產品設定檔的詳細檢視會顯示產品設定檔主題（使用者、群組等）的重要詳細資訊。 它也會顯示產品設定檔所啟用的權限和資源。

產品描述檔的詳細資訊可匯出至CSV檔案。 「匯 [!UICONTROL 出CSV] 」選項會產生兩個CSV檔案：

* 主旨詳細資訊（使用者、使用者群組、開發人員、整合、管理員）
* 權限和資源項目

## 摘要部分

本節顯示產品設定檔的摘要，包括：

* 產品設定檔名稱
* 使用者人數
* 開發人員人數
* 整合次數
* 相關產品
* 例項

## 詳細的主題清單

本節顯示指派給產品設定檔的所有使用者、使用者群組、開發人員、整合和管理員的完整清單。

| 定位 | 說明 |
|---------|----------|
| [!UICONTROL 使用者] | 產品設定檔中包含的使用者清單。 使用者群組關聯會顯示在「依群 [!UICONTROL 組指派」欄] 中。 |
| [!UICONTROL 使用者群組] | 與產品設定檔相關聯的使用者群組清單。 |
| [!UICONTROL 開發人員] | 與產品設定檔相關的開發人員清單。 |
| [!UICONTROL 整合] | 與產品設定檔相關聯的整合清單。 |
| [!UICONTROL 管理員] | 與產品設定檔關聯的管理員清單。 |

## 詳細的權限和資源清單

本節顯示產品設定檔可用權限和資源的完整清單。 產品設定檔中包含的權限和資源已標示為「✔」。 權限和資源清單已分類為標籤和欄，以方便檢視。 標籤和欄會顯示套用至目前產品的區段清單。
