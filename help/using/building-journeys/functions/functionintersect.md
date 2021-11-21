---
product: adobe campaign
title: 相交
description: 了解函式相交
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 12%

---

# 相交{#intersect}

傳回兩個輸入清單中的公用值。 如果兩個清單之一為null，則返回空清單。

## 類別

清單

## 函式語法

`intersect(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單1 | 清單 |
| 清單2 | 清單 |

## 簽名和返回的類型

`intersect(listString,listString)`:listString
`intersect(listDecimal,listDecimal)`:listDecimal
`intersect(listInteger,listInteger)`:listInteger
`intersect(listDateTime,listDateTime)`:listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`:listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`:listDateOnly
`intersect(listDuration,listDuration)`:listDuration
`intersect(listBoolean,listBoolean)`:listBoolean

傳回清單。

## 範例

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

傳回 [&quot;sports&quot;、&quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

傳回設定檔屬性和指定類別清單之間的通用項目。

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

傳回設定檔屬性和指定事件欄位之間的通用項目。
