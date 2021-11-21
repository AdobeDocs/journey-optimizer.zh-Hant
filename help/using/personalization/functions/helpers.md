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

## 預設後援值{#default-value}

此 `Default Fallback Value` 如果屬性為空或null，則使用helper返回預設的回退值。 此機制適用於設定檔屬性和歷程事件。

**語法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: 'there' %}!
```

在此範例中，值 `there` 若 `firstName` 此配置檔案的屬性為空或null。

## 條件{#if-function}

此 `if` Helper用於定義條件塊。
如果運算式評估傳回true，則會轉譯區塊，否則會跳過該區塊。

**語法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

遵循 `if` 幫手，你可以輸入 `else` 語句，指定要執行的代碼塊（如果相同條件為false）。
此 `elseif` 語句將指定一個新條件以測試第一個語句是否返回false。


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

1. **根據條件運算式呈現不同的商店連結**

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

1. **新增條件式連結**

   以下操作將僅將具有「.edu」電子郵件地址的配置檔案的「www.adobe.com/academia&#39;網站」、具有「.org」電子郵件地址的配置檔案的「www.adobe.com/org&#39;網站」以及所有其他配置檔案的預設URL「www.adobe.com/users&#39;」添加連結：

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **根據區段成員資格的條件式內容**

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
>若要進一步了解分段和分段服務，請參閱 [節](../../segment/about-segments.md).


## 除非{#unless}

此 `unless` Helper用於定義條件塊。 由反對 `if`  helper，如果運算式評估傳回false，則會轉譯區塊。

**語法**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**範例**

根據電子郵件地址擴充功能呈現部分內容：

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## 每個{#each}

此 `each` helper可用來迭代運算陣列。
協助程式的語法為 ```{{#each ArrayName}}``` YourContent {{/each}}我們可以使用關鍵字來參照個別陣列項目 **此** 在街區裡。 可使用{{@index}}呈現陣列元素的索引。

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

呈現此使用者購物車中的產品清單：

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## 使用{#with}

此 `with` helper可用來變更template-part的評估令牌。

**語法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

此 `with` 協助程式對於定義快速鍵變數也很實用。

**範例**

使用，將長變數名稱與短變數名稱混用：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## 讓{#let}

此 `let` 函式可讓運算式儲存為變數，以供稍後在查詢中使用。

**語法**

```sql
{% let variable = expression %} {{variable}}
```

**範例**

以下示例允許以美元表示的交易的所有產品總和，其中總和大於$100且小於$1000。

```sql
{% let variable = expression %} {{variable}}
```
