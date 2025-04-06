---
description: 了解 Experience Cloud 中央介面元件。在 Admin Console 中取得使用者和產品管理的說明；啟用 Experience Cloud 服務的應用程式。取得客群庫、客戶屬性、Experience Cloud 資產等說明。
title: Experience Cloud 介面文件
uuid: aec6f689-e617-4876-ae6c-e961cfcb991a
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: aedad5cb-3282-4a97-8e7e-6d65f7b75ba9
source-git-commit: 0740361094aac0e63207e5e60aa666a1613d0e94
workflow-type: tm+mt
source-wordcount: '911'
ht-degree: 82%

---

# Experience Cloud 中央介面概觀

[Experience Cloud](https://experience.adobe.com) 為 Adobe 的整合式數位行銷應用程式產品和服務系列。您可透過它的直觀式介面，快速存取您的雲端應用程式、產品功能和服務。

![Experience Cloud](assets/landing.png)

在 Experience Cloud 封面中，您可以：

* 存取您所有的 Experience Cloud 應用程式和服務
* 在「說明」選單中搜尋產品文件、教學課程和社群貼文。在 Experience League 中檢視結果。
* 在「搜尋」欄位使用全域搜尋功能，全域搜尋商業物件 (僅適用於 Experience Platform 使用者)。
* 管理您的帳戶[偏好設定](features/account-preferences.md) (警示、通知和訂閱)


從GSPM提取：

## 探索功能

<table style="table-layout:fixed">
<tr style="border: 0;">
   <td valign="top">
      <a href="../user-guide/effective-prompts.md">
      <img alt="右&gt;形箭號" src="../assets/icons/icon-chevronRight.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/effective-prompts.md">
         <strong>寫入有效提示</strong>
         </a>
      </div>
      <p>
         <em>製作描述性提示，以產生品牌內數位體驗。</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/create/overview.md">
      <img alt="繪圖筆刷" src="../assets/icons/icon-create.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/create/overview.md">
         <strong>建立體驗</strong>
         </a>
      </div>
      <p>
         <em>建立績效、品牌內電子郵件和中繼廣告。</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/approvals/overview.md">
      <img alt="核取記號" src="../assets/icons/icon-checkmarkCircle.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/approvals/overview.md">
         <strong>檢閱與核准</strong>
         </a>
      </div>
      <p>
         <em>協調行銷資產的簡化稽核與核准。</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/content/overview.md">
      <img alt="格線" src="../assets/icons/icon-images.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/content/overview.md">
         <strong>管理內容</strong>
         </a>
      </div>
      <p>
         <em>尋找、管理內容以及重新使用內容，同時維護品牌方針。</em>
      </p>
   </td>
   <td valign="top">
      <a href="../user-guide/insights/overview.md">
      <img alt="圖表" src="../assets/icons/icon-dataAnalytics.svg" width="35">
      </a>
      <div>
         <a href="../user-guide/insights/overview.md">
         <strong>檢視深入分析</strong>
         </a>
      </div>
      <p>
         <em>分析付費媒體管道的內容有效性。</em>
      </p>
   </td>
</tr>
</table>

## 瞭解如何

<table style="table-layout:fixed">
<td valign="top">
   <div>
      <a href="/help/user-guide/guidelines/add-guidelines.md">
      <img alt="新增准則" src="../assets/card-guidelines.png">
      <strong>新增准則</strong>
      </a>
   </div>
   <p>
      <em>瞭解如何新增准則（品牌、產品和角色）至GenStudio for Performance Marketing。</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-email-experience.md">
      <img alt="創意、書籍、鉛筆、電腦" src="../assets/card-create-assets.png">
      <strong>建立電子郵件體驗</strong>
      </a>
   </div>
   <p>
      <em>瞭解如何建立品牌內電子郵件體驗。</em>
   </p>
</td>
<td valign="top">
   <div>
      <a href="/help/user-guide/create/create-meta-ad.md">
      <img alt="將檔案移至資料夾的人員" src="../assets/card-manage-content.png">
      <strong>建立中繼廣告體驗</strong>
      </a>
   </div>
   <p>
      <em>瞭解如何建立品牌一致的中繼廣告體驗。</em>
   </p>
</td>
</table>


（GSPM結尾）







## 登入 Experience Cloud {#signin}

登入並確認您隸屬於正確的[組織](administration/organizations.md)。

1. 瀏覽至 [Adobe Experience Cloud](https://experience.adobe.com)。
1. 輸入您的 Adobe 電子郵件地址，然後按一下「**[!UICONTROL 繼續]**」。
1. 選取帳戶。
1. 輸入密碼。
1. 確認您隸屬於正確的組織。

   ![確認您隸屬於正確的組織](assets/organizations-menu.png)

   **確認您的組織**

   [組織](administration/organizations.md)顯示在介面封面中。

   如果貴組織使用 Federated ID，Experience Cloud 可讓您使用組織的單一登入進行登入，而不需要輸入您的電子郵件地址和密碼。將 `#/sso:@domain` 新增到 Experience Cloud URL (`https://experience.adobe.com`) 以完成此任務。

   例如，如果組織擁有 Federated ID 和網域 `adobecustomer.com`，請將您的 URL 連結設定為 `https://experience.adobe.com/#/sso:@adobecustomer.com`。您也可以將此 URL (有附加應用程式路徑) 加入書籤，即可直接前往特定的應用程式。(例如，Adobe Analytics 的 URL 為 `https://experience.adobe.com/#/sso:@adobecustomer.com/analytics`。)

## 存取 Experience Cloud 應用程式 {#navigation}

登入 Experience Cloud 之後，您可以從統一的封面快速存取您的所有應用程式、服務和組織。

若要存取貴組織內為您佈建的 Experience Cloud 應用程式和服務，請前往應用程式選擇器![選單](assets/menu-icon.png)。

![存取 Experience Cloud 應用程式](assets/platform-core-services.png)

## 取得說明和支援 {#support}

使用封面中的&#x200B;**[!UICONTROL 說明中心]** (![資產](assets/help-icon.png)) 來存取學習資源和說明，包括有關 [Experience League](https://experienceleague.adobe.com/#home) 的說明內容 (文件、教學課程和其他課程)，以及個別應用程式的其他資源。您還可以提交開放式意見回饋，並建立有優先權的支援服務單。

![取得說明和支援](assets/search-menu.png)

「[!UICONTROL 說明]」選單也可讓您存取：

* **[!UICONTROL 支援]：**&#x200B;建立支援服務單，或使用 Twitter 聯絡[!UICONTROL 支援人員]。
* **[!UICONTROL 意見回饋]：**&#x200B;分享您對 Experience Cloud 體驗的意見。您的意見回饋會用於改善 Adobe 產品和服務。
* **[!UICONTROL 狀態]：**&#x200B;瀏覽至 `https://status.adobe.com/experience_cloud`，以檢查產品操作狀態及[!UICONTROL 管理訂閱]。
* **[!UICONTROL Developer Connection]：**&#x200B;瀏覽至 `adobe.io` 以尋找開發人員文件。

## 管理您的使用者設定檔

在[!UICONTROL 設定檔]選單中，您可以：

* 指定深色主題 (並非所有應用程式都支援這個主題)
* 管理 Experience Cloud [偏好設定](features/account-preferences.md)
* 選取或搜尋「[組織](administration/organizations.md)」
* 檢視[!UICONTROL 法律注意事項]
* 登出
* 設定帳戶偏好設定、通知和訂閱

## 檢視產品內通知及公告 {#notifications}

按一下鈴鐺圖示，檢視通知和公告。公告可能會提供相關且可操作的更新資訊，包括產品發行版本、維護通知、共用項目及核准請求。

![通知和公告](assets/notifications-menu-small.png)

若要管理通知和警報，請參閱「[帳戶偏好設定和通知](features/account-preferences.md)」


## 新增功能

瞭解Experience Cloud中央介面元件的最新增強功能。

>[!BEGINTABS]

>[!TAB Slack與Experience Cloud整合]

您可以設定帳戶偏好設定，以將Experience Cloud通知傳送至[!DNL Slack]頻道。

[!BADGE Beta]{type=Informative url="https://experienceleague.adobe.com/en/docs/core-services/interface/features/account-preferences#notifications" tooltip="瞭解Slack"}


>[!TAB Campaign Web 新使用者介面]

體驗 Adobe Campaign 新用者介面。更現代、更直覺、更動態！

[![影像](assets/do-not-localize/learn-more-button.svg)](start/campaign-ui.md#ac-web-ui)


>[!TAB 推播頻道近期變更]

Android Firebase Cloud Messaging (FCM) 服務的一些重要變更將於 2024 年發行，並可能影響 Adobe Campaign 實施。Android 推播訊息訂閱服務設定可能需要更新，才能支援此變更。您已經可以檢查並採取動作。

[![影像](assets/do-not-localize/learn-more-button.svg)](../technotes/upgrades/push-technote.md)



>[!ENDTABS]

## 從基礎知識開始

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
    <a href="start/whats-new.md"><img src="assets/do-not-localize/start-capabilities.png"></a>
    <div><strong>主要功能</strong><br/>探索 Adobe Campaign v8 的跨頻道行銷活動管理主要功能。</div>
    </td>
    <td>
    <a href="start/connect.md"><img src="assets/do-not-localize/start-connect.jpeg"></a>
    <div><strong>連線至 Campaign v8</strong><br/>了解如何連線至 Adobe Campaign v8，並透過安裝及設定用戶端主控台來展開您的行銷活動管理歷程。</div><br/>
    </td>
    <td>
    <a href="start/create-message.md"><img src="assets/do-not-localize/start-send.jpeg"></a>
    <div><strong>傳送訊息</strong><br/>了解如何跨各種頻道傳送訊息，例如電子郵件、簡訊、推播通知等。
    </div></td>
    <td>
    <a href="audiences/create-profiles.md"><img src="assets/do-not-localize/start-profiles.png"></a>
    <div><strong>匯入輪廓</strong><br/>輕鬆探索如何在 Adobe Campaign v8 資料庫建立輪廓。手動或透過匯入新增輪廓，輕鬆精簡客戶資料和自訂行銷活動。</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="start/whats-new.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/connect.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="start/create-message.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="audiences/create-profiles.md"><img src="assets/do-not-localize/learn-more-button.svg"></a></td>
    </tr>
</table>

## 探索文件

<table style="table-layout:auto">
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon-start.svg" width="35px">
    <br/>
      <strong>開始使用</strong><br/><a href="start/campaign-ui.md">使用者介面</a> - <a href="start/ac-components.md">元件與流程</a> - <a href="start/v7-to-v8.md">從 Classic v7 到 v8</a> - <a href="start/campaign-faq.md">常見問題集</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-experience.svg" width="35px">
    <br/>
      <strong>客戶體驗</strong><br/><a href="../automation/workflow/about-workflows.md" target="_blank">使用工作流程自動化</a> - <a href="../automation/campaigns/set-up-campaigns.md" target="_blank">Campaign 協調流程</a> - <a href="interaction/interaction.md">決策管理</a> - <a href="send/personalize.md">個人化</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-send.svg" width="35px">
    <br/>
      <strong>傳送訊息</strong><br/><a href="start/create-message.md">開始使用</a> - <a href="send/preview-and-proof.md">預覽及校樣</a> - <a href="send/predictive.md">傳送時間最佳化</a> - <a href="reporting/gs-reporting.md">報告及分析</a>
    </td>
  </tr>
  <tr style="border: 0;">
    <td>
      <img src="assets/do-not-localize/icon_profile-audience.svg" width="35px">
    <br/>
      <strong>輪廓與客群</strong><br/><a href="audiences/create-profiles.md">新增輪廓</a> - <a href="audiences/create-audiences.md">建立客群</a> - <a href="start/subscriptions.md">管理訂閱</a> - <a href="start/privacy.md">隱私權</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-configure.svg" width="35px">
    <br/>
      <strong>架構與設定</strong><br/><a href="architecture/architecture.md">架構</a> - <a href="start/implement.md">Campaign v8 實施</a> - <a href="connect/integration.md">連結其他解決方案</a> - <a href="start/gs-permissions.md">使用者與權限</a>
    </td>
    <td>
      <img src="assets/do-not-localize/icon-dev.svg" width="35px">
    <br/>
      <strong>開發人員資源</strong><br/><a href="dev/datamodel.md">Campaign v8 資料模型</a> - <a href="dev/schemas.md">結構描述</a> - <a href="dev/api.md">API</a>
    </td>
  </tr>
</table>

## 其他資源

[Adobe Campaign v8 產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-campaign-managed-cloud-services.html){target="_blank"} - [Adobe Campaign Web 使用者介面檔案](https://experienceleague.adobe.com/docs/campaign-web/v8/campaign-web-home.html?lang=zh-Hant){target="_blank"} - [教學課程](https://experienceleague.adobe.com/docs/campaign-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"} - [[!DNL Adobe Campaign] 自動化指南](https://experienceleague.adobe.com/docs/campaign/automation/home.html?lang=zh-Hant){target="_blank"} - [Campaign v8 的控制面板](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/key-features.html?lang=zh-Hant){target="_blank"}

