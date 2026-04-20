---
description: 尋找Adobe CX Enterprise中可用的應用程式整合。
solution: Experience Cloud
title: Experience Cloud 整合
uuid: a9893c6b-bccc-4fb5-b724-724644c7def5
feature: Admin Console
topic: Administration
role: Admin
level: Experienced
exl-id: 7f8fa610-32f0-4b18-8054-3ba05436a10e
TQID: https://experienceleague.adobe.com/6Sh6sOZ--ct2sz5sMR-qRwZmvoC51zQkV9LqVRXmi-o
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: dab36b01-8bfa-48f3-8392-626455a058e6
  - id: fc7979f3-56c3-43ca-9784-f1ea3dc69c4b
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: d27b1945-f442-4607-91bd-537a0b16e687
  - id: ecb4a972-6786-444c-a014-abc528b9407a
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 1111
ht-degree: 30%

---

# CX Enterprise整合

本頁說明開始整合CX Enterprise應用程式的幾種方法。 如需詳細資訊，請瀏覽Experience League上的[整合教學課程影片](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant)資料庫。

## 為平台服務啟用您的CX Enterprise應用程式

作業方式說明：

* 在CX Enterprise中布建您的公司。
* 讓您成為管理員。
* [實作CX Enterprise ID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)。
* 透過[!UICONTROL Platform Data Collection]更新您的[!DNL Analytics]和[!DNL Target]實作。
* 開始使用CX Enterprise服務，例如[客戶屬性](../services/customer-attributes/attributes.md)和[對象庫](../services/audiences/overview.md)。

解決方案或服務：

* [[!DNL Experience Platform Data Collection]](https://experienceleague.adobe.com/docs/experience-platform.html?lang=zh-Hant)
* [[!DNL Analytics]](https://experienceleague.adobe.com/docs/analytics.html?lang=zh-Hant)
* [[!DNL Target]](https://experienceleague.adobe.com/docs/target.html?lang=zh-Hant)
* [CX Enterprise ID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)

## CX Enterprise ID服務

ID服務提供永續性的通用ID，可識別CX Enterprise所有應用程式中的訪客。 這可取代Analytics、Audience Manager、Adobe Target、視訊心率等服務及其他CX Enterprise應用程式和產品的ID產生碼。

請參閱[CX Enterprise ID服務](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=zh-Hant)

**適用的應用程式或服務**

* [Adobe Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics/implementation/id/overview)
* [Adobe Target](https://experienceleague.adobe.com/zh-hant/docs/id-service/using/implementation/setup-target)

## 客群

說明：[客群](/help/interface/services/audiences/overview.md)

在CX Enterprise [!UICONTROL Audience Library]中建立和管理對象。 您可以建立客群，或從各種來源衍生出客群，例如：

* 在[!DNL CX Enterprise]中建立新的對象。
* 從[!DNL Analytics]個區段發佈至[!DNL CX Enterprise]。
* 開始日期 [!DNL Audience Manager].

**適用的解決方案或服務**

* [Adobe Target 中的活動](https://experienceleague.adobe.com/docs/target/using/activities/activities.html?lang=zh-Hant)
* Audience Manager 中的[細分](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/audience-analytics-workflow/aam-analytics-segments.html?lang=zh-Hant)
* [Advertising Cloud](https://enterprise.efrontier.com/CMDashboard/?ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D&ticket=JrciD7q2bF1y2mDWFHmEyibmxtHqnZFSOMml-n993zOBc-ovZGNZkX5vgePWqKNMoMmPSqf9PkzFeYF4UN6GqSXDVNDvwgnvv9KT8PvVxk8%3D) （需要登入）

## 客戶屬性

說明：[客戶屬性](/help/interface/services/customer-attributes/attributes.md)

如果您在客戶關係管理(CRM)資料庫中擷取企業客戶資料，您可將該資料上傳至CX Enterprise的客戶屬性資料來源。 上傳後，即可在 [!DNL Adobe Analytics] 和 [!DNL Adobe Target] 中運用這些資料。

**適用的解決方案或服務**

* Adobe Analytics：客戶屬性報表
* Adobe Target：設定Adobe Target的[訂閱](/help/interface/services/customer-attributes/subscription.md)以使用客戶屬性

## CX Enterprise Assets

說明： [與Creative Cloud共用CX Enterprise資料夾](/help/interface/services/assets/share.md)

在CX Enterprise和Creative Cloud之間共用資料夾和資產。 共同作業、為共用資產加上註釋，以及在CX Enterprise應用程式（例如Adobe Target）中使用這些資產。

**適用的應用程式或服務**

* Adobe CX Enterprise
* Adobe Creative Cloud
* Adobe Target

## Analytics - 在 Analytics 中進行 AEM Assets 報告

說明：[在 Analytics 中製作 AEM Assets 報表](https://experienceleague.adobe.com/docs/analytics/integration/aem-assets-reporting.html?lang=zh-Hant)

啟用 Analytics，收集 Assets 的曝光次數與點擊次數 (由 AEM Asset 見解分析提供)。

**適用的應用程式或服務**

* [!DNL Analytics]
* [!DNL Experience Manager]

## Audience Manager 整合

[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/implementation-and-integration.html?lang=zh-Hant)

在Audience Manager中處理CX Enterprise應用程式或其他外部系統的資料。

**適用的應用程式或服務**

* [Analytics伺服器端轉送功能](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=zh-Hant)
* [將Audience Manager區段傳送至Analytics](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html?lang=zh-Hant)
* [Adobe Target資料整合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-applications/aam-target-integration.html?lang=zh-Hant)

## Adobe Target

說明： [整合Adobe Target與CX Enterprise](/help/interface/services/audiences/overview.md)

將Adobe Target與Adobe Analytics及其他CX Enterprise應用程式整合後，即可在上述兩個應用程式中使用相同的資料、對象、屬性及量度。

**適用的應用程式或服務**

* 客戶屬性：設定 Adobe Target 的客戶屬性[訂閱](/help/interface/services/customer-attributes/subscription.md)
* CX Enterprise對象： [CX Enterprise對象庫](/help/interface/services/audiences/overview.md)
* Analytics：[Adobe Analytics 作為 Adobe Target 的報表來源](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html?lang=zh-Hant)。
* Audience Manager：[Adobe Target 資料與 Adobe Audience Manager 整合](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/integration-other-solutions/aam-target-integration.html?lang=zh-Hant)
* Campaign：[將 Adobe Target 與 Campaign 整合](https://experienceleague.adobe.com/docs/target/using/integrate/campaign-and-target.html?lang=zh-Hant)

## Experience Manager 整合

* 教學影片： [Experience Manager整合](https://experienceleague.adobe.com/docs/integrations-learn/experience-cloud/integrations-between-applications/overview.html?lang=zh-Hant)

* 產品檔案： [Experience Manager檔案](https://experienceleague.adobe.com/docs/experience-manager-cloud-service.html?lang=zh-Hant)

## Experience Manager - Assets

說明： [設定AEM Assets與CX Enterprise和Creative Cloud的整合](https://experienceleague.adobe.com/docs/?lang=zh-Hant)

將 Adobe Experience Manager (AEM) Assets 中的資產與 Adobe Creative Cloud 同步，反之亦然。 您也可以將資產與CX Enterprise同步，反之亦然。 您可以透過CX Enterprise設定此同步。

**適用的應用程式或服務**

* AEM
* Creative Cloud
* [CX Enterprise](https://experienceleague.adobe.com/docs/?lang=zh-Hant)

## [!DNL Adobe Advertising]

* 說明（需要登入）： [與Adobe CX Enterprise解決方案和服務整合](https://enterprise.efrontier.com/CMDashboard?ticket=JrciD7q2bF1y2mDWFHmEyhyMKZp71ZLeaANvF-RcNMF7oNuZNABh76cKJLNlJJeJ1hQ5vAW1AO1t1DW8tZWM3lYZ8TSh96YAQISUdtHCCgA%3D&ticket=JrciD7q2bF1y2mDWFHmEyibbOnNwb2JBRF7z6tKAOIWkBimlPxCUaZyJnPLqsfdqsf3fpxWoxGasvatKA8S6-h4tlDvxQcm8Gc10dSF9q_E%3D)

* Experience League上的[Adobe Advertising檔案](https://experienceleague.adobe.com/docs/advertising.html?lang=zh-Hant)

**適用的應用程式或服務**

**Analytics：**&#x200B;可以每天傳送網站互動和轉換資料至 [!DNL Adobe Advertising]，以供其改善廣告和建立報表。 此外，[!DNL Advertising] 亦可每天傳送搜尋引擎和社交網路流量資料至 Analytics，以供其 Reports &amp; Analytics、Report Builder 及 Ad Hoc Analysis 功能建立報表。

**標籤：**&#x200B;您可以使用[Experience Platform標籤，為您的搜尋、社交和顯示廣告登陸頁面建立Advertising畫素式轉換追蹤標籤](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html?lang=zh-Hant)和協力廠商追蹤標籤。 (您也可以直接在 [!DNL Advertising] 中建立 [!DNL Advertising] 標記。)

**CX Enterprise對象：** （可管理顯示內容的廣告商）您可以使用任何[Adobe CX Enterprise對象](../services/audiences/overview.md)作為顯示廣告的目標。 您可以自動使用已在CX Enterprise中建立的受眾和已發佈至CX Enterprise的Analytics受眾。 當[!DNL Adobe Advertising]帳戶設定為允許時，您也可從Audience Manager使用對象。

如需深入瞭解如何存取Adobe CX Enterprise和設定檔與受眾，以及[!DNL Adobe Advertising]與Adobe CX Enterprise受眾之間的初始設定，請聯絡您的客戶經理。 **注意：**&#x200B;如果您也使用Adobe Target，您發佈至Adobe CX Enterprise的對象也可供Adobe Target中的活動使用。

**CX Enterprise Assets：** （可管理顯示內容的廣告商）您可以透過「全新顯示Beta」檢視，使用任何Adobe CX Enterprise資產作為顯示廣告的廣告創意。 您必須透過Adobe CX Enterprise[&#128279;](https://enterprise.efrontier.com/CMDashboard) 登入Adobe Advertising，才能存取Adobe CX Enterprise資產。 如需存取Adobe CX Enterprise的相關資訊，請聯絡您的客戶經理。

**CX Enterprise通知：**&#x200B;從每頁頂端的通知連結中，您可以檢視搜尋測試版提示範本產生的所有提示。 您也可以取得CX Enterprise系統更新、貼文、相關記錄和共用的資產。 您必須[透過Adobe CX Enterprise登入Adobe Advertising](https://enterprise.efrontier.com/CMDashboard)，才能存取通知。 如需存取Adobe CX Enterprise的相關資訊，請聯絡您的客戶經理。

