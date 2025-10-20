---
title: 陣列函式庫
description: 陣列函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: dfe611fb-9c50-473c-9eb7-b983e1e6f01e
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 6%

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

下列作業會傳回價格最高的前五個訂單中的第一個。 有關`topN`函式的詳細資訊可在陣列[區段的`n`第一個](#first-n)中找到。

```sql
{%= head(topN(orders,price, 5)) %}
```

## 陣列中的前`n` {#first-n}

當根據給定的數值運算式依遞增順序排序時，`topN`函式用來傳回陣列中的前`N`個專案。

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

## 陣列中的最後`n`{#last-n}

當根據給定的數值運算式依遞增順序排序時，`bottomN`函式用於傳回陣列中的最後`N`個專案。

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
