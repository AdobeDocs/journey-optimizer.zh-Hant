---
solution: Journey Optimizer
product: journey optimizer
title: 個人化語法
description: 了解如何使用個人化語法。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，語法，個人化
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 9%

---

# 個人化語法 {#personalization-syntax}

中的個人化 [!DNL Journey Optimizer] 是以名為Handlebars的範本語法為基礎。
有關Handlebars語法的完整說明，請參閱 [HandlebarsJS檔案](https://handlebarsjs.com/).

它使用模板和輸入對象來生成HTML或其他文本格式。 Handlebars範本看起來像帶有內嵌Handlebars運算式的規則文字。

簡單運算式範例：

`{{profile.person.name}}`

其中：

* `profile` 是命名空間。
* `person.name` 是由屬性組成的代號。 屬性結構是在Adobe Experience Platform XDM結構中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

## 語法一般規則 {#general-rules}

標識符可以是除以下字元之外的任意Unicode字元：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

語法區分大小寫。

這些字 **true**, **false**, **null** 和 **未定義** 僅允許在路徑表達式的第一部分中。

在Handlebars中， {{expression}} 為 **HTML逸出**. 如果運算式包含 `&`，則傳回的HTML逸出輸出會產生為 `&amp;`. 如果你不希望Handlebars逸出某個值，請使用「三藏」。

關於常值函式引數，模板語言解析器不支援單個非逸出反斜線(`\`)符號。 此字元必須以其他反斜線(`\`)符號。 範例：

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## 設定檔

此命名空間可讓您參考描述檔架構中定義的所有屬性，如 [Adobe Experience Platform Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

屬性必須先在結構中定義，才能在 [!DNL Journey Optimizer] 個人化區塊。

>[!NOTE]
>
>了解如何在中的條件中運用設定檔屬性 [本節](functions/helpers.md#if-function).

**範例參考：**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 區段{#perso-segments}

了解如何在中的條件中運用設定檔屬性 [本節](functions/helpers.md#if-function).

>[!NOTE]
>若要進一步了解分段和分段服務，請參閱 [本節](../segment/about-segments.md).

## 優惠 {#offers-syntax}

此命名空間可讓您參考現有的選件決策。
若要參考選件，您必須宣告路徑，其中包含定義選件的不同資訊。

此路徑的結構如下：

`offers.Type.[Placement Id].[Activity Id].Attribute`

其中：

* `offers` 識別屬於選件命名空間的路徑運算式
* `Type`  決定選件表示的類型。 可能的值包括： `image`, `html` 和 `text`
* `Placement Id` 和 `Activity Id` 是版位和活動識別碼
* `Attributes` 取決於選件類型的選件特定屬性。 範例： `deliveryUrl` 影像

如需決策API和選件表示法的詳細資訊，請參閱 [本頁](../offers/api-reference/offer-delivery-api/decisioning-api.md)

所有參考都會根據選件結構來驗證，其驗證機制如 [本頁](personalization-validation.md)

**範例參考：**

* 影像托管位置：

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 按一下影像時的Target URL:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 來自決策引擎之優惠方案的文字內容：

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML來自決策引擎的優惠方案內容：

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 輔助程式{#helpers-all}

Handlebars幫手是簡單的標識符，後面可能有參數。
每個參數都是Handlebars運算式。 這些幫助器可從模板中的任何上下文中訪問。

這些塊幫助器由幫助器名稱前面的#標識，並且需要同名的匹配的關閉/。
區塊是具有開啟區塊({{# }}) and closing ({{/}})。


>[!NOTE]
>
>協助程式功能在 [本節](functions/helpers.md).

## 常值類型 {#literal-types}

[!DNL Adobe Journey Optimizer] 支援下列常值類型：

| 常值 | 定義 |
| ------- | ---------- |
| 字串 | 由雙引號包住的字元組成的資料類型。 <br>範例: `"prospect"`, `"jobs"`, `"articles"` |
| 布林值 | 資料類型為true或false。 |
| 整數 | 代表整數的資料類型。 可以是正、負或零。 <br>範例: `-201`, `0`, `412` |
| 陣列 | 由一組其他常值組成的資料類型。 它使用方括弧來分組，並以逗號來分隔不同的值。 <br> **注意：** 您無法直接存取陣列內項目的屬性。 <br> 範例: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>使用 **xEvent** 變數無法用於個人化運算式。 任何對xEvent的參考都會導致驗證失敗。

## URL個人化{#perso-urls}

個人化 URL 會根據設定檔屬性，將收件者帶往網站特定頁面或個人化微網站。 在Adobe Journey Optimizer中，您可以將個人化新增至訊息內容中的URL。 URL 個人化可套用至文字和影像，同時使用個人資料或內容資料。

Journey Optimizer可讓您透過新增個人化欄位，個人化訊息中的一或多個URL。 若要個人化URL，請遵循下列步驟：

1. 在訊息內容中建立連結。 [了解更多](../email/message-tracking.md#insert-links)
1. 從個人化圖示中，選取屬性。 個人化圖示僅適用於下列類型的連結： **外部連結**, **取消訂閱連結** 和 **退出**.

![](assets/perso-url.png)

>[!NOTE]
>
>在運算式編輯器中，當您編輯個人化URL時，會基於安全原因停用協助程式函式和區段成員資格。

**個人化URL範例**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>url內使用的個人化代號不支援空格。
