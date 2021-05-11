---
title: 函式館
description: 函式館
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 6%

---

# 映射函式{#maps}

![](../../assets/do-not-localize/badge.png)

[!DNL Profile Query Language] (PQL)提供函式，讓與地圖的互動更輕鬆。

## 取得

`get`函式用於檢索給定鍵的映射值。

**格式**

```sql
get({MAP},{STRING})
```

**範例**

以下PQL查詢獲取鍵`example@example.com`的標識映射值。

```sql
get(identityMap,"example@example.com")
```

## 按鍵

`keys`函式用於檢索給定映射的所有鍵。

**格式**

```sql
keys({MAP})
```

**範例**

以下PQL查詢獲取映射`identityMap`的所有鍵。

```sql
keys(identityMap)
```

## 值

`values`函式用於檢索給定映射的所有值。

**格式**

```sql
values({MAP})
```

**範例**

以下PQL查詢獲取映射`identityMap`的所有值。

```sql
values(identityMap)
```
