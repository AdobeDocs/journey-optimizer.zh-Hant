---
solution: Journey Optimizer
product: journey optimizer
title: 個人化語法
description: 瞭解如何使用個人化語法。
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: 運算式，編輯器，語法，個人化
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 9c013883e1bcdbf7dffffa599a910178def80e39
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 2%

---

# 個人化語法 {#personalization-syntax}

[!DNL Journey Optimizer]中的Personalization是以名為Handlebars的範本語法為基礎。 如需Handlebars語法的完整說明，請參閱[HandlebarsJS檔案](https://handlebarsjs.com/)。

它會使用範本和輸入物件來產生HTML或其他文字格式。 Handlebars範本看起來像含有內嵌Handlebars運算式的規則文字。

簡單運算式範例：

`{{profile.person.name}}`

其中：

* `profile`是名稱空間。
* `person.name`是由屬性組成的Token。 屬性結構是在Adobe Experience Platform XDM結構描述中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。

## 語法一般規則 {#general-rules}

* 識別碼可以是任何Unicode字元，但以下專案除外：

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* 語法區分大小寫。

* 字詞&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**未定義**&#x200B;只允許在路徑運算式的第一個部分中。

* 在Handlebars中，{{expression}}傳回的值是&#x200B;**HTML逸出**。 如果運算式包含`&`，則會產生傳回的HTML逸出輸出為`&amp;`。 如果您不希望Handlebars逸出值，請使用「三重儲存」。

  假設欄位`profile.person.name`的值為「Mark &amp; Mary」。 語法`{{profile.person.name}}`將顯示`Mark &amp; Mary`，而`{{{profile.person.name}}}`將顯示`Mark & Mary`。

* 關於常值函式引數，範本化語言剖析器不支援單一未逸出的反斜線(`\`)符號。 此字元必須使用其他反斜線(`\`)符號逸出。 範例：

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## 保留關鍵字 {#reserved-keywords}

某些關鍵字在Profile Query Language (PQL)中會保留，並且無法直接用作個人化運算式中的欄位或變數名稱。 如果您的XDM結構描述包含名稱符合保留關鍵字的欄位，您必須使用反引號(`` ` ``)將其逸出，以便在運算式中參照。

**保留的關鍵字包括：**

* `next`
* `last`
* `this`

**範例：**

如果您的設定檔結構描述有名為`next`的欄位，您必須以反引號將其換行：

```
{{profile.person.`next`.name}}
```

如果沒有反引號，個人化編輯器將會因錯誤而無法通過驗證。

## 可用的名稱空間 {#namespaces}

* **輪廓**

  此名稱空間可讓您參考[Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中所述的設定檔結構描述中定義的所有屬性。

  屬性必須先在結構描述中定義，才能在[!DNL Journey Optimizer]個人化區塊中參考。

  如需如何在條件中運用設定檔屬性的詳細資訊，請參閱[本節](functions/helpers.md#if-function)。

  +++範例參考

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **客群**

  若要深入瞭解細分服務，請參閱[此檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}。

* **產品建議**

  此名稱空間可讓您參考現有的優惠決定。

  若要參照選件，您必須使用定義選件的不同資訊來宣告路徑。 此路徑的結構如下：

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  其中：

   * `offers`會識別屬於優惠方案名稱空間的路徑運算式
   * `Type`決定優惠方案宣告的型別。 可能的值為： `image`、`html`和`text`
   * `Placement Id`和`Activity Id`是位置與活動識別碼
   * `Attributes`是優惠方案特定屬性，其取決於優惠方案型別。 範例： `deliveryUrl`影像

  如需有關Decisions API和優惠宣告的詳細資訊，請參閱[此頁面](../offers/api-reference/offer-delivery-api/decisioning-api.md)

  所有參考資料都是透過在[此頁面](../personalization/personalization-build-expressions.md)中說明的驗證機制針對優惠方案結構描述進行驗證

  +++範例參考

   * 影像的託管位置：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * 按一下影像時的目標URL：

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * 來自決策引擎的優惠方案文字內容：

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * 來自決策引擎之優惠方案的HTML內容：

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## 輔助程式{#helpers-all}

Handlebars協助程式是簡單識別碼，後面可能會接著引數。 每個引數都是Handlebars運算式。 這些協助程式可從範本中的任何內容存取。

這些區塊協助程式由協助程式名稱前的`#`識別，並需要相同名稱的相符結尾`/`。

區塊是具有區塊開啟(`{{# }}`)和結束(`{{/}}`)的運算式。

如需協助程式函式的詳細資訊，請參閱[本節](functions/helpers.md)。

## 常值型別 {#literal-types}

[!DNL Adobe Journey Optimizer]支援下列常值型別：

| 常值 | 定義 |
| ------- | ---------- |
| 字串 | 由雙引號包住的字元所組成的資料型別。 <br>範例： `"prospect"`， `"jobs"`， `"articles"` |
| 布林值 | 為true或false的資料型別。 |
| 整數 | 代表整數的資料型別。 可以是正數、負數或零。 <br>範例： `-201`， `0`， `412` |
| 陣列 | 一種資料型別，由一組其他常值組成。 它使用方括弧將不同值分組，並使用逗號分隔不同值。<br> **注意：**&#x200B;您無法直接存取陣列中專案的屬性。 <br>範例： `[1, 4, 7]`， `["US", "FR"]` |

>[!CAUTION]
>
>個人化運算式無法使用&#x200B;**xEvent**&#x200B;變數。 對xEvent的任何參考都會導致驗證失敗。
