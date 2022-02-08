---
product: adobe campaign
title: toInteger
description: 瞭解函式toInteger
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 901a91d1-13dd-4283-b87f-223196eb072f
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 14%

---

# 到整數 {#toInteger}

將參數值轉換為整數。

## 類別

轉換

## 函式語法

`toInteger(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 | 將字串值轉換為整數 |
| 日期時間 | 將日期轉換為毫秒數（新紀元毫秒） |
| 小數 | 通過刪除小數部分轉換為整數(示例：1.5變為1 |
| 布林值 | 如果為true，則將布爾值轉換為1；如果為false，則將布爾值轉換為0 |

## 簽名和返回的類型

`toInteger(<dateTime>)`

`toInteger(<decimal>)`

`toInteger(<integer>)`

`toInteger(<string>)`

`toInteger(<boolean>)`

返回整數。

## 範例

`toInteger("4")`

返回4。
