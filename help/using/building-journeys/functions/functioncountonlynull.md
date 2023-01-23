---
product: journey optimizer
title: countOnlyNull
description: 了解函式countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull，函式，運算式，歷程
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# countOnlyNull {#countOnlyNull}

計算清單中的空值數。

## 類別

彙總

## 函式語法

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

傳回整數。

## 範例

`countOnlyNull([10,2,10,null])`

傳回1。
