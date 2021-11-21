---
product: adobe campaign
title: setHours
description: 了解函式setHours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 8%

---

# setHours {#setHours}

僅設定日期時間或日期時間的小時數。 例如，如果您想要等到明天某個小時，您可以強制該小時。

## 類別

Date

## 函式語法

`setHours(<parameter>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 小時 | 整數 |

## 簽名和返回類型

`setHours(<dateTime>,<hours>)`

返回日期時間。

`setHours(<dateTimeOnly>,<hours>)`

返回日期時間，而不考慮時區。

## 範例

`setHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回2010-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

明天晚上8:XY返回，XY是當前時間評估時的分鐘。 如果評估發生在凌晨2:45，則返回時間為晚上8:45。
