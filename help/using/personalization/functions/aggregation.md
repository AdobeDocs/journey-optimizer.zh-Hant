---
title: 聚合函式庫
description: 聚合函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 8%

---

# 聚合函式 {#aggregation}

匯總函式用於將多個值組合在一起，以形成單個匯總值。

## 計數{#count}

此 `count` 函式會傳回指定陣列中的元素數。

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

此 `sum` 函式會傳回陣列內所有選取值的總和。

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

此 `average` 函式返回陣列內所有選定值的算術平均值。

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

此 `min` 函式會傳回陣列中所有選取值的最小值。

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

此 `max` 函式會傳回陣列中所有選取值中最大的值。

**格式**

```sql
{%= max(array) %}
```

**範例**

以下操作返回所有訂單的最高價格。

```sql
{%=max(orders.order.price)%}
```
