---
product: journey optimizer
title: toDecimal
description: 了解Decimal的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# toDecimal {#toDecimal}

根據參數值的類型，將參數值轉換為小數值。

## 類別

轉換

## 函式語法

`toDecimal(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為小數 |
| dateTime | 將日期轉換為毫秒數（epoch毫秒） |
| 布林值 | 若為true，則將布林值轉換為1，若為false，則將0 |
| 整數 | 轉換為小數（範例）。:1變成1.0) |

## 簽名和返回的類型

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

傳回小數。

## 範例

`toDecimal("4.0")`

傳回4.0。
