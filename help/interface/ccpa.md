---
title: '加州消費者隱私法的客戶屬性支援 '
description: 了解加州消費者隱私法的客戶屬性支援
feature: 客戶屬性
topic: 管理
role: Administrator
level: Experienced
exl-id: 320defc7-2cd5-4481-955d-77cf6fbfef6d
source-git-commit: 40fd81f8a293dc5bca3b41e8f6e708d1be4bae5d
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 66%

---

# 加州消費者隱私法的客戶屬性支援

本頁面說明[!UICONTROL 客戶屬性]對加州消費者隱私法 (CCPA) 的支援。

>[!IMPORTANT]
>
>本文件的內容並非法律建議，其宗旨並非取代專業的法律建議。如需 CCPA 的相關建議，請諮詢法律顧問。

CCPA 是加州的最新隱私權法，自 2020 年 1 月 1 日起生效。CCPA 賦予加州居民個人資訊方面的新權利，並針對在加州營運的特定實體加諸資料保護責任。CCPA讓消費者有權存取和刪除其個人資訊，並有權選擇退出符合「銷售」第三方個人資訊資格的特定活動。

身為企業，您可以決定要由Adobe Experience Cloud代表您處理和儲存的個人資料。

Adobe Experience Cloud身為您的服務提供者，可協助您的企業履行CCPA所規定的義務，這些義務適用於Experience Cloud產品和服務的使用。 此支援包括管理存取和刪除個人資訊的請求。

本檔案說明[!UICONTROL 客戶屬性]如何使用Adobe Experience Platform Privacy Service API和Privacy ServiceUI，支援您的資料主體存取CCPA資料和刪除權限。

如需 CCPA 適用 Adobe 隱私權服務的詳細資訊，請參閱 [Adobe 隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## 傳送[!UICONTROL 客戶屬性]請求的必要設定

若要請求存取和刪除[!UICONTROL 客戶屬性]的資料，您必須：

1. 識別下列項目：

   * IMS 組織 ID
   * 您要對其採取動作之 CRS 資料來源的別名 ID
   * 您要對其採取動作之設定檔的 CRM ID

   IMS 組織 ID 是 24 個字元的英數字串，通常會加上 @AdobeOrg。如果您的行銷團隊或內部 Adobe 系統管理員不知道您組織的 IMS 組織 ID，請寄信至 gdprsupport@adobe.com 與 Adobe 客戶服務團隊連絡。您需要IMS組織ID才能將請求提交至隱私權API。

1. 在[!UICONTROL 隱私權服務]中，您可以將存取和刪除請求提交至客戶屬性，以及查看現有請求的狀態。

## [!UICONTROL 客戶屬性] JSON 請求中的必填欄位值

&quot;company context&quot;：

* &quot;namespace&quot;：**imsOrgID**
* &quot;value&quot;：&lt;*您的 IMS 組織 ID 值*>

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