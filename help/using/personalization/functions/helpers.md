---
title: 輔助程式
description: 輔助程式
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 5df4856c7be31a75116d906320ae50cd5dc6a2dc
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 4%

---

# 輔助程式 {#gs-helpers}

## 預設回退值{#default-value}

的 `Default Fallback Value` 如果屬性為空或為null，則使用helper返回預設回退值。 此機制適用於配置檔案屬性和行程事件。

**語法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

在此示例中， `there` 的 `firstName` 此配置檔案的屬性為空或空。

## 條件{#if-function}

的 `if` helper用於定義條件塊。
如果表達式求值返回true，則呈現該塊，否則跳過該塊。

**語法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

遵循 `if` 幫助程式，可以輸入 `else` 語句，以指定要執行的代碼塊（如果相同條件為false）。
的 `elseif` 如果第一個語句返回false，則語句將指定要test的新條件。


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

1. **基於條件表達式呈現不同的儲存連結**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **確定電子郵件地址擴展**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **添加條件連結**

   以下操作將添加一個連結至「www.adobe.com/academia&#39;」網站（僅包含「.edu」電子郵件地址的配置檔案）、「www.adobe.com/org&#39;網站（包含「.org」電子郵件地址的配置檔案）和預設URL「www.adobe.com/users&#39;」（用於所有其他配置檔案）:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **基於段成員資格的條件內容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **確定配置檔案是否已是成員**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>要瞭解有關分段和分段服務的詳細資訊，請參閱此 [節](../../segment/about-segments.md)。


## 除非{#unless}

的 `unless` helper用於定義條件塊。 反對The `if`  helper，如果表達式計算返回false，則呈現該塊。

**語法**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**範例**

根據電子郵件地址擴展呈現某些內容：

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 每個{#each}

的 `each` 幫助程式用於在陣列上迭代。
幫助程式的語法為 ```{{#each ArrayName}}``` YourContent {{/each}}我們可以使用關鍵字引用各個陣列項 **這個** 在街區內。 可以使用{{@index}}呈現陣列元素的索引。

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

呈現此用戶在其購物車中擁有的產品清單：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 與{#with}

的 `with` helper用於更改template-part的評估令牌。

**語法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

的 `with` helper對於定義快捷方式變數也很有用。

**範例**

用於將長變數名稱與短變數名稱混用：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## 讓{#let}

的 `let` 函式允許將表達式儲存為變數，以便稍後在查詢中使用。

**語法**

```sql
{% let variable = expression %} {{variable}}
```

**範例**

以下示例允許以USD表示的交易記錄的所有產品合計，其合計大於$100且小於$1000。

```sql
{% let variable = expression %} {{variable}}
```
