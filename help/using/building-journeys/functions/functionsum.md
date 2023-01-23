---
product: journey optimizer
title: sum
description: 了解函式總和
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum，函式，表達式，歷程
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

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
