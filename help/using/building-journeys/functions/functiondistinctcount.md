---
product: journey optimizer
title: distinctCount
description: 瞭解函式distinctCount
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCount、函式、表達式、旅程
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

---

# distinctCount{#distinctCount}

計數忽略空值的不同值數。

## 類別

彙總

## 函式語法

`distinctCount(<listAny>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單 | 清單字串 |
| 清單 | list布爾 |
| 清單 | listInteger |
| 清單 | 清單十進位 |
| 清單 | listDuration（持續時間） |
| 清單 | 清單日期時間 |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

## 簽名和返回的類型

`distinctCount(<listAny>)`

返回整數。

## 範例

`distinctCount([10,2,10,null])`

返回2。
