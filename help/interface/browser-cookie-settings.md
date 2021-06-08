---
description: 了解如何啟用瀏覽器 Cookie 的隱私設定。您可將已封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。
keywords: Cookie;隱私
solution: Experience Cloud, Analytics, Target, Social
title: '瀏覽器 Cookie 的隱私設定 '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookie
topic: 管理
role: Administrator
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
source-git-commit: 40fd81f8a293dc5bca3b41e8f6e708d1be4bae5d
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 60%

---

# 啟用瀏覽器 Cookie 的隱私設定{#enable-privacy-settings-for-browser-cookies}

您可將已封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。此功能為隱私權設定，可排除選擇退出資料收集的使用者，讓您尊重使用者停止Analytics處理的意願。

**啟用瀏覽器 Cookie 隱私設定的方式**

1. 導覽至&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 報表套裝]**。
1. 按一下&#x200B;**[!UICONTROL 編輯設定]** > **[!UICONTROL 一般]** > **[!UICONTROL 隱私設定]**。
1. 啟用&#x200B;**[!UICONTROL 隱私設定]** (適用於桌面或行動瀏覽器)。

>[!IMPORTANT]
>
>許多行動應用程式(例如Facebook或Twitter的應用程式內瀏覽器)可能顯示為標準行動瀏覽器，但不允許所有Cookie。 若啟用此功能，可能會從 Analytics 報表中排除高比例的行動流量。

**關於瀏覽器隱私設定**

法律和法規指引表示，使用者封鎖 Cookie 的動作等同於使用者選擇退出設定檔分析的動作。啟用此功能後，從使用者已將瀏覽器設定為封鎖所有Cookie的案頭瀏覽器所收集的資料，將從Analytics報表中排除。 如果Adobe無法識別Web瀏覽器，資料將包含在[!DNL Analytics]報表中。

全球立法者 (無論在指導或和解協議方面) 都聲明，Cookie 瀏覽器設定可表明使用者是否偏好選擇退出設定檔分析。具體而言，這些立法者已聲明，封鎖第三方 Cookie 的瀏覽器設定，即為選擇退出第三方 (跨網站) 追蹤的請求。封鎖所有 Cookie 便為選擇退出所有追蹤的請求。雖然伺服器端識別碼（例如IP位址或使用者代理）可能是繞過Cookie瀏覽器設定的理想選項，但有些立法者將其視為規避使用者的選擇。
