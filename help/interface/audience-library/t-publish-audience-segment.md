---
description: 發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。
keywords: 核心服務
seo-description: 發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。
seo-title: 發佈 Analytics 受眾區隔
solution: Experience Cloud
title: 發佈 Analytics 受眾區隔
uuid: 4201dc22-4b79-457c-a614-949bba087617
translation-type: ht
source-git-commit: 85879d92104d8b6d739fb4d17dc8cfb7483a9343

---


# 發佈 Analytics 受眾區隔

發佈 Analytics 受眾區隔到 Experience Cloud 和 Adobe Target，以利進行受眾促銷活動。

1. 在 Analytics 中[建立區段](https://marketing.adobe.com/resources/help/zh_TW/analytics/segment/seg_build.html)。
1. 在區段產生器中，啟用 **[!UICONTROL 將此變為 Experience Cloud 受眾]** 選項。

   ![](assets/ec_audience_example.png)

   | 元素 | 說明 |
   |--- |---|
   | 將此變為 Experience Cloud 受眾 (用來 &lt;報告套件名稱&gt;) | 將此區段發佈至 Experience Cloud。受眾可供 Adobe Target 中的行銷活動以及 Audience Manager 中的區隔使用。<br>需要填寫標題和說明欄位才能發佈區隔。<br>啟用此選項後，會共用標題和受眾區隔定義，但不共用實際資料。將受眾與 Target 中的活動建立關聯後，Analytics 會開始傳送 ID 給符合 Experience Cloud 和 Target 受眾資格的訪客。此時，在 Experience Cloud「受眾」頁面上會開始顯示受眾名稱和相應資料。<br>透過 Analytics 與 Experience Cloud 共用的受眾不能超過 2,000 萬個受眾成員。<br>由於快取關係，Experience Cloud 會在 12 小時後才顯示 Analytics 中刪除的報表套裝資訊。<br>您可以在 Analytics 中編輯或刪除發佈的區隔。如果該區隔正在使用中，系統會在您編輯該區隔時發出警告訊息。您無法刪除 Adobe Target 正在使用的已發佈區隔。<br>訪客符合從 Analytics 共用的受眾資格後，此項資訊會延遲 24 至 48 小時，然後才能在 Target、Advertising Cloud 和 Campaign 中操作。<br>**資料隱私權**<br>不會根據訪客的驗證狀態篩選受眾。如果訪客可在未驗證和已驗證狀態下瀏覽您的網站，當訪客未驗證時發生的動作仍會使系統將訪客納入受眾。檢閱 [Analytics 隱私權概述](https://marketing.adobe.com/resources/help/zh_TW/reference/?f=c_Privacy_Overview)，全面瞭解受眾共用對隱私權的可能影響。 |
   | 選取受眾建立視窗 | 請注意，這是 **滾動式** 時間視窗，並非固定式時間視窗。 |

1. 按一下 **[!UICONTROL 儲存]**。
1. 存取 [!DNL Adobe Target]，按一下[!UICONTROL 受眾]。
1. 在[!UICONTROL 受眾]頁面上，找出來源為 Experience Cloud 的受眾。

   這些受眾可在活動中使用。
