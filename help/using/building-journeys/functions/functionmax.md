---
product: journey optimizer
title: max
description: 瞭解函式最大值
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: max，函式，運算式，歷程
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# max{#max}

傳回一組運算式中的最大值，以清單或兩個運算式形式提供。 會忽略Null值。

## 類別

彙總

## 函式語法

`max(<parameter>)`

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

`max(<listDuration>)`

傳回持續時間。

`max(<listInteger>)`

傳回持續時間。

`max(<listDateTimeOnly>)`

傳回日期時間，不考慮時區。

`max(<listDateTime>)`

傳回日期時間。

`max(<listDateOnly>)`

傳回日期。

`max(<listDecimal>)`

傳回小數。

`max(<decimal>,<decimal>)`

傳回小數。

`max(<duration>,<duration>)`

傳回持續時間。

`max(<dateTime>,<dateTime>)`

傳回日期時間。

`max(<dateTimeOnly>,<dateTimeOnly>)`

傳回日期時間，不考慮時區。

`max(<integer>,<integer>)`

傳回整數。

## 範例

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

傳回10。

`max([10,null,8])`

傳回10。
