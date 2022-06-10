---
title: 聚合函式館
description: 聚合函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 284d95976ab1b58aaea2a4c41db20a3ea5a9b761
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 8%

---

# 聚合函式 {#aggregation}

聚合函式用於將多個值組合在一起，以形成單個匯總值。

## 平均{#average}

的 `average` 函式返回陣列中所有選定值的算術平均值。

**格式**

```sql
{%= average(array) %}
```

**範例**

以下操作返回所有訂單的平均價格。

```sql
{%=average(orders.order.price)%}
```

## 計數{#count}

的 `count` 函式返回給定陣列中的元素數。

**格式**

```sql
{%= count(array) %}
```

**範例**

以下操作返回陣列中的訂單數。

```sql
{%= count(orders) %}
```

## 最大{#max}

的 `max` 函式返回陣列中所有選定值中的最大值。

**格式**

```sql
{%= max(array) %}
```

**範例**

以下操作返回所有訂單的最高價格。

```sql
{%=max(orders.order.price)%}
```

## 最小{#min}

的 `min` 函式返回陣列中所有選定值中最小的值。

**格式**

```sql
{%= min(array) %}
```

**範例**

以下操作返回所有訂單的最低價格。

```sql
{%=min(orders.order.price) %}
```

## 和{#sum}

的 `sum` 函式返回陣列中所有選定值的總和。

**格式**

```sql
{%= sum(array) %}
```

**範例**

以下操作返回所有訂單價格之和。

```sql
{%=sum(orders.order.price)%}
```
