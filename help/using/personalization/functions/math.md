---
title: 數學函式程式庫
description: 數學函式程式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b9149ad6-2be7-4bdf-82eb-7ab52780cb4e
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 11%

---

# 數學函數 {#math}

瞭解如何在個人化編輯器中使用數學函式。

## 絕對 {#absolute}

`absolute`函式可用來轉換絕對值的數字。

**語法**

```sql
{%= absolute(int) %}: int
```

## formatnumber {#format-number}

`formatNumber`函式可用來將任何數字格式化成語言感應表示法。

它接受數字和代表地區設定的字串，並傳回所需地區設定中數字的格式化字串。

**語法**

```sql
{%= formatNumber(number/double,string) %}: string
```

您可以使用[Oracle檔案](https://docs.oracle.com/javase/8/docs/api/java/util/Locale.html)和[支援的區域設定](https://www.oracle.com/java/technologies/javase/jdk11-suported-locales.html){_blank}中概述的格式設定和有效區域設定

**範例**

此查詢會傳回對應至123456.789的阿拉伯文格式化字串作為輸入數字。

```sql
{%= formatNumber(123456.789, "ar_EG") %}
```

## 隨機 {#random}

`random`函式用來傳回0到1之間的隨機值。

**語法**

```sql
{%= random() %}: double
```

## 向下四捨五入 {#round-down}

`roundDown`函式用於向下舍入數字。

**語法**

```sql
{%= roundDown(double) %}: double
```

## 向上四捨五入 {#round-up}

`Count only null`函式用於向上四捨五入數字。

**語法**

```sql
{%= roundUp(double) %}: double
```

## 至十六進位字串 {#to-hex-string}

`toHexString`函式將任何數字轉換成其十六進位字串。

**語法**

```sql
{%= toHexString(number) %}: string
```

**範例**

此查詢傳回158的十六進位值，即9e。

```sql
{%= toHexString(158) %}
```

## 至整數 {#to-int}

`toInt`函式可用來將任何這些型別（數字、雙精度浮點數、整數、長整數、浮點數、短整數、位元組、布林值、字串）轉換成整數。

**語法**

```sql
{%= toInt(<valueToConvert>) %}: integer
```

**範例**

此查詢傳回42,6的整數值，即42。

```sql
{%= toInt(42.6) %}: integer
```

## 至百分比 {#to-percentage}

`toPercentage`函式用於將數字轉換為百分比。

**語法**

```sql
{%= toPercentage(double) %}: string
```

## 至精確度 {#to-precision}

`toPrecision`函式用於將數字轉換為所需的精確度。

**語法**

```sql
{%= toPrecision(double,int) %}: string
```

## 至字串 {#to-string}

**toString**&#x200B;函式將任何數字轉換成其字串表示方式。

**語法**

```sql
{%= toString(string) %}: string
```

**範例**

此查詢傳回「12」。

```sql
{%= toString(12) %} 
```
