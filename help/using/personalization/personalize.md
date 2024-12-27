---
solution: Journey Optimizer
product: journey optimizer
title: 在 Journey Optimizer 中個人化內容
description: 開始使用個人化。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Beginner
keywords: 運算式，編輯器，開始，個人化
exl-id: f448780b-91bc-455e-bf10-9a9aee0a0b24
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 35%

---

# 開始使用個人化{#add-personalization}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card5"
>title="個人化體驗"
>abstract="使用 **Adobe Journey Optimizer**，利用手邊關於他們的資料與資訊，調整給各個特定接收者的訊息。可以是他們的姓氏、興趣、居住的地方、購買的產品等等。"

探索[!DNL Adobe Journey Optimizer]個人化功能，利用您擁有的訊息相關資料與資訊，根據每位特定收件者調整您的訊息。 可以是他們的姓氏、興趣、居住的地方、購買的產品等等。

➡️[瞭解如何在這些影片中個人化訊息](#video-perso)
➡️[探索利用個人化的使用案例](personalization-use-case.md)

## 使用專用語法建立個人化運算式 {#syntax}

[!DNL Journey Optimizer]使用以Handlebars為基礎的&#x200B;**inline**&#x200B;簡單個人化語法，可讓您建立包含雙大括弧&#x200B;**{{}}**&#x200B;之內容的運算式。 您可以在相同的內容或欄位中新增多個運算式，不受限制。 [進一步瞭解個人化語法](personalization-syntax.md)。

**範例：**

* `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`
* `Hello {{profile.person.name.fullName}}`

處理訊息（電子郵件和推播）時，Journey Optimizer會以Experience Platform資料庫中包含的資料取代運算式： `Hello {{profile.person.name.firstName}} {{profile.person.name.lastName}}`會變成「Hello John Doe」。

## 運用設定檔資料個人化您的訊息 {#data}

根據由 Adobe Experience Platform 定義的 **XDM 個人輪廓**&#x200B;方案管理的輪廓資料進行個人化。 在[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

>[!CAUTION]
>**XDM Individual Profile**&#x200B;結構描述是唯一可用來個人化[!DNL Journey Optimizer]中內容的結構描述。

此外，您也可以運用&#x200B;**計算屬性**&#x200B;來個人化您的內容。 計算屬性以擷取到Adobe Experience Platform中的已啟用設定檔體驗事件資料集為基礎，並當做儲存在客戶設定檔中的彙總資料點，彙總個別行為事件[瞭解如何使用計算屬性](../audience/computed-attributes.md)

## 使用個人化編輯器 {#editor}

[!DNL Journey Optimizer]提供個人化編輯器，您可在其中選取、排列、自訂及驗證所有資料，以建立內容的自訂個人化。 有數個工具可協助您建置個人化內容，例如：Felper函式、預先定義的運算式程式庫、受歡迎的屬性等等。

* [瞭解如何使用個人化編輯器](personalization-build-expressions.md)
* [瞭解您可在何處執行個人化](personalization-contexts.md)。

## 作法影片{#video-perso}

瞭解如何使用歷程中的內容事件資訊來個人化訊息。

>[!VIDEO](https://video.tv.adobe.com/v/334165?quality=12)

了解如何將以輪廓為基礎的個人化新增至訊息，以及如何使用客群成員資格作為個人化區塊的先決條件。

>[!VIDEO](https://video.tv.adobe.com/v/334078?quality=12)

