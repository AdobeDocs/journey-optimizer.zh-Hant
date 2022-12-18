---
product: journey optimizer
title: distinctCount
description: 了解函式distinctCount
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 32%

---

# distinctCount{#distinctCount}

計算忽略空值的不同值的數量。

## 類別

彙總

## 函式語法

`distinctCount(<listAny>)`

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

`distinctCount(<listAny>)`

傳回整數。

## 範例

`distinctCount([10,2,10,null])`

傳回2。
