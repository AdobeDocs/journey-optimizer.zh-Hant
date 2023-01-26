---
title: 陣列函式庫
description: 陣列函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 6%

---

# 陣列和清單功能 {#arrays}

使用這些函式可讓您更輕鬆地與陣列、清單和字串互動。

## 僅計數null {#count-only-null}

此 `countOnlyNull` 函式來計算清單中空值的數量。

**語法**

```sql
{%= countOnlyNull(array) %}
```

**範例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回3。

## 計數為空 {#count-with-null}

此 `countWithNull` 函式來計算清單中的所有元素，包括null值。

**語法**

```sql
{%= countWithNull(array) %}
```

**範例**

```sql
{%= countOnlyNull([4,0,1,6,0,0]) %}
```

返回6。

## 不重複{#distinct}

此 `distinct` 函式可用來從陣列或清單中取得值，並移除重複值。

**語法**

```sql
{%= distinct(array) %}
```

**範例**

以下操作指定在多個儲存中下過訂單的人員。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## 包含Null的不重複計數 {#distinct-count-with-null}

此 `distinctCountWithNull` 函式來計算清單中包含空值的不同值數目。

**語法**

```sql
{%= distinctCountWithNull(array) %}
```

**範例**

```sql
{%= distinctCountWithNull([10,2,10,null]) %}
```

返回3。

## 第一項{#head}

此 `head` 函式可用來傳回陣列或清單中的第一個項目。

**語法**

```sql
{%= head(array) %}
```

**範例**

以下操作返回價格最高的前5個訂單中的第一個。 有關 `topN` 函式 [first `n` 陣列](#first-n) 區段。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 第一個 `n` 陣列 {#first-n}

此 `topN` 函式來傳回第一個 `N` 陣列中的項目，根據指定的數值運算式以升序排序。

**語法**

```sql
{%= topN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下操作將返回價格最低的前5個訂單。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

此 `in` 函式用於確定項是否為陣列或清單的成員。

**語法**

```sql
{%= in(value, array) %}
```

**範例**

下列操作會以3月、6月或9月的生日來定義人員。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包含{#includes}

此 `includes` 函式來判斷陣列或清單是否包含指定項目。

**語法**

```sql
{%= includes(array,item) %}
```

**範例**

以下操作定義其喜愛的顏色包括紅色的人員。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 相交{#intersects}

此 `intersects` 函式用於確定兩個陣列或清單是否具有至少一個公共成員。

**語法**

```sql
{%= intersects(array1, array2) %}
```

**範例**

以下操作定義其最喜愛的顏色至少包括紅色、藍色或綠色之一的人。

```sql
{%= intersects(person.favoriteColors,["red", "blue", "green"]) %}
```


<!-- ## Intersection{#intersection}

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

## 上次 `n` 陣列{#last-n}

此 `bottomN` 函式來傳回最後一個 `N` 陣列中的項目，根據指定的數值運算式以升序排序。

**語法**

```sql
{%= bottomN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下操作將返回價格最高的最後5個訂單。

```sql
{%= bottomN(orders,price, 5) %}
```

## 不在{#notin}

此 `notIn` 函式用於確定項目是否不是陣列或清單的成員。

>[!NOTE]
>
>此 `notIn` 函式 *an* 確保兩個值均不等於null。 因此，結果並非對 `in` 函式。

**語法**

```sql
{%= notIn(value, array) %}
```

**範例**

下列操作會以不在3月、6月或9月的生日來定義人員。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集{#subset}

此 `subsetOf` 函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的子集。 換句話說，陣列A中的所有元素都是陣列B的元素。

**語法**

```sql
{%= subsetOf(array1, array2) %}
```

**範例**

以下操作定義了訪問過他們所有喜愛城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

此 `supersetOf` 函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的超集。 換句話說，陣列A包含陣列B中的所有元素。

**語法**

```sql
{%= supersetOf(array1, array2) %}
```

**範例**

以下操作將定義至少吃過壽司和披薩的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
