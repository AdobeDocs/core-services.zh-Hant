---
title: Experience Cloud使用的IP位址
description: 如果貴組織的防火牆封鎖來自Adobe的IP位址，請使用此清單來更新防火牆設定。
exl-id: 1fca8d3b-ae8b-4095-96ef-d165f912b4c6
source-git-commit: a18b61cb32286680cb1ab2a296df33509fd95a00
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 11%

---

# Experience Cloud使用的IP位址

有些防火牆設定會封鎖來自Adobe的資料收集伺服器或負責存取資料的伺服器之IP位址。 您可以使用此範圍清單來變更組織的防火牆設定，以允許存取並在組織內傳送資料。 此頁面包含Adobe使用的輸入系統（例如資料收集）和輸出系統(例如Adobe Analytics中的資料摘要)。

>[!IMPORTANT]
>
>雖然Adobe會儘可能即時更新此檔案，但無法保證IP範圍清單維持不變。 可能的變更包括企業成長與擴充、網際網路登入需要變更Adobe的IP位址空間，或網際網路服務供應商停止運作。

除了下列IP位址區塊外，各個Adobe Experience Cloud產品也各有專屬的IP位址：

* [Adobe Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics/technotes/ip-addresses)
* [Customer Journey Analytics](https://experienceleague.adobe.com/zh-hant/docs/analytics-platform/using/technotes/ip-addresses)
* [Marketo Engage](https://experienceleague.adobe.com/zh-hant/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo#step-allowlist-marketo-ips)
* [Adobe Workfront](https://experienceleague.adobe.com/zh-hant/docs/workfront/using/administration-and-setup/get-started-administration/configure-your-firewall)

## 所有Adobe IP位址區塊

下表涵蓋所有Adobe擁有的IP位址。 此表格包含Adobe在全球執行的所有Adobe員工辦公室和資料中心。 但不包含公用雲端上託管的服務。

| IP區塊（CIDR標籤法） |
| --- |
| `63.140.32.0/19` |
| `66.117.16.0/20` |
| `66.235.128.0/19` |
| `130.248.0.0/16` |
| `172.82.192.0/18` |
| `185.34.188.0/22` |
| `192.243.240.0/22` |

{style="table-layout:auto"}

## Adobe Experience Cloud資料收集和FTP IP位址區塊

如果您的組織偏好使用特定的IP位址範圍，請參閱下表。 其功能包括:

* 所有Experience Cloud產品的資料收集伺服器
* 適用於所有Experience Cloud產品的FTP伺服器

上表包含本節中的所有IP範圍。

| 位置 | IP範圍（CIDR標籤法） |
| --- | --- |
| 澳大利亞 | `63.140.55.0/24` |
| 澳大利亞 | `63.140.56.0/23` |
| 加利福尼亞 | `63.140.32.0/23` |
| 加利福尼亞 | `63.140.34.0/24` |
| 法國 | `63.140.62.0/23` |
| 印度 | `66.117.22.0/23` |
| 日本 | `130.248.169.0/23` |
| 日本 | `63.140.50.0/23` |
| 日本 | `66.117.31.0/24` |
| 倫敦 | `66.235.156.0/24` |
| 倫敦 | `185.34.188.0/22` |
| 倫敦 | `130.248.152.0/22` |
| 倫敦 | `130.248.244.0/23` |
| 俄亥俄 | `66.117.20.0/24` |
| 俄勒岡 | `66.235.132.0/22` |
| 俄勒岡 | `130.248.130.0/23` |
| 俄勒岡 | `130.248.150.0/24` |
| 俄勒岡 | `130.248.160.0/21` |
| 俄勒岡 | `192.243.242.0/24` |
| 新加坡 | `130.248.170.0/23` |
| 新加坡 | `130.248.240.0/24` |
| 新加坡 | `63.140.44.0/22` |
| 新加坡 | `63.140.48.0/23` |
| 新加坡 | `66.117.30.0/24` |
| 新加坡 | `172.82.240.8/29` |
| 新加坡 | `172.82.240.88/29` |
| 維吉尼亞 | `63.140.38.0/23` |
| 維吉尼亞 | `63.140.54.0/24` |
| 維吉尼亞 | `67.202.5.244` |

{style="table-layout:auto"}

Adobe Experience Cloud也支援有限容量的IPv6。 這些IP區塊的資料收集用途與上方的IPv4區塊類似，但不包含FTP。

| 位置 | Host |
| --- | --- |
| 澳大利亞 | `2406:da1c:406:1a00::/56` |
| 澳大利亞 | `2406:da1c:ce5:b400::/56` |
| 加利福尼亞 | `2600:1f1c:366:d900::/56` |
| 法國 | `2a05:d012:706:d000::/56` |
| 印度 | `2406:da1a:f34:6a00::/56` |
| 愛爾蘭 | `2a05:d018:309:600::/56` |
| 日本 | `2406:da14:b07:ab00::/56` |
| 俄亥俄 | `2600:1f16:130f:7d00::/56` |
| 俄勒岡 | `2600:1f14:1eb:7d00::/56` |
| 俄勒岡 | `2600:1f14:9d3:2b00::/56` |
| 新加坡 | `2406:da18:6e8:1e00::/56` |
| 維吉尼亞 | `2600:1f18:1a20:e800::/56` |
| 維吉尼亞 | `2600:1f18:4fd:6000::/56` |
| 維吉尼亞 | `2600:1f18:b00:e100::/56` |
| 維吉尼亞 | `2600:1f18:d1f:bd00::/56` |

>[!TIP]
>
>Adobe Analytics匯出功能的FTP連線(包括Data Warehouse和資料摘要)只會來自倫敦、奧勒岡和新加坡位置的IPv4位址。
