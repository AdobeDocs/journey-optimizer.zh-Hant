---
title: 個人化語法
description: 瞭解如何使用個性化語法。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 9%

---

# 個人化語法 {#personalization-syntax}

個性化 [!DNL Journey Optimizer] 是基於稱為Handlebar的模板語法。
有關Handlebar語法的完整說明，請參閱 [HandlebarsJS文檔](https://handlebarsjs.com/)。

它使用模板和輸入對象生成HTML或其它文本格式。 車把模板看起來像帶有嵌入式車把表達式的常規文本。

簡單表達式示例：

`{{profile.person.name}}`

其中：

* `profile` 是命名空間。
* `person.name` 是由屬性組成的標籤。 屬性結構在Adobe Experience PlatformXDM架構中定義。 [進一步了解](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}.

## 語法一般規則 {#general-rules}

標識符可以是除以下字元之外的任何Unicode字元：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

語法區分大小寫。

詞 **真**。 **假**。 **空** 和 **未定義** 僅允許在路徑表達式的第一部分中。

在Handlebar中， {{expression}} 是 **HTML逃逸**。 如果表達式包含 `&`，然後生成返回的HTML轉義輸出 `&amp;`。 如果你不想Handlebar逃出一個值，請使用「三重存貨」。

## 設定檔

此命名空間允許您引用在中所述的配置檔案架構中定義的所有屬性 [Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。

在中引用屬性之前，需要在架構中定義這些屬性 [!DNL Journey Optimizer] 個性化塊。

>[!NOTE]
>
>瞭解如何在中的條件中利用配置檔案屬性 [此部分](functions/helpers.md#if-function)。

**示例引用：**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## 區段{#perso-segments}

瞭解如何在中的條件中利用配置檔案屬性 [此部分](functions/helpers.md#if-function)。

>[!NOTE]
>要瞭解有關分段和分段服務的詳細資訊，請參閱 [此部分](../segment/about-segments.md)。

## 優惠 {#offers-syntax}

此命名空間允許您引用現有的聘用決定。
要引用聘用，您需要聲明包含定義聘用的不同資訊的路徑。

此路徑具有以下結構：

`offers.Type.[Placement Id].[Activity Id].Attribute`

其中：

* `offers` 標識屬於提供命名空間的路徑表達式
* `Type`  確定聘用表示的類型。 可能的值為： `image`。 `html` 和 `text`
* `Placement Id` 和 `Activity Id` 是放置和活動標識符
* `Attributes` 提供取決於服務類型的特定屬性。 示例： `deliveryUrl` 用於影像

有關決策API和優惠表示法的詳細資訊，請參閱 [此頁](../offers/api-reference/offer-delivery-api/decisioning-api.md)

所有引用都通過「提供方案」進行驗證，驗證機制如所述 [此頁](personalization-validation.md)

**示例引用：**

* 映像的承載位置：

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* 按一下影像時的目標URL:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* 決策引擎提供的內容：

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* HTML決策引擎提供的內容：

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## 輔助程式{#helpers-all}

Handlebars幫助程式是一個簡單的標識符，可以跟隨參數。
每個參數都是Handlebars表達式。 可以從模板中的任何上下文訪問這些幫助程式。

這些塊幫助程式由幫助程式名稱前的#標識，並需要具有相同名稱的匹配關閉/。
塊是具有塊開口({{# }})和關閉({{/}})。


>[!NOTE]
>
>幫助程式函式的詳細資訊請參閱 [此部分](functions/helpers.md)。

## 文字類型 {#literal-types}

[!DNL Adobe Journey Optimizer] 支援以下文字類型：

| 文字 | 定義 |
| ------- | ---------- |
| 字串 | 一種資料類型，由雙引號環繞的字元組成。 <br>範例: `"prospect"`, `"jobs"`, `"articles"` |
| 布爾型 | 為true或false的資料類型。 |
| 整數 | 表示整數的資料類型。 可以是正的、負的或零的。 <br>範例: `-201`, `0`, `412` |
| 陣列 | 作為一組其他文字值組成的資料類型。 它使用方括弧對不同值進行分組，使用逗號分隔。 <br> **注：** 不能直接訪問陣列中項的屬性。 <br> 範例: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>使用 **x事件** 變數在個性化表達式中不可用。 對xEvent的任何引用都將導致驗證失敗。

## URL個性化{#perso-urls}

個人化 URL 會根據設定檔屬性，將收件者帶往網站特定頁面或個人化微網站。 在Adobe Journey Optimizer，您可以將個性化添加到消息內容中的URL。 URL 個人化可套用至文字和影像，同時使用個人資料或內容資料。

Journey Optimizer允許您通過向郵件中添加個性化欄位來個性化郵件中的一個或多個URL。 要個性化URL，請執行以下步驟：

1. 在郵件內容中建立連結。 [了解更多](../design/message-tracking.md#insert-links)
1. 從個性化表徵圖中，選擇屬性。 個性化表徵圖僅可用於以下類型的連結： **外部連結**。 **取消訂閱連結** 和 **選擇退出**。

![](assets/perso-url.png)

>[!NOTE]
>
>在表達式編輯器中，編輯個性化URL時，出於安全原因，會禁用幫助程式函式和段成員身份。

**個性化URL示例**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>在URL內使用的個性化標籤中不支援空格。
