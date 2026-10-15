---
description: 瞭解如何設定安全憑證以與Adobe CX Enterprise第一方Cookie搭配使用。
solution: Experience Cloud,Analytics
title: Adobe 託管的憑證計劃
index: true
snippet: 'y'
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
autotag-review: '2026-09-09T20:12:24.943Z'
TQID: 'https://experienceleague.adobe.com/8CSBLQaw3KOByyxxCYr1By4gyAQsDIhiofOdAzn38dg'
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
    internal-label: Metrics
  - id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7a
    internal-label: Implementations
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
    internal-label: API
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
    internal-label: Administration
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
    internal-label: Support
  - id: c8add8f2-4250-4fd9-9cde-9707036c567d
    internal-label: Methods
  - id: d2311670-43bd-4c2e-bc98-1da2aaba9cef
    internal-label: Appmeasurement implementation
  - id: e992d880-33bc-4949-a648-aa7d410276cd
    internal-label: Validation
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
    internal-label: Customer experience
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
    internal-label: Troubleshooting
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 2%
---
# Adobe 託管的憑證計劃

Adobe管理的憑證方案是設定CNAME實作所需的第一方憑證的建議程式。 設定後，程式將完全自動化。 它會及時更新憑證，因此不會因為憑證過期而影響資料收集。 前100個CNAME可免費使用此程式。

Adobe管理的憑證方案不支援透過內容傳遞網路(CDN)路由資料收集。 如果您使用CDN，請參閱[透過CDN路由資料集合](cdn.md)。 需要管理自己憑證的組織可以改用[客戶管理的憑證](customer-managed-cert.md)。 如果您目前管理自己的憑證，且想要移至Adobe管理的憑證計畫，請聯絡Adobe客戶服務。

## 實作

若要針對第一方資料收集實作新憑證，請遵循下列步驟：

1. 下載並填寫[第一方網域要求表單](cookies/assets/First_Party_Domain_Request_Form.xlsx)
1. 向Adobe客戶服務開立票證，要求在Adobe管理的憑證方案上設定第一方資料收集。 如果您的組織有資料駐留或法規遵循要求，請在您的要求中指定您想要的[RDC型別](rdc.md)。
1. Adobe代表在收到支援工單後，會提供CNAME記錄給您。 您必須在貴公司的DNS伺服器上設定此記錄，Adobe才能代表您購買憑證。 例如，主機名稱`data.example.com`指向`hiodsibxvip01.data.adobedc.net`。 如果您的組織使用DNS Certificate Authority (CAA)記錄，請確定您的CAA記錄允許DigiCert發行憑證。 請參閱[維護與更新](#renewals)。
1. 當CNAME記錄位於您組織的伺服器上時，Adobe會與DigiCert合作，購買憑證並安裝到Adobe資料收集伺服器上。
1. 如果您需要在Adobe CNAME代管時更新您的`robots.txt`檔案以用於第一方用途，請提出要求聯絡客戶服務。 當您想要更新`robots.txt`檔案以防止抓取您的子網域時，這類請求會具有相關性。

## 驗證主機名稱轉送

在Adobe安裝憑證後，您可以使用下列其中一種方法來驗證憑證是否正常運作。

+++**瀏覽器驗證**

您可以使用任何瀏覽器來驗證憑證是否已正確安裝。 在位址列中輸入`_check`作為路徑的CNAME。 例如：

`data.example.com/_check`

如果一切運作正常，瀏覽器會顯示`SUCCESS`。 如果憑證未正確安裝，系統會顯示安全性警告。

+++

+++**命令列(`curl`)**

大部分的現代作業系統已安裝[`curl`](https://curl.se)。

在命令列中鍵入下列內容：

```sh
curl data.example.com/_check
```

如果一切正常運作，主控台會傳回`SUCCESS`。

>[!TIP]
>
>您可以使用`-k`旗標停用安全性警告以協助疑難排解。

+++

+++**命令列(`nslookup`)**

在命令列中鍵入下列內容：

```sh
nslookup data.example.com
```

如果一切正常運作，Adobe的資料收集伺服器會傳回：

```text
Server: hiodsibxvip01.corp.adobe.com
Address: 10.50.112.247

Name: example.com.ssl.d1.sc.omtrdc.net
Addresses: 63.140.37.126
    63.140.37.206
    63.140.36.51
    63.140.36.145
Aliases: data.example.com
```

+++

## 更新實作程式碼

若要使用新的CNAME主機名稱，請在驗證憑證正確運作後，更新您的Adobe實作。 請參閱[更新您的實作](collection-domain.md#update-implementation)。

## 維護與更新 {#renewals}

Adobe會自動更新您的憑證。 在憑證到期三十天前，Adobe會驗證CNAME是否仍然有效及使用中，然後代表您續約憑證。 若要讓續約保持運作，請避免下列DNS變更：

* **移除或重新指向您的CNAME記錄**：如果CNAME記錄已移除或不再指向Adobe安全主機名稱，Adobe無法更新憑證。 此條件包括將CNAME記錄指向內容傳遞網路(CDN)。 如果您打算使用CDN，請參閱[在變更DNS記錄之前，將現有的第一方實作移至CDN](cdn.md#migrate)。
* **新增未授權DigiCert的CAA記錄**：憑證授權單位會檢查主機名稱及其上層網域上的憑證授權單位(CAA)記錄。 如果您使用CAA記錄，請包含`digicert.com`作為授權簽發者。 例如 `example.com. IN CAA 0 issue "digicert.com"`。
* **限制DigiCert發行至特定帳戶**： DigiCert的網域鎖定功能會將`account=`引數新增至CAA記錄，例如`example.com. IN CAA 0 issue "digicert.com; account=<token>"`。 此引數限制發行至您組織的DigiCert帳戶，即使`digicert.com`已授權，這可防止Adobe取得憑證。 如果您的組織需要DigiCert網域鎖定，請改用[客戶管理的憑證](customer-managed-cert.md)。 在您的網域註冊機構設定的網域鎖定（有時稱為傳輸鎖定）是無關的，不會影響Adobe管理的憑證。

>[!IMPORTANT]
>
>如果您的CNAME記錄不再指向Adobe安全主機名稱，Adobe系統中的專案會標示為移除，而不需要進一步通訊。

## 常見問題

+++此程式是否安全？

可以。 Adobe管理的憑證方案比[客戶管理的憑證](customer-managed-cert.md)更安全。 在Adobe和核發憑證授權單位之外不會傳輸憑證或私密金鑰。

+++

+++Adobe如何為網域購買憑證？

唯有當您將指定的主機名稱指向Adobe擁有的主機名稱時，才能購買憑證。 您將此主機名稱委派給Adobe，並允許Adobe代表您購買憑證。

+++

+++我可以要求撤銷憑證嗎？

可以。 身為網域擁有者，您有權要求撤銷憑證。 請聯絡Adobe客戶服務以開始此程式。

+++

+++使用哪種加密型別？

Adobe與DigiCert合作，核發SHA-2憑證。

+++

+++此計畫是否會產生額外費用？

Adobe為所有Adobe CX Enterprise客戶提供此程式，前100個CNAME不需額外付費。

+++

+++Adobe提供哪些密碼安全等級？

Adobe提供兩種密碼安全等級，以滿足不同客戶對第一方資料收集的安全需求。 這些層級會決定與Adobe伺服器建立HTTPS連線時支援的加密演演算法。 Adobe會根據目前的安全實務，定期審查並更新支援的演演算法集。 若要變更您的密碼安全設定，請聯絡客戶服務。

* **Standard**&#x200B;需要TLS 1.2或更新版本，以及至少128位元加密。 其設計可提供最廣泛的裝置相容性，同時維持安全加密。
* **高**&#x200B;需要TLS 1.2或更新版本，並移除對較弱加密的支援。 專為需要最強加密功能的客戶所設計。 在2015年之前發行的使用者端通常無法在加密安全性設定為&#x200B;**高**&#x200B;時連線。

+++

+++支援哪些HTTPS憑證型別？

Adobe同時支援RSA和ECC憑證，新式使用者端也支援這兩種憑證型別。 ECC憑證在伺服器和使用者端上都需要較少的處理。 對於Adobe管理的憑證，Adobe同時提供RSA和ECC憑證。 對於[客戶管理的憑證](customer-managed-cert.md)，需要RSA，建議使用ECC。

+++

