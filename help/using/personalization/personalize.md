---
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 25%

---

# 開始個性化{#add-personalization}

發現 [!DNL Adobe Journey Optimizer] 個性化功能，通過利用您擁有的有關郵件的資料和資訊，將郵件調整為每個特定收件人。 它可以是他們的名字、興趣、居住地、購買的東西，等等。

➡️ [瞭解如何個性化這些視頻中的郵件](#video-perso)
➡️ [利用個性化發現使用案例](personalization-use-case.md)

## 使用專用語法生成個性化表達式 {#syntax}

[!DNL Journey Optimizer] 使用 **內** 基於Handlebar的簡單個性化語法，允許您建立包含雙大括弧的內容的表達式 **{{}}**。 您可以在相同的內容或欄位中新增多個運算式，不受限制。 瞭解詳情 [個性化語法](personalization-syntax.md)。

**範例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

處理消息（電子郵件和推送）時，Journey Optimizer用Experience Platform資料庫中包含的資料替換表達式：  `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}` 變成&quot;你好，無名氏&quot;

## 利用配置檔案資料個性化您的郵件 {#data}

根據由 Adobe Experience Platform 定義的 **XDM 個人設定檔**&#x200B;方案管理的設定檔資料進行個人化。 瞭解詳情 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

>[!CAUTION]
>的 **XDM個人配置檔案** 架構是唯一可用於個性化內容的架構 [!DNL Journey Optimizer]。

## 在不同上下文中添加個性化 {#contexts}

[!DNL Journey Optimizer] 允許您以多種不同方式個性化內容和顯示消息。 瞭解有關上下文的詳細資訊，您可以在 [此部分](personalization-contexts.md)。

## 使用表達式編輯器 {#editor}

[!DNL Journey Optimizer] 提供表達式編輯器，在該編輯器中，您將選擇、排列、自定義和驗證所有資料，以便為您的內容建立自定義個性化。

有幾種工具可幫助構建個性化內容（幫助程式函式、預定義表達式庫、屬性優先……）

瞭解有關 [!DNL Journey Optimizer] 表達式編輯器 [此部分](personalization-build-expressions.md)

## 作法影片{#video-perso}

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)
