---
product: journey optimizer
title: toBool
description: 瞭解函式toBool
feature: Journeys
role: Engineer
level: Experienced
keywords: tobool，函式，運算式，歷程
exl-id: 0bb68d05-bb90-48b7-aff3-82ab15d55ebe
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---

# toBool {#toBool}

根據其型別，將引數值轉換為布林值。

* 從字串：嘗試將字串值轉換為布林值，如果字串值為「true」，則從「true」，否則為false
* 從數值：如果數值不等於0，則為true；否則為false

## 類別

轉換

## 函式語法

`toBool(<parameter>)`

## 參數

* 小數
* 布林值
* 字串
* 整數

## 簽章與傳回的型別

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
