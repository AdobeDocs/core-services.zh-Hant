---
description: 瞭解用於將廣告參與事件對應至轉換事件的Adobe AdvertisingCookie，並可能使用該資訊來最佳化廣告競標。
title: Adobe AdvertisingCookie
uuid: 2eec48a3-3e81-488e-8e30-5fd62885de0b
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 6818edea-31b1-49fc-bca2-32828c7ca78d
source-git-commit: 2a80851c0a7d4ef7dbcc2565177b239f3e063164
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 12%

---

# Adobe Advertising Cookie

Adobe Advertising (前身為Adobe Advertising Cloud)會使用Cookie將廣告參與事件對應至轉換事件，並可能使用該資訊來最佳化廣告競標。

>[!NOTE]
>
>使用[Adobe Experience Cloud ID (ECID) Service](https://experienceleague.adobe.com/docs/id-service/using/intro/overview.html?lang=zh-Hant)的測試版Adobe AdvertisingJavascript標籤會建立第一方[Experience Cloud](experience-cloud.md) `s_ecid` Cookie，而非Adobe AdvertisingCookie。

| Cookie 名稱 | 有效期限 | 大小 | 位置 | 說明 |
| --- | --- | --- | --- | --- |
| **`_lcc`** | 15 分鐘 | 52 位元組 | `everesttech.net` | 儲存顯示點按的ID和時間戳記。 判斷顯示廣告上的點選事件是否適用於Adobe Analytics點選。 |
| **`_tmae`** | 1 年 | 1 KB | `everesttech.net` | 使用DSP追蹤儲存廣告互動的編碼ID和時間戳記。 包含使用者與廣告的互動，例如上次檢視的廣告 |
| **`_tmid`** | 1 年 | ~20 位元組 | `everesttech.net` | 儲存Adobe AdvertisingDemand Side Platform(DSP) ID。 對應至`everest_g_v2` Cookie中的訪客ID。 |
| **`adcloud`** | 1 年 | 50-150位元組 | 第一方 | 訪客上次造訪您網站的時間戳記和訪客上次搜尋點選。 也會儲存訪客點按廣告時所建立的`ef_id`。 繫結訪客ID與相關受眾區段和轉換。 避免向Adobe提出不必要的請求，有助於最佳化頁面載入時間。 |
| **`ev_sync_*`** |  | 8 位元組 | `everesttech.net` | 以`yyymmdd`格式執行同步的日期。 將Adobe Advertising訪客ID與合作夥伴廣告交換同步。 這是為新訪客建立的檔案，並在過期時傳送同步處理要求。 包含Cookie `ev_sync_ax`、`ev_sync_bk`、`ev_sync_dd`、`ev_sync_fs`、`ev_sync_ix`、`ev_sync_nx`、`ev_sync_ox`、`ev_sync_pm`、`ev_sync_rc`、`ev_sync_tm`和`ev_sync_yh`。 |
| **`everest_g_v2`** | 1 年 | ~27 位元組 | `everesttech.net` | 儲存瀏覽器和訪客ID。 在使用者首次點按廣告後建立。 用於將目前和後續點按對應到您網站上的其他事件。 |
| **`everest_session_v2`** | Session | ~16 位元組 | `everesttech.net` | 儲存目前的工作階段ID。 |
| **`id_adcloud`** | 91 天 | 16 位元組 | 第一方 | 儲存訪客ID。 |

{style="table-layout:auto"}
