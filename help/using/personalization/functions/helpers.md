---
title: 輔助程式
description: 輔助程式
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 7e7ff2f6451947d4d52efb2963d940ba3f50819f
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 4%

---

# 輔助程式 {#gs-helpers}

## 預設遞補值{#default-value}

此 `Default Fallback Value` 如果屬性為空白或null，會使用helper傳回預設後援值。 此機制適用於設定檔屬性和歷程事件。

**語法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此範例中，值 `there` 顯示條件為 `firstName` 此設定檔的屬性是空的或null。

## 條件{#if-function}

此 `if` 協助程式用於定義條件區塊。
如果運算式評估傳回true，則會轉譯區塊，否則會略過該區塊。

**語法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

遵循 `if` 協助程式，您可以輸入 `else` 陳述式，指定要在相同條件為false時執行的程式碼區塊。
此 `elseif` 陳述式會指定新條件來測試第一個陳述式是否傳回false。


**格式**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**範例**

1. **根據條件運算式轉譯不同的存放區連結**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **決定電子郵件地址副檔名**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **新增條件式連結**

   下列作業會將連結新增至僅含有&#39;.edu&#39;電子郵件地址之設定檔的「www.adobe.com/academia&#39;」網站、含有&#39;.org&#39;電子郵件地址之設定檔的「www.adobe.com/org&#39;」網站，以及所有其他設定檔的預設URL「www.adobe.com/users&#39;」：

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **根據受眾成員資格的條件式內容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>若要深入瞭解對象與細分服務，請參閱此 [區段](../../audience/about-audiences.md).


## Unless{#unless}

此 `unless` 協助程式用於定義條件區塊。 藉由反對the `if`  協助程式，如果運算式評估傳回false，則會轉譯區塊。

**語法**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**範例**

根據電子郵件地址副檔名轉譯某些內容：

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 每個{#each}

此 `each` 協助程式用於反複處理陣列。
協助程式的語法為 ```{{#each ArrayName}}``` 您的內容 {{/each}}
我們可以使用關鍵字來參照個別陣列專案 **此** 區塊內部。 陣列元素的索引可以使用來轉譯 {{@index}}.

**語法**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**範例**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**範例**

呈現此使用者在購物車中擁有的產品清單：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 替換為{#with}

此 `with` 協助程式可用來變更範本部分的評估權杖。

**語法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

此 `with` 協助程式也可用來定義捷徑變數。

**範例**

搭配使用，將長變數名稱等同為短變數名稱：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

此 `let` 函式可將運算式儲存為變數，以便稍後在查詢中使用。

**語法**

```sql
{% let variable = expression %} {{variable}}
```

**範例**

下列範例可讓您計算購物車中價格介於100到1000之間的產品的總價。

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```
