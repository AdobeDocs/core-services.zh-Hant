---
description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
keywords: 客戶屬性;核心服務
seo-description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
seo-title: 選用 - 透過 FTP 上傳資料檔案
solution: Experience Cloud
title: 選用 - 透過 FTP 上傳資料檔案
uuid: 5df565dd-b6f8-420e-981f-4b6fc6f7d0e4
translation-type: tm+mt
source-git-commit: d304e625bd2125854d9ed932674522284995e030

---


# 選用 - 透過 FTP 上傳資料檔案

如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。

在 Experience Cloud 中建立客戶屬性來源和 FTP 帳戶後，您就可以上傳資料。您為每一屬性來源建立一個 FTP 帳戶。上傳的檔案會儲存在該帳戶的根目錄中。資料必須是 `.csv` 格式，並另有一個 `.fin` 檔案用以指出上傳完成。

>[!IMPORTANT]
>
>請先檢閱[上傳客戶屬性的資料檔案需求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，然後再上傳檔案。

上傳檔案至客戶屬性 FTP 網站可透過 FTP 或 SFTP 完成。

* 您需要支援 SFTP 連線的用戶端。
* 您可以使用者名稱/密碼或以無密碼與 SFTP 連線，如[此處](https://docs.adobe.com/help/en/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/ftp-sftp-cert-auth.html)所述。

**透過 FTP 上傳資料檔案**

1. [建立客戶屬性來源及上傳資料檔案...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   請確定您已登入您的 FTP 網站 [!DNL ftp.adobe.com/<sftpname>]。

1. 按一下&#x200B;**[!UICONTROL 動作]** &gt; **[!UICONTROL 檔案上傳]**。

1. 上傳 `.fin` 檔案，使系統可以擷取您的檔案。

   `.fin` 檔案類型由使用者建立，是上傳完成的訊號。可以是空白的記事檔案。例如，如果上傳 [!DNL crs123.csv]，也要上傳 [!DNL crs123.fin] 檔案。

   如果上傳完成，兩個檔案都會移至 **processed** 資料夾。

   請參閱[針對上傳客戶屬性的資料檔案需求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以取得有關檔案名稱和結構的重要資訊。
