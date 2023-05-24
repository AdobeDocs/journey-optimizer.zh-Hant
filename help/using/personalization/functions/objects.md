---
title: 對象函式館
description: 對象函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 對象函式 {#objects}

## 為空{#isNull}

的 `isNull` 函式確定對象引用是否不存在。

**語法**

```sql
{%= isNull(object) %}
```

**範例**

以下操作將檢查人員的住宅地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不為空{#isNotNull}

的 `isNotNull` 函式確定是否存在對象引用。

**語法**

```sql
{%= isNotNull(object) %}
```

**範例**

以下操作將檢查人員的住宅地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
