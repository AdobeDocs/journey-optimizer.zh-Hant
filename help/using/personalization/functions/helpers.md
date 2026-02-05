---
title: 輔助程式
description: 輔助程式
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: dc417c88021bdb042d7a600ee13a7cbab0ceeb4a
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 5%

---

# 輔助程式 {#gs-helpers}

## 預設遞補值{#default-value}

如果屬性為空白或null，則會使用`Default Fallback Value`協助程式傳回預裝置援值。 此機制適用於設定檔屬性和歷程事件。

**語法**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

在此範例中，如果此設定檔的`there`屬性為空白或Null，則會顯示值`firstName`。

## 條件{#if-function}

`if`協助程式用於定義條件區塊。
如果運算式評估傳回true，則會轉譯區塊，否則會略過該區塊。

**語法**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

在`if`協助程式之後，您可以輸入`else`陳述式，以指定要執行的程式碼區塊（如果相同條件為false）。
`elseif`陳述式將指定新條件來測試第一個陳述式是否傳回false。


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

1. **根據條件運算式演算不同的存放區連結**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
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

1. **以對象成員資格為基礎的條件式內容**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>若要深入瞭解對象和細分服務，請參閱[本節](../../audience/about-audiences.md)。


## Unless{#unless}

`unless`協助程式用於定義條件區塊。 藉由與`if`協助程式相對，如果運算式評估傳回false，則會轉譯區塊。

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
Some edu specific content
{%/unless%}
```

## 每個{#each}

`each`協助程式是用來反複處理陣列。
協助程式的語法為```{{#each ArrayName}}``` YourContent `{{/each}}`
我們可以在區塊內使用關鍵字**this**&#x200B;來參照個別陣列專案。 可以使用`{{@index}}`轉譯陣列專案的索引。

**語法**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
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
{{/each}}
```

>[!NOTE]
>
>您也可以使用`each`協助程式來反複處理自訂動作回應傳回的陣列。 如需從自訂動作回應反複處理巢狀陣列的範例，請參閱[在原生通道中使用自訂動作回應](../../action/action-response.md#response-in-channels)。

## 替換為{#with}

`with`協助程式可用來變更範本部分的評估權杖。

**語法**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

`with`協助程式也可用來定義捷徑變數。

**範例**

搭配使用，將長變數名稱等同為短變數名稱：

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

`let`函式允許將運算式儲存為變數，以便稍後在查詢中使用。

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

## 執行中繼資料 {#execution-metadata}

>[!AVAILABILITY]
>
>此功能為有限可用性。請聯絡您的 Adobe 代表以取得存取權。

`executionMetadata`協助程式允許動態擷取自訂索引鍵值配對，並將其儲存到訊息執行內容中。

**語法**

```
{{executionMetadata key="your_key" value="your_value"}}
```

在此語法中，`key`參考中繼資料名稱，而`value`是要儲存的中繼資料。

**使用案例**

透過此功能，您可以將內容相關資訊附加至行銷活動或歷程中的任何原生動作。 這可讓您將即時傳遞內容資料匯出至外部系統，用於各種用途，例如追蹤、分析、個人化和下游處理。

>[!NOTE]
>
>[自訂動作](../../action/action.md)不支援執行中繼資料函式。

例如，您可以使用執行中繼資料協助程式，將特定ID附加至每個傳送至設定檔的每個傳送。 此資訊會在執行階段產生，然後可匯出擴充的執行中繼資料，以供與外部報告平台進行下游調解。

**運作方式**

從行銷活動或歷程內的管道內容中選取任何元素，並使用個人化編輯器將`executionMetadata`協助程式新增至此元素。

>[!NOTE]
>
>顯示內容本身時，不會顯示執行中繼資料函式。


在執行階段中，中繼資料值新增至現有的&#x200B;**[!UICONTROL 訊息回饋事件資料集]**，並加入下列結構描述：

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>在[本節](../../data/get-started-datasets.md)中進一步瞭解資料集。

**限制**

每個動作的機碼值組有2kb的上限。 如果超過2Kb限制，訊息仍會傳送，但任何索引鍵值配對都可能遭截斷。

系統不會為動作中排除的設定檔擷取中繼資料。 當設定檔被排除而無法接收訊息時，資料集中不會為該設定檔建立中繼資料專案。

**範例**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

在此範例中，假設`profile.person.name.firstName` = &quot;Alex&quot;，則產生的實體為：

```
{
  "key": "firstName",
  "value": "Alex"
}
```

