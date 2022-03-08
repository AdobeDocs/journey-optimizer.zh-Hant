---
title: 映射函式館
description: 映射函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 6%

---

# 映射函式{#maps}

在個性化設定中使用映射函式使與映射的交互更容易。

## 取得{#get}

的 `get` 函式用於檢索給定鍵的映射值。

**格式**

```sql
{%= get(map, string) %}
```

**範例**

以下操作獲取密鑰的標識映射值 `example@example.com`。

```sql
{%= get(identityMap,"example@example.com") %}
```

## 鍵{#keys}

的 `keys` 函式用於檢索給定映射的所有鍵。

**格式**

```sql
{%= keys(map) %}
```

**範例**

以下操作將獲取映射的所有鍵 `identityMap`。

```sql
{%= keys(identityMap) %}
```

## 值{#values}

的 `values` 函式用於檢索給定映射的所有值。

**格式**

```sql
{%= values(map) %}
```

**範例**

以下操作將獲取映射的所有值 `identityMap`。

```sql
{%= values(identityMap) %}
```
