---
product: journey optimizer
title: count
description: 了解函式計數
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

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
