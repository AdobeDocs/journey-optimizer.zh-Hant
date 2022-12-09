---
title: 數學函式庫
description: 數學函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# 數學函式 {#math}

了解如何在運算式編輯器中使用數學函式。

## 絕對 {#absolute}

此 `absolute` 函式用來轉換數字的絕對值。

**格式**

```sql
{%= absolute(int) %}: int
```

## 隨機 {#random}

此 `random` 函式可用來傳回0到1之間的隨機值。

**格式**

```sql
{%= random() %}: double
```

## 向下捨入 {#round-down}

此 `roundDown` 函式來捨入數字。

**格式**

```sql
{%= roundDown(double) %}: double
```

## 向上 {#round-up}

此 `Count only null` 函式會將數字捨入。

**格式**

```sql
{%= roundUp(double) %}: double
```

## 結束百分比 {#to-percentage}

此 `toPercentage` 函式將數字轉換為百分比。

**格式**

```sql
{%= toPercentage(double) %}: string
```

## 精準 {#to-precision}

此 `toPrecision` 函式將數字轉換為所需的精度。

**格式**

```sql
{%= toPrecision(double,int) %}: string
```
