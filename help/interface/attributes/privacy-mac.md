---
description: 針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳做法。
keywords: 客戶屬性；核心服務
seo-description: 針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳做法。
seo-title: 隱私權考量-客戶屬性
solution: Experience Cloud
title: 隱私權考量-客戶屬性
uuid: 5666dc4e-55fa-4196-9985-cf530 clib9247
translation-type: tm+mt
source-git-commit: 979b2202a70e2a5362aa86a65a17d7c4279b3a1a

---


# 隱私權考量-客戶屬性

針對 Adobe Experience Cloud 中已上傳及使用的個人身份資訊 (PII) 的考量事項和最佳做法。


<!-- <p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> -->


* 名字和姓氏
* 住家或其他實體地址
* 電子郵件地址
* 電話號碼
* 社會安全號碼
* 其他允許實體或線上聯絡個人的識別資訊。(依地點而異。請在您執行業務的所有地方，確認並遵守當地有關隱私權和 PII 的法律和法規)。


Adobe 提供工具讓廣告商收集造訪其網站或使用其應用程式之消費者的行為資訊。Adobe 也提供工具讓廣告商運用在其他資訊管理系統中的離線或外部客戶記錄來增強這項資訊。

廣告商會這麼做的常見原因，是想要在做出適合消費者的行銷和廣告決策時，增進資訊的可用性。Adobe Analytics 和 Target 允許廣告商上傳個人身份資訊 (PII)，如電子郵件地址，前提是資訊變混雜而無法用於聯絡個人。混雜的資訊仍可用於分析或行銷目的。提醒您，Adobe 禁止廣告商將敏感個人資訊傳送給 Adobe，如醫療記錄、金融帳戶資訊及未成年人相關資訊。

Adobe 瞭解這類行銷和廣告決策可能隱含消費者隱私，因此 Adobe 用內建隱私權控制來幫助廣告商符合其消費者的期望。Adobe 建議廣告商謹慎思考哪些資訊適合用於行銷目的，以及廣告商在什麼情況下有權使用這些資訊。

**最佳實務**

要上傳 PII 至 Adobe Analytics 或 Target 時，Adobe 建議客戶先將 PII 進行雜湊處理再上傳至 Adobe。混雜的資訊仍可用於分析或行銷目的。提醒您，Adobe 禁止廣告商將醫療記錄、金融帳戶資訊及未成年人相關資訊等敏感個人資訊，傳送給 Adobe Analytics 和 Target。

Adobe 建議廣告商謹慎思考哪些資訊適合用於行銷目的，以及廣告商在什麼情況下有權使用這些資訊。

由於消費者隱私權法律仍在繼續增補，Adobe 建議廣告商謹守三個通用原則:

1. 做您 (在您的隱私權政策中) 說的事。
1. 說您 (在您的隱私權政策中) 做的事。
1. 別讓消費者出乎意料。

記住這幾個期望，Adobe 建議廣告商將瀏覽活動關聯至 PII 時，要提供指出消費者驗證的提醒或個人化選擇。做法之一是在網站標題中加入歡迎訊息。Adobe 也建議廣告商在其隱私權政策中說明他們會將何種瀏覽資訊與 PII 關聯，以及在什麼情況下會將瀏覽資訊與 PII 關聯。最後，Adobe 強烈建議廣告商檢閱他們提供給消費者的退出選擇，以瞭解在退出後他們是否可以使用未驗證設定檔資訊以及如何使用。

<!-- <p> <b>Vinay Geol</b> should help craft privacy regarding how all MAC uses privacy/cookies. Privacy implications around each part of the workflow. Moving from CRM to MAC. Can it include PII? What is PII? What isn't PII? </p> 
<p>CRM data is Known Data or Info. Going to combine with activity that occurs when visitor was not authenticated. PII wiki: </p> 
<p>https://wiki.corp.adobe.com/display/omtrplatform/Visitor+Enrichment+and+privacy#VisitorEnrichmentandprivacy-INFORMATIONASSOCIATIONOPTIONS </p> 
<p>Refactoring of implementation docs as it relates to privacy and cookies. </p> 
<p>Add content to https://marketing.adobe.com/resources/help/en_US/mcloud/t-publish-audience-segment.html, as follows: </p> 
<p> Audiences are not filtered based on the authentication state of a visitor. If a visitor can browse your site in un-authenticated and authenticated states, actions that occur when a visitor is un-authenticated can still cause a visitor to be included in an audience. Please review <link> to understand the full privacy implications of audience sharing. </p> 
<p>That "link" goes to a topic dedicated to PII, with this text: </p> 
<p> - Adobe Analytics allows its advertisers to upload personally identifiable information (PII) such as email addresses. When uploading PII to Adobe Analytics, Adobe recommends that the customer should hash PII prior to uploading it to Adobe. Hashed information can still be used for analysis and for marketing purposes. As a reminder, Adobe prohibits advertisers from sending sensitive personal information to Adobe Analytics, such as medical records, financial account information, and information about minors. </p> 
<p> - Adobe recommends its advertisers carefully consider which information is appropriate to use for marketing purposes and in which circumstances the advertiser has permission to use such information. </p> 
<p> - As consumer privacy law remains in flux, Adobe recommends that advertisers respect three common tenets: 1) Do what you say (in your privacy policy); 2) Say what you do (in your privacy policy); and 3) Don't surprise your consumers. </p> 
<p> - With these expectations in mind, Adobe recommends that when an advertiser associates browsing activities to PII, the advertiser provide notices/personalization indicating that the consumer is authenticated. An example of this is including a 'Hello, Jane' greeting within the header of the website. Adobe also recommends that advertisers describe in its privacy policy what type of browsing information it associates with PII and under what circumstances browsing information is associated with PII. Lastly, Adobe strongly recommends advertisers review the opt out choices they provide their consumers to understand whether and how they can use unauthenticated profile information post opt out. </p> 
<p>Possibly revamp the cookies to include privacy, with best practices: https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/ </p> -->
