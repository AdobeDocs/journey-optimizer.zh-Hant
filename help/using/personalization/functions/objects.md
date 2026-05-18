---
title: 物件函式庫
description: 物件函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 6ce70e32-aac3-4a2c-bfeb-c370521853ca
TQID: https://experienceleague.adobe.com/EdvzBXdtv1Mm4yIZ8ehu4tx6uQBxnpcXTMVQIc1oQkI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 57
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
