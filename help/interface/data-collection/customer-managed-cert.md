---
title: 客戶管理的憑證
description: 瞭解何時將客戶管理的憑證用於第一方資料收集，以及貴組織續訂憑證的責任。
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
    internal-label: CX Enterprise
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
    internal-label: Security
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 18fd590d6f0fd1800e3d5c62851453aa91d9db5f
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 1%
---
# 客戶管理的憑證

透過客戶管理的憑證，您的組織會取得第一方資料收集主機名稱的憑證，並將其提供給Adobe。 Adobe在其資料收集伺服器上託管憑證。 貴組織有責任續約憑證，並在目前憑證過期前，將每個已續約的憑證提供給Adobe。

>[!TIP]
>
>對於大多數第一方實作，Adobe建議使用[Adobe管理的憑證方案](adobe-managed-cert.md)。 這樣會更安全，並且會自動更新憑證。 只有在貴組織需要時才使用客戶管理的憑證。

## 何時使用客戶管理的憑證

* **您透過具有第一方來源的CDN路由資料收集**： [Adobe管理的憑證方案](adobe-managed-cert.md)不支援CDN實作。 請參閱[使用第一方來源設定CDN](cdn.md#first-party-origin)。
* **您的安全性原則需要直接控制憑證**：例如，您的組織必須能夠透過自己的憑證授權單位撤銷憑證，而非透過Adobe客戶服務要求撤銷。
* **您的組織需要特定的憑證授權單位或憑證型別**： Adobe管理的憑證程式使用DigiCert所發行的憑證。

## 比較憑證方法

| | Adobe 管理的憑證 | 客戶管理的憑證 |
| --- | --- | --- |
| **取得憑證的人員** | Adobe，透過DigiCert | 您的組織，透過您選擇的商業憑證授權單位 |
| **續約** | Adobe會自動更新憑證 | 您的組織會更新憑證，並在每次到期前提供憑證給Adobe |
| **憑證型別** | Adobe同時提供RSA和ECC憑證 | 需要RSA；建議使用ECC |
| **支援CDN** | 無 | 是，作為第一方來源 |

## 設定客戶管理的憑證

1. 聯絡Adobe客戶服務，使用客戶管理的憑證來要求第一方資料收集。 包含您的第一方主機名稱，例如`data.example.com`。 如果您的組織有資料駐留或法規遵循要求，請在您的要求中指定您想要的[RDC型別](rdc.md)。
1. Adobe客戶服務提供主機名稱的憑證簽署要求(CSR)。 Adobe會產生並保留私密金鑰，讓您的組織絕不會處理私密金鑰。 Adobe需要RSA憑證，並建議ECC憑證。 每種憑證型別都需要各自的CSR，因此如果您想要ECC憑證，請向Adobe客戶服務要求ECC CSR。
1. 將每個CSR提交給所需的商業憑證授權單位，以取得簽署的憑證。 不支援免費的憑證服務。 按照客戶服務的指示，提供已核發給Adobe的憑證。
1. Adobe安裝憑證後，將主機名稱的流量導向至Adobe：
   * **沒有CDN**：依照Adobe客戶服務的指示，更新您組織的DNS記錄。
   * **使用CDN**：將您的CDN來源設定為第一方主機名稱。 請參閱[使用第一方來源設定CDN](cdn.md#first-party-origin)。
1. 如果您的實作尚未傳送資料至此主機名稱，請[更新您的實作](collection-domain.md#update-implementation)。

## 更新您的憑證 {#renewals}

貴組織有責任續約憑證，並在目前的憑證過期前，將已續約的憑證提供給Adobe客戶服務。

如果Adobe伺服器上的憑證過期，瀏覽器和CDN會拒絕與您的主機名稱的連線，且會遺失這些要求的資料。 CDN不需通知您即可捨棄此資料。

憑證存留期的上限正在縮短，這使得更新更頻繁。 如需詳細資訊，請參閱CA/Browser Forum伺服器憑證基準需求中的[6.3.2憑證操作期間與金鑰組使用期間](https://cabforum.org/working-groups/server/baseline-requirements/requirements/#632-certificate-operational-periods-and-key-pair-usage-periods)。 若要避免資料收集出現間隙：

* 追蹤您提供給Adobe之每個憑證的到期日。
* 指定續約的擁有者，並記錄續約流程，以便繼續處理員工變更。

Adobe目前正在探索自助服務憑證續約流程。

## 停止使用客戶管理的憑證

* **若要移至Adobe管理的憑證方案**：請連絡Adobe客戶服務。 Adobe管理的憑證計畫要求您的主機名稱直接指向Adobe，而非CDN。
* **若要停止使用您的第一方主機名稱**：更新所有使用該主機名稱的實作，然後聯絡Adobe客戶服務以從Adobe伺服器移除憑證。
* **若要移至具有第三方來源的CDN**：請參閱[將現有的第一方實作移至CDN](cdn.md#migrate)。
