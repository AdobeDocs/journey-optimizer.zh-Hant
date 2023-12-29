---
product: journey optimizer
title: toDecimal
description: 瞭解函式toDecimal
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 十進位，函式，運算式，歷程
exl-id: d761fa4d-5f99-4dee-b747-3eab464c4071
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# toDecimal {#toDecimal}

根據其型別，將引數值轉換為十進位值。

## 類別

轉換

## 函式語法

`toDecimal(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為小數 |
| dateTime | 將日期轉換為毫秒數（紀元毫秒） |
| 布林值 | 如果為true，則將布林值轉換為1，如果為false，則轉換為0 |
| 整數 | 轉換為小數（範例）。：1變為1.0) |

## 簽章與傳回的型別

`toDecimal(<integer>)`

`toDecimal(<decimal>)`

`toDecimal(<string>)`

`toDecimal(<boolean>)`

傳回小數。

## 範例

`toDecimal("4.0")`

傳回4.0。
