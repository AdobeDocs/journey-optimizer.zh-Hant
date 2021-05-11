---
title: 個人化語法
description: 瞭解如何使用個人化語法
translation-type: tm+mt
source-git-commit: 568b37f0bbcb663cf7062f26b90d57d89452e862
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 個人化語法{#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## 簡介

Journey Optimizer的個人化是基於稱為Handlebars的模板語法。
有關Handlebars語法的完整說明，請參見[HandlebarsJS](https://handlebarsjs.com/)。

它使用範本和輸入物件來產生HTML或其他文字格式。 手把範本看起來像規則文字，內嵌有Handlebar運算式。

簡單運算式範例：

```
{{profile.person.name}}
```

其中：

* **描述** 檔是命名空間。
* **person.** name是由屬性組成的標籤。屬性結構在Adobe Experience PlatformXDM模式中定義。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

## 語法一般規則

識別碼可以是除下列以外的任何Unicode字元：

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

語法區分大小寫。

僅允許在路徑表達式的第一部分中使用字詞&#x200B;**true**、**false**、**null**&#x200B;和&#x200B;**undefined**。

在Handlebars中，{{expression}}傳回的值是&#x200B;**HTML-escaped**。 如果運算式包含&amp;，則傳回的HTML逸出輸出會產生為&amp;。 如果你不想讓Handlebars逃出一個值，請使用「三重隱藏」。

## 設定檔

此命名空間允許您引用[Adobe Experience Platform資料模型(XDM)文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html)中描述的配置檔案架構中定義的所有屬性。

在Journey Optimizer個人化區塊中參考屬性之前，必須先在架構中定義屬性。

所有引用都通過[此處](personalization-validation.md)所述的驗證機制對配置檔案方案進行驗證。

**參考範例：**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**確定電子郵件地址擴展**:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## 區段

若要進一步瞭解分段和分段服務，請參閱此[節](../segment/about-segments.md)。

**根據區段會籍演算不同的內容**:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**確定配置式是否已是成員**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## 優惠方案

此命名空間可讓您參考現有選件決策。
若要參考選件，您必須使用定義選件的不同資訊來宣告路徑。

此路徑具有以下結構：
0 - &#39;offers&#39;:識別屬於選件名稱空間的路徑運算式
1 —— 類型：決定選件表示法的類型。 有效值為&#39;image&#39;、&#39;html&#39;和&#39;text&#39;
2 —— 位置ID
3 —— 活動ID
4 —— 提供特定屬性。 可使用的屬性視選件類型而定。 例如，影像`deliveryUrl`。

有關Decisions API的詳細資訊，請參閱此[頁面](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

如需選件表示法的詳細資訊，請參閱此[頁面](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers)。

所有參考都會以[此處](personalization-validation.md)所述的驗證機制，根據選件架構進行驗證。

**參考範例：**

* 影像托管位置：

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* 當您按一下影像時的目標URL:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* 來自決策引擎的選件文字內容：

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* 來自決策引擎的選件HTML內容：

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## 幫手

Handlebars幫助程式是一個簡單的標識符，可以跟隨參數。
每個參數都是Handlebars運算式。 這些協助工具可從範本中的任何內容存取。

這些塊幫助器由位於幫助器名稱前面的#標識，並需要同名的匹配關閉/。
塊是具有塊開啟({{# }})和關閉({{/})的表達式。

### 若  

使用&#x200B;**if**幫助器來定義條件塊。
如果運算式評估傳回true，則會轉譯區塊，否則會跳過區塊。

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在&#x200B;**if**&#x200B;協助程式後，如果相同的條件為false，您可輸入&#x200B;**else**陳述式，以指定要執行的程式碼區塊。
**else if**&#x200B;陳述式將指定新條件來測試第一個陳述式是否傳回false。

**根據條件運算式來轉換不同的商店連結**:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### 除非

**#** unlesshelper用於定義條件區塊。如果運算式評估傳回false，則會轉譯區塊，但是與&#x200B;**#if**&#x200B;協助程式相反。

**根據電子郵件地址擴充功能來轉譯某些內容**:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### 每個

**each**幫助器用於在陣列上迭代。
幫助程式的語法為```{{#each ArrayName}}``` YourContent {{/each}}
我們可以使用區塊內的關鍵字**this**&#x200B;來參考個別陣列項目。 使用{{@index}}可呈現陣列元素的索引。

範例：

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**呈現此使用者購物車中的產品清單**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### 使用

**#with**&#x200B;協助程式可用來變更template-part的評估Token。

範例：

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

**#with**&#x200B;協助程式也適用於定義捷徑變數。

**搭配使用鋸齒較長的變數名稱，以縮短變數名稱**:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## 限制

* 個人化運算式中無法使用&#x200B;**xEvent**&#x200B;變數。 任何對xEvent的參考都會導致驗證失敗。
