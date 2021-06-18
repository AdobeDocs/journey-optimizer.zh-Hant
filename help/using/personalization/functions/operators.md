---
title: 運算子函式庫
description: 運算子函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 12%

---

# 操作者 {#operators}

## 布林函式

布林函式用於對不同元素執行布林邏輯。

### 和{#and}

`and`函式用於建立邏輯連接。

**格式**

```sql
{%= query1 and query2 %}
```

**範例**

以下行動將返回所有以法國為母國的人，1985年出生年。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

`or`函式用於建立邏輯分離。

**格式**

```sql
{%= query1 or query2 %}
```

**範例**

以下行動將把所有以法國或1985年出生年為母國的人返回。

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Format**

```sql
not ({QUERY})
!({QUERY})
```

**Example**

The following operation will return all people who do not have their home country as Canada.

```sql
not (homeAddress.countryISO = "CA")
```
-->





## 比較函式

比較函式可用來比較不同運算式和值，並據以傳回true或false。

### 等於{#equals}

`=`（等於）函式會檢查一個值或運算式是否等於另一個值或運算式。

**格式**

```sql
{%= expression = value %}
```

**範例**

以下操作將檢查主地址國家/地區是否為法國。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等於{#notequal}

`!=`（不等於）函式檢查一個值或表達式是否為&#x200B;**不**&#x200B;等於另一個值或表達式。

**格式**

```sql
{%= expression != value %}
```

**範例**

以下操作將檢查主地址國家/地區是否不是法國。

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

`>`（大於）函式用來檢查第一值是否大於第二值。

**格式**

```sql
{%= expression1 > expression2 %}
```

**範例**

以下操作嚴格定義了1970年後出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### Greater than or equal to{#greaterthanorequal}

`>=`（大於或等於）函式用於檢查第一值是否大於或等於第二值。

**格式**

```sql
{%= expression1 >= expression2 %}
```

**範例**

以下操作定義1970年或之後出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### Less than{#lessthan}

`<`（小於）比較函式用於檢查第一值是否小於第二值。

**格式**

```sql
{%= expression1 < expression2 %}
```

**範例**

以下操作定義2000年以前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### Less than or equal to{#lessthanorequal}

使用`<=`（小於或等於）比較函式來檢查第一值是否小於或等於第二值。

**格式**

```sql
{%= expression1 <= expression2 %}
```

**範例**

以下操作定義2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**具有數字的操作**

