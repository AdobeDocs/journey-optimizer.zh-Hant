---
title: 地圖函式庫
description: 地圖函式庫
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: de6a8da2-55cf-4105-ba93-40c556732626
TQID: https://experienceleague.adobe.com/KeitEe0NQxxc-snCyWSGlov-OyUgiva6ddzrCTxEKSs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 6%

---

# 地圖函式{#maps}

在個人化中使用地圖功能，以便更輕鬆與地圖互動。

## Get{#get}

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
