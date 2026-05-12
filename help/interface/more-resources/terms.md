---
description: 瞭解Adobe產品和介面術語在CX企業版、Experience Cloud解決方案、Creative Cloud、Experience League和其他支援體驗之間有何差異。
solution: Experience Cloud
title: 術語
feature-set: Experience Cloud Services
feature: Central Interface Components
topic: Administration
role: Admin
level: Experienced
exl-id: 3799f806-2794-43ab-9e70-06ee693871e7
product_v2:
  - id: d0a3eab4-7b10-4d96-a71e-6c0f8e7b7c87
feature_v2:
  - id: fdbb8fc9-ffa3-4b86-88fe-aa4c5a3e1bc6
subfeature_v2:
  - id: b75843fa-0a67-4a44-a6b1-cc627b0481dc
  - id: bdea9bc8-5600-45db-b85e-d74bb59dfcff
  - id: fef08361-6ac5-460c-93fe-d063e40b6a49
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 50012e2564e88e1a6e16578e3331136c7df0cb21
workflow-type: tm+mt
source-wordcount: 692
ht-degree: 5%

---

# 術語

<!--
TQID: https://experienceleague.adobe.com/6wm7HcuAbaV1iV3AgN55dY5WR---BnMM7lJgN0HZDsk
-->

當相同的字出現在不同的Adobe體驗（CX企業版、行銷應用程式、設計應用程式或支援網站）中時，請使用此表格。 這不是完整的字彙表；如需深入定義，請參閱[Experience League](https://experienceleague.adobe.com)的產品特定說明。

| 術語 | CX Enterprise及本指南 | Adobe的其他常見用法 |
| --- | --- | --- |
| **Adobe CX Enterprise** | 在`experience.adobe.com`的統一Web體驗，您可在此開啟行銷應用程式、設定偏好設定和通知，以及存取共用介面服務（例如客戶屬性和[對象庫](../services/audiences/overview.md)）。 先前稱為&#x200B;*Adobe Experience Cloud*。 | 與&#x200B;**Adobe Experience Platform**&#x200B;的產品不同（客戶資料基礎結構、沙箱、資料集）。 不是&#x200B;**Adobe Creative Cloud** （設計與媒體應用程式）。 |
| **Adobe Experience Platform** | 當您將資料收集、身分或平台代理程式連線至解決方案時出現；某些導覽搜尋和AI功能有平台支援。 | 資料與協調平台。 當您是指CX Enterprise殼層或首頁時，請勿使用「Experience Platform」。 |
| **Experience League** | 說明和產品內連結會傳送給Adobe解決方案的&#x200B;**檔案**、**教學課程**、學習播放清單、發行說明和社群內容的您。 從[Experience League首頁](https://experienceleague.adobe.com)開始。 | 補充&#x200B;**[Adobe說明中心](https://helpx.adobe.com/support.html)**，強調針對個人和團隊的&#x200B;**帳戶**、**計畫**、**帳單**、下載和跨產品疑難排解。 使用「說明中心」進行密碼重設、計畫變更和類似工作；使用Experience League進行產品操作說明內容。 |
| **AI助理/代理式AI** | 本指南的AI主題中所述的產品內助理和協調代理；存取和點數取決於產品權益。 | 其他Adobe介面（例如，**Firefly**&#x200B;或&#x200B;**Express**）會使用具有不同範圍與原則的「AI」功能。 |
| **組織** | 您的&#x200B;**IMS組織**： CX Enterprise中的企業授權、使用者目錄、SSO和Admin Console管理的界限。 檢視[組織和帳戶連結](../administration/organizations.md)。 | 不是Analytics *報告套裝*、Target *屬性*&#x200B;或Experience Platform *沙箱* （這些是產品專屬容器）。 |
| **Admin Console** | 位於`adminconsole.adobe.com`的Enterprise控制面，適用於使用者、產品設定檔和身分；連結自CX Enterprise **管理**&#x200B;主題。 請參閱[使用者和產品管理](../administration/admin-console.md)。 | 不同於&#x200B;**產品內管理員** （在每個應用程式中，例如Analytics管理工具或Journey Optimizer許可權畫面）。 |
| **產品設定檔** | Admin Console中的授權套件組合可授予產品或功能的存取權；使用者必須屬於可取得許可權的設定檔。 請參閱[管理產品和輪廓](https://helpx.adobe.com/tw/enterprise/using/manage-products.html)。 | 不可與產品內的所有「工作區」、「容器」或「屬性」名稱互換；這些名稱會因解決方案而異。 |
| **帳戶連結** | 為組織將應用程式登入（例如，Analytics或Target憑證）連線至您的Adobe ID，讓服務可識別一位使用者。 檢視[組織和帳戶連結](../administration/organizations.md)。 | 與&#x200B;**目錄同步**、**SSO**&#x200B;或&#x200B;**同盟**&#x200B;安裝程式不同（這些是Admin Console中的組織範圍身分識別決策）。 |
| **Experience Cloud ID服務/ ECID** | 跨解決方案使用的永久性訪客識別碼；通常使用標籤或網頁SDK部署。 在舊版Analytics討論中，仍常被當作&#x200B;**Experience Cloud ID**&#x200B;或&#x200B;**MID**&#x200B;參考。 請參閱[ID服務總覽](https://experienceleague.adobe.com/docs/id-service/using/home.html)。 | 與單一應用程式的舊版Cookie名稱或&#x200B;**Experience Platform**&#x200B;身分圖表概念不同，不過這些概念在實施中可能有所關聯。 |
| **客戶屬性** | 您可透過People服務上傳及對應，用於Analytics、Target及相關工作流程的CRM或企業屬性。 請參閱[客戶屬性](../services/customer-attributes/attributes.md)主題。 | 在未檢查產品界限的情況下，不要單獨等同於&#x200B;**Audience Manager特徵**，或等同於每個&#x200B;**Real-Time CDP**&#x200B;設定檔欄位。 |
| **客群庫** | CX Enterprise UI可在整合的應用程式間撰寫和共用對象。 | **Audience Manager**&#x200B;和&#x200B;**Target**&#x200B;也使用「對象」，但區段規則和目的地會依產品而有所不同。 |
| **區段** （分析） | 規則型對象定義，您可以在Adobe Analytics中建立，並在支援時發佈至共用對象。 | 在&#x200B;**Audience Manager**&#x200B;中，區段結合&#x200B;**特徵**；命名重疊，但實作不相同。 在&#x200B;**Target**&#x200B;中，「對象」在許多位置取代舊版的「區段」標籤。 |
| **Assets (Experience Cloud Assets)** | 共用資料夾和檔案，供CX Enterprise行銷工作流程與核准的&#x200B;**Creative Cloud**&#x200B;使用者共同作業。 請參閱[Assets概觀](../services/assets/experience-cloud-assets.md)。 | 在&#x200B;**Creative Cloud**&#x200B;中，「資產」通常是指設計檔案(PSD、AI、INDD)。 相同的字詞、不同的共用和治理模式。 |

{style="table-layout:auto"}

