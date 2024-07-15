---
description: 瞭解如何設定安全憑證以與Adobe Experience Cloud第一方Cookie搭配使用。
solution: Experience Cloud,Analytics
title: Adobe 託管的憑證計劃
index: y
snippet: y
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: e15abde5-8027-4aed-a0c1-8a6fc248db5e
source-git-commit: 028b11dfbcfc0c5c9f6fd1c69350574f81f2846b
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 4%

---

# Adobe 託管的憑證計劃

Adobe管理的憑證方案是設定CNAME實作所需的第一方憑證的建議程式。 設定後，程式將完全自動化。 它會及時更新憑證，因此不會因為憑證過期而影響資料收集。 前100個CNAME可免費使用此程式。

如果您目前管理自己的憑證，便需負責購買、維護並提供憑證以Adobe第一方Cookie使用。 您可以聯絡Adobe客戶服務，討論移轉至Adobe管理的憑證計畫事宜。

## 實作

請依照下列步驟，為第一方資料收集實作新憑證：

1. 下載並填寫[第一方網域要求表單](cookies/assets/First_Party_Domain_Request_Form.xlsx)

1. 向Adobe客戶服務開立票證，要求在Adobe管理的憑證方案上設定第一方資料收集。

1. 在收到支援工單時，Adobe代表會提供CNAME記錄給您。 您必須在貴公司的 DNS 伺服器上設定這些記錄，Adobe 才能代表您購買憑證。 例如，主機名稱`data.example.com`指向`hiodsibxvip01.data.adobedc.net`。

1. 當CNAME記錄位於您組織的伺服器上時，Adobe會與DigiCert合作，購買憑證並安裝到Adobe資料收集伺服器上。

## 驗證主機名稱轉送 {#validate}

在Adobe安裝憑證後，您可以使用以下方法之一來驗證憑證是否正常運作。

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
Aliases: smetrics.example.com
```

+++

## 更新實作程式碼 {#update}

在驗證憑證正確運作後，您可以更新Adobe實作以使用這些值。

* 針對Adobe AnalyticsAppMeasurement實作，請更新[`trackingServer`](https://experienceleague.adobe.com/en/docs/analytics/implementation/vars/config-vars/trackingserver)設定變數。 若您已有實作，請參閱[訪客移轉](https://experienceleague.adobe.com/en/docs/analytics/technotes/visitor-migration)，以瞭解如何防止將現有訪客計為新訪客的其他步驟。
* 針對Web SDK實作，請更新[`configure`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/overview)命令中的[`edgeDomain`](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/edgedomain)屬性。

## 維護與更新

在第一方憑證到期三十天前，Adobe會驗證CNAME是否仍然有效及使用中。 若是如此，Adobe會假設您想要繼續使用服務，並代表您自動續約憑證。

>[!IMPORTANT]
>
>如果您組織的CNAME記錄已移除或不再對應至提供的Adobe安全主機名稱，Adobe將無法更新憑證。 Adobe系統中的專案會標示為移除，而不需進一步通訊。

## 常見問答

+++此程式是否安全？

可以。Adobe管理的憑證計畫比為Adobe提供憑證的組織更安全。 憑證或私密金鑰不會在Adobe和發行憑證授權機構之外易手。

+++

+++Adobe如何為網域購買憑證？

唯有當您將指定的主機名稱指向Adobe擁有的主機名稱時，才能購買憑證。 您基本上會將此主機名稱委派給Adobe，並允許Adobe代表您購買憑證。

+++

+++我可以要求撤銷憑證嗎？

可以。身為網域擁有者，您有權要求撤銷憑證。 請聯絡Adobe客戶服務以開始此程式。

+++

+++使用哪種加密型別？

Adobe與DigiCert搭配使用，以核發SHA-2憑證。

+++

+++此計畫是否會產生額外費用？

不可以。 Adobe免費提供此服務給所有Adobe Experience Cloud客戶。

+++

+++Adobe提供哪些密碼安全等級？

Adobe提供兩種密碼安全等級，以滿足不同客戶對第一方資料收集的安全需求。 這些等級會決定與Adobe伺服器建立HTTPS連線時支援的加密演演算法。 Adobe會根據目前的安全實務，定期審查並更新支援的演演算法集。 如果您想要變更密碼安全設定，請聯絡客戶服務。

* **Standard**&#x200B;需要TLS 1.2或更新版本，以及至少128位元加密。 其設計可提供最廣泛的裝置相容性，同時維持安全加密。
* **高**&#x200B;加密安全等級需要TLS 1.2或更新版本，並移除對較弱加密的支援。 它專為希望擁有最強大加密功能，且不擔心支援舊裝置的客戶所設計。

已知下列使用者端無法連線設定為&#x200B;**高**&#x200B;的加密安全性：

* Windows 8.1和較舊版本（最後更新於2018年）
* Windows Phone 8.1和較舊版本（最後更新於2016年）
* OS X 10.10和較舊版本（最後更新於2017年）
* iOS 8.4和較舊版本（最後更新於2015年）

+++

+++支援哪些HTTPS憑證型別？

Adobe同時支援RSA和ECC憑證型別，以滿足不同的客戶需求。 RSA憑證在使用者端上受到更廣泛的支援，但ECC憑證在伺服器和使用者端上使用的處理較少。 對於Adobe管理的憑證，會同時提供RSA和ECC。 對於客戶管理的憑證，需要RSA且建議使用ECC。 新式使用者端同時支援RSA和ECC。 下列使用者端通常只支援RSA憑證：

* Windows Vista和較舊版本（最後更新於2012年）
* Windows Phone 8.0和較舊版本（最後更新於2014年）
* OS X 10.8和較舊版本（最後更新於2013年）
* iOS 5.1和較舊版本（最後更新於2012年）
* Android 4.3和較舊版本（最後更新於2013年）

+++
