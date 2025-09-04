---
product: journey optimizer
title: 相交
description: 瞭解函式交集
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 相交，函式，運算式，歷程
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---

# 相交{#intersect}

傳回兩個輸入清單中的通用值。 如果兩個清單之一為空，則會傳回空白清單。

## 類別

清單

## 函式語法

`intersect(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單1 | list |
| 清單2 | list |

## 簽章與傳回的型別

`intersect(listString,listString)`： listString
`intersect(listDecimal,listDecimal)`： listDecimal
`intersect(listInteger,listInteger)`： listInteger
`intersect(listDateTime,listDateTime)`： listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`： listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`： listDateOnly
`intersect(listDuration,listDuration)`： listDuration
`intersect(listBoolean,listBoolean)`：清單布林值

傳回清單。

## 範例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

傳回[&quot;sports&quot;，&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "documentary"]
)
```

傳回設定檔屬性和指定類別清單之間的通用專案。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @event{myEvent.sport_interests}
)
```

傳回設定檔屬性和指定事件欄位之間的通用專案。
