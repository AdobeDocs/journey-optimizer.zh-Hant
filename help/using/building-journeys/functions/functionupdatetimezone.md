---
product: journey optimizer
title: updateTimeZone
description: 了解函式updateTimeZone
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: updateTimeZone，函式，表達式，歷程
exl-id: 1bf4662e-55d0-4631-af93-1430ec7ed7e2
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# updateTimeZone {#updateTimeZone}

傳回新日期時間，並在同一時間內傳回新時區。

## 類別

日期

## 函式語法

`updateTimeZone(<parameters>)`

## 參數

* 時區id:字串
* dateTime

## 簽名和返回類型

`updateTimeZone(<dateTime>,<timeZone id>)`

返回日期時間。

## 範例

`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), "Europe/Paris"))`

傳回2019-08-28T17:15:30.123+02:00。

<!--`updateTimeZone( toDateTime("2019-08-28T08:15:30.123-07:00"), toTimeZone("Europe/Paris")))`
Returns "2019-08-28T17:15:30.123+02:00".-->

`updateTimeZone(@{MyExpEvent.timestamp}, "Australia/Sydney")`

如果時間戳記欄位的值為 `2021-11-16T16:55:12.939318+01:00`，則函式會傳回 `2021-11-17T02:55:12.942115+11:00`.
