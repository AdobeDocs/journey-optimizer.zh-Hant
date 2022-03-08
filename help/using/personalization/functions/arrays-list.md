---
title: 陣列函式館
description: 陣列函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 5%

---

# 陣列和清單功能 {#arrays}

使用這些函式可使與陣列、清單和字串的交互更容易。

## 獨特{#distinct}

的 `distinct` 函式用於從刪除重複值的陣列或清單中獲取值。

**格式**

```sql
{%= distinct(array) %}
```

**範例**

以下操作指定在多個商店中下訂單的人員。

```sql
{%= distinct(person.orders.storeId).count() > 1 %}
```

## 第一項{#head}

的 `head` 函式用於返回陣列或清單中的第一項。

**格式**

```sql
{%= head({array}) %}
```

**範例**

以下操作返回價格最高的前五個訂單中的第一個。 有關 `topN` 函式 [第一 `n` 在陣列中](#first-n) 的子菜單。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 第一個 `n` 在陣列中 {#first-n}

的 `topN` 函式用於返回第一個 `N` 陣列中的項，根據給定的數值表達式按升序排序。

**格式**

```sql
{%= topN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 對陣列或清單進行排序的屬性。 |
| `{AMOUNT}` | 要返回的項數。 |

**範例**

以下操作返回價格最高的前五個訂單。

```sql
{%= topN(orders,price, 5) %}
```

## 在{#in}

的 `in` 函式用於確定項目是否是陣列或清單的成員。

**格式**

```sql
{%= in(value, array) %}
```

**範例**

以下操作定義3月、6月或9月的人生日。

```sql
{%= in (person.birthMonth, [3, 6, 9]) %}
```

## 包括{#includes}

的 `includes` 函式用於確定陣列或清單是否包含給定項。

**格式**

```sql
{%= includes(array,item) %}
```

**範例**

以下操作定義其喜愛顏色包括紅色的人。

```sql
{%= includes(person.favoriteColors,"red") %}
```

## 交叉{#intersects}

的 `intersects` 函式用於確定兩個陣列或清單是否具有至少一個公共成員。

**格式**

```sql
{%= intersects(array1, array2) %}
```

**範例**

以下操作定義其喜愛的顏色至少包括紅色、藍色或綠色之一的人。

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

## 最後 `n` 在陣列中{#last-n}

的 `bottomN` 函式用於返回最後一個 `N` 陣列中的項，根據給定的數值表達式按升序排序。

**格式**

```sql
{%= bottomN(array, value, amount) %}
```

| 引數 | 說明 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 對陣列或清單進行排序的屬性。 |
| `{AMOUNT}` | 要返回的項數。 |

**範例**

以下操作將返回價格最低的前五個訂單。

```sql
{%= bottomN(orders,price, 5) %}
```


## 不在{#notin}

的 `notIn` 函式用於確定項目是否不是陣列或清單的成員。

>[!NOTE]
>
>的 `notIn` 函式 *也* 確保兩個值均不等於null。 因此，結果不是對 `in` 的子菜單。

**格式**

```sql
{%= notIn(value, array) %}
```

**範例**

以下操作定義生日不在三月、六月或九月的人。

```sql
{%= notIn(person.birthMonth ,[3, 6, 9]) %}
```


## 子集{#subset}

的 `subsetOf` 函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的子集。 換句話說，陣列A中的所有元素都是陣列B的元素。

**格式**

```sql
{%= subsetOf(array1, array2) %}
```

**範例**

以下操作定義訪問了所有其喜愛城市的人員。

```sql
{%= subsetOf(person.favoriteCities,person.visitedCities) %}
```

## 超集{#superset}

的 `supersetOf` 函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的超集。 換句話說，陣列A包含陣列B中的所有元素。

**格式**

```sql
{%= supersetOf(array1, array2) %}
```

**範例**

以下操作定義了至少吃過一次壽司和披薩的人。

```sql
{%= supersetOf(person.eatenFoods,["sushi", "pizza"] %}
```
