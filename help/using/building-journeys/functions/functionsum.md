---
product: adobe campaign
title: sum
description: 了解函式總和
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---

# sum {#sum}

傳回一組運算式的值之和。 忽略Null值。

## 類別

彙總

## 函式語法

`sum(<parameters>)`

## 參數

* listInteger
* listDecimal
* 持續時間
* 整數
* 小數

## 簽名和返回的類型

`sum(<listDecimal>)`

傳回小數。

`sum(<listInteger>)`

傳回整數。

`sum(<integer>,<integer>)`

傳回整數。

`sum(<decimal>,<decimal>)`

傳回小數。

## 範例

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

傳回21。

`sum([10.5,null,8.1])`

返回18.6。
