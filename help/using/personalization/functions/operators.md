---
title: 運算子函式館
description: 運算子函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 操作者 {#operators}

## 布爾函式 {#boolean-functions}

布爾函式用於對不同的元素執行布爾邏輯。

### 和{#and}

的 `and` 函式用於建立邏輯連接。

**格式**

```sql
{%= query1 and query2 %}
```

**範例**

這次行動將把所有在法國和1985年出生的人送回本國。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

的 `or` 函式用於建立邏輯斷開。

**格式**

```sql
{%= query1 or query2 %}
```

**範例**

以下行動將返回所有在法國或1985年出生的人。

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





## 比較函式 {#comparison-functions}

比較函式用於比較不同的表達式和值，從而返回true或false。

### 等於{#equals}

的 `=` （等於）函式檢查一個值或表達式是否等於另一個值或表達式。

**格式**

```sql
{%= expression = value %}
```

**範例**

以下操作將檢查家庭地址國家是否為法國。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等於{#notequal}

的 `!=` （不相等）函式檢查一個值或表達式 **不** 等於另一個值或表達式。

**格式**

```sql
{%= expression != value %}
```

**範例**

以下操作將檢查家庭地址國家（地區）是否不是法國。

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

的 `>` （大於）函式用於檢查第一值是否大於第二值。

**格式**

```sql
{%= expression1 > expression2 %}
```

**範例**

下面的操作對1970年後出生的人進行了嚴格的定義。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大於或等於{#greaterthanorequal}

的 `>=` （大於或等於）函式用於檢查第一值是否大於或等於第二值。

**格式**

```sql
{%= expression1 >= expression2 %}
```

**範例**

以下操作定義1970年或之後出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 少於{#lessthan}

的 `<` （小於）比較函式用於檢查第一值是否小於第二值。

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

的 `<=` 比較函式用於檢查第一值是否小於或等於第二值。

**格式**

```sql
{%= expression1 <= expression2 %}
```

**範例**

以下操作定義2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**帶數字的操作**
