---
product: adobe campaign
title: listSize
description: 了解函式listSize
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 34%

---

# listSize {#listSize}

計算清單中的元素數。

## 類別

清單

## 函式語法

`listSize(<parameters>)`

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

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

`listSize(<listPoint>)`

傳回整數。

## 範例

`listSize([10,2,3])`

返回3。
