---
title: 對通用資料保護法規的客戶屬性支援
description: 對通用資料保護法規的客戶屬性支援
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 0%

---


# 對通用資料保護法規的客戶屬性支援

本頁介紹客戶屬性如何支援通用資料保護規則(GDPR)。

>[!IMPORTANT]
>
>本檔案內容並非法律建議或用來取代法律建議。 請洽詢您的法律顧問，以取得有關GDPR的建議。

2018 [年5月](https://www.adobe.com/privacy/general-data-protection-regulation/what-is-gdpr.html)25日生效的《通用資料保護條例》賦予歐盟(EU)境內所有個人（資料主體）個人資料的控制權。 它還簡化了國際業務的監管環境。 本法適用於在處理個人資料時向歐盟境內的個人提供商品或服務、監控其行為或收集個人資料的所有企業（資料掌控者），不論資料掌控者的營業地點為何。

Adobe Experience Cloud是Adobe代表其客戶收到和儲存的任何個人資料的資料處理者。 身為資料掌控者，您可以代表您決定Adobe Experience Cloud處理和儲存的個人資料。

本檔案說明客 [!UICONTROL 戶屬性] (Customer Attributes)如何使用Adobe Experience Platform隱私服務API和隱私服務UI支援您資料主體的GDPR資料存取和刪除權。

如需有關GDPR對您企業的意義的詳細資訊，請參 [閱GDPR和您的企業](https://www.adobe.com/tw/privacy/general-data-protection-regulation.html)。

## 傳送客戶屬性請求的必 [!UICONTROL 要設定]

若要要求存取和刪除客戶屬 [!UICONTROL 性的資料]，您必須：

1. 識別下列項目：

   * IMS組織ID
   * 您要對之採取行動之CRS資料來源的別名ID
   * 您要處理之設定檔的CRM ID
   IMS組織ID是附加有@AdobeOrg的24個字元英數字串。 如果您的行銷團隊或內部Adobe系統管理員不知道您組織的IMS組織ID，請聯絡Adobe客戶服務，來信請寄至gdprsupport@adobe.com。 您將需要IMS組織ID，才能將請求提交至隱私權API。

1. 在隱 [!UICONTROL 私權服務]，您可以將存取和刪除請求提交至客戶屬性，並檢查現有請求的狀態。

## 客戶屬性 [!UICONTROL JSON請求中的必] 要欄位值

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

* 「規章」: **gdpr** （此為適用於要求的隱私權規定）

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
