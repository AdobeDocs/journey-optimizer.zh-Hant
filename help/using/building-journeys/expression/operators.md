---
solution: Journey Optimizer
product: journey optimizer
title: 操作者
description: 瞭解進階運算式中的運運算元
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 運算式，語法，運運算元，編輯器，歷程
exl-id: 706e2e02-9bd9-46e7-a73d-dda3c9ae4ba8
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 5%

---

# 操作者 {#operators}

運運算元有兩種型別：一元運運算元和二進位運運算元。 有左一元運運算元和右一元運運算元。

```json
// left-hand unary operators
// <operator> <operand> 
// operand is an expression
not (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example@adobe.com")

// right-hand unary operators
// <operator> <operand> 
// operand is an expression
@event{LobbyBeacon.endUserIDs._experience.emailid.id} is not null

// binary operators
// <operand1> <operator> <operand2>
// operand is an expression
(@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example1@adobe.com") or (@event{LobbyBeacon.endUserIDs._experience.emailid.id}=="example2@adobe.com") 
```

## 重要備註{#important-notes}

* 使用乘法(`*`)時，兩個作業欄位必須具有相同的型別，可以是整數或小數。 範例：
   * 下列範例是正確的： `3.0 * 4.0`
   * `3 * 4.0`將導致錯誤

* 使用`+`運運算元時，運算式必須封裝在括弧之間。 範例：
   * `toDateTimeOnly(toDateTime((currentTimeInMillis()) + 1))`正確
   * `toDateTimeOnly(toDateTime(currentTimeInMillis() + 1))`將導致錯誤

## 邏輯  {#logical}

### 和

```json
<expression1> and <expression2>
```

&lt;expression1>和&lt;expression2>都必須是布林值。 結果是布林值。

範例：

```json
3.14 > 2 and 3.15 < 1
```

### 或

```json
<expression1> or <expression2>
```

&lt;expression1>和&lt;expression2>都必須是布林值。 結果是布林值。

範例：

```json
3.14 > 2 or 3.15 < 1
```

### 非

```json
not <expression>
```

&lt;expression>必須為布林值。 結果是布林值。

範例：

```json
not 3.15 < 1
```

## 比較 {#comparison}

### 為null

```json
<expression> is null
```

結果是布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@event{BarBeacon.location} is null
```

### 不是null

```json
<expression> is not null
```

結果是布林值。

請注意，null表示運算式沒有評估值。

範例：

```json
@event{BarBeacon.location} is not null
```

### 具有null

```json
<expression> has null
```

&lt;expression>必須是清單。 結果是布林值。

用於識別清單是否包含至少一個Null值。

範例：

```json
["foo", "bar", null] has null
```

傳回true

```json
["foo", "bar", ""] has null
```

傳回false，因為「」不視為null。

### ==

```json
<expression1> == <expression2>
```

>[!NOTE]
>
>&lt;expression1>和&lt;expression2>沒有資料型別控制項。

範例：

```json
3.14 == 42
```

```json
"foo" == "bar"
```

### ！=

```json
<expression1> != <expression2>
```

>[!NOTE]
>
>&lt;expression1>和&lt;expression2>沒有資料型別控制項。

結果是布林值。

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

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
3.14 > 42
```

### >=

```json
<expression1> >= <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
42 >= 3.14
```

### &lt;

```json
<expression1> < <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

範例：

```json
42 < 3.14
```

### &lt;=

```json
<expression1> <= <expression2>
```

日期時間可以與日期時間比較。

Datetimeonly可以與Datetimeonly比較。

整數或小數點都可以與整數或小數點進行比較。

禁止任何其他組合。

結果是布林值。

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

結果也是數字。

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

結果也是數字。

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

結果也是數字。

&lt;expression2>不可以等於0 （傳回0）。

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

結果也是數字。

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

結果也是數字。

範例：

```json
3 % 2
```

傳回1。

## 數學 {#math}

### 是數值

```json
<expression> is numeric
```

運算式的型別是整數或小數。

範例：

```json
@ is numeric
```

### 為整數

```json
<expression> is integer
```

運算式的型別是整數。

範例：

```json
@ is integer
```

### 為小數

```json
<expression> is decimal
```

運算式的型別是十進位。

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

它會串連兩個運算式。

一個運算式必須是鏈結字串。

範例：

```json
"the current time is " + (now())
```

傳回「目前時間是2023-09-23T09:30:06.693Z」

```json
(now()) + " is the current time"
```

傳回「2023-09-23T09:30:06.693Z為目前時間」

```json
"a" + "b" + "c" + 1234
```

傳回「abc1234」。

## 日期 {#date}

### +

```json
<expression> + <duration>
```

將期間附加至dateTime、dateTimeOnly或duration。

範例：

```json
(toDateTime("2023-12-03T15:15:30Z")) + (toDuration("PT15M"))  
```

傳回&#x200B;_dateTime_ 2023-12-03T15:30:30Z

```json
(toDateTimeOnly("2023-12-03T15:15:30")) + (toDuration("PT15M"))
```

傳回&#x200B;_dateTimeOnly_ 2023-12-03T15:30:30

```json
(now()) + (toDuration("PT1H"))
```

從目前時間後一小時傳回&#x200B;_dateTime_ （含UTC時區）

```json
(toDuration("PT1H")) + (toDuration("PT1H"))
```

傳回&#x200B;_持續時間_ PT2H
