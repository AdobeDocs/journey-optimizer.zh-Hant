---
title: 對象函式庫
description: 對象函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 10%

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
