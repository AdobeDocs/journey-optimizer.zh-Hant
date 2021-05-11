---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 7%

---

# 聚集函式{#aggregation}

![](../../assets/do-not-localize/badge.png)

聚合函式用於將[!DNL Profile Query Language](PQL)陣列中的多個值組合在一起，以形成單個摘要值。

## 計數

`count`函式返回給定陣列中的元素數。

**格式**

```sql
count({ARRAY})
```

**範例**

以下PQL查詢返回陣列中的訂單數。

```sql
count(orders)
```

## 總和

`sum`函式返回陣列中所有選定值的總和。

**格式**

```sql
sum({ARRAY})
```

**範例**

以下PQL查詢返回所有訂單價格的總和。

```sql
sum(orders.order.price)
```

## 平均

`average`函式會傳回陣列中所有選取值的算術平均值。

**格式**

```sql
average({ARRAY})
```

**範例**

以下PQL查詢返回所有訂單的平均價格。

```sql
average(orders.order.price)
```

## 最小

`min`函式返回陣列中所有選定值的最小值。

**格式**

```sql
min({ARRAY})
```

**範例**

以下PQL查詢返回所有訂單的最低價格。

```sql
min(orders.order.price)
```

## 最大

`max`函式返回陣列中所有選定值中最大的值。

**格式**

```sql
max({ARRAY})
```

**範例**

以下PQL查詢返回所有訂單的最高價格。

```sql
max(orders.order.price)
```
