---
product: journey optimizer
title: countOnlyNull
description: 瞭解函式countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull，函式，表達式，旅程
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 30%

---

# countOnlyNull {#countOnlyNull}

計算清單中空值的數量。

## 類別

彙總

## 函式語法

`countOnlyNull(<listAny>)`

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

`countOnlyNull(<listAny>)`

返回整數。

## 範例

`countOnlyNull([10,2,10,null])`

返回1。
