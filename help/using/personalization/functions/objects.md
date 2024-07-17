---
title: 物件函式庫
description: 物件函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 19%

---

# 物件函數 {#objects}

## 是 Null{#isNull}

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

## 不是 Null{#isNotNull}

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
