---
description: 了解 Adobe Experience Cloud 中可用的應用程式整合。
solution: Experience Cloud
title: Experience Cloud 整合
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
source-git-commit: 361175f290d73f1637673420700874a2415e3fca
workflow-type: tm+mt
source-wordcount: '903'
ht-degree: 69%

---

# Experience Cloud 整合概觀

本頁說明開始整合Experience Cloud應用程式的幾種方法。 如需詳細資訊，請瀏覽Experience League上的[整合教學課程影片](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant)資料庫。

## 為 Platform 服務啟用您的 Experience Cloud 應用程式 {#section_A3D024994DA3492F8435CFCC4EF035C2}

作業方式說明：

* 在Experience Cloud中布建您的公司。
* 讓您成為管理員。
* [實作 Experience Cloud ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)。
* 透過[!UICONTROL Platform Data Collection]更新您的[!DNL Analytics]和[!DNL Target]實作。
* 開始使用Experience Cloud服務，例如[[!DNL customer attributes]](../services/customer-attributes/attributes.md)和[[!DNL Audience Library]](../services/audiences/overview.md)。

解決方案或服務：

* [[!DNL Experience Platform Data Collection]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=zh-Hant)
* [[!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics.html?lang=zh-Hant)
* [[!DNL Target]](https://experienceleague.adobe.com/docs/target.html?lang=zh-Hant)
* [Experience Cloud ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)

## Experience Cloud ID 服務 {#section_6ECCCFA2D84D4D4F88C879C799CA9D78}

ID服務提供永續性的通用ID，可識別Experience Cloud所有應用程式中的訪客。 這可取代 Analytics、Audience Manager、Adobe Target、視訊心率等服務及其他 Experience Cloud 應用程式和產品的 ID 產生碼。

請參閱 [Experience Cloud ID 服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)

**適用的應用程式或服務**

* [Adobe Analytics](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-analytics.html?lang=zh-Hant)
* [Adobe Target](https://experienceleague.adobe.com/docs/id-service/using/implementation/setup-target.html?lang=zh-Hant)

## 客群 {#section_5F60D7B0833348B9A1D74663AADCB42C}

說明：[客群](/help/interface/services/audiences/overview.md)

在Experience Cloud [!UICONTROL 對象庫]中建立和管理對象。 您可以建立客群，或從各種來源衍生出客群，例如：

* 在 [!DNL Experience Cloud] 中建立新的對象。
* 從 [!DNL Analytics] 區隔發佈至 [!DNL Experience Cloud]。
* 開始日期 [!DNL Audience Manager].

**適用的解決方案或服務**

* [Adobe Target 中的活動](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=zh-Hant)
* Audience Manager 中的[細分](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=zh-Hant)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （需要登入）

## 客戶屬性 {#section_6A9EA6847F654F129381869E5016626C}

說明： [客戶屬性](/help/interface/services/customer-attributes/attributes.md)

如果您在客戶關係管理(CRM)資料庫中擷取企業客戶資料，您可將該資料上傳至Experience Cloud的客戶屬性資料來源。 上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

**適用的解決方案或服務**

* Adobe Analytics：客戶屬性報表
* Adobe Target：設定 Adobe Target 的客戶屬性[訂閱](/help/interface/services/customer-attributes/subscription.md)

## Experience Cloud Assets {#section_92BC5DFDB0E0499CB0DD34B85E06F79A}

說明：[與 Creative Cloud 共用 Experience Cloud 資料夾](/help/interface/services/assets/creative-cloud.md)

在 Experience Cloud 和 Creative Cloud 之間共用資料夾和資產。共同作業、為共用資產加上註釋，以及在Experience Cloud應用程式(例如Adobe Target)中使用這些資產。

**適用的應用程式或服務**

* Adobe Experience Cloud
* Adobe Creative Cloud
* Adobe Target

## Analytics - 在 Analytics 中進行 AEM Assets 報告 {#section_0A16AE14F128470AA02EFC6457BDCE75}

說明：[在 Analytics 中製作 AEM Assets 報表](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html?lang=zh-Hant)

啟用 Analytics，收集 Assets 的曝光次數與點擊次數 (由 AEM Asset 見解分析提供的 Assets)。

**適用的應用程式或服務**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 整合 {#section_8FEFE1746E26416EB7E73095BBAD5345}

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html?lang=zh-Hant)

在 Audience Manager 中處理 Experience Cloud 應用程式或其他外部系統的資料。

**適用的應用程式或服務**

* [Analytics 伺服器端轉送功能](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=zh-Hant)
* [將 Audience Manager 區段傳送至 Analytics](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=zh-Hant)
* [Adobe Target 資料整合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-applications/aam-target-integration.html?lang=zh-Hant)

## Adobe Target {#section_739716AB6022424CBC38724CDED10701}

說明： [整合Adobe Target與Experience Cloud](/help/interface/services/audiences/overview.md)

將 Adobe Target 與 Adobe Analytics 及其他 Experience Cloud 應用程式整合後，即可在上述兩個應用程式中使用相同的資料、客群、屬性及量度。

**適用的應用程式或服務**

* 客戶屬性：將Adobe Target的[訂閱](/help/interface/services/customer-attributes/subscription.md)設定到客戶屬性
* Experience Cloud Audiences：[Experience Cloud 對象庫](/help/interface/services/audiences/overview.md)
* Analytics：[Adobe Analytics 作為 Adobe Target 的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hant)。
* Audience Manager：[Adobe Target 資料與 Adobe Audience Manager 整合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=zh-Hant)
* Campaign：[將 Adobe Target 與 Campaign 整合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=zh-Hant)

## Experience Manager 整合 {#section_32FB010EF8B4429FBC63C8DC2A9BE98F}

* 教學影片： [Experience Manager整合](https://experienceleague.adobe.com/docs/integrations-learn/experience-cloud/integrations-between-applications/overview.html?lang=zh-Hant)

* 產品檔案： [Experience Manager檔案](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=zh-Hant)

## Experience Manager - Assets {#section_CB865F8EFE4C4147BF8E2E4B66B5A318}

說明：[設定 AEM Assets 與 Experience Cloud 和 Creative Cloud 的整合](https://experienceleague.adobe.com/docs/?lang=zh-Hant)

將 Adobe Experience Manager (AEM) Assets 中的資產與 Adobe Creative Cloud 同步，反之亦然。您也可以將資產與 Experience Cloud 同步，反之亦然。您可以透過 Experience Cloud 設定此同步。

**適用的應用程式或服務**

* AEM
* Creative Cloud
* [Experience Cloud](https://experienceleague.adobe.com/docs/?lang=zh-Hant)

## [!DNL Adobe Advertising] {#section_9B1935F8BBC147C89C6DB68A35CB1BAB}

* 說明 (需登入)：[與 Adobe Experience Cloud 解決方案和服務整合](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

* Experience League上的[Adobe Advertising檔案](https://experienceleague.adobe.com/docs/advertising.html?lang=zh-Hant)

**適用的應用程式或服務**

**Analytics：**&#x200B;可以每天傳送網站互動和轉換資料至 [!DNL Adobe Advertising]，以供其改善廣告和建立報表。 此外，[!DNL Advertising] 亦可每天傳送搜尋引擎和社交網路流量資料至 Analytics，以供其 Reports &amp; Analytics、Report Builder 及 Ad Hoc Analysis 功能建立報表。

**標籤：**&#x200B;您可以使用[Experience Platform標籤，為您的搜尋、社交和顯示廣告登陸頁面建立Advertising畫素式轉換追蹤標籤](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant)和協力廠商追蹤標籤。 (您也可以直接在 [!DNL Advertising] 中建立 [!DNL Advertising] 標記。)

**Experience Cloud 客群：**(可管理顯示內容的廣告商) 您可以使用任何 [Adobe Experience Cloud 客群](../services/audiences/overview.md)作為顯示廣告的目標。 您可以自動使用已在Experience Cloud中建立的受眾和已發佈至Experience Cloud的Analytics受眾。 當[!DNL Adobe Advertising]帳戶設定為允許時，您也可從Audience Manager使用對象。

如需深入了解如何存取 Adobe Experience Cloud 和輪廓與客群，以及 [!DNL Adobe Advertising] 與 Adobe Experience Cloud 客群之間的初始設定，請聯絡您的客戶經理。 **注意：**&#x200B;如果您也有使用 Adobe Target，您發佈至 Adobe Experience Cloud 的客群也可以用於 Adobe Target 中的活動。

**Experience Cloud 資產:** (可管理顯示內容的廣告商) 您可以透過 New Display 測試版檢視，使用任何 Adobe Experience Cloud 資產作為顯示廣告的廣告創意。您必須透過Adobe Experience Cloud[&#128279;](https://enterprise.efrontier.com/CMDashboard) 登入Adobe Advertising，才能存取Adobe Experience Cloud資產。 如需存取 Adobe Experience Cloud 的相關資訊，請聯絡您的客戶經理。

**Experience Cloud 通知：**&#x200B;在每個頁面上方的通知連結中，您可以查看搜尋測試版提示範本產生的所有提示。您還可以取得 Experience Cloud 系統更新、貼文、相關記錄和共用的資產。您必須[透過Adobe Experience Cloud登入Adobe Advertising](https://enterprise.efrontier.com/CMDashboard)，才能存取通知。 如需存取 Adobe Experience Cloud 的相關資訊，請聯絡您的客戶經理。
