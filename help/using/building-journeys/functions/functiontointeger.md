---
product: adobe campaign
title: toInteger
description: 了解函式toInteger
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 14%

---

# toInteger {#toInteger}

將引數值轉換為整數。

## 類別

轉換

## 函式語法

`toInteger(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為整數 |
| dateTime | 將日期轉換為毫秒數（epoch毫秒） |
| 小數 | 通過刪除小數部分將轉換為整數(示例：1.5變成1) |
| 布林值 | 若為true，則將布林值轉換為1，若為false，則將0 |

## 簽名和返回類型

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

傳回整數。

## 範例

`toInteger("4")`

返回4。
