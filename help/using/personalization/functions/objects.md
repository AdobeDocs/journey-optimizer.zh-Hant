---
title: 物件函式庫
description: 物件函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 7%

---

# 物件函式 {#objects}

## 為空{#isNull}

`isNull`函式決定物件參考是否不存在。

**語法**

```sql
{%= isNull(object) %}
```

**範例**

下列作業會檢查人員的住家地址是否不存在。

```sql
{%= isNull(person.homeAddress) %}
```

## 不是Null{#isNotNull}

`isNotNull`函式決定物件參考是否存在。

**語法**

```sql
{%= isNotNull(object) %}
```

**範例**

下列作業會檢查人員的住家地址是否存在。

```sql
{%= isNotNull(person.homeAddress) %}
```
