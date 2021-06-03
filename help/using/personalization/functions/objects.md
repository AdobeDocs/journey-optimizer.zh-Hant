---
title: 函式庫
description: 函式庫
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# 物件函式 {#objects}

![](../../assets/do-not-localize/badge.png)

## 為null{#isNull}

`isNull`函式確定對象引用是否不存在。

**格式**

```sql
{%= isNull(object) %}
```

**範例**

以下操作將檢查該人員的家庭地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 非空{#isNotNull}

`isNotNull`函式確定是否存在對象引用。

**格式**

```sql
{%= isNotNull(object) %}
```

**範例**

以下操作將檢查該人員的家庭地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
