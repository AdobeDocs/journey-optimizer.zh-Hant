---
title: 算術函式庫
description: 算術函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 7%

---

# 算術函式 {#maths}

算術函式用於對值執行基本計算。

## 新增{#add}

`+`（加法）函式用於查找兩個參數表達式的總和。

**格式**

```sql
{%= double + double %}
```

**範例**

以下操作將加總兩種不同產品的價格。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

`*`（乘法）函式用於查找兩個參數表達式的乘積。

**格式**

```sql
{%= double * double %}
```

**範例**

以下操作將查找庫存產品和產品價格，以查找產品的總值。

```sql
{%= product.inventory * product.price %}
```

## 減去{#substract}

`-`（減法）函式用於查找兩個參數表達式的差異。

**格式**

```sql
{%= double - double %}
```

**範例**

以下操作將查找兩個不同產品之間的價格差異。

```sql
{%= product1.price - product2.price %}
```

## 除{#divide}

`/`（除法）函式用於查找兩個參數表達式的商。

**格式**

```sql
{%= double / double %}
```

**範例**

以下操作將查找銷售的產品總數與收入總額之間的商，以查看每項的平均成本。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 余數{#remainder}

`%`（模數/余數）函式用於在將兩個參數表達式除以後查找余數。

**格式**

```sql
{%= double % double %}
```

**範例**

下列操作會檢查人員的年齡是否可除以5。

```sql
{%= person.age % 5 = 0 %}
```
