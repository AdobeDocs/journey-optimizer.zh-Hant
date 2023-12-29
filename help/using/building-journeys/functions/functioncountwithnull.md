---
product: journey optimizer
title: countWithNull
description: 瞭解函式countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函式，運算式，歷程
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 14%

---

# countWithNull {#countWithNull}

計算清單的所有元素，包括null值。

## 類別

彙總

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

## 簽章與傳回的型別

`countWithNull(<listAny>)`

傳回整數。

## 範例

`countWithNull([10,2,10,null])`

傳回4。
