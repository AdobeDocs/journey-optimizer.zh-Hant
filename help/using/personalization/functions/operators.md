---
title: 運運算元函式庫
description: 運運算元函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 操作者 {#operators}

## 布林函式 {#boolean-functions}

布林值函式用於對不同元素執行布林值邏輯。

### 與{#and}

此 `and` 函式用來建立邏輯結合。

**語法**

```sql
{%= query1 and query2 %}
```

**範例**

下列作業將傳回原籍國為法國及1985年出生年份的所有人。

```sql
{%= profile.homeAddress.country = "France" and profile.person.birthYear = 1985 %}
```

### 或{#or}

此 `or` 函式用來建立邏輯分離。

**語法**

```sql
{%= query1 or query2 %}
```

**範例**

下列作業將傳回原籍國為法國或1985年出生年份的所有人。

```sql
{%= profile.homeAddress.country = "France" or profile.person.birthYear = 1985 %}
```

<!--
## Not{#not}

The `not` (or `!`) function is used to create a logical negation.

**Syntax**

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

比較函式是用來比較不同運算式和值之間的差異，並據此傳回true或false。

### 等於{#equals}

此 `=` （等於）函式檢查一個值或運算式是否等於另一個值或運算式。

**語法**

```sql
{%= expression = value %}
```

**範例**

下列作業會檢查住家地址國家/地區是否為法國。

```sql
{%= profile.homeAddress.country = "France" %}
```

### 不等於{#notequal}

此 `!=` （不等於）函式檢查一個值或運算式是否為 **非** 等於另一個值或運算式。

**語法**

```sql
{%= expression != value %}
```

**範例**

下列作業會檢查住家地址國家/地區是否不是France。

```sql
{%= profile.homeAddress.country != "France" %}
```

### Greater than{#greaterthan}

此 `>` （大於）函式來檢查第一個值是否大於第二個值。

**語法**

```sql
{%= expression1 > expression2 %}
```

**範例**

下列作業會嚴格定義1970年後出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大於或等於{#greaterthanorequal}

此 `>=` （大於或等於）函式來檢查第一個值是否大於或等於第二個值。

**語法**

```sql
{%= expression1 >= expression2 %}
```

**範例**

下列作業定義1970年或之後出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 少於{#lessthan}

此 `<` （小於）比較函式用於檢查第一個值是否小於第二個值。

**語法**

```sql
{%= expression1 < expression2 %}
```

**範例**

下列作業定義2000年以前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### Less than or equal to{#lessthanorequal}

此 `<=` （小於或等於）比較函式用於檢查第一個值是否小於或等於第二個值。

**語法**

```sql
{%= expression1 <= expression2 %}
```

**範例**

下列作業會定義2000年或之前出生的人。

```sql
{%= profile.person.birthYear <= 2000 %}
```

**含數字的作業**
