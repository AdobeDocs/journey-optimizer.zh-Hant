---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 對象函式{#objects}

![](../../assets/do-not-localize/badge.png)

## 為空

`isNull`函式確定對象引用是否不存在。

**格式**

```sql
isNull({OBJECT})
```

**範例**

以下PQL查詢會檢查人員的家庭地址是否不存在。

```sql
isNull(person.homeAddress)
```

## 非空值

`isNotNull`函式確定是否存在對象引用。

**格式**

```sql
isNotNull({OBJECT})
```

**範例**

以下PQL查詢會檢查人員的家庭地址是否存在。

```sql
isNotNull(person.homeAddress)
```
