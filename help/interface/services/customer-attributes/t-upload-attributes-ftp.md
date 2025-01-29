---
description: 瞭解如何透過FTP將客戶屬性資料上傳至Experience Cloud。
solution: Experience Cloud
title: 透過FTP上傳客戶屬性資料檔案
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: ed9e4a8f-493a-4a0f-a87e-674c7da95b99
source-git-commit: 163dc8ef83fb83a0e51879520bcb3ae697c95144
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 76%

---

# 選用 - 透過 FTP 上傳資料檔案

如果您不是以拖放方式上傳，可以透過FTP將客戶屬性資料上傳至Experience Cloud。

在Experience Cloud中建立客戶屬性來源和FTP帳戶後，便可上傳資料。 您需為每個屬性來源建立一個 FTP 帳戶。上傳的檔案會儲存在該帳戶的根資料夾中。資料必須是 `.csv` 格式，並另有一個 `.fin` 檔案用以指出上傳完成。

>[!IMPORTANT]
>
>請先詳閱[上傳客戶屬性的資料檔案需求](crs-data-file.md)，再上傳檔案。

您可以透過 FTP 或 SFTP 將檔案上傳至客戶屬性 FTP 站台：

* 您需要支援 SFTP 連線的用戶端。
* 您可以使用使用者名稱/密碼或不使用密碼來與 SFTP 連線，如[此處](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)所說明。

**透過 FTP 上傳資料檔案**

1. [建立客戶屬性來源及上傳資料檔案...](t-crs-usecase.md).

   確定您已登入您的 FTP 網站 (`ftp.adobe.com/<sftpname>`)。

1. 按一下&#x200B;**[!UICONTROL 「動作]** > **[!UICONTROL 檔案上傳」]**。

1. 上傳 `.fin` 檔案，使系統可以擷取您的檔案。

   `.fin` 檔案類型由使用者建立，是上傳完成的訊號。可以是空白的記事檔案。例如，如果上傳 `crs123.csv`，也要上傳 `crs123.fin` 檔案。

   如果上傳成功，兩個檔案都會移至名為 **processed** 的資料夾。

   請參閱[上傳客戶屬性的資料檔案需求](crs-data-file.md)，以了解檔案名稱和結構的重要資訊。
