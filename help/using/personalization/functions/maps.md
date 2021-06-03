---
title: 函式庫
description: 函式庫
source-git-commit: 8c58dd667ea59a17833bbe3482b1a233ac2e28fe
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

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
