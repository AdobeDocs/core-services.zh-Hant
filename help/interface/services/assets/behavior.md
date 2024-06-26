---
description: 了解共用資料夾在 Experience Cloud 中遭到移動、刪除和還原時的行為規則。
keywords: 資產共用;Creative Cloud;核心服務
solution: Experience Cloud
title: 共用資料夾的行為
uuid: 86348401-f4b1-4efe-acd1-7e73a7030edf
feature: Assets
topic: Administration
role: Admin
level: Experienced
exl-id: 5ddcb2f0-b491-466d-b357-aeacbfcf0b8e
source-git-commit: c39672f0d8a0fd353b275b2ecd095ada1e2bf744
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 99%

---

# 共用資料夾的行為

共用資料夾遭到移動、刪除和還原時的行為規則。

>[!NOTE]
>
>共用的 Experience Cloud 資料夾和資產是以 1:1 的關係鏡像到 Creative Cloud 桌面。如果 Experience Cloud 使用者變更資料夾 (刪除、新增或移除共用)，動作會反映到 Creative Cloud 桌面版和網頁版。因此，如果資料夾取消共用，資料夾和資產會從本機電腦中刪除。移除共用後，資料夾及其內容會移至本機電腦上的垃圾桶，您可在此手動將它們還原至電腦。

## 非共用資料夾放入共用資料夾 {#section_A9BAC1A244A246A984AC62660E61E0C0}

您可以將非共用資料夾移至共用資料夾：

![將非共用資料夾移至共用資料夾](../../assets/01_assets_move.png)

**結果**：兩個資料夾都會變成共用資料夾。

## 共用資料夾放入非共用資料夾 {#section_8BA83001DCEC4CF084B980C4A660F59A}

您可以將共用資料夾移至非共用資料夾。

![將共用資料夾移至非共用資料夾](../../assets/02_assets_move.png)

**結果**：非共用資料夾仍為非共用資料夾。共用資料夾會維持共用狀態。

## 非共用資料夾的內容放入共用資料夾 {#section_2941ED0DC52E4573AC1AB4C22313DD8E}

您可以將內容從非共用資料夾移至共用資料夾。

![將非共用資料夾的內容移至共用資料夾](../../assets/03_assets_move.png)

**結果：**&#x200B;內容現在已共用，所有共同作業人員都能看到。儲存空間會隨著內容大小增加。

## 封存的及刪除的共用內容 {#section_5210D5F4943A44D0BA675D8EB4EAE20F}

您可以封存或刪除共用資料夾中的內容。

![已封存及刪除的共用內容](../../assets/04_assets_move.png)

**結果：**&#x200B;系統會為資料夾的擁有者封存內容。未擁有該內容的共同作業人員無法再存取內容。

## 擁有的共用內容放入非共用資料夾 {#section_3810A364B67E4B8C9CA244BC52BF91BB}

您可以將擁有的共用資料夾內容移至非共用資料夾。

![將擁有的共用內容移至非共用資料夾](../../assets/05_assets_move.png)

**結果：**&#x200B;內容現在會取消共用。共用資料夾的共同作業人員無法再存取該內容。

## 非擁有的內容放入非共用資料夾 {#section_310766EBF0DC4C0BB4AB3E8A4DAEBE07}

您可以將其他人擁有的共用資料夾內容移至非共用資料夾。

![將其他人擁有的內容移至非共用資料夾](../../assets/06_assets_move.png)

**結果：**&#x200B;內容會顯示在非共用資料夾中，並從共用資料夾中移除。共用資料夾的共同作業人員無法再存取該內容。系統會為共用資料夾的擁有者封存內容。

擁有者和編輯者可以移動他們未擁有的內容，但檢視者無法。如果擁有者和編輯者移動內容，就無法供任何使用者在共用資料夾中使用。

## 封存的或刪除的已擁有資料夾 {#section_B314B13512A5409C87C49DFDB7602E14}

您可以封存 (透過網頁版) 或刪除 (透過桌面版) 您擁有的共用資料夾。

![已封存或刪除的自有資料夾](../../assets/07_assets_move.png)

**結果：**&#x200B;資料夾會取消共用然後封存。共同作業人員無法再存取該資料夾。

## 共用資料夾放入另一個共用資料夾 {#section_0A3F203D048D4D1586E9850DC92C51E9}

您可以將擁有的共用資料夾移至另一個您可能擁有或未擁有的共用資料夾。

![將共用資料夾移至另一個共用資料夾](../../assets/09_assets_move.png)

**結果：**&#x200B;由於資料夾已移至「資料夾 2」，所以會與新的共同作業人員共用。

## 共用內容放入另一個共用資料夾 {#section_69F6C312792A4CD2831BD14A340F850E}

您可以將共用資料夾的內容移至另一個共用資料夾。

![將共用內容移至另一個共用資料夾](../../assets/11_assets_move.png)

**結果：**&#x200B;內容會顯示在「資料夾 2」中，且已與新的共同作業人員共用。內容會從「資料夾 1」中移除，擁有者會看到已封存狀態，其他共同作業人員無法再存取。

## 從封存還原內容 {#section_DEA990B3581741F89FBB81D18C2AB449}

從屬於共用資料夾的封存還原內容。您在封存內容時擁有該內容。

![已從封存還原內容](../../assets/12_assets_move.png)

**結果：**&#x200B;內容會還原至共用資料夾，所有共同作業人員都可再次存取。如果共用資料夾已不再存，內容會放入其原始父資料夾的非共用副本中。
