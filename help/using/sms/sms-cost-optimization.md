---
solution: Journey Optimizer
product: journey optimizer
title: 成本最佳化的簡訊最佳實務
description: 瞭解如何在Journey Optimizer中管理字元限制、編碼和個人化，以最佳化SMS訊息成本
feature: SMS
topic: Content Management
role: User
level: Intermediate
source-git-commit: 13b3c8aa7fce85029167ef31feb7272e4877b7b0
workflow-type: tm+mt
source-wordcount: '521'
ht-degree: 0%

---

# 簡訊成本最佳化的最佳實務 {#sms-cost-optimization}

SMS訊息通常會根據每則訊息160個字元的限制由提供者計費。 如果訊息被分割成多個部分，傳送SMS訊息可能會產生額外成本。

請遵循這些准則，最佳化您的傳訊策略並減少費用。

## 保持訊息簡短 {#keep-messages-short}

Journey Optimizer允許在SMS訊息本文中最多使用1,500個字元。 超過此限制時會出現警告，超過此臨界值的訊息會觸發錯誤。

大部分的SMS提供者支援GSM 7位元編碼，其中單一SMS最多可包含160個字元。 超過此長度的訊息會自動分割為多個SMS部分（串連）：

* **少於160個字元**： 1個SMS部分
* **161-306個字元**： 2個SMS部分
* **307-459個字元**： 3個SMS部分

**為了將成本降至最低**，請將訊息長度保持在160個字元以下，以便作為單一SMS部分計費。

例如，1,600個字元的訊息可能會耗用10個簡訊積分，即使它在Journey Optimizer中顯示為單一訊息亦然。

## 避免使用會增加長度的特殊字元 {#avoid-special-characters}

某些字元（例如`| ^ € { } [ ] ~ \`）在GSM編碼中會計為兩個字元。 包含這些字元可能會讓您的訊息更快地超過&#x200B;**160個字元的上限**。

## 防止UCS-2編碼 {#prevent-ucs2-encoding}

如果訊息包含非GSM字元，例如中文或阿拉伯文字、商標符號，或豐富格式工具的硬退貨，則提供者會使用UCS-2編碼訊息，該工具僅支援每個SMS 70個字元。

使用UCS-2編碼可能會增加字元計數，從而影響服務提供商的郵件計費。

例如，200個字元的Unicode訊息將以3個SMS部分傳送。

## 製作最佳實務 {#authoring-best-practices}

直接在Journey Optimizer中撰寫最終SMS訊息，或從純文字應用程式貼上。

避免使用RTF應用程式，因為它們可能會引入隱藏字元或分行符號來觸發UCS-2編碼，從而可能增加SMS部分的數量和相關成本。

## 傳送前檢查字元計數 {#check-character-count}

使用純文字應用程式或Journey Optimizer **[!UICONTROL 模擬內容]**&#x200B;功能表以驗證字元計數。

雖然Journey Optimizer在內容模擬期間會顯示字元計數，包括空格，但請注意：

* 它&#x200B;**不**&#x200B;包含透過動態個人化產生的字元或某些特殊字元。

* **x/1500計數**&#x200B;是技術承載限制的視覺指標，而非每則訊息限制，例如160字元的GSM 7位元限制。

* Adobe在編輯器中支援UTF-8編碼，這與GSM-7位元編碼不同。

## 瞭解報告 {#understanding-reporting}

**Journey Optimizer報告**&#x200B;會將完整訊息計為單次傳送，不考慮SMS部分。

**提供者報告**&#x200B;反映用於傳遞的實際SMS訊息部分數量，並應參考以確認帳單及任何可能的超額費用。 如果Adobe是您透過Sinch的簡訊提供者，您將每月單獨收到此計費報告。

## Personalization注意事項 {#personalization-considerations}

動態個人化可能會增加訊息的長度。 例如，以長名字取代變數可新增其他字元。

## 其他資源 {#additional-resources}

檢閱[Sinch字元支援指南](https://developers.sinch.com/docs/sms/resources/message-info/character-support/)中支援的字元和編碼規則

