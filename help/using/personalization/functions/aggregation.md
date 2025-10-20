---
title: 彙總函式庫
description: 彙總函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: a029f716-ea1e-4d79-82b7-59770f05161b
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---

# 彙總函式 {#aggregation}

彙總函式用於將多個值分組在一起，以形成單一摘要值。

## 平均{#average}

`average`函式傳回陣列中所有選取值的算術平均值。

**語法**

```sql
{%= average(array) %}
```

**範例**

下列作業會傳回所有訂單的平均價格。

```sql
{%=average(orders.order.price)%}
```

## Count{#count}

`count`函式傳回指定陣列中的元素數目。

**語法**

```sql
{%= count(array) %}
```

**範例**

下列作業會傳回陣列中的訂單數。

```sql
{%= count(orders) %}
```

## 最大值{#max}

`max`函式傳回陣列中所有選取值的最大值。

**語法**

```sql
{%= max(array) %}
```

**範例**

下列作業會傳回所有訂單的最高價格。

```sql
{%=max(orders.order.price)%}
```

## 最小值{#min}

`min`函式傳回陣列中所有選取值的最小值。

**語法**

```sql
{%= min(array) %}
```

**範例**

下列作業會傳回所有訂單的最低價格。

```sql
{%=min(orders.order.price) %}
```

## Sum{#sum}

`sum`函式傳回陣列中所有選取值的總和。

**語法**

```sql
{%= sum(array) %}
```

**範例**

下列作業會傳回所有訂單價格的總和。

```sql
{%=sum(orders.order.price)%}
```
