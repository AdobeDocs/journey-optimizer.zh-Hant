---
title: 算術函式庫
description: 算術函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 21ef8f50-8389-4675-a8e5-0438a3eee592
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 7%

---

# 算術函式 {#maths}

算術函式用於對值執行基本計算。

## 新增{#add}

此 `+` (addition)函式可用來尋找兩個引數運算式的總和。

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

此 `*` （乘法）函式用於查找兩個參數表達式的乘積。

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

此 `-` （減法）函式用於尋找兩個引數運算式的差異。

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

此 `/` （除法）函式用於求兩個參數表達式的商。

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

此 `%` (modulo/remaind)函式用於在將兩個參數表達式除以後查找余數。

**格式**

```sql
{%= double % double %}
```

**範例**

下列操作會檢查人員的年齡是否可除以5。

```sql
{%= person.age % 5 = 0 %}
```
