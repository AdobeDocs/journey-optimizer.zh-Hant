---
product: journey optimizer
title: avg
description: 瞭解函式avg
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: avg，函式，表達式，旅程
exl-id: cc70f90c-2d12-42a0-829f-5f28c3c29cad
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---

# avg {#avg}

返回一組表達式中的平均值，以清單或兩個表達式的形式給出。 忽略空值。


## 類別

彙總

## 函式語法

`avg(<parameter>)`

## 參數

支援的類型：

* listInteger
* 清單十進位
* 小數
* 整數

## 簽名和返回的類型

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

返回十進位。

## 範例

`avg(@{BarBeacon.inventory},5)`

`avg([10,3,8])`

返回7.0。

`avg(10.2, 3)`

返回6.6。
