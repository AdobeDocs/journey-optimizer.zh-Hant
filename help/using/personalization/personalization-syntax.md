---
solution: Journey Optimizer
product: journey optimizer
title: 個人化語法
description: 瞭解如何使用個人化語法。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，語法，個人化
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 7%

---

# 個人化語法 {#personalization-syntax}

中的個人化 [!DNL Journey Optimizer] 是以名為Handlebars的範本語法為基礎。
如需Handlebars語法的完整說明，請參閱 [HandlebarsJS檔案](https://handlebarsjs.com/).

它使用範本和輸入物件來產生HTML或其他文字格式。 Handlebars範本看起來像含有內嵌Handlebars運算式的規則文字。

簡單運算式範例：

`{{profile.person.name}}`

其中：

* `profile` 是名稱空間。
* `person.name` 是由屬性構成的權杖。 屬性結構是在Adobe Experience Platform XDM結構描述中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}。

## 語法一般規則 {#general-rules}

識別碼可以是任何Unicode字元，但以下專案除外：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

語法區分大小寫。

字詞 **true**， **false**， **null** 和 **未定義** 僅允許在路徑運算式的第一個部分中使用。

在Handlebars中，傳回的值來自 {{expression}} 為 **HTML逸出**. 如果運算式包含 `&`，則傳回的HTML逸出輸出會產生為 `&amp;`. 如果您不希望Handlebars逸出值，請使用「三重儲存」。

關於常值函式引數，範本化語言剖析器不支援單一未逸出的反斜線(`\`)符號。 此字元必須使用其他反斜線(`\`)符號。 範例：

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## 設定檔

此名稱空間可讓您參照中所述之設定檔結構描述中定義的所有屬性。 [Adobe Experience Platform資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

屬性需要在結構描述中定義，才能在中參照 [!DNL Journey Optimizer] 個人化區塊。

>[!NOTE]
>
>瞭解如何在中利用條件中的設定檔屬性 [本節](functions/helpers.md#if-function).

**範例參考：**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 對象{#perso-segments}

瞭解如何在中利用條件中的設定檔屬性 [本節](functions/helpers.md#if-function).

>[!NOTE]
>若要瞭解分段服務的詳細資訊，請參閱 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}.

## 優惠 {#offers-syntax}

此名稱空間可讓您參考現有的優惠決定。
若要參照選件，您必須使用定義選件的不同資訊來宣告路徑。

此路徑的結構如下：

`offers.Type.[Placement Id].[Activity Id].Attribute`

其中：

* `offers` 會識別屬於優惠方案名稱空間的路徑運算式
* `Type`  決定優惠方案代表的型別。 可能的值包括： `image`， `html` 和 `text`
* `Placement Id` 和 `Activity Id` 是位置與活動識別碼
* `Attributes` 是選件特定屬性，屬性視選件型別而定。 範例： `deliveryUrl` 針對影像

如需Decisions API和優惠方案表示的詳細資訊，請參閱 [此頁面](../offers/api-reference/offer-delivery-api/decisioning-api.md)

所有參考資料都會根據選件結構描述進行驗證，驗證機制如下 [此頁面](personalization-validation.md)

**範例參考：**

* 影像的託管位置：

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 按一下影像時的目標URL：

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 來自決策引擎的優惠方案文字內容：

  `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* 來自決策引擎的優惠方案HTML內容：

  `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 輔助程式{#helpers-all}

Handlebars協助程式是簡單識別碼，後面可能會接著引數。
每個引數都是Handlebars運算式。 這些協助程式可從範本中的任何內容存取。

這些區塊協助程式是使用協助程式名稱前的#來識別，並需要相同名稱的相符結尾/ 。
區塊是含有區塊開頭的運算式({{# }}) and closing ({{/}})。


>[!NOTE]
>
>協助程式函式的詳細資訊，請參見 [本節](functions/helpers.md).
>

## 常值型別 {#literal-types}

[!DNL Adobe Journey Optimizer] 支援下列常值型別：

| 常值 | 定義 |
| ------- | ---------- |
| 字串 | 由雙引號包住的字元所組成的資料型別。 <br>範例： `"prospect"`， `"jobs"`， `"articles"` |
| 布林值 | 為true或false的資料型別。 |
| 整數 | 代表整數的資料型別。 可以是正數、負數或零。 <br>範例： `-201`， `0`， `412` |
| 陣列 | 一種資料型別，由一組其他常值組成。 它使用方括弧將不同值分組，並使用逗號分隔不同值。 <br> **注意：** 您無法直接存取陣列中專案的屬性。 <br> 範例： `[1, 4, 7]`， `["US", "FR"]` |

>[!CAUTION]
>
>使用 **xEvent** 變數無法用於個人化運算式。 對xEvent的任何參考都會導致驗證失敗。

## URL個人化{#perso-urls}

個人化 URL 會根據設定檔屬性，將收件者帶往網站特定頁面或個人化微網站。 在Adobe Journey Optimizer中，您可以將個人化新增至訊息內容中的URL。 URL 個人化可套用至文字和影像，同時使用個人資料或內容資料。

Journey Optimizer可讓您新增個人化欄位，以個人化訊息中的一或多個URL。 若要個人化URL，請遵循下列步驟：

1. 在您的訊息內容中建立連結。 [了解更多](../email/message-tracking.md#insert-links)
1. 從個人化圖示中，選取屬性。 個人化圖示僅適用於下列型別的連結： **外部連結**， **取消訂閱連結** 和 **選擇退出**.

   ![](assets/perso-url.png)

>[!NOTE]
>
>在個人化編輯器中，當您編輯個人化URL時，基於安全理由，會停用協助程式功能和對象成員資格。
>

**個人化URL範例**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>url內使用的個人化權杖不支援空格。
