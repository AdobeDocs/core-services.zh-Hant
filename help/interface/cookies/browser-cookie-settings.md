---
description: 將封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。此隱私權設定會排除選擇退出Analytics資料收集的使用者。
keywords: cookies;privacy
seo-description: 將封鎖桌面和行動瀏覽器上所有 Cookie 的使用者移除。此隱私權設定會排除選擇退出Analytics資料收集的使用者。
seo-title: 啟用瀏覽器 Cookie 的隱私權設定
solution: Marketing Cloud,Adobe Analytics,Adobe Target,Adobe Social
title: 啟用瀏覽器 Cookie 的隱私權設定
uuid: f6a56e8b-b021-49db-8eb4-6c14af0c7243
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 啟用瀏覽器 Cookie 的隱私權設定{#enable-privacy-settings-for-browser-cookies}

您可以移除封鎖案頭和行動瀏覽器上所有Cookie的使用者。 這項功能是排除退出資料收集的使用者的隱私權設定，讓您尊重使用者停止分析處理的意願。

**若要啟用瀏覽器Cookie的隱私權設定**

1. Navigate to **[!UICONTROL Admin Tools]** > **[!UICONTROL Report Suites]**.
1. Click **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Privacy Settings]**.
1. 啟用&#x200B;**[!UICONTROL 「隱私設定」]** (適用於桌面或行動瀏覽器)。

>[!IMPORTANT]
>
>請注意，許多行動應用程式（例如Facebook或Twitter的應用程式內瀏覽器）可能會顯示為標準行動瀏覽器，但不允許所有Cookie。 啟用此功能可能會從Analytics報表中排除高比例的行動流量。

**關於瀏覽器隱私權設定**

法律和法規指引已表示，使用者封鎖Cookie的動作與使用者選擇退出設定檔的動作相同。 啟用此功能後，從使用者已將瀏覽器設定為封鎖所有Cookie的案頭瀏覽器收集的資料將會從Analytics報表中排除。 如果Adobe無法辨識網頁瀏覽器，資料將會包含在Analytics報表中。

全球立法者（無論在指導或和解方面）都表示，Cookie瀏覽器設定是使用者偏好選擇退出分析的指標。 具體而言，這些立法者已聲明封鎖第三方Cookie的瀏覽器設定是來自第三方（跨網站）追蹤的退出要求。 封鎖所有Cookie是所有追蹤的退出要求。 雖然伺服器端識別碼（例如IP位址或使用者代理）可能是繞過Cookie瀏覽器設定的理想選項，但有些立法者卻視為規避使用者選擇。