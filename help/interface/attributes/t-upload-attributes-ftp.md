---
description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
keywords: Customer Attributes;core services
seo-description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
seo-title: 選用 - 透過 FTP 上傳資料檔案
solution: Experience Cloud
title: 選用 - 透過 FTP 上傳資料檔案
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: 0bc7032d0052ba03beac1140dfbfd630e1802bfd
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 54%

---


# 選用 - 透過 FTP 上傳資料檔案

如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。

在Experience Cloud中建立客戶屬性來源和FTP帳戶後，您可以上傳資料。 您會為每個屬性來源建立一個FTP帳戶。 上傳的檔案會儲存在該帳戶的根資料夾中。 資料必須是 `.csv` 格式，並另有一個 `.fin` 檔案用以指出上傳完成。

>[!IMPORTANT]
>
>Review [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) before uploading the file.

可透過FTP或SFTP將檔案上傳至客戶屬性FTP網站。

* 您需要支援SFTP連線的用戶端。
* 您可以使用使用者名稱／密碼或不使用密碼與SFTP連線，如 [下所述](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)。

**透過 FTP 上傳資料檔案**

1. [建立客戶屬性來源及上傳資料檔案...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   請確定您已登入您的 FTP 網站 [!DNL ftp.adobe.com/<sftpname>]。

1. Click **[!UICONTROL Actions]** > **[!UICONTROL File Upload]**.

1. 上傳 `.fin` 檔案，使系統可以擷取您的檔案。

   `.fin` 檔案類型由使用者建立，是上傳完成的訊號。可以是空白的記事檔案。例如，如果上傳 [!DNL crs123.csv]，也要上傳 [!DNL crs123.fin] 檔案。

   如果上傳成功，兩個檔案都會移至名為「已處理」的 **檔案夾**。

   See [Data file requirements for uploading Customer Attributes](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) for important information about file names and structure.
