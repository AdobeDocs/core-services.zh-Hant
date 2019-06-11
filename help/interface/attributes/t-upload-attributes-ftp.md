---
description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
keywords: 客戶屬性；核心服務
seo-description: 如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。
seo-title: 選用 - 透過 FTP 上傳資料檔案
solution: Experience Cloud
title: 選用 - 透過 FTP 上傳資料檔案
uuid: 5df565dd-b6 f8-420e-981f-4b6 fc6 f7 d0 e
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 選用 - 透過 FTP 上傳資料檔案

如果您不是以拖放方式上傳，可以透過 FTP 將客戶屬性資料上傳至 Experience Cloud。

在 Experience Cloud 中建立客戶屬性來源和 FTP 帳戶後，您就可以上傳資料。您為每一屬性來源建立一個 FTP 帳戶。上傳的檔案會儲存在該帳戶的根目錄中。資料必須 [!DNL .csv] 採用格式，並使用第二 [!DNL .fin] 個檔案指出上傳完成。

>[!IMPORTANT]
>
>在上傳檔案之前，先檢視 [資料檔案需求以上傳客戶屬性](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19) 。


上傳檔案至客戶屬性 FTP 網站可透過 FTP 或 SFTP 完成。

* 您需要支援 SFTP 連線的用戶端。
* 您可以使用者名稱/密碼或以無密碼與 SFTP 連線，如[此處](https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/?f=ftp_sftp_cert_auth)所述。



<!-- <p>Error states - get with Matt and Dave </p> 
<p>What are the most common reasons for doing this? Retail? Do a use case example, then show an AN example. </p> 
<p>You create one FTP per attribute source. Files go to the root folder in that account. The file type .fin is user-created. (For example, upload a .csv then a .fin of the same name, which signals you have completed the upload. https://wiki.corp.adobe.com/display/marketingcloud/Customer+Record+Services#CustomerRecordServices-FileFormats (leverage for doc). Possibly link from FTP File Reqs page to a help file about naming conventions. Need a new file type page for this. Similar content here: https://marketing.adobe.com/resources/help/en_US/reference/c_general_file_structure.html and here: https://marketing.adobe.com/resources/help/en_US/whitepapers/ftp/ftp_datasources.html </p> 
<p>Drag-n-drop and zip functionality for uploads - 1/21/2015. S/b less than 100 megs for drag and drop zip file. Fin file not required for drag/drop. </p> 
<p>Preview Data - shows the last upload (?) </p> 
<p>Need a link to the "instructions" on that information icon with the image. </p> 
<p>Workflow: Drag and drop, validate schema, configure subscription, save/activate. </p> -->
**透過 FTP 上傳資料檔案**

1. [建立客戶屬性來源及上傳資料檔案...](../attributes/t-crs-usecase.md#task_BCC327B2A0EF4A1BBB2934013AB92B78).

   確定您已登入FTP網站，網址 [!DNL 為ftp. adobe. com/<sftpname>]。

1. 按一下 **[!UICONTROL 「動作]** &gt; **[!UICONTROL 檔案上傳]**」。

1. 上傳 [!DNL .fin] 檔案，以便擷取您的檔案。

   檔案類型 [!DNL .fin] 是由使用者建立，並指出上傳完成。可以是空白的記事檔案。例如，上傳 [!DNL crs123.csv]時，您也會上傳 [!DNL crs123.fin]。

   如果上傳完成，兩個檔案都會移至 **processed** 資料夾。


   請參閱[針對上傳客戶屬性的資料檔案需求](../attributes/crs-data-file.md#concept_DE908F362DF24172BFEF48E1797DAF19)，以取得有關檔案名稱和結構的重要資訊。
