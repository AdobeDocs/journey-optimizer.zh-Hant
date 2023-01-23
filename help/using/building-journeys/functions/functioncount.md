---
product: journey optimizer
title: count
description: 了解函式計數
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 計數，函式，運算式，歷程
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: ad113c0414b20ac2f758ad06a44315b24a3d3d0c
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 28%

---

# count {#count}

計算清單的元素，而不考慮null值。

## 類別

彙總

## 函式語法

`count(<listAny>)`

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

`count(<listAny>)`

傳回整數。

## 範例

`count([10,2,10,null])`

返回3。
