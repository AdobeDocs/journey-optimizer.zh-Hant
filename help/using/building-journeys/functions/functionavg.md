---
product: journey optimizer
title: avg
description: 了解函式平均
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 0%

---

# avg {#avg}

傳回一組運算式中的平均值，以清單或兩個運算式的形式提供。 忽略Null值。


## 類別

匯總

## 函式語法

`avg(<parameter>)`

## 參數

支援的類型：

* listInteger
* listDecimal
* 小數
* 整數

## 簽名和返回類型

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

傳回小數。

## 範例

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

返回7.0。

`avg(10.2, 3)`

返回6.6。
