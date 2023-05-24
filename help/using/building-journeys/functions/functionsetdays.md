---
product: journey optimizer
title: setDays
description: 瞭解函式setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays，函式，表達式，旅程
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

---

# setDays {#setDays}

僅設定日期時間或日期時間的日期。 例如，如果要等到月中某一天，則可以強制該日。

## 類別

日期

## 函式語法

`setDays(<parameter>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | 日期時間 |
| 不考慮區域的日期時間 | 日期僅時間 |
| 天 | 整數 |

## 簽名和返回的類型

`setDays(<dateTime>,<days>)`

返回日期時間。

`setDays(<dateTimeOnly>,<days>)`

返回不考慮時區的日期時間。

## 範例

`setDays(toDateTime('2010-12-12T01:11:00Z'), 25)`

返回2010-12-25T01:11:00Z。

`setDays(toDateTimeOnly(@{MyEvent.registrationDate}), 1)`
