---
title: 地圖函式庫
description: 地圖函式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 8%

---

# 地圖函式{#maps}

在個人化中使用地圖功能，以便更輕鬆與地圖互動。

## 取得{#get}

`get`函式用於擷取給定索引鍵的對應值。

**語法**

```sql
{%= get(map, string) %}
```

**範例**

下列作業取得索引鍵`example@example.com`的識別對應值。

```sql
{%= get(identityMap,"example@example.com") %}
```

## 索引鍵{#keys}

`keys`函式用於擷取給定對應的所有索引鍵。

**語法**

```sql
{%= keys(map) %}
```

**範例**

下列作業取得對應`identityMap`的所有索引鍵。

```sql
{%= keys(identityMap) %}
```

## 值{#values}

`values`函式用於擷取給定對應的所有值。

**語法**

```sql
{%= values(map) %}
```

**範例**

下列作業取得對應`identityMap`的所有值。

```sql
{%= values(identityMap) %}
```
