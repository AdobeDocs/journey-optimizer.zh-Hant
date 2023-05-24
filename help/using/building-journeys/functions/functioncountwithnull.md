---
product: journey optimizer
title: countWithNull
description: 瞭解函式countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函式，表達式，journey
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 30%

---

# countWithNull {#countWithNull}

計算清單的所有元素，包括空值。

## 類別

彙總

## 函式語法

`countWithNull(<listAny>)`

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

`countWithNull(<listAny>)`

返回整數。

## 範例

`countWithNull([10,2,10,null])`

返回4。
