---
title: 數學函式館
description: 數學函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 8%

---

# 數學函式 {#math}

瞭解如何在表達式編輯器中使用數學函式。

## 絕對 {#absolute}

的 `absolute` 函式用於轉換其絕對值的數字。

**格式**

```sql
{%= absolute(int) %}: int
```

## Random {#random}

的 `random` 函式用於返回介於0和1之間的隨機值。

**格式**

```sql
{%= random() %}: double
```

## 向下 {#round-down}

的 `roundDown` 函式用於捨入數字。

**格式**

```sql
{%= roundDown(double) %}: double
```

## 向上捨入 {#round-up}

的 `Count only null` 函式用於捨入數字。

**格式**

```sql
{%= roundUp(double) %}: double
```

## 至百分比 {#to-percentage}

的 `toPercentage` 函式將數字轉換為百分比。

**格式**

```sql
{%= toPercentage(double) %}: string
```

## 到精度 {#to-precision}

的 `toPrecision` 函式用於將數字轉換為所需的精度。

**格式**

```sql
{%= toPrecision(double,int) %}: string
```
