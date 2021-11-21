---
product: adobe campaign
title: toDateTimeOnly
description: 了解函式toDateTime
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: db54c119-5080-403a-b254-43645be6b4a8
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 16%

---

# toDateTimeOnly{#toDateTimeOnly}

將引數值轉換為僅限日期時間的值。

## 類別

轉換

## 函式語法

`toDateTimeOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間格式為ISO-8601或「YYYY-MM-DD」（XDM日期格式） | 字串 |
| 日期時間 | dateTime |

## 簽名和返回的類型

`toDateTimeOnly(<dateTime>)`

`toDateTimeOnly(<string>)`
<!--`toDateTimeOnly(<integer>,<integer>,<integer>)`
`toDateTimeOnly(<integer>,<integer>,<integer>,<integer>,<integer>,<integer>)`-->

不考慮時區而返回日期時間。

## 範例

`toDateTimeOnly ("2016-08-18")`

傳回代表2016-08-18T00的dateTime:00:00.000

`toDateTimeOnly(now())`

<!--`toDateTimeOnly(2016,8,18,23,17,59)`

Returns 2016-08-18T23:17:59.000.

`toDateTimeOnly(2016,8,18)`

Returns 2016-08-18T00:00:00.000.-->
