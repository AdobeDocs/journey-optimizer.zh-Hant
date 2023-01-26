---
solution: Journey Optimizer
product: journey optimizer
title: 操作者
description: 了解進階運算式中的運算子
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 運算式，語法，運算子，編輯器，歷程
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 6%

---

# 操作者 {#operators}

運算子有兩種：一元運算子和二進位運算子。 有左一元運算子和右一元運算子。

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 重要備註{#important-notes}

* 使用乘法時(`*`)，則兩個操作欄位必須具有相同類型，可以是整數或小數。 範例：
   * 下列範例正確： `3.0 * 4.0`
   * `3 * 4.0` 會導致錯誤

## 邏輯  {#logical}

### 和

```json
<expression1> and <expression2>
```

兩者 &lt;expression1> 和 &lt;expression2> 必須是布林值。 結果為布林值。

範例：

```json
3.14 > 2 and 3.15 < 1
```

### 或

```json
<expression1> or <expression2>
```

兩者 &lt;expression1> 和 &lt;expression2> 必須是布林值。 結果為布林值。

範例：

```json
3.14 > 2 or 3.15 < 1
```

### not

```json
not <expression>
```

&lt;expression> 必須是布林值。 結果為布林值。

範例：

```json
not 3.15 < 1
```

## 比較 {#comparison}

### 為null

```json
<expression> is null
```

結果為布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@{BarBeacon.location} is null
```

### 非null

```json
<expression> is not null
```

結果為布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@{BarBeacon.location} is not null
```

### 為null

```json
<expression> has null
```

&lt;expression> 必須是清單。 結果為布林值。

用於識別清單至少包含一個null值。

範例：

```json
["foo", "bar", null] has null
```

傳回true

```json
["foo", "bar", ""] has null
```

傳回false，因為「」不視為Null。

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>針對 &lt;expression1> 和 &lt;expression2> 沒有資料類型控制項。

範例：

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### !=

```json
<expression1> != <expression2>
```

>[!NOTE]
針對 &lt;expression1> 和 &lt;expression2> 沒有資料類型控制項。

結果為布林值。

範例：

```json
3.14 != 42
```

```json
"foo" != "bar"
```

### >

```json
<expression1> > <expression2>
```

可以將日期時間與日期時間進行比較。

Datetimeonly可與Datetimeonly進行比較。

整數或小數都可與整數或小數進行比較。

禁止使用其他組合。

結果為布林值。

範例：

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

可以將日期時間與日期時間進行比較。

Datetimeonly可與Datetimeonly進行比較。

整數或小數都可與整數或小數進行比較。

禁止使用其他組合。

結果為布林值。

範例：

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

可以將日期時間與日期時間進行比較。

Datetimeonly可與Datetimeonly進行比較。

整數或小數都可與整數或小數進行比較。

禁止使用其他組合。

結果為布林值。

範例：

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

可以將日期時間與日期時間進行比較。

Datetimeonly可與Datetimeonly進行比較。

整數或小數都可與整數或小數進行比較。

禁止使用其他組合。

結果為布林值。

範例：

```json
42 <= 3.14
```

## 算術 {#arithmetic}

### +

```json
<expression1> + <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也為數值。

範例：

```json
1 + 2
```

傳回3

### -

```json
<expression1> - <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也為數值。

範例：

```json
2 - 1 
```

傳回1

### /

```json
<expression1> / <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也為數值。

&lt;expression2> 不得等於0（傳回0）。

範例：

```json
4 / 2
```

傳回2

### *

```json
<expression1> * <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也為數值。

範例：

```json
3 * 4
```

傳回12

### %

```json
<expression1> % <expression2>
```

這兩個運算式都必須是數值（整數或小數）。

結果也為數值。

範例：

```json
3 % 2
```

傳回1。

## Math {#math}

### 為數值

```json
<expression> is numeric
```

運算式的類型為整數或小數。

範例：

```json
@ is numeric
```

### 為整數

```json
<expression> is integer
```

運算式的類型為整數。

範例：

```json
@ is integer
```

### 小數

```json
<expression> is decimal
```

運算式的類型為小數。

範例：

```json
@ is decimal
```

## 字串 {#string}

### +

```json
<string> + <expression>
```

```json
<expression> + <string>
```

它串連兩個運算式。

一個表達式必須是鏈結字串。

範例：

```json
"the current time is " + (now())
```

傳回「目前時間為2019-09-23T09:30:06.693Z」

```json
(now()) + " is the current time"
```

傳回「2019-09-23T09」:30:06.693Z是當前時間」

```json
"a" + "b" + "c" + 1234
```

傳回「abc1234」。

## 日期 {#date}

### +

```json
<expression> + <duration>
```

將持續時間附加至dateTime、dateTimeOnly或持續時間。

範例：

```json
(toDateTime("2011-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

傳回 _dateTime_ 2011-12-03T15:30:30Z

```json
(toDateTimeOnly("2011-12-03T15:15:30")) + (toDuration("PT15M"))
```

傳回 _dateTimeOnly_ 2011-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

傳回 _dateTime_ （含UTC時區）從目前時間起1小時後

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

傳回 _持續時間_ PT2H
