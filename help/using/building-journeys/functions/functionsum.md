---
product: journey optimizer
title: sum
description: 瞭解函式總和
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sum，函式，運算式，歷程
exl-id: a9085f4d-6434-4bc5-8e5d-3f2b6033defc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 12%

---

# sum {#sum}

傳回一組運算式的值總和。 會忽略Null值。

## 類別

彙總

## 函式語法

`sum(<parameters>)`

## 參數

* listInteger
* listDecimal
* 期間
* 整數
* 小數

## 簽章與傳回的型別

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

傳回18.6。
