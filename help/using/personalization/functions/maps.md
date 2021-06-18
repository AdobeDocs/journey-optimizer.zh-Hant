---
title: 映射函式庫
description: 映射函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: e3b7e80b72e6be71d5b38cd5507d20ad2e8ca8d4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 8%

---

# 地圖函式{#maps}

在個人化中使用地圖功能，讓與地圖的互動更輕鬆。

## 取得{#get}

`get`函式用於檢索給定鍵的映射值。

**格式**

```sql
{%= get(map, string) %}
```

**範例**

以下操作獲取鍵`example@example.com`的標識映射值。

```sql
{%= get(identityMap,"example@example.com") %}
```

## 金鑰{#keys}

`keys`函式用於檢索給定映射的所有鍵。

**格式**

```sql
{%= keys(map) %}
```

**範例**

以下操作獲取映射`identityMap`的所有鍵。

```sql
{%= keys(identityMap) %}
```

## 值{#values}

`values`函式用於檢索給定映射的所有值。

**格式**

```sql
{%= values(map) %}
```

**範例**

以下操作獲取映射`identityMap`的所有值。

```sql
{%= values(identityMap) %}
```
