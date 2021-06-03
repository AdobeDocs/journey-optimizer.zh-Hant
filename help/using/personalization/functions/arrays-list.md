---
title: 函式庫
description: 函式庫
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 5%

---

# 陣列和清單函式 {#arrays}

![](../../assets/do-not-localize/badge.png)

使用這些函式可讓您更輕鬆地與陣列、清單和字串互動。

## 不重複{#distinct}

`distinct`函式用於從陣列或清單中獲取值，並刪除重複值。

**格式**

```sql
{%= distinct(array) %}
```

**範例**

以下操作指定在多個儲存中下過訂單的人員。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## 第一項{#head}

`head`函式用於返回陣列或清單中的第一個項目。

**格式**

```sql
{%= head({array}) %}
```

**範例**

以下操作返回價格最高的前5個訂單中的第一個。 有關`topN`函式的更多資訊，請參閱陣列](#first-n)區段的[第一個`n`。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 陣列{#first-n}中的第一個`n`

當根據給定的數值表達式按升序排序時，`topN`函式用於返回陣列中的第一個`N`項。

**格式**

```sql
{%= topN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下操作將返回價格最高的前5個訂單。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

`in`函式用於確定項是否為陣列或清單的成員。

**格式**

```sql
{%= in(value, array) %}
```

**範例**

下列操作會以3月、6月或9月的生日來定義人員。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包含{#includes}

`includes`函式用於確定陣列或清單是否包含給定項。

**格式**

```sql
{%= includes(array,item) %}
```

**範例**

以下操作定義其喜愛的顏色包括紅色的人員。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 相交{#intersects}

`intersects`函式用於確定兩個陣列或清單是否至少具有一個公共成員。

**格式**

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

**Format**

```sql
intersection({ARRAY},{ARRAY})
```

**Example**

The following operation defines if person 1 and person 2 both have favorite colors of red, blue, and green.

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```
-->

## 陣列{#last-n}中的最後`n`

當根據給定的數值表達式按升序排序時，`bottomN`函式用於返回陣列中的最後`N`項。

**格式**

```sql
{%= bottomN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下操作返回價格最低的前5個訂單。

```sql
{%= bottomN(orders,price, 5) %}
```


## 不在{#notin}

`notIn`函式用於確定項目是否不是陣列或清單的成員。

>[!NOTE]
>
>`notIn`函式&#x200B;*also*&#x200B;確保兩個值均不等於null。 因此，結果並非`in`函式的完全否定。

**格式**

```sql
{%= notIn(value, array) %}
```

**範例**

下列操作會以不在3月、6月或9月的生日來定義人員。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集{#subset}

`subsetOf`函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的子集。 換句話說，陣列A中的所有元素都是陣列B的元素。

**格式**

```sql
{%= subsetOf(array1, array2) %}
```

**範例**

以下操作定義了訪問過他們所有喜愛城市的人。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

`supersetOf`函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的超集。 換句話說，陣列A包含陣列B中的所有元素。

**格式**

```sql
{%= supersetOf(array1, array2) %}
```

**範例**

以下操作將定義至少吃過壽司和披薩的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```







