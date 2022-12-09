---
product: journey optimizer
title: countWithNull
description: 了解函式countWithNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 0%

---

# countWithNull {#countWithNull}

計算清單的所有元素，包括空值。

## 類別

匯總

## 函式語法

`countWithNull(<listAny>)`

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

`countWithNull(<listAny>)`

傳回整數。

## 範例

`countWithNull([10,2,10,null])`

返回4。
