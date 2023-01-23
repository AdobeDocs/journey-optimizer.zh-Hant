---
product: journey optimizer
title: toBool
description: 了解函式至Bool
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: tobool，函式，運算式，歷程
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 11%

---

# toBool {#toBool}

根據參數值的類型，將參數值轉換為布爾值。

* 從字串：嘗試將字串值轉換為布林值（如果字串值為「true」，則從「true」），否則從false
* 從數值：若數值不等於0，則為true；否則為false

## 類別

轉換

## 函式語法

`toBool(<parameter>)`

## 參數

* 小數
* 布林值
* 字串
* 整數

## 簽名和返回的類型

`toBool(<decimal>)`

`toBool(<boolean>)`

`toBool(<string>)`

`toBool(<integer>)`

傳回布林值。

## 範例

`toBool("true")`

`toBool(1)`

傳回true。

`toBool("this is not a boolean")`

傳回false。
