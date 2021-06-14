---
title: 映射函式庫
description: 映射函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# 地圖函式{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)提供的功能可讓您更輕鬆地與地圖互動。

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
