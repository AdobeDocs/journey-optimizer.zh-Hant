---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 5%

---

# 陣列和清單函式{#arrays}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)提供的功能可讓與陣列、清單和字串的交互更輕鬆。

## 在

`in`函式用於確定項目是否是陣列或清單的成員。

**格式**

```sql
in ({VALUE},{ARRAY})
```

**範例**

以下PQL查詢定義了3月、6月或9月的生日。

```sql
in (person.birthMonth, [3, 6, 9])
```

## 不在

`notIn`函式用於確定項目是否不是陣列或清單的成員。

>[!NOTE]
>
>`notIn`函式&#x200B;*allo*&#x200B;可確保兩個值均不等於null。 因此，結果不是對`in`函式的完全否定。

**格式**

```sql
notIn ({VALUE},{ARRAY})
```

**範例**

以下PQL查詢定義人們的生日不是在3月、6月或9月。

```sql
notIn (person.birthMonth ,[3, 6, 9])
```

## Intercests

`intersects`函式用於確定兩個陣列或清單是否具有至少一個公共成員。

**格式**

```sql
intersects({ARRAY},{ARRAY})
```

**範例**

以下PQL查詢定義了喜愛的顏色至少包含紅色、藍色或綠色之一的人。

```sql
intersects(person.favoriteColors,["red", "blue", "green"])
```

## 交集

`intersection`函式用於確定兩個陣列或清單的公共成員。

**格式**

```sql
intersection({ARRAY},{ARRAY})
```

**範例**

以下PQL查詢定義人員1和人員2是否都具有紅色、藍色和綠色的收藏夾顏色。

```sql
intersection(person1.favoriteColors,person2.favoriteColors) = ["red", "blue", "green"]
```

## 子集

`subsetOf`函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的子集。 換言之，陣列A中的所有元素都是陣列B的元素。

**格式**

```sql
subsetOf({ARRAY},{ARRAY})
```

**範例**

以下PQL查詢定義已訪問其所有最愛城市的訪客。

```sql
subsetOf(person.favoriteCities,person.visitedCities)
```

## 超集

`supersetOf`函式用於確定特定陣列（陣列A）是否是另一陣列（陣列B）的超集。 換言之，陣列A包含陣列B中的所有元素。

**格式**

```sql
supersetOf({ARRAY},{ARRAY})
```

**範例**

以下PQL查詢定義至少吃過壽司和披薩的人。

```sql
supersetOf(person.eatenFoods,["sushi", "pizza"])
```

## 包含

`includes`函式用於確定陣列或清單是否包含給定項。

**格式**

```sql
includes({ARRAY},{ITEM})
```

**範例**

以下PQL查詢定義其收藏夾顏色包含紅色的人。

```sql
includes(person.favoriteColors,"red")
```

## Distinct

`distinct`函式用於從陣列或清單中刪除重複值。

**格式**

```sql
distinct({ARRAY})
```

**範例**

以下PQL查詢指定在多個儲存中下了訂單的人員。

```sql
distinct(person.orders.storeId).count() > 1
```

## 陣列{#first-n}中第一個`n`

`topN`函式用於根據給定的數值表達式按升序排序時，返回陣列中的第一個`N`項。

**格式**

```sql
topN({ARRAY},{VALUE}, {AMOUNT})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下PQL查詢返回價格最高的前5個訂單。

```sql
topN(orders,price, 5)
```

## 陣列中最後一個`n`

`bottomN`函式用於根據給定的數值表達式按升序排序時，返回陣列中最後一個`N`項。

**格式**

```sql
bottomN({ARRAY},{VALUE}, {AMOUNT})
```

| 引數 | 說明 |
| --------- | ----------- | 
| `{ARRAY}` | 要排序的陣列或清單。 |
| `{VALUE}` | 排序陣列或清單的屬性。 |
| `{AMOUNT}` | 要傳回的項目數。 |

**範例**

以下PQL查詢返回價格最低的前5個訂單。

```sql
bottomN(orders,price, 5)
```

## 第一項

`head`函式用於返回陣列或清單中的第一個項目。

**格式**

```sql
head({ARRAY})
```

**範例**

以下PQL查詢返回價格最高的前5個訂單中的第一個。 有關`topN`函式的更多資訊，請參閱array](#first-n)部分的[first `n`。

```sql
head(topN(orders,price, 5))
```
