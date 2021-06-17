---
title: Helpers
description: Helpers
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 4%

---


# Helpers {#gs-helpers}

## 條件{#if-function}

`if`幫助程式用於定義條件塊。
如果運算式評估傳回true，則會轉譯區塊，否則會跳過該區塊。

**語法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在`if`幫助程式之後，如果相同的條件為false，您可以輸入`else`陳述式來指定要執行的代碼塊。
`elseif`陳述式將指定新條件以測試第一個陳述式是否傳回false。


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

   以下操作將僅將具有&#39;.edu&#39;電子郵件地址的設定檔的連結新增至&#39;www.adobe.com/academia&#39;網站，將具有&#39;.org&#39;電子郵件地址的設定檔的連結新增至&#39;www.adobe.com/org&#39;網站，並將所有其他設定檔的預設URL &#39;www.adobe.com/users&#39;:

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
>若要進一步了解分段和分段服務，請參閱此[區段](../../segment/about-segments.md)。


## 除非{#unless}

`unless`幫助程式用於定義條件塊。 與`if`協助程式相對，如果運算式評估傳回false，則會轉譯區塊。

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

`each`幫助程式用於迭代陣列。
協助程式的語法為```{{#each ArrayName}}``` YourContent {{/each}}
我們可以使用區塊內的關鍵字**this**&#x200B;來參照個別陣列項目。 可使用{{@index}}呈現陣列元素的索引。

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

`with`幫助程式用於更改template-part的評估令牌。

**語法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with`協助程式對於定義快捷方式變數也很有用。

**範例**

使用，將長變數名稱與短變數名稱混用：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## 讓{#let}

`let`函式允許將表達式儲存為變數，以便稍後在查詢中使用。

**語法**

```sql
{% let variable = expression %} {{variable}}
```

**範例**

以下示例允許以美元表示的交易的所有產品總和，其中總和大於$100且小於$1000。

```sql
{% let variable = expression %} {{variable}}
```
