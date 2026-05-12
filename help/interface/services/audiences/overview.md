---
title: '[!DNL Audience Library]'
description: 瞭解如何在CX Enterprise [!DNL Audience Library]中管理將訪客資料轉譯為對象細分。
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
TQID: https://experienceleague.adobe.com/QEAfCWPNI-JhDw-HjZwBGv0TlqyctIqSwz8eVQqS6Gg
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
  - id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 745
ht-degree: 44%

---

# CX Enterprise對象

[!DNL Audience Library]會在CX Enterprise中顯示對象。 客群是訪客的集合 ([!DNL CX Enterprise] ID 的清單)。 您可以管理訪客資料轉譯為客群細分的過程。 因此，建立和管理對象類似於建立和使用區隔。 您也可以將客群細分分享至 [!DNL CX Enterprise] 的產品和服務。

![CX Enterprise對象](assets/audiences.png)

您可以建立客群，或從各種來源衍生出客群，例如：

* 在[!DNL CX Enterprise]中建立新的受眾
* [!DNL Analytics]區段已發佈至[!DNL CX Enterprise]
* [!DNL Audience Manager]

**即時客群與歷史客群**

即時鎖定使用案例可以存取所有客群，無論客群來源為何。 不過，即時鎖定目標功能無法存取從 Analytics 共用到 Audience Manager 的對象。 系統會以兩種方式評估客群：

* 每四小時評估一次 Analytics 的歷史客群； 處理和共用花費總共需要最多八小時。 歷史客群一律包含回訪訪客。
* 即時受眾源自於CX企業受眾，且為即時評估。

## 應用程式如何使用客群

下表說明如何在CX Enterprise應用程式中使用對象：

| 解決方案 | 說明 |
| --- | --- |
| CX Enterprise對象 | 使用對象庫以原生方式建立、管理和共用對象。 您可以：<ul><li>透過原始分析屬性來使用即時受眾。</li><li>結合對象以建立複合對象，加入即時和歷史資料。</li><li>檢視預估對象規模的圖形檢視。</li></ul><br>如需您要建立何種客群類型的建議，請參閱 [客群建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=zh-Hant)。 |
| Analytics | 在細分中，您可以建立區段、將其與報表套裝結合，然後將區段發佈至CX Enterprise。 發佈區段會顯示在CX Enterprise的[!DNL Audience Library]頁面上。 （如需詳細資訊，請參閱[!DNL Analytics]說明中的[將區段發佈至CX Enterprise](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=zh-Hant)。） 對象也可作為[!DNL Adobe Target]提供之行銷活動體驗以及[!DNL Audience Manager]中的目標對象。 當您共用[!DNL Adobe Analytics]的對象並選擇在作用中的行銷活動中使用後，符合過去90天達到區段定義條件的訪客設定檔會傳送至[!UICONTROL Audience Services]。 共用客群的限制數已提高至 75 個。 透過[!DNL Analytics]與CX Enterprise共用的對象不能超過2,000萬個不重複的成員。 此外，由於快取關係，CX Enterprise會在12小時後才顯示Analytics中刪除的報表套裝資訊。 |
| Mobile Services | 使用[!UICONTROL Device Types]報表中的放射環狀圖視覺效果分析行動流量。 |
| [!DNL Target] | [ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)會將訪客 ID 與資料統整於單一可操作的輪廓中，以便用於各種應用程式。 Adobe Analytics區段建立程式中會顯示[!UICONTROL Publish to CX Enterprise]核取方塊，一旦勾選，該區段即可供Adobe Target的自訂對象庫使用。 在 [!DNL Analytics] 或 [!DNL Audience Manager] 中建立的區段皆適用於 [!DNL Target] 中的活動。 例如，您可以根據 [!DNL Analytics] 中建立的 [!DNL Analytics] 轉換量度和客群區段來建立行銷活動。 |
| [!DNL Audience Manager] | 在 [!DNL Audience Manager] 細分中可用共用客群。 所有CX Enterprise對象都可在[!DNL Audience Manager]中以原生方式使用，提供：<ul><li>內建有關如何在應用程式工作流程中共用和使用對象的自動化功能</li><li>離站目的地</li><li>相似建模</li></ul> |
| 促銷活動 | <ul><li>從不同的Adobe CX Enterprise應用程式匯入共用對象至Adobe Campaign。</li><li>以共用客群的形式匯出收件者清單。 這些共用對象可用於您所使用的不同Adobe CX Enterprise應用程式。</li></ul> |
| Advertising Cloud | 使用客群作為目標。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>訪客符合 Analytics 的共用客群資格後，此資訊會延遲 4 至 8 小時才能在 [!DNL Target]、Ad Cloud 和 Campaign Standard 中操作。

## 客群庫介面元素

[!DNL CX Enterprise]提供一個資料庫，能讓您利用原始的即時對象識別來建立和管理對象。

**[!UICONTROL CX Enterprise]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL Audience Library]**

![在客群庫中新增客群](assets/audience_library.png)


| 元素 | 說明 |
| --- | --- |
| 新增 | [建立客群](https://experienceleague.adobe.com/zh-hant/docs/core-services/interface/services/audiences/create)。 |
| 標題與說明 | 用來識別和說明客群的欄標題。 |
| 作者 | 建立客群區段的人。 |
| 來源 | 識別建立客群的位置。<ul><li>**Analytics：**&#x200B;在Adobe Analytics中建立區段，然後發佈至CX Enterprise。</li><li>**CX Enterprise：**&#x200B;在CX Enterprise Audiences[&#128279;](https://experienceleague.adobe.com/zh-hant/docs/core-services/interface/services/audiences/create)中建立的新對象。</li><li>**Audience Manager：** Audience Manager建立的對象會自動顯示在CX Enterprise Audiences中。</li></ul> |
| 目前規模 | 目前的客群規模。 |
| 作用中 | 區段的作用中狀態。 |

{style="table-layout:auto"}

## 從Adobe Analytics發佈對象

如需詳細資訊，請參閱Adobe Analytics檔案中的[將區段發佈至CX Enterprise](https://experienceleague.adobe.com/zh-hant/docs/analytics/components/segmentation/segmentation-workflow/seg-publish)。
