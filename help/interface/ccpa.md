---
title: '加州消費者隱私法的客戶屬性支援 '
description: 了解加州消費者隱私法的客戶屬性支援
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 55c81003b94b7e033cddb6854b5c1f1c1ffa199c
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 90%

---

# 加州消費者隱私法的客戶屬性支援

本頁面說明[!UICONTROL 客戶屬性]對加州消費者隱私法 (CCPA) 的支援。

>[!IMPORTANT]
>
>本文件的內容並非法律建議，其宗旨並非取代專業的法律建議。如需 CCPA 的相關建議，請諮詢法律顧問。

CCPA 是加州的最新隱私權法，自 2020 年 1 月 1 日起生效。CCPA 賦予加州居民個人資訊方面的新權利，並針對在加州營運的特定實體加諸資料保護責任。CCPA 給予消費者存取及刪除其個人資訊的權利，且消費者有權選擇退出能將個人資訊「銷售」給協力廠商的相關活動。

企業能決定哪些個人資料要交由 Adobe Experience Cloud 代表您處理和儲存。

Adobe Experience Cloud 是您的服務提供者，只要是與使用 Experience Cloud 產品和服務相關的事務，Adobe Experience Cloud 均可支援您的企業履行 CCPA 所規定的相關義務。此支持包括管理存取和刪除個人資訊的請求。

本文件說明[!UICONTROL 客戶屬性]如何使用 Adobe Experience Platform Privacy Service API 和隱私權服務 UI，支援您的資料主體存取 CCPA 資料和刪除權限。

如需 CCPA 適用 Adobe 隱私權服務的詳細資訊，請參閱 [Adobe 隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## 傳送[!UICONTROL 客戶屬性]請求的必要設定

若要請求存取和刪除[!UICONTROL 客戶屬性]的資料，您必須：

1. 識別下列項目：

   * [組織 ID](#organizations.md)
   * 您要對其採取動作之 CRS 資料來源的別名 ID
   * 您要對其採取動作之個人資料的 CRM ID

   您 [組織ID](#organizations.md) 是附加有@AdobeOrg的24個字元的字母數字字串。 您需要組織的ID才能將請求提交到隱私API。 聯繫Adobe客戶關注： `gdprsupport@adobe.com` 找不到ID。

1. 在[!UICONTROL 隱私權服務]中，您可以將存取和刪除請求提交至客戶屬性，以及查看現有請求的狀態。

## [!UICONTROL 客戶屬性] JSON 請求中的必填欄位值

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;值&quot;:&lt;*組織ID值*>

&quot;users&quot;：

* &quot;key&quot;：&lt;*通常是客戶名稱*>

* &quot;action&quot;：**存取**&#x200B;或&#x200B;**刪除**

* &quot;user IDs&quot;：

   * &quot;namespace&quot;：&lt;*CRS 資料來源的別名 ID*>

   * &quot;type&quot;：**integrationCode**

   * &quot;value&quot;：&lt;*CRM ID*>

* &quot;include&quot;：**CRS** (適用於此請求的 Adobe 產品)

* &quot;regulation&quot;：**ccpa** (適用於此請求的隱私權法規)

## JSON 請求範例

```
{
  "companyContexts": [
    {
      "namespace": "imsOrgID",
      "value": "<IMS_ORG_ID>"
    }
  ],
  "users": [
    {
      "key": "<KEY>",
      "action": [
        "<access/delete>"
      ],
      "userIDs": [
        {
          "namespace": "<Alias ID of CRS Data Source>",
          "type": "integrationCode",
          "value": "<CRM ID>"
        }
      ]
    }
  ],
  "regulation": "<gdpr/ccpa/pdpa>",
  "include": [
    "CRS"
  ]
}
```

## 針對存取請求所傳回的資料欄位

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
