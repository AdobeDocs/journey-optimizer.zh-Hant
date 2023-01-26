---
title: 數學函式庫
description: 數學函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
source-git-commit: dc313d7cbee9e412b9294b644fddbc7840f90339
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# 數學函式 {#math}

了解如何在運算式編輯器中使用數學函式。

## 絕對 {#absolute}

此 `absolute` 函式用來轉換數字的絕對值。

**語法**

```sql
{%= absolute(int) %}: int
```

## formatNumber {#format-number}

此 `formatNumber` 函式用於將任何數字格式化為其語言敏感表示。

它接受表示區域設定的數字和字串，並返回所需區域設定中數字的格式化字串。

**語法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用格式設定和有效的地區設定，如 [Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的地區設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**範例**

此查詢返回與123456.789對應的阿拉伯文格式字串作為輸入數字。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

此 `random` 函式可用來傳回0到1之間的隨機值。

**語法**

```sql
{%= random() %}: double
```

## 向下捨入 {#round-down}

此 `roundDown` 函式來捨入數字。

**語法**

```sql
{%= roundDown(double) %}: double
```

## 向上 {#round-up}

此 `Count only null` 函式會將數字捨入。

**語法**

```sql
{%= roundUp(double) %}: double
```

## 到十六進位字串 {#to-hex-string}

此 `toHexString` 函式將任何數字轉換為十六進位字串。

**語法**

```sql
{%= toHexString(number) %}: string
```

**範例**

此查詢返回十六進位值158，即9e。

```sql
{%= toHexString(158) %}
```

## 結束百分比 {#to-percentage}

此 `toPercentage` 函式將數字轉換為百分比。

**語法**

```sql
{%= toPercentage(double) %}: string
```

## 精準 {#to-precision}

此 `toPrecision` 函式將數字轉換為所需的精度。

**語法**

```sql
{%= toPrecision(double,int) %}: string
```

## 至字串 {#to-string}

此 **toString** 函式會將任何數字轉換為其字串表示。

**語法**

```sql
{%= toString(string) %}: string
```

**範例**

此查詢會傳回「12」。

```sql
{%= toString(12) %} 
```
