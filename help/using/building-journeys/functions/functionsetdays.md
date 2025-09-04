---
product: journey optimizer
title: setDays
description: 瞭解函式setDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setDays，函式，運算式，歷程
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 12%

---

# setDays {#setDays}

僅設定日期時間或日期時間的日期。 例如，如果您要等到月份的某一天，則可以強制該天。

## 類別

日期

## 函式語法

`setDays(<parameter>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 天 | 整數 |

## 簽章與傳回型別

`setDays(<dateTime>,<days>)`

傳回日期時間。

`setDays(<dateTimeOnly>,<days>)`

傳回日期時間，不考慮時區。

## 範例

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

傳回2023-12-25T01:11:00Z。

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
