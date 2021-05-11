---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 9%

---

# 運算子 {#operators}

![](../../assets/do-not-localize/badge.png)

## 和

`and`函式用於建立邏輯連接。

**格式**

```sql
{QUERY} and {QUERY}
```

**範例**

以下PQL查詢將返回所有在加拿大和1985年出生的人。

```sql
homeAddress.countryISO = "CA" and person.birthYear = 1985
```

## 或

`or`函式用於建立邏輯分離。

**格式**

```sql
{QUERY} or {QUERY}
```

**範例**

以下PQL查詢將返回所有在加拿大或1985年出生的人。

```sql
homeAddress.countryISO = "CA" or person.birthYear = 1985
```

## Not

`not`（或`!`）函式用於建立邏輯否定。

**格式**

```sql
not ({QUERY})
!({QUERY})
```

**範例**

以下PQL查詢將返回所有沒有其祖國為加拿大的人員。

```sql
not (homeAddress.countryISO = "CA")
```

## 若  

`if`函式用於解析表達式，具體取決於指定的條件是否為真。

**格式**

```sql
if ({TEST_EXPRESSION}, {TRUE_EXPRESSION}, {FALSE_EXPRESSION})
```

| 引數 | 說明 |
| --------- | ----------- |
| `{TEST_EXPRESSION}` | 正在測試的布爾表達式。 |
| `{TRUE_EXPRESSION}` | 如果`{TEST_EXPRESSION}`為true，則使用其值的表達式。 |
| `{FALSE_EXPRESSION}` | 如果`{TEST_EXPRESSION}`為false，則使用其值的運算式。 |

**範例**

以下PQL查詢將將值設定為`1`（如果原始國家為加拿大），如果原始國家為`2`（如果原始國家為加拿大）。

```sql
if (homeAddress.countryISO = "CA", 1, 2)
```

## 等於

`=`(equals)函式會檢查一個值或運算式是否等於另一個值或運算式。

**格式**

```sql
{EXPRESSION} = {VALUE}
```

**範例**

以下PQL查詢檢查主地址國家／地區是否位於加拿大。

```sql
homeAddress.countryISO = "CA"
```

## 不等於

`!=`（不等於）函式會檢查一個值或運算式是否為&#x200B;**not**&#x200B;等於另一個值或運算式。

**格式**

```sql
{EXPRESSION} != {VALUE}
```

**範例**

以下PQL查詢會檢查主地址國家／地區是否不在加拿大。

```sql
homeAddress.countryISO != "CA"
```

## Greater than

`>`（大於）函式用於檢查第一值是否大於第二值。

**格式**

```sql
{EXPRESSION} > {EXPRESSION} 
```

**範例**

以下PQL查詢定義生日不在1月或2月的人。

```sql
person.birthMonth > 2
```

## Greater than or equal to

使用`>=`（大於或等於）函式來檢查第一值是否大於或等於第二值。

**格式**

```sql
{EXPRESSION} >= {EXPRESSION} 
```

**範例**

以下PQL查詢定義生日不在1月或2月的人。

```sql
person.birthMonth >= 3
```

## Less than

使用`<`（小於）比較函式來檢查第一值是否小於第二值。

**格式**

```sql
{EXPRESSION} < {EXPRESSION} 
```

**範例**

以下PQL查詢定義生日在1月的人。

```sql
person.birthMonth < 2
```

## Less than or equal to

使用`<=`（小於或等於）比較函式來檢查第一值是否小於或等於第二值。

**格式**

```sql
{EXPRESSION} <= {EXPRESSION} 
```

**範例**

以下PQL查詢定義生日在1月或2月的人。

```sql
person.birthMonth <= 2
```

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
