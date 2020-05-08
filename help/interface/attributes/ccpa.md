---
title: California Consumer Privacy Act的客戶屬性支援
description: California Consumer Privacy Act的客戶屬性支援
translation-type: tm+mt
source-git-commit: 2e8c8aee39546a345e72cda2dad08ad866cd90f9
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 4%

---


# California Consumer Privacy Act的客戶屬性支援


>[!IMPORTANT]
>
>本文件的內容不是法律建議，且用意並非要取代法律建議。請洽詢您的法律顧問，以取得有關加州消費者隱私權法案的建議。

加州消費者隱私法(CCPA)是加州新推出的隱私權法，自2020年1月1日起生效。 CCPA為加州居民提供個人資訊的新權利，並對在加州經營業務的特定實體負有資料保護責任。 CCPA讓消費者有權存取和刪除其個人資訊，並有權選擇退出某些符合「銷售」個人資訊資格的活動給第三方。

身為企業，您將代表您決定Adobe Experience Cloud處理和儲存的個人資料。

Adobe Experience Cloud是您的服務供應商，可協助您的企業履行CCPA規定的義務，此義務適用於使用Experience Cloud產品和服務，包括管理存取和刪除個人資訊的要求。

本檔案說明客戶屬性如何使用Adobe Experience Platform Privacy Service API和隱私服務UI支援您資料主體的CCPA資料存取和刪除權限。

如需CCPA專用Adobe隱私權服務的詳細資訊，請參閱 [Adobe隱私權中心](https://www.adobe.com/privacy/ccpa.html)。

## 傳送客戶屬性請求的必要設定

若要要求存取和刪除客戶屬性的資料，您必須：

1. 識別下列項目：

* IMS組織ID
* 您要對之採取行動之CRS資料來源的別名ID
* 您要處理之設定檔的CRM ID

IMS組織ID是附加有@AdobeOrg的24個字元英數字串。 如果您的行銷團隊或內部Adobe系統管理員不知道您組織的IMS組織ID，請聯絡Adobe客戶服務，來信請寄至gdprsupport@adobe.com。 您將需要IMS組織ID，才能將請求提交至隱私權API。

2. 使用隱私權服務UI將存取權和刪除請求提交至客戶屬性，並檢查現有請求的狀態。

## 客戶屬性JSON請求中的必填欄位值

「公司上下文」:

* &quot;namespace&quot;: **imsOrgID**
* 「值」: &lt;*您的IMS組織ID值*>

「使用者」:

* &quot;key&quot;: &lt;*通常是客戶名稱*>

* 「動作」: 存 **取** 或刪 **除**

* &quot;用戶ID&quot;:

   * &quot;namespace&quot;: &lt;*CRS資料來源的別名ID*>

   * 「類型」: **integrationCode**

   * 「值」: &lt;*CRM ID*>

* 「包含」: **CRS** （此為套用至要求的Adobe產品）

* 「規章」: **ccpa** （此為適用於要求的隱私權規定）

## JSON請求範例

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

## 針對存取請求傳回的資料欄位

```
attributes:
{
"value”:<*value*>,
"key”:<*key*>,
"displayName”:<*displayName*>
}
```
