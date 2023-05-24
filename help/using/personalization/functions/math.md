---
title: 數學函式館
description: 數學函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 6%

---

# 數學函式 {#math}

瞭解如何在表達式編輯器中使用數學函式。

## 絕對 {#absolute}

的 `absolute` 函式用於轉換其絕對值的數字。

**語法**

```sql
{%= absolute(int) %}: int
```

## 格式編號 {#format-number}

的 `formatNumber` 函式用於將任何數字格式化為其語言敏感表示。

它接受表示區域設定的數字和字串，並返回所需區域設定中數字的格式化字串。

**語法**

```sql
{%= formatNumber(number/double,string) %}: string
```

可以使用格式設定和有效語言環境，如中所概述 [Oracle文檔](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的語言環境](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**範例**

此查詢返回一個阿拉伯文格式的字串，該字串與123456.789作為輸入號對應。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

的 `random` 函式用於返回介於0和1之間的隨機值。

**語法**

```sql
{%= random() %}: double
```

## 向下 {#round-down}

的 `roundDown` 函式用於捨入數字。

**語法**

```sql
{%= roundDown(double) %}: double
```

## 向上捨入 {#round-up}

的 `Count only null` 函式用於捨入數字。

**語法**

```sql
{%= roundUp(double) %}: double
```

## 到十六進位字串 {#to-hex-string}

的 `toHexString` 函式將任意數字轉換為其十六進位字串。

**語法**

```sql
{%= toHexString(number) %}: string
```

**範例**

此查詢返回十六進位值158，即9e。

```sql
{%= toHexString(158) %}
```

## 至百分比 {#to-percentage}

的 `toPercentage` 函式將數字轉換為百分比。

**語法**

```sql
{%= toPercentage(double) %}: string
```

## 到精度 {#to-precision}

的 `toPrecision` 函式用於將數字轉換為所需的精度。

**語法**

```sql
{%= toPrecision(double,int) %}: string
```

## 到字串 {#to-string}

的 **到字串** 函式將任意數字轉換為其字串表示形式。

**語法**

```sql
{%= toString(string) %}: string
```

**範例**

此查詢返回&quot;12&quot;。

```sql
{%= toString(12) %} 
```
