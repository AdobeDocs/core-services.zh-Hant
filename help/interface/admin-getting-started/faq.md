---
description: 有關 Experience Cloud 管理員的常見問題和答案。
keywords: core services
seo-description: 有關 Experience Cloud 管理員的常見問題和答案。
seo-title: 常見問題集
solution: Experience Cloud
title: 常見問題集
uuid: 3ed0b4eb-690f-4c14-a31c-0cc1118fb3b4
translation-type: tm+mt
source-git-commit: 5e57aedb38e6914f7e99b1b26df9e4bb52b9e13d

---


# 常見問題集

有關 Experience Cloud 管理員的常見問題和答案。

**我該如何確認自己的解決方案已啟用做為核心服務?**

如果尚未針對核心服務佈建實作，請參閱[啟用核心服務的解決方案](../core-services/core-services.md#concept_07ED1D5C64234E77976E6D572E78FB9C)，其中會說明如何:


1. [加入 Experience Cloud 並成為管理員](../core-services/core-services.md#section_2423F0BD3DF642658103310EE5EA6154)
1. [使用動態標籤管理器](../core-services/core-services.md#section_3C9F6DF37C654D939625BB4D485E4354) (或新的 [Experience Platform Launch](https://docs.adobe.com/content/help/en/launch/using/intro/get-started/quick-start.html))實作Experience Cloud ID服務
1. [將報表套裝對應至 Experience Cloud 組織](../core-services/core-services.md#concept_apg_zq2_rw)
1. [(僅限 Analytics) 最新化 Analytics AppMeasurement 代碼](../core-services/core-services.md#section_1798D9D0F05C47E29816AC4EEB9A0913)
1. [(僅限 Target) 最新化 Adobe Target 實作](../core-services/core-services.md#section_C2F4493C7A36406DAE2266B429A4BD24)
1. [確認核心服務實作](../core-services/core-services.md#section_E641782A0F4F44AF8C9C91216BE330D5)
1. [管理使用者和產品](../core-services/core-services.md#section_B6E95F4E0E12483CB9DA99CBC0C5A4AF)
1. [開始使用核心服務](../core-services/core-services.md#section_960C06093623462E8EA247B3E97274A1)




如需進一步的協助，請 [聯絡 Adobe 支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)。

**Adobe 會向公司收取 Experience Cloud 的使用費嗎?**

不會。Experience Cloud 為隨附項目，不必另外付費。不過，某些核心服務可能要另外計費。

**公司為何要透過 Experience Cloud 介面登入?**

Experience Cloud 介面提供的功能可為公司帶來新價值。它也將逐漸成為存取解決方案的標準途徑，最終取代其他個別解決方案的登入流程。透過 Experience Cloud 登入將有利於日後的順暢轉換。

**如何解決我對移轉公司的疑慮?**

[聯絡 Adobe 支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)。

**什麼是&#x200B;*`provisioning`*?**

Experience Cloud 中的佈建意思是:

* 您的使用者可以開始登入 [!DNL Experience Cloud] 及連結解決方案。
* 他們可以開始使用透過 Experience Cloud 提供的功能，例如「People」。
* 您可以為解決方案專用登入程序的退休先做好準備。
* 您可以保留對解決方案的存取控制。

**我該如何管理使用者和產品設定檔?**

* 相關說明請參閱 [Admin Console 使用指南](https://helpx.adobe.com/enterprise/administering/user-guide.html)。

* 您可以在 [Adobe Admin Console](https://adminconsole.adobe.com/enterprise) (產品連結) 中管理使用者權益和產品。

* **重要事項:** Analytics 管理員請參閱[在 Admin Console 中管理 Analytics 使用者](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)，瞭解如何將使用者 ID 從 Analytics 管理工具遷移至 Admin Console。

**如果有人無法登入 Experience Cloud，我該怎麼做?**

Admin Console 管理員可授予使用者存取權。使用者會收到內含登入指示的電子郵件。

您可能需要[聯絡 Adobe 支援](https://helpx.adobe.com/marketing-cloud/contact-support.html)，確認貴公司已全面完成佈建作業。

**使用者可以前往哪裡管理帳戶連結?**

部分使用者可能需要將自己的解決方案 (Analytics) 帳戶連結至 Adobe ID 或 Enterprise ID。

請參閱[將解決方案帳戶連結至 Adobe ID](../admin-getting-started/organizations.md#task_FD389E78640848919E247AC5E95B8369)。

**我該如何管理使用者帳戶設定檔和組織?**

請參閱[管理使用者帳戶](../admin-getting-started/organizations.md#topic_C31CB834F109465A82ED57FF0563B3F1)。

**什麼是組織?**

** 組織是可讓管理員設定群組和使用者，以及控制 Experience Cloud 單一登入的實體。組織的作用就像一個登入公司，可跨越所有的 Experience Cloud 產品和解決方案。最常見的組織就是您的公司名稱。不過，公司可以有許多組織。

**在哪裡可以找到我的 IMS 組織 ID?**

請參閱[找出組織 ID](organizations.md)。

組織 ID 會顯示在 Experience Cloud 登陸頁面和 [Admin Console 登陸頁面](https://adminconsole.adobe.com) 上。

或者，管理員也可以登入 Admin Console (導覽至 [https://adminconsole.adobe.com](https://adminconsole.adobe.com#)) 尋找特定的組織，您可以透過網址找出自己的 IMS 組織 ID。

舉例來說，在以下網址中:

`https://adminconsole.adobe.com/C538193582390300A495CC9@AdobeOrg/overview`

ID 是:

`C538193582390300A495CC9@AdobeOrg`

**我的使用者離職時我該做什麼?**

應該從解決方案本身移除其存取權。他們將無法再從 Experience Cloud 或透過直接登入存取產品。您也應該將其從 Experience Cloud 層級中移除。

**什麼是 Adobe ID?**

請參閱[身分類型](https://helpx.adobe.com/enterprise/help/identity.html)。

**我可以替我的使用者連結解決方案帳戶嗎?**

不會。使用者必須使用他們的使用者名稱和密碼，自行連結他們的解決方案。

**我的公司沒有 Social，為什麼我可以看到它?**

Adobe Social 產品可與 Analytics 搭配販售。因此，若您有 Analytics，就會看到此解決方案，但除非您有購買，否則無法存取它。