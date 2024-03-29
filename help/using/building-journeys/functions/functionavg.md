---
product: journey optimizer
title: avg
description: 瞭解函式avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 平均，函式，運算式，歷程
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: cb1fed2460ddbf3b226fe191b9695008970937c1
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# avg {#avg}

傳回一組運算式中的平均值（以清單或兩個運算式形式提供）。 會忽略Null值。


## 類別

彙總

## 函式語法

`avg(<parameter>)`

## 參數

支援的型別：

* listInteger
* listDecimal
* 小數
* 整數

## 簽章與傳回型別

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

傳回小數。

## 範例

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

傳回7.0。

`avg(10.2, 3)`

傳回6.6。
