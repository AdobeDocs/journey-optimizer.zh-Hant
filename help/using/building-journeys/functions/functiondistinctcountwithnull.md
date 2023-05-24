---
product: journey optimizer
title: distinctCountWithNull
description: 瞭解函式distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull，函式，表達式，journey
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 22%

---

# distinctCountWithNull {#distinctCountWithNull}

計算包括空值在內的不同值的數量。

>[!NOTE]
>
>如果目標清單是listObject，則此函式只能用於自定義操作表達式。

## 類別

彙總

## 函式語法

`distinctCountWithNull(<listAny>)`

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

`distinctCountWithNull(<listAny>)`

返回整數。

## 範例

`distinctCountWithNull([10,2,10,null])`

返回3。
