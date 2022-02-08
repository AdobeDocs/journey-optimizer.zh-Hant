---
title: 算術函式館
description: 算術函式館
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

的 `+` (addition)函式用於查找兩個參數表達式的和。

**格式**

```sql
{%= double + double %}
```

**範例**

以下操作將計算兩個不同產品的價格。

```sql
{%= product1.price + product2.price %}
```

## 乘{#multiply}

的 `*` （乘法）函式用於查找兩個參數表達式的乘積。

**格式**

```sql
{%= double * double %}
```

**範例**

以下操作將查找庫存產品和產品價格，以查找產品的總價值。

```sql
{%= product.inventory * product.price %}
```

## 減{#substract}

的 `-` （減法）函式用於查找兩個參數表達式的差。

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

的 `/` （除法）函式用於求兩個參數表達式的商。

**格式**

```sql
{%= double / double %}
```

**範例**

以下操作將查找已銷售產品總數與查看每個物料的平均成本所得總金額之間的商數。

```sql
{%= totalProduct.price / totalProduct.sold %}
```

## 余數{#remainder}

的 `%` (modulo/remainder)函式用於在分割兩個參數表達式後查找余數。

**格式**

```sql
{%= double % double %}
```

**範例**

以下操作將檢查人員的年齡是否可被5除。

```sql
{%= person.age % 5 = 0 %}
```
