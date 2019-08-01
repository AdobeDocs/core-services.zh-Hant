---
description: 發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。
keywords: 核心服務
seo-description: 發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。
seo-title: 發佈 Analytics 受眾區隔
solution: Experience Cloud
title: 發佈 Analytics 受眾區隔
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: tm+mt
source-git-commit: b74e0a08b43dfa8e5b35c5a650d159a58485883c

---


# 發佈 Analytics 受眾區隔

發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。

1. 在 Analytics 中[建立一個區段](https://marketing.adobe.com/resources/help/en_US/analytics/segment/seg_build.html)。
1. On the Segment Builder, enable the **[!UICONTROL Publish this segment to the Experience Cloud]** option.

   ![](assets/ec_audience_example.png)

   | 元素 | 說明 |
   |--- |---|
   | 將此區段發佈至Experience Cloud(對於&lt;報表套裝名稱&gt;) | 將此區段發佈至 Experience Cloud。您可以在Adobe Target、Audience Manager、Advertising Cloud、Campaign和Audience Analytics中的行銷和分段活動中使用觀眾。<br>需要填寫標題和說明欄位才能發佈區隔。<br>啟用此選項後，會共用標題和受眾區隔定義，但不共用實際資料。將受眾與 Target 中的活動建立關聯後，Analytics 會開始傳送 ID 給符合 Experience Cloud 和 Target 受眾資格的訪客。此時，在 Experience Cloud「受眾」頁面上會開始顯示受眾名稱和相應資料。<br>透過 Analytics 與 Experience Cloud 共用的受眾不能超過 2,000 萬個受眾成員。<br>由於快取關係，Experience Cloud 會在 12 小時後才顯示 Analytics 中刪除的報表套裝資訊。<br>若要刪除已發佈至Experience Cloud的區段，必須先解除發佈。To unpublish a segment, just **unclick** the checkbox that you used to publish it. You **cannot** unpublish a segment that is currently in use by any of the following Adobe solutions: [!DNL Analytics] (in [!DNL Audience Analytics]), [!DNL Campaign], [!DNL Advertising Cloud] (for [!DNL Core Service] &amp; [!DNL Audience Manager] customers) and all other external partners (for [!DNL Audience Manager] customers). You **can** unpublish a segment that is in use by [!DNL Target].<br>訪客符合從 Analytics 共用的受眾資格後，此項資訊會延遲 24 至 48 小時，然後才能在 Target、Advertising Cloud 和 Campaign 中操作。<br>**資料隱私權**<br>不會根據訪客的驗證狀態篩選受眾。如果訪客可在未驗證和已驗證狀態下瀏覽您的網站，當訪客未驗證時發生的動作仍會使系統將訪客納入受眾。請閱讀 [Analytics 隱私權概觀](https://marketing.adobe.com/resources/help/en_US/reference/?f=c_Privacy_Overview)以瞭解受眾共用的完整隱私權隱含意義。 |
   | 選取受眾建立視窗 | 請注意，這是&#x200B;**滾動式**&#x200B;時間視窗，並非固定式時間視窗。 |

1. 按一下&#x200B;**[!UICONTROL 儲存]**。
1. 存取 [!DNL Adobe Target]，按一下[!UICONTROL 受眾]。
1. 在[!UICONTROL 受眾]頁面上，找出來源為 Experience Cloud 的受眾。

   這些受眾可在活動中使用。
