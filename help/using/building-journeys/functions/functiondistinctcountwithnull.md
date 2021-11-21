---
product: adobe campaign
title: distinctCountWithNull
description: 了解函式distinctCountWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCountWithNull {#distinctCountWithNull}

計算包含空值的不同值的數量。

## 類別

彙總

## 函式語法

`distinctCountWithNull(<listAny>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單 | listString |
| 清單 | listBoolean |
| 清單 | listInteger |
| 清單 | listDecimal |
| 清單 | listDuration |
| 清單 | listDateTime |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

## 簽名和返回類型

`distinctCountWithNull(<listAny>)`

傳回整數。

## 範例

`distinctCountWithNull([10,2,10,null])`

返回3。
