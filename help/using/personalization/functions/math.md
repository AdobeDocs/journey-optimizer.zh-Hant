---
title: 數學函式程式庫
description: 數學函式程式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 6%

---

# 數學函式 {#math}

瞭解如何在運算式編輯器中使用數學函式。

## 絕對 {#absolute}

此 `absolute` 函式可將數字轉換為絕對值。

**語法**

```sql
{%= absolute(int) %}: int
```

## formatnumber {#format-number}

此 `formatNumber` 函式可用來將任何數字格式化為語言感應式表示法。

它接受數字和代表地區設定的字串，並傳回所需地區設定中數字的格式化字串。

**語法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用格式設定和有效地區設定，如中所述 [oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html) 和 [支援的語言環境](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}

**範例**

此查詢會傳回對應至123456.789的阿拉伯文格式化字串作為輸入數字。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## Random {#random}

此 `random` 函式來傳回0到1之間的隨機值。

**語法**

```sql
{%= random() %}: double
```

## 向下四捨五入 {#round-down}

此 `roundDown` 函式用於對數字進行向下四捨五入。

**語法**

```sql
{%= roundDown(double) %}: double
```

## 向上四捨五入 {#round-up}

此 `Count only null` 函式用於對數字進行向上四捨五入。

**語法**

```sql
{%= roundUp(double) %}: double
```

## 至十六進位字串 {#to-hex-string}

此 `toHexString` 函式將任何數字轉換為十六進位字串。

**語法**

```sql
{%= toHexString(number) %}: string
```

**範例**

此查詢傳回158的十六進位值，即9e。

```sql
{%= toHexString(158) %}
```

## 至百分比 {#to-percentage}

此 `toPercentage` 函式用於將數字轉換為百分比。

**語法**

```sql
{%= toPercentage(double) %}: string
```

## 至精確度 {#to-precision}

此 `toPrecision` 函式用於將數字轉換為所需的精確度。

**語法**

```sql
{%= toPrecision(double,int) %}: string
```

## 至字串 {#to-string}

此 **toString** 函式將任何數字轉換為其字串表示法。

**語法**

```sql
{%= toString(string) %}: string
```

**範例**

此查詢傳回「12」。

```sql
{%= toString(12) %} 
```
