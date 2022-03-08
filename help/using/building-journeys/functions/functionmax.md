---
product: adobe campaign
title: max
description: 瞭解函式max
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5c792d33-32b9-4b1b-ab99-3ebfac391678
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 6%

---

# 最大{#max}

返回一組表達式中的最大值，以清單或兩個表達式的形式給定。 忽略空值。

## 類別

彙總

## 函式語法

`max(<parameter>)`

## 參數

* listDuration（持續時間）
* listInteger
* 清單十進位
* 清單日期時間
* listDateTimeOnly
* listDateOnly
* 持續時間
* 整數
* 小數
* 日期時間
* 日期僅時間

## 簽名和返回的類型

`max(<listDuration>)`

返回持續時間。

`max(<listInteger>)`

返回持續時間。

`max(<listDateTimeOnly>)`

返回不考慮時區的日期時間。

`max(<listDateTime>)`

返回日期時間。

`max(<listDateOnly>)`

返回日期。

`max(<listDecimal>)`

返回十進位。

`max(<decimal>,<decimal>)`

返回十進位。

`max(<duration>,<duration>)`

返回持續時間。

`max(<dateTime>,<dateTime>)`

返回日期時間。

`max(<dateTimeOnly>,<dateTimeOnly>)`

返回不考慮時區的日期時間。

`max(<integer>,<integer>)`

返回整數。

## 範例

`max(@{BarBeacon.inventory},5)`

`max([10,3,8])`

返回10。

`max([10,null,8])`

返回10。
