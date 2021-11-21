---
title: 運算子函式庫
description: 運算子函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 11%

---

# 操作者 {#operators}

## 布林函式

布林函式用於對不同元素執行布林邏輯。

### 和{#and}

此 `and` 函式用來建立邏輯連接。

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

此 `or` 函式用於建立邏輯分離。

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

此 `=` （等於）函式會檢查某個值或運算式是否等於另一個值或運算式。

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

此 `!=` （不等於）函式檢查一個值或表達式是否為 **not** 等於其他值或運算式。

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

此 `>` （大於）函式用來檢查第一值是否大於第二值。

**格式**

```sql
{%= expression1 > expression2 %}
```

**範例**

以下操作嚴格定義了1970年後出生的人。

```sql
{%= profile.person.birthYear > 1970 %}
```

### 大於或等於{#greaterthanorequal}

此 `>=` （大於或等於）函式用來檢查第一值是否大於或等於第二值。

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

此 `<` （小於）比較函式用來檢查第一值是否小於第二值。

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

此 `<=` （小於或等於）比較函式用於檢查第一值是否小於或等於第二值。

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
