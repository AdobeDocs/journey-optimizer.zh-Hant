---
product: journey optimizer
title: min
description: 瞭解函式最小值
feature: Journeys
role: Developer
level: Experienced
keywords: min，函式，運算式，歷程
exl-id: 1c425d1d-08b4-446b-83ce-db376b2bf39f
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# min {#min}

傳回一組運算式中的最小值，以清單或兩個運算式形式提供。 會忽略Null值。

## 類別

彙總

## 函式語法

`min(<parameters>)`

## 參數

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 期間
* 整數
* 小數
* dateTime
* dateTimeOnly

## 簽章與傳回的型別

`min(<listDuration>)`

傳回持續時間。

`min(<listInteger>)`

傳回持續時間。

`min(<listDateTimeOnly>)`

傳回日期時間，不考慮時區。

`min(<listDateTime>)`

傳回日期時間。

`min(<listDateOnly>)`

傳回日期。

`min(<listDecimal>)`

傳回小數。

`min(<decimal>,<decimal>)`

傳回小數。

`min(<duration>,<duration>)`

傳回持續時間。

`min(<dateTime>,<dateTime>)`

傳回日期時間。

`min(<dateTimeOnly>,<dateTimeOnly>)`

傳回日期時間，不考慮時區。

`min(<integer>,<integer>)`

傳回整數。

## 範例

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

傳回3。

`min([10,null,8])`

傳回8。
