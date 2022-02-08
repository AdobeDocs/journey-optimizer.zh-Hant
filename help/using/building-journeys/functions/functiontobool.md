---
product: adobe campaign
title: toBool
description: 瞭解到Bool的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 10%

---

# 到布爾 {#toBool}

根據參數值的類型將參數值轉換為布爾值。

* 從字串：嘗試將字串值轉換為布爾值，如果字串值為&quot;true&quot;，則從&quot;true&quot;轉換為false，否則
* 從數字：如果數值不等於0，則返回true；否則返回false

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

返回布爾值。

## 範例

`toBool("true")`

`toBool(1)`

返回true。

`toBool("this is not a boolean")`

返回false。
