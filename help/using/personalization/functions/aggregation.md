---
title: 聚合函式庫
description: 聚合函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 9%

---

# 聚合函式 {#aggregation}

匯總函式用於將多個值組合在一起，以形成單個匯總值。

## 計數{#count}

`count`函式返回給定陣列內的元素數。

**格式**

```sql
{%= count(array) %}
```

**範例**

以下操作返回陣列中的訂單數。

```sql
{%= count(orders) %}
```

## 總和{#sum}

`sum`函式返回陣列內所有選定值的總和。

**格式**

```sql
{%= sum(array) %}
```

**範例**

以下操作返回所有訂單價格的總和。

```sql
{%=sum(orders.order.price)%}
```

## 平均{#average}

`average`函式返回陣列內所有選定值的算術平均值。

**格式**

```sql
{%= average(array) %}
```

**範例**

以下操作返回所有訂單的平均價格。

```sql
{%=average(orders.order.price)%}
```

## 最小{#min}

`min`函式返回陣列內所有選定值的最小值。

**格式**

```sql
{%= min(array) %}
```

**範例**

以下操作返回所有訂單的最低價格。

```sql
{%=min(orders.order.price)%}
```

## 最大{#max}

`max`函式返回陣列內所有選定值中最大的值。

**格式**

```sql
{%= max(array) %}
```

**範例**

以下操作返回所有訂單的最高價格。

```sql
{%=max(orders.order.price)%}
```
