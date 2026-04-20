---
description: 瞭解CX Enterprise中已上傳及使用之個人身分資訊(PII)的相關考量事項和最佳作法。
solution: Experience Cloud
title: ' [!DNL Customer Attributes]的隱私權考量事項'
feature: Customer Attributes
topic: Administration
role: Admin
level: Experienced
exl-id: 27c026ff-198b-4f49-9718-f25f77a9e716
TQID: https://experienceleague.adobe.com/4L-qz0n3h97DduJvPGGoJPl1VvrPAKJTeUnkJGs6xvc
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 1a77ef8d31211fb11c790152e78037a8c3b238a2
workflow-type: tm+mt
source-wordcount: 511
ht-degree: 92%

---

# [!DNL Customer Attributes] 的隱私權考量事項

Adobe CX Enterprise中已上傳及使用之個人身分資訊(PII)的相關考量事項和最佳做法。

* 名字和姓氏
* 住家或其他實體地址
* 電子郵件地址
* 電話號碼
* 身分證字號
* 允許個人進行實體或線上連絡的其他識別碼。 (因地而異。 請確認並遵守您所有事業所在地的當地隱私權和 PII 相關法律與法規。)

Adobe 提供的工具讓廣告商可收集有關消費者造訪其網站或使用其應用程式的行為資訊。 廣告商的其他資訊管理系統中可能有離線或外部客戶記錄，而 Adobe 提供的工具也可讓廣告商利用這些記錄來增強上述資訊。

廣告商這麼做的一個常見原因，是為了改善在做出適合消費者的行銷和廣告決策時可使用的資訊。 Adobe Analytics 和 Target 允許廣告商上傳個人識別資訊 (PII)，例如電子郵件地址，但必須經過雜湊處理，使其無法用於連絡個人。 雜湊資訊仍可用於分析和行銷用途。 提醒您，Adobe 禁止廣告商將敏感的個人資訊傳送給 Adobe，例如醫療記錄、財務帳戶資訊和未成年人相關資訊。

Adobe 了解這些類型的行銷和廣告決策可能隱含消費者隱私疑慮，因此 Adobe 已內建隱私控制功能，可協助廣告商達到其消費者的期望。 Adobe 建議廣告商仔細考慮哪些資訊適合用於行銷目的，以及廣告商在哪些情況下有權使用這類資訊。

## 最佳做法

將 PII 上傳至 Adobe Analytics 或 Adobe Target 時，Adobe 建議客戶在將 PII 上傳至 Adobe 之前先對其進行雜湊處理。 雜湊資訊仍可用於分析和行銷用途。 提醒您，Adobe 禁止廣告商將敏感的個人資訊傳送至 Adobe Analytics 和 Adobe Target，例如醫療記錄、財務帳戶資訊和未成年人相關資訊。

Adobe 建議廣告商仔細考慮哪些資訊適合用於行銷目的，以及廣告商在哪些情況下有權使用這類資訊。

由於消費者隱私權法不斷變動，Adobe 建議廣告商遵守三個通用原則：

1. 說到做到 (在您的隱私權政策中)。
1. 據實以告 (在您的隱私權政策中)。
1. 不要讓消費者感到驚訝。

考慮到這些期望，Adobe 建議廣告商在將瀏覽活動與 PII 建立關聯時，提供通知或個人化內容，指出消費者已通過驗證。 此情況的範例是在網站標題中包含問候語。 Adobe 也建議廣告商在其隱私權政策中說明會與 PII 建立關聯的瀏覽資訊類型，以及何種情況下瀏覽資訊會與 PII 建立關聯。 最後，Adobe 強烈建議廣告商檢閱自己提供給消費者的選擇退出選項，瞭解是否可以以及如何在選擇退出後使用未經驗證的輪廓資訊。
