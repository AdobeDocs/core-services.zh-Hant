---
description: 瞭解如何使用Adobe Campaign standard中的選件和共用欄位。
seo-description: 瞭解如何使用Adobe Campaign standard中的選件和共用欄位。
seo-title: 促銷活動
title: 促銷活動
uuid: ceeec50c-6441-4ced-915b-c73f349f7a21
index: y
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: 2f0c2eb70313c42da9e7ac1d75429ec768dea10d

---


# 促銷活動{#campaign}

瞭解如何使用Adobe Campaign standard中的選件和共用欄位。

在您建立至少一個後援選件和一個一般選件後，您就可以在Campaign Standard中使用電子郵件建立選件活動。 選件活動只能在一般的電子郵件促銷活動中建立。 無法將它新增至交易式電子郵件促銷活動（例如，事件觸發的循環電子郵件，例如購物車放棄電子郵件）。

選件活動會提示您選取一組選件和備援選件，這些選件可能會顯示在電子郵件範本的位置。 根據位置、日期、優惠狀態和客戶個人檔案資料，在準備電子郵件時從這些優惠中選取最佳優惠。

## 將促銷活動屬性共用至選 [!UICONTROL 件管理]{#task_4DFA9A20D7B04E1F9AFF4774D67B6EBC}

在「選件管理」中建立選 [!UICONTROL 件時]，您可以設定資格規則，限制哪些個人檔案可接收特定選件。 這些資格規則可根據「促銷活動」設定檔中存在的屬性（或欄位）來設定。 這些欄位必須先從Campaign共用，才能顯示在「選件管理」 [!UICONTROL 資格規則] 產生器中。

>[!NOTE]
>
>若要共用屬性，您必須在Campaign中擁有管理員權限。

1. 按一 **[!UICONTROL 下Adobe Campaign]**以存取導覽。
1. 導覽至「管 **[!UICONTROL 理]**>例項設**[!UICONTROL &#x200B;定]** >選件管 **[!UICONTROL 理」，然後]******按一下「屬性」。

   此頁顯示已共用的屬性。 您可以編輯或刪除這些屬性。

   ![](assets/campaign-share5.png)

   >[!NOTE]
   >
   >如果資格規則中的選件管理 [!UICONTROL 當前正在使用屬性] ，則無法刪除屬性。

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 按一下資料夾圖示以定義促銷活動資料來源，並選取您要共用的元素。

   ![](assets/campaign-share7.png)

1. 選擇目標資料標籤。

   這是屬性的名稱，會顯示在選件管理的資格規則產生器 [!UICONTROL 中]。

1. 按一下&#x200B;**[!UICONTROL 建立]**。

   建立和編輯選件時，屬 [!UICONTROL 性會顯示在「選件管理] 」資格規則產生器中。

   ![](assets/campaign-share2.png)

## Create an offer activity {#task_F63ADDA52BD949779DB491E4D56E664E}

將選件活動插入Campaign Standard中電子郵件範本內的任何影像或文字區塊。

1. 若要在影像位置中插入選件活動，請在影像上按一下，以顯示「插入選件」圖示。

   ![](assets/insert-offer-activity.png)

1. （替代）:若要將選件活動插入文字區塊，請按兩下文字區塊上的兩次，以顯示「插入選件」圖示。

1. 在「建立選件活動」畫面 [!UICONTROL 的「活動詳細資訊] 」標籤 [!UICONTROL 中填入詳細資訊] :

   | 欄位 | 說明 |
   |---|---|
   | 活動名稱 | 命名您的活動。您無法輸入已用於其他選件活動的活動名稱。 |
   | 位置 | 選擇將用於此位置的位置。 這是為了確保只有內容表示符合的選件才能提供給使用者位置。 在活動建立的其餘期間，只有具有此位置的選件會顯示在選件清單中。 |

1. 在「選 [!UICONTROL 擇選件] 」標籤中，選取您要包含在活動中的選件。

   您可以使用標籤或個別選件逐一選取選件群組。

   * **使用標籤選取選件群組：**

      若要使用標籤選取選件群組，請按一下「規則產 **[!UICONTROL 生器」標籤]**，然後按一**[!UICONTROL &#x200B;下「新增標籤規則」]**。 若要建立規則以決定要包含在選件活動中的選件，請選取標籤。 標籤 _之間將會出現AND_ 運算子。 若要將運算子從 _AND_ 變更 _為OR_，請按一下運算子。

      ![](assets/offer-actvity-rule-builder.png)

   * **選取個別選件：**

      若要選取個別選件，請按一下「選 **[!UICONTROL 件清單」標籤]**。 使用者可依選件名稱、選件ID或已新增至選件的標籤，在選件清單中進行搜尋。

      按一下加號，將選件新增至清單的「選取的選件」區段。

      ![](assets/create-offer2.png)

      若要在規則產生器和選件清單中同時提供選件，它必須：

   * 符合今天的日期。
   * 狀態為已批准。
   * 具有與步驟1中選定的位置匹配的內容表示。

      >[!NOTE]
      >
      >「選件清單」標籤中列出的選件僅會依位置和核准狀態篩選。 尚未篩選這些變數，以符合Adobe Campaign中電子郵件的定位條件集。

1. 在「備援選 [!UICONTROL 件」標籤] ，選取備援選件。 備援選件僅在客戶不符合其他選件的資格時，才會傳送給客戶。 您只能從清單中選取一個備援選件。
1. 檢視選件活動的摘要，然後按一下「完 **[!UICONTROL 成]**」。

   為每位使用者提供最佳服務的優惠方案，將在電子郵件準備時透過評估下列項目來決定：

* **** 位置檢查：所有選件都必須有符合選取為選件活動一部分之位置的內容表示法。 如果選件的位置在活動建立時間和準備時間之間（如果時間超過三分鐘）被刪除，則不會考慮該選件。
* **** 日期檢查：所有選件都必須在目前日期有效(這 _不是_ 選件傳送日期)。 準備電子郵件促銷活動的日期是決定要提供哪個選件的日期。 例如，如果您在1/15/17準備電子郵件促銷活動，而其中一個選取的選件在1/16/17之前無效，則不會提供選件。

* **** 資格規則檢查：所有優惠都必須符合資 [格規則](offers.md#task_6C4AE487377D424FA133ACCA6AF741D4)。

* **** 優先順序檢查：如果使用者符合多個選件的資格， [!UICONTROL 選件管理] (Offer Management)會使用使用者設定的優先順序來決定要向每個使用者顯示哪個選件。

   您的電子郵件現在已可供傳送。 選取首 [!UICONTROL 頁上的] 「報表」 [!DNL Adobe Campaign] 標籤，以檢查選件的執行方式。

   如需有關使用Adobe Campaign的詳細資訊，請參閱下列指南：

* [撰寫電子郵件](https://docs.campaign.adobe.com/doc/standard/en/CHA_Email_messages_Creating_an_email.html)
* [傳送電子郵件](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/about-sending-messages-with-campaign.html)
* [關於動態報表](https://docs.campaign.adobe.com/doc/standard/en/RPT_About_reporting_About_dynamic_reports.html)

## 選件報表

Adobe Campaign提供三個選件維度（選件、選件活動、選件位置）和一個量度（選件點按），可讓您監控選件並評估其影響。 若要檢視報表，請造訪Adobe Campaign Standard中的「報表」標籤。 您可以建立報表，並將不同的選件維度拖放至報表面板，以開始篩選資料。

![](assets/offers-reports.png)

如需如何在促銷活動中建立動態報表的詳細資訊，請參閱關於 [動態報表](https://docs.campaign.adobe.com/doc/standard/en/RPT_About_reporting_About_dynamic_reports.html)。