---
title: 陣列函式庫
description: 陣列函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
TQID: https://experienceleague.adobe.com/CUiT5GFH9o4q-oOSWuKC8ZyLbRbH9lj88M92LhMIX9E
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5ecc28ec44a9c608f4fe5011e061cad62d92e2b
workflow-type: tm+mt
source-wordcount: 742
ht-degree: 4%

---

# 陣列和清單功能 {#arrays}

使用這些函式可讓與陣列、清單和字串的互動更容易。

## 只計算null {#count-only-null}

`countOnlyNull`函式用於計算清單中null值的數目。

**語法**

```sql
{%= countOnlyNull(array) %}
```

**範例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

傳回3。

## Null計數 {#count-with-null}

`countWithNull`函式用於計算包含null值的清單的所有元素。

**語法**

```sql
{%= countWithNull(array) %}
```

**範例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

傳回6。

## Distinct{#distinct}

`distinct`函式用於從移除重複值的陣列或清單中取得值。

**語法**

```sql
{%= distinct(array) %}
```

**範例**

下列作業會指定在多個商店下訂單的人員。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## Null的相異計數 {#distinct-count-with-null}

`distinctCountWithNull`函式用於計算清單中包括null值的不同值數目。

**語法**

```sql
{%= distinctCountWithNull(array) %}
```

**範例**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

傳回3。

## 第一個專案{#head}

`head`函式用來傳回陣列或清單中的第一個專案。

**語法**

```sql
{%= head(array) %}
```

**範例**

下列作業會傳回價格最高的前五個訂單中的第一個。 有關`topN`函式的詳細資訊可在陣列](#first-n)區段的[第一個`n`中找到。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 排序並取得陣列中的前N個 {#first-n}

`topN`函式根據給定的數值運算式以遞減順序排序陣列，並傳回前`N`個專案。 如果陣列大小小於`N`，則會傳回整個已排序陣列。

此函式
**語法**

```sql
{%= topN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 要排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的專案數。 |

**範例**

下列作業會傳回價格最低的前五個訂單。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

`in`函式是用來判斷專案是陣列或清單的成員。

**語法**

```sql
{%= in(value, array) %}
```

**範例**

下列作業會定義3月、6月或9月有生日的人員。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包含{#includes}

`includes`函式是用來判斷陣列或清單是否包含指定的專案。

**語法**

```sql
{%= includes(array,item) %}
```

**範例**

下列作業會定義哪些人最喜愛的顏色包括紅色。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 相交{#intersects}

`intersects`函式是用來判斷兩個陣列或清單是否至少有一個通用成員。

**語法**

```sql
{%= intersects(array1, array2) %}
```

**範例**

下列作業會定義哪些人最喜愛的顏色至少包括紅色、藍色或綠色之一。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!--
## Intersection{#intersection}

The `intersection` function is used to determine the common members of two arrays or lists.

**Syntax**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 排序並取得陣列中的最後N個 {#last-n}

`bottomN`函式根據給定的數值運算式以遞增順序排序陣列，並傳回前`N`個專案。 如果陣列大小小於`N`，則會傳回整個已排序陣列。

**語法**

```sql
{%= bottomN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 要排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的專案數。 |

**範例**

下列作業會傳回價格最高的前5個訂單。

```sql
{%= bottomN(orders,price, 5) %}
```

## 不在{#notin}

`notIn`函式是用來判斷專案是否不是陣列或清單的成員。

>[!NOTE]
>
>`notIn`函式&#x200B;*也*&#x200B;可確保這兩個值都不等於null。 因此，結果不是`in`函式的完全否定。

**語法**

```sql
{%= notIn(value, array) %}
```

**範例**

下列作業會定義非三月、六月或九月的人員生日。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集：{#subset}

`subsetOf`函式是用來判斷特定陣列（陣列A）是否是另一個陣列（陣列B）的子集。 換句話說，陣列A中的所有元素都是陣列B的元素。

**語法**

```sql
{%= subsetOf(array1, array2) %}
```

**範例**

下列作業會定義造訪過其所有最喜愛城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

`supersetOf`函式是用來判斷特定陣列（陣列A）是否是另一個陣列（陣列B）的超集。 換句話說，該陣列A包含陣列B中的所有元素。

**語法**

```sql
{%= supersetOf(array1, array2) %}
```

**範例**

下列作業會定義已吃過至少一次壽司和比薩的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"]) %}
```

## 反複處理陣列 {#each-loop}

使用Handlebars `{{#each}}`區塊協助程式來循環陣列並轉譯&#x200B;**個人化內容** （電子郵件、簡訊、推播）中每個專案的內容。

>[!NOTE]
>
>`{{#each}}`僅可在&#x200B;**個人化編輯器**&#x200B;中使用（電子郵件內文、簡訊、推播內容）。 歷程條件活動中不支援&#x200B;**1}。**&#x200B;若要篩選或比對歷程條件中陣列的專案，請改用[集合管理函式](../../building-journeys/expression/collection-management-functions.md)。

**語法**

```handlebars
{{#each arrayAttribute}}
  {{this}}
{{/each}}
```

+++範例 — 列出陣列中的所有專案

```handlebars
{{#each profile.purchases.items}}
  - {{this.name}}: {{this.price}}€
{{/each}}
```

輸出（範例）：

```
- Running shoes: 89€
- Water bottle: 15€
- Gym bag: 45€
```

+++

+++範例 — 存取回圈索引

使用`@index`存取目前的回圈位置（以0為基礎）：

```handlebars
{{#each profile.preferences.languages}}
  {{@index}}: {{this}}
{{/each}}
```

輸出（範例）：

```
0: English
1: French
2: Spanish
```

+++

+++範例 — 回圈內的條件式彩現

只有在符合條件時，才使用`{{#each}}`內的`{%#if%}`區塊來轉譯內容：

>[!NOTE]
>
>不支援`{% if %}` / `{% endif %}`。 請改用`{%#if%}` / `{%/if%}`。 此外，`this.<field>`在PQL條件運算式中無法運作 — 請使用屬性名稱（例如`order.status`）直接參照欄位。

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Your order {{order.id}} is still pending.
  {%/if%}
{{/each}}
```

這是模擬「條件中斷」的建議模式 — 只有符合條件的專案才會產生輸出。

+++
