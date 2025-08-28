---
title: 一般資料保護規範的[!DNL Customer attributes]支援
description: 瞭解一般資料保護規範的客戶屬性支援
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 02417c0c-6780-4699-9470-f1685c3cd25d
source-git-commit: b296b7fe76ad686d45a5927c55f798dc0203c684
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 95%

---

# [!DNL Customer attributes] 支援一般資料保護規範

本頁面旨在說明 [!DNL Customer Attributes] 如何支援一般資料保護規範 (GDPR)。

>[!IMPORTANT]
>
>本文件的內容並非法律建議，且宗旨並非取代專業的法律建議。如需 GDPR 的相關建議，請諮詢法律顧問。

2018 年 5 月 25 日生效的[一般資料保護規範](https://business.adobe.com/privacy/general-data-protection-regulation.html)賦予歐盟 (EU) 境內所有個人 (資料主體) 掌控其個人資料的權利。此外，也簡化國際業務的監管環境。針對向歐盟境內之個人提供商品或服務、監控其行為或收集其個人資料的所有企業 (資料控管單位)，不論資料控管單位的營業地點為何，其資料處理行為均需接受本法規範。

Adobe Experience Cloud 代表客戶擔任資料處理者的角色，依指示接收和儲存的任何個人資料。身為資料控管方，您可以決定要由 Adobe Experience Cloud 代表您處理和儲存哪些個人資料。

本文件說明 [!DNL Customer Attributes] 如何使用 Adobe Experience Platform Privacy Service API 和隱私權服務 UI，支援您的資料主體存取 GDPR 資料和刪除權限。

如需深入了解 GDPR 對您業務所代表的意義，請參閱 [GDPR 與您的業務](https://business.adobe.com/privacy/general-data-protection-regulation.html)。

## 傳送 [!DNL Customer Attributes] 請求的必要設定

若要請求存取和刪除 [!DNL Customer Attributes] 的資料，您必須：

1. 識別下列項目：

   * [組織 ID](../../administration/organizations.md)
   * 您要對其採取動作之 CRS 資料來源的別名 ID
   * 您要對其採取動作之輪廓的 CRM ID

   您的[組織 ID](../../administration/organizations.md) 是 24 個字元的英數字串，後面接著 @AdobeOrg。您需先取得組織 ID，才能向隱私權 API 提交請求。如果您找不到 ID，請聯絡 Adobe 客戶服務`gdprsupport@adobe.com`。

1. 在[!UICONTROL 隱私權服務]中，您可以將存取和刪除請求提交至 [!DNL Customer Attributes]，以及查看現有請求的狀態。

## 在 [!DNL Customer Attributes] JSON 請求中的必填欄位值

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
* &quot;regulation&quot;：**gdpr** (適用於此請求的隱私權法規)

## JSON 請求範例

```json
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

```json
attributes:
{
"value": "<*value*>",
"key": "<*key*>",
"displayName": "<*displayName*>"
}
```
