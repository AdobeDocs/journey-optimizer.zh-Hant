---
product: journey optimizer
title: updateTimeZone
description: 瞭解函式updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone，函式，運算式，歷程
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 9%

---

# updateTimeZone {#updateTimeZone}

傳回新的日期時間，而在同一時間傳回新的時區。

## 類別

日期

## 函式語法

`updateTimeZone(<parameters>)`

## 參數

* 時區id：字串
* dateTime

## 簽章與傳回的型別

`updateTimeZone(<dateTime>,<timeZone id>)`

傳回日期時間。

## 範例

`updateTimeZone( toDateTime("2023-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

傳回2023-08-28T17:15:30.123+02:00。

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@event{MyExpEvent.timestamp}, "Australia/Sydney")`

如果時間戳記欄位的值為`2021-11-16T16:55:12.939318+01:00`，則函式會傳回`2021-11-17T02:55:12.942115+11:00`。
