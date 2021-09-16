---
description: 了解如何啟用瀏覽器 Cookie 的隱私設定。您可將已封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。
keywords: Cookie;隱私
solution: Experience Cloud, Analytics, Target, Social
title: '瀏覽器 Cookie 的隱私設定 '
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
feature: Cookies
topic: Administration
role: Admin
level: Experienced
exl-id: 5d852e0e-4004-4f94-a6f7-3a14a96cd42f
source-git-commit: 1fb1abc7311573f976f7e6b6ae67f60ada10a3e7
workflow-type: ht
source-wordcount: '295'
ht-degree: 100%

---

# 啟用瀏覽器 Cookie 的隱私設定{#enable-privacy-settings-for-browser-cookies}

您可將已封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。 此功能為隱私設定，可排除選擇退出資料收集的使用者，讓您尊重使用者希望停止 Analytics 處理程序的意願。

**啟用瀏覽器 Cookie 隱私設定的方式**

1. 導覽至&#x200B;**[!UICONTROL 管理工具]** > **[!UICONTROL 報表套裝]**。
1. 移至「**[!UICONTROL 編輯設定]** > **[!UICONTROL 一般]** > **[!UICONTROL 隱私設定]**」。
1. 啟用「**[!UICONTROL 隱私設定]**」(適用於桌面或行動瀏覽器)。

>[!IMPORTANT]
>
>許多行動應用程式 (例如 Facebook 或 Twitter 內建的應用程式瀏覽器) 或許看似一般行動瀏覽器，但並未允許所有 Cookie。若啟用此功能，可能會從 Analytics 報表中排除高比例的行動流量。

**關於瀏覽器隱私設定**

法律和法規指引表示，使用者封鎖 Cookie 的動作等同於使用者選擇退出個人資料分析的動作。一旦啟用此功能，若使用者已將瀏覽器設定為封鎖所有 Cookie，則 Analytics 報表會排除從其桌面瀏覽器收集的資料。如果 Adobe 無法辨識網頁瀏覽器，資料將會包含在 [!DNL Analytics] 報表中。

全球立法者 (無論在指導或和解協議方面) 都聲明，Cookie 瀏覽器設定可表明使用者是否偏好選擇退出個人資料分析。具體而言，這些立法者已聲明，封鎖第三方 Cookie 的瀏覽器設定，即為選擇退出協力廠商 (跨網站) 追蹤的請求。封鎖所有 Cookie 便為選擇退出所有追蹤的請求。雖然伺服器端識別碼 (例如 IP 位址或使用者代理) 可能是繞過 Cookie 瀏覽器設定的理想選項，但有些立法者將其視為規避使用者的選擇。
