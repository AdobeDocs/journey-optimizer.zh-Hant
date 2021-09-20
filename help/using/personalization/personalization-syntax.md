---
title: 個人化語法
description: 了解如何使用個人化語法
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: fe39570b-cbd2-4b24-af10-e12990a9a885
source-git-commit: 1cf3475d7b2b990db4b2217bb03a47b76692142c
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 4%

---

# 個人化語法 {#personalization-syntax}

[!DNL Journey Optimizer]中的個人化是以稱為Handlebars的範本語法為基礎。
如需Handlebars語法的完整說明，請參閱[HandlebarsJS檔案](https://handlebarsjs.com/)。

它使用模板和輸入對象來生成HTML或其他文本格式。 Handlebars範本看起來像帶有內嵌Handlebars運算式的規則文字。

簡單運算式範例：

`{{profile.person.name}}`

其中：

* `profile` 是命名空間。
* `person.name` 是由屬性組成的代號。屬性結構是在Adobe Experience Platform XDM結構中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

## 語法一般規則

標識符可以是除以下字元之外的任意Unicode字元：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

語法區分大小寫。

僅在路徑表達式的第一部分允許使用字&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

在Handlebars中，{{expression}}返回的值為&#x200B;**HTML-escaped**。 如果運算式包含`&`，則傳回的HTML逸出輸出會產生為`&amp;`。 如果你不希望Handlebars逸出某個值，請使用「三重藏匿」。

## 設定檔

此命名空間可讓您參考設定檔架構中定義的所有屬性，如[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}所述。

在[!DNL Journey Optimizer]個人化區塊中參考屬性之前，必須先在結構中定義屬性。

>[!NOTE]
>
>了解如何在[此區段](functions/helpers.md#if-function)的條件中運用設定檔屬性。

**範例參考：**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 區段{#perso-segments}

了解如何在[此區段](functions/helpers.md#if-function)的條件中運用設定檔屬性。

>[!NOTE]
>若要進一步了解分段和分段服務，請參閱[本區段](../segment/about-segments.md)。

## 優惠

此命名空間可讓您參考現有的選件決策。
若要參考選件，您必須宣告路徑，其中包含定義選件的不同資訊。

此路徑的結構如下：

`offers.Type.[Placement Id].[Activity Id].Attribute`

其中：

* `offers` 識別屬於選件命名空間的路徑運算式
* `Type`  決定選件表示的類型。可能的值包括：`image`、`html`和`text`
* `Placement Id` 和 `Activity Id` 版位和活動識別碼
* `Attributes` 取決於選件類型的選件特定屬性。範例：影像的`deliveryUrl`

如需決策API和選件表示法的詳細資訊，請參閱[本頁面](../../using/offers/api-reference/decisions-api/deliver-offers.md)

所有參考都會根據選件結構來驗證，其驗證機制如[本頁](personalization-validation.md)所述

**範例參考：**

* 影像托管位置：

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 按一下影像時的Target URL:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 來自決策引擎之優惠方案的文字內容：

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* 來自決策引擎的選件HTML內容：

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 輔助程式{#helpers-all}

Handlebars幫手是簡單的標識符，後面可能有參數。
每個參數都是Handlebars運算式。 這些幫助器可從模板中的任何上下文中訪問。

這些塊幫助器由幫助器名稱前面的#標識，並且需要同名的匹配的關閉/。
區塊是具有區塊開頭({{# }})和結尾({{/}})的運算式。


>[!NOTE]
>
>[本節](functions/helpers.md)中詳細說明了幫助程式函式。

## 常值類型

[!DNL Adobe Journey Optimizer] 支援下列常值類型：

| 常值 | 定義 |
| ------- | ---------- |
| 字串 | 由雙引號包住的字元組成的資料類型。 <br>範例: `"prospect"`, `"jobs"`, `"articles"` |
| 布林值 | 資料類型為true或false。 |
| 整數 | 代表整數的資料類型。 可以是正、負或零。 <br>範例: `-201`, `0`, `412` |
| 陣列 | 由一組其他常值組成的資料類型。 它使用方括弧來分組，並以逗號來分隔不同的值。<br> **注意：** 您無法直接存取陣列內項目的屬性。<br> 範例: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>個人化運算式中無法使用&#x200B;**xEvent**&#x200B;變數。 任何對xEvent的參考都會導致驗證失敗。

## URL個人化{#perso-urls}

Journey Orchestration可讓您透過新增個人化欄位，個人化訊息中的一或多個URL。 執行方法：

* 在您的電子郵件或推播內容中建立連結。 若要深入了解建立連結的相關資訊，請參閱[此頁面](../message-tracking.md#insert-links))。
* 按一下個人化圖示。 此圖示適用於下列特定類型的連結：**外部連結**、**取消訂閱連結**&#x200B;和&#x200B;**選擇退出**。

![](assets/perso-url.png)

>[!NOTE]
>
>在運算式編輯器中，當您編輯個人化URL時，會基於安全原因停用協助程式函式和區段成員資格。

**個人化URL範例**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

