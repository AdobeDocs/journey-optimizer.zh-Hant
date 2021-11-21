---
title: 映射函式庫
description: 映射函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# 地圖函式{#maps}

在個人化中使用地圖功能，讓與地圖的互動更輕鬆。

## 取得{#get}

此 `get` 函式可用來擷取指定索引鍵的對應值。

**格式**

```sql
{%= get(map, string) %}
```

**範例**

下列操作會取得索引鍵的身分對應值 `example@example.com`.

```sql
{%= get(identityMap,"example@example.com") %}
```

## 金鑰{#keys}

此 `keys` 函式可用來擷取指定地圖的所有索引鍵。

**格式**

```sql
{%= keys(map) %}
```

**範例**

以下操作獲取映射的所有鍵 `identityMap`.

```sql
{%= keys(identityMap) %}
```

## 值{#values}

此 `values` 函式來擷取指定地圖的所有值。

**格式**

```sql
{%= values(map) %}
```

**範例**

以下操作獲取映射的所有值 `identityMap`.

```sql
{%= values(identityMap) %}
```
