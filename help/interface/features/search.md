---
description: 了解 Experience Cloud 中某些應用程式的整合式搜尋功能。
solution: Experience Cloud
title: Experience Cloud 整合式搜尋
index: yes
feature: Central Interface Components
topic: Administration
role: Admin
level: Beginner
exl-id: 70586f18-6f84-4308-bab3-1da7fab823d6
TQID: https://experienceleague.adobe.com/xE4H6kdjbKSwVygCsOV4zTBqPoBHAVMHfJMyYOummg0
product_v2: id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2: id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2: id: b75843fa-0a67-4a44-a6b1-cc627b0481dcid: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0d253888322194189fea6d492ae19cf248357960
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 80%

---

# Experience Cloud 中的 [!UICONTROL Unified Search]

[!UICONTROL Unified Search]搜尋可讓您透過順暢一致的一鍵式體驗，尋找可搜尋的商業物件或實體。 此搜尋也會顯示您最近存取的物件。

![全域搜尋物件和實體](../assets/platform-search.png)

## 存取 [!UICONTROL Unified Search]

[!UICONTROL Unified Search]可在每個頁面頁面最上方的Experience Cloud標題中使用。 您也可以使用鍵盤快速鍵 `command /` 或 `ctrl /` 來存取該搜尋。

此功能只提供給受支援的產品，目前包括：

* Experience Platform (AEP)
* Journey Optimizer (AJO)

當有更多內容編製索引時，這項功能會新增到相關應用程式。

## 可搜尋的物件和欄位

當您輸入時，最符合的結果來自您有權顯示的物件。

我們的演算法會先顯示最相關的記錄。 結果的順序取決於幾個因素，例如：

您的功能和物件權限、相符的百分比、是否有完全相符的項目

Experience Cloud![[!UICONTROL Unified Search]中的](../assets/unified-search-results.png)

可搜尋的商業物件包括：

* 區段（名稱、說明、ID）
* 結構（名稱、說明、ID）
* 資料集（名稱、說明、ID）
* 來源（名稱、說明、ID）
* 目的地（名稱、說明、ID）
* 查詢（名稱、說明、ID）
* 訊息（名稱、說明、ID）
* 選件（名稱、說明、ID）
* 元件（名稱、說明、ID）
* 歷程（名稱、說明、ID）

如果關鍵字符合導覽頁面，您可以取得導覽頁面範例資料集的快速存取連結。排名最前結果區段會顯示排名前 30 筆結果。

您也可以從 Experience League 和 Communities 尋找說明文件。 支援自然語言查詢。

例如，_如何建立結構描述_&#x200B;會從&#x200B;_[!UICONTROL Learning]_下的Experience League產生結果：

Experience Cloud說明中的![[!UICONTROL Unified Search]](../assets/unified-search-learning.png)

搜尋演算法會最先顯示最相關的記錄。 結果的順序取決於幾個因素，例如：

* 存取物件的使用者權限
* 相符的百分比
* 完全符合的項目
* _[!UICONTROL Top Results]_區段會顯示前30個結果。

若要調整搜尋，請按一下下列其中一項：

* **[!UICONTROL All Learning]**：在Experience League中開啟搜尋。
* **[!UICONTROL Show all...]**：讓您進一步調整及篩選結果。

## [!UICONTROL Unified Search]功能

整合式搜尋中可提供以下功能。

| 功能 | 說明 |
| ------- | ------- |
| 全球語言支援 | 全球搜尋可了解德文、西班牙文、法文、義大利文、日文、韓文、葡萄牙文和中文的查詢與產生結果。 |
| 拼寫錯誤容許度 | 整合式搜尋可使用進階演算法提供強大的拼寫錯誤容許度。這些演算法會運算編輯並提供適當的結果。 |
| 重點提示 | 搜尋回應會重點提示搜尋查詢的相符關鍵字，以便您可以輕鬆找到與查詢相符的區段和字詞。重點提示也會顯示拼錯的字詞。 |
| 程式碼片段 | 在搜尋回應中，您可查看結果的程式碼片段。程式碼片段會傳回相符的字詞以及相符關鍵字周圍的部分內容。 |
| 停用詞 | 部分英文中的常用字詞會定義為&#x200B;_停用詞_。如果搜尋查詢中包含停用詞，給予該查詢結果的權重會較低。<br>停用詞包括：_一、一個、和、是、成為、在、但、前、為、如果、至、它、否、不、的、或、之類、那、該、他們的 (她們的、它們的)、接著、那裡、這些、他們 (她們、它們)、這、到、將、有_。<br>其他全球性語言中並不支援停用詞。 |
| 自然語言查詢 | 當您從 Experience League 社群搜尋說明文章或討論時，您可以使用自然語言輸入您的問題並獲得回答。範例搜尋：「如何建立結構描述？」 |
| 利用引號進行精確搜尋 | 您可以在查詢中使用引號來進行精確搜尋。精確搜尋查詢中不會完成拼寫錯誤校正。例如：「Luma Journey 2022」。 |
| 篩選器 | 您可以套用篩選器，例如&#x200B;_物件類型_&#x200B;和其他完全搜尋結果快顯視窗中的物件特定篩選器。當您在綁定搜尋查詢後按下 Enter 鍵時，一個包含篩選器的整頁快顯視窗會隨即開啟。 |

{style="table-layout:auto"}

## 找不到嗎？

嘗試以下提示：

* 輸入更具體的搜尋字詞
* 檢查拼寫
* 設法寫出完整的搜尋字詞
* 確保您對於要搜尋的物件擁有權限

