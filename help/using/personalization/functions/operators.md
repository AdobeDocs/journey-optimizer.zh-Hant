---
title: 運運算元函式庫
description: 運運算元函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 75b0b380-d9a6-418e-b9f6-e64de385ba8d
TQID: https://experienceleague.adobe.com/b4Tz4auDyWb-iaUYAie31DL5hlHh97n3rYm7EP-JjIw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: b08de542c4f952f82a503103c783e54196c6d5b6
workflow-type: tm+mt
source-wordcount: 461
ht-degree: 9%

---

# 操作者 {#operators}

## 布林函式 {#boolean-functions}

布林值函式用於對不同元素執行布林值邏輯。

### 與{#and}

`and`函式用來建立邏輯結合。

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

`or`函式用來建立邏輯分離。

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

`=` （等於）函式檢查一個值或運算式是否等於另一個值或運算式。

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

`!=` （不等於）函式檢查一個值或運算式是否為&#x200B;**不**&#x200B;等於另一個值或運算式。

**語法**

```sql
{%= expression != value %}
```

**範例**

下列作業會檢查住家地址國家/地區是否不是France。

```sql
{%= profile.homeAddress.country != "France" %}
```

### 大於{#greaterthan}

`>` （大於）函式用於檢查第一個值是否大於第二個值。

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

`>=` （大於或等於）函式用於檢查第一個值是否大於或等於第二個值。

**語法**

```sql
{%= expression1 >= expression2 %}
```

**範例**

下列作業定義1970年或之後出生的人。

```sql
{%= profile.person.birthYear >= 1970 %}
```

### 小於{#lessthan}

`<` （小於）比較函式可用來檢查第一個值是否小於第二個值。

**語法**

```sql
{%= expression1 < expression2 %}
```

**範例**

下列作業定義2000年以前出生的人。

```sql
{%= profile.person.birthYear < 2000 %}
```

### 小於或等於{#lessthanorequal}

`<=` （小於或等於）比較函式是用來檢查第一個值是否小於或等於第二個值。

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

## 範本移轉功能 {#template-migration-functions}

個人化編輯器中提供範本移轉功能，以協助將現有範本移轉至Journey Optimizer。

### 透過運運算元比較{#amp-compare}

`ampCompare`函式使用指定的比較運運算元比較兩個值。

**語法**

```sql
{%= ampCompare(value1, value2, operator) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `value1` | 要比較的第一個值。 |
| `value2` | 要比較的第二個值。 |
| `operator` | 表示要使用的比較運運算元的整數。 |

**範例**

```sql
{%= ampCompare(profile.person.age, 18, 4) %}
```

### 子字串範圍{#amp-substr}

`ampSubstr`函式傳回指定開始與結束索引之間的字串部分。

**語法**

```sql
{%= ampSubstr(string, startIndex, endIndex) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `string` | 來源字串。 |
| `startIndex` | 子字串的開始索引（整數）。 |
| `endIndex` | 子字串的結束索引（整數）。 |

**範例**

下列運算式會傳回字串「Hello World」的前五個字元。

```sql
{%= ampSubstr("Hello World", 0, 5) %}
```

傳回`Hello`。

### 比較對象{#compare-to}

`compareTo`函式會以字典方式比較兩個字串。 如果第一個字串在第二個字串之前，則傳回負整數；如果相等，則傳回零；如果第一個字串在第二個字串之後，則傳回正整數。

**語法**

```sql
{%= compareTo(string1, string2) %}
```

| 引數 | 說明 |
| --------- | ----------- |
| `string1` | 要比較的第一個字串。 |
| `string2` | 要比較的第二個字串。 |

**範例**

```sql
{%= compareTo("apple", "banana") %}
```
