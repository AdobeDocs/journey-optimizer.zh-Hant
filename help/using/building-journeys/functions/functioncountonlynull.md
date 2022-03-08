---
product: adobe campaign
title: countOnlyNull
description: 瞭解函式countOnlyNull
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 33%

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
