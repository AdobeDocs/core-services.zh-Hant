---
title: "[!DNL Audience Library]"
description: 瞭解如何在Experience Cloud中管理將訪客資料轉譯為受眾細分 [!DNL Audience Library].
solution: Experience Cloud
type: Documentation
uuid: 92faf3a8-1375-4e32-905b-74cad48144d3
feature: Audience Library
topic: Administration
role: Admin
level: Experienced
exl-id: 1c6e54ac-4886-46ed-9df7-201d2df31847
source-git-commit: 064f3c981b921fd5aec9b252b839d8b7f59b3dee
workflow-type: tm+mt
source-wordcount: '732'
ht-degree: 61%

---

# Experience Cloud 對象 {#topic_679810123CAA4E0CA4FA3417FB0100C7}

此 [!DNL Audience Library] 會以Experience Cloud顯示對象。 對象是訪客的集合（一個清單） [!DNL Experience Cloud] IDs)。 您可以管理將訪客資料轉譯為受眾細分。 因此，建立和管理觀眾與建立和使用細分類似。您也可以將對象細分分享至 [!DNL Experience Cloud] 的產品和服務。

![Experience Cloud 對象](assets/audiences.png)

您可以建立對象，或從各種來源衍生出對象，例如：

* 在 [!DNL Experience Cloud] 中建立新的對象
* 發佈至 [!DNL Experience Cloud] 的 [!DNL Analytics] 細分
* [!DNL Audience Manager]

**即時對象與歷史對象**

即時鎖定使用案例可以存取所有對象，無論對象來源為何。不過，即時鎖定目標功能無法存取從 Analytics 共用到 Audience Manager 的對象。系統會以兩種方式評估對象：

* 每四小時評估一次 Analytics 的歷史對象；處理和共用花費總共需要最多八小時。歷史對象一律包含回訪訪客。
* 即時受眾源自於Experience Cloud受眾，且為即時評估。

## 應用程式如何使用對象 {#concept_01EB9345C5344597BC94A864EDD38EE1}

下表說明如何在 Experience Cloud 應用程式中使用對象：

| 解決方案 | 說明 |
|--- |--- |
| Experience Cloud 對象 | 使用以原生方式建立、管理和共用對象 [[!DNL Audience Library]](audience-library.md). 您可以：<ul><li>運用原始分析屬性來使用即時對象</li><li>結合對象以建立複合對象，加入即時和歷史資料</li><li>查看預估對象規模的圖形檢視</li></ul><br>如需您要建立何種對象型別的建議，請參閱 [對象建立選項](https://experienceleague.adobe.com/docs/experience-cloud-kcs/kbarticles/KA-16471.html?lang=zh-Hant). |
| Analytics | 在細分中，您可以建立區段、將其與報表套裝結合，然後將區段發佈至Experience Cloud。 區段發佈後，會顯示於 [!DNL Audience Library] 頁面的Experience Cloud。 (請參閱 [將區段發佈至Experience Cloud](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-publish.html?lang=zh-Hant) 在 [!DNL Analytics] 詳細資料說明。) 受眾也可作為所傳遞行銷活動體驗的目標受眾 [!DNL Adobe Target]、和 [!DNL Audience Manager]. 在您分享對象之後，從 [!DNL Adobe Analytics]，並選取它以用於作用中的行銷活動，符合過去90天達到區段定義條件的訪客設定檔會傳送至 [!UICONTROL 受眾服務]. 共用對象的限制數已提高至 75 個。分享給Experience Cloud的對象，從 [!DNL Analytics] 不可以超過2,000萬個不重複成員。 此外，由於快取關係，Experience Cloud會在12小時後才顯示Analytics中刪除的報表套裝資訊。 |
| Mobile Services | 使用[!UICONTROL 裝置類型]報表中的放射環狀圖視覺效果分析行動流量。 |
| [!DNL Target] | [ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)會將訪客 ID 與資料統整於單一可操作的設定檔中，以便用於各種應用程式。 此 [發佈至Experience Cloud](audience-library.md) Adobe Analytics區段建立程式中勾選的核取方塊，可讓該區段在Adobe Target的自訂對象庫中提供。 在中建立的區段 [!DNL Analytics] 或 [!DNL Audience Manager] 可用於中的活動 [!DNL Target]. 例如，您可以根據 [!DNL Analytics] 中建立的 [!DNL Analytics] 轉換量度和對象區段來建立行銷活動。 |
| [!DNL Audience Manager] | 共用對象位於 [!DNL Audience Manager] 細分。 所有Experience Cloud對象原本都可在中取得 [!DNL Audience Manager]，可提供：<ul><li>內建有關如何在應用程式工作流程中共用和使用對象的自動化功能</li><li>離站目的地</li><li>相似建模</li></ul> |
| Campaign | <ul><li>從不同的 Adobe Experience Cloud 應用程式將共用對象匯入到 Adobe Campaign。</li><li>以共用對象的形式匯出收件者清單。 這些共用對象可用於您所使用的不同 Adobe Experience Cloud 應用程式。</li></ul> |
| Advertising Cloud | 使用對象作為目標。 |

{style="table-layout:auto"}

>[!IMPORTANT]
>
>訪客符合 Analytics 的共用對象資格後，此資訊會延遲 4 至 8 小時才能在 [!DNL Target]、Ad Cloud 和 Campaign Standard 中操作。

## 更多說明 - 問題、指南和使用個案 {#section_C7F151644D8A45F7B6FC54F58845635D}

| 相關協助 | 資源 |
|--- |--- |
| 找不到對象？ | 請確定您已佈建。請參閱[快速入門 - 為核心服務啟用您的應用程式](core-services.md)。<br>前往[這裡](https://adobe.allegiancetech.com/cgi-bin/qwebcorporate.dll?idx=X8SVES)來請求對設定檔與對象 (整合佈建表單) 的存取權。 |
| 論壇 | [Audiences 論壇](https://experienceleaguecommunities.adobe.com/t5/Adobe-Experience-Cloud-Audiences/ct-p/experience-cloud-audiences-community)是可取得對象說明的額外資源。 |

{style="table-layout:auto"}

## 對象庫介面元素 {#section_D04ACEF61CEF4B189AE6BA9F40D0DBF4}

[!DNL Experience Cloud] 提供一個資料庫，能讓您利用原始的即時對象識別來建立和管理對象。

**[!UICONTROL Experience Cloud]** > **[!UICONTROL Experience Platform]** > **[!UICONTROL People]** > **[!UICONTROL 對象庫]**

![在對象庫中新增對象](assets/audience_library.png)

| 元素 | 說明 |
|--- |--- |
| 新增 | [建立對象](audience-library.md)。 |
| 標題與說明 | 用來識別和說明對象的欄標題。 |
| 作者 | 建立對象區段的人。 |
| 來源 | 識別建立對象的位置。<ul><li>**Analytics：** 在Adobe Analytics中建立的區段，然後 [已發佈至Experience Cloud](audience-library.md).</li><li>**Experience Cloud：**[在 Experience Cloud Audiences 中建立](audience-library.md)的新對象。</li><li>**Audience Manager：** 在Audience Manager建立的對象會自動顯示在Experience Cloud對象中。</li></ul> |
| 目前規模 | 目前的對象規模。 |
| 作用中 | 區段的作用中狀態。 |

{style="table-layout:auto"}
