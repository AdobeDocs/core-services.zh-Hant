---
description: 針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳作法。
keywords: customer attributes;core services
seo-description: 針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳作法。
seo-title: 隱私權考量 - 客戶屬性
solution: Experience Cloud
title: 隱私權考量 - 客戶屬性
uuid: 5666dc4e-55fa-4196-9985-cf530cfb9247
translation-type: tm+mt
source-git-commit: f7ec8bf6087a18be41c9efbf05f60e6cfd24e566

---


# 隱私權考量 - 客戶屬性

針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳作法。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 名字和姓氏
* 首頁或其他實體地址
* 電子郵件地址
* 電話號碼
* 社會安全號碼
* 允許個人進行實體或線上聯絡的其他識別碼。 (視地點而定。 請確認並遵守與您業務所在地的隱私權和PII相關的當地法律和法規。)


Adobe提供工具，讓廣告商可收集有關造訪其網站或使用其應用程式之消費者的行為資訊。 Adobe也提供工具讓廣告商利用廣告商在其他資訊管理系統中可能擁有的離線或外部客戶記錄來增強這項資訊。

廣告商這麼做的一個常見原因，是要改善在做出適合消費者的行銷和廣告決策時可用的資訊。 Adobe Analytics和Target允許廣告商上傳個人識別資訊(PII)，例如電子郵件地址，但必須經過雜湊處理，才無法用於聯絡個人。 雜湊資訊仍可用於分析和行銷用途。 提醒您，Adobe禁止廣告商將敏感的個人資訊傳送給Adobe，例如醫療記錄、財務帳戶資訊和未成年人相關資訊。

Adobe瞭解這些類型的行銷和廣告決策可能會影響消費者的隱私權，因此Adobe已內建隱私權控制功能，協助廣告商符合其消費者的期望。 Adobe建議廣告商仔細考慮哪些資訊適合用於行銷目的，以及廣告商在哪些情況下有權使用此類資訊。

**最佳作法**

當將PII上傳至Adobe Analytics或Adobe Target時，Adobe建議客戶在將PII上傳至Adobe之前先加以雜湊。 雜湊資訊仍可用於分析和行銷用途。 提醒您，Adobe禁止廣告商將敏感的個人資訊傳送至Adobe Analytics和Adobe Target，例如醫療記錄、財務帳戶資訊和未成年人相關資訊。

Adobe建議廣告商仔細考慮哪些資訊適合用於行銷目的，以及廣告商在哪些情況下有權使用此類資訊。

由於消費者隱私權法仍在不斷變動，Adobe建議廣告商遵守三項共同原則：

1. 依照您的隱私權政策，盡情發揮。
1. 說說您的工作（在您的隱私權政策中）。
1. 不要讓您的消費者驚訝。

考慮到這些期望，Adobe建議當廣告商將瀏覽活動關聯至PII時，廣告商會提供通知或個人化，指出消費者已通過驗證。 其範例是在網站標題中包含問候語。 Adobe也建議廣告商在其隱私權政策中說明其與PII關聯的瀏覽資訊類型，以及在何種情況下瀏覽資訊與PII關聯。 最後，Adobe強烈建議廣告商檢閱他們提供給其消費者的選擇退出選項，以瞭解他們是否以及如何在選擇退出後使用未驗證的個人檔案資訊。

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to t-publish-audience-segment, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://docs.adobe.com/content/help/en/core-services/interface/ec-cookies/cookies-privacy.html </p> -->
