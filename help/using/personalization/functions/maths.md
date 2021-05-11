---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---

# 數學函式{#math}

![](../../assets/do-not-localize/badge.png)

算術函式用於對[!DNL Profile Query Language](PQL)中的值執行基本計算。

## 新增

`+`（加法）函式用於查找兩個引數表達式的總和。

**格式**

```sql
{NUMBER} + {NUMBER}
```

**範例**

以下PQL查詢總結了兩個不同產品的價格。

```sql
product1.price + product2.price
```

## 乘

`*`（乘法）函式用於查找兩個參數表達式的乘積。

**格式**

```sql
{NUMBER} * {NUMBER}
```

**範例**

以下PQL查詢可查找庫存的產品和產品價格，以查找產品的總值。

```sql
product.inventory * product.price
```

## 去除

`-`（減法）函式用於查找兩個參數表達式的差。

**格式**

```sql
{NUMBER} - {NUMBER}
```

**範例**

以下PQL查詢可查找兩個不同產品之間的價格差異。

```sql
product1.price - product2.price
```

## 除法

`/`（除法）函式用於查找兩個引數表達式的商。

**格式**

```sql
{NUMBER} / {NUMBER}
```

**範例**

以下PQL查詢會查找售出產品總數與收入總額之間的商數，以查看每個項目的平均成本。

```sql
totalProduct.price / totalProduct.sold
```

## 剩餘

`%`(modulo/remainder)函式用於在將兩個引數表達式除以後查找余數。

**格式**

```sql
{NUMBER} % {NUMBER}
```

**範例**

以下PQL查詢會檢查人員的年齡是否可除以5。

```sql
person.age % 5 = 0
```
