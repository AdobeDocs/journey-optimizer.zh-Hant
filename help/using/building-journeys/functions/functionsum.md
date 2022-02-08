---
product: adobe campaign
title: sum
description: 瞭解函式和
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 11%

---

# 總和 {#sum}

返回一組表達式的值之和。 忽略空值。

## 類別

彙總

## 函式語法

`sum(<parameters>)`

## 參數

* listInteger
* 清單十進位
* 持續時間
* 整數
* 小數

## 簽名和返回的類型

`sum(<listDecimal>)`

返回十進位。

`sum(<listInteger>)`

返回整數。

`sum(<integer>,<integer>)`

返回整數。

`sum(<decimal>,<decimal>)`

返回十進位。

## 範例

`sum(@{BarBeacon.inventory},5)`

`sum([10,3,8])`

返回21。

`sum([10.5,null,8.1])`

返回18.6。
