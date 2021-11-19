---
product: adobe campaign
title: distinctWithNull
description: 了解函式distinctWithNull
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: d786f3d42515d65a6574f51b6cff4b85063a0126
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

---

# distinctWithNull {#distinctWithNull}

傳回清單的不同值。 如果清單至少包含一個空值，則返回的清單中將包含一個空值。

## 類別

清單

## 函式語法

`distinctWithNull(<parameter>)`

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

## 簽名和返回的類型

`distinctWithNull(<listInteger>)`

傳回整數清單。

`distinctWithNull(<listDecimal>)`

傳回小數清單。

`distinctWithNull(<listString>)`

傳回字串清單。

`distinctWithNull(<listDateTimeOnly>)`

返回不考慮時區的datetimes清單。

`distinctWithNull(<listDateTime>)`

返回datetimes清單。

`distinctWithNull(<listDateOnly>)`

傳回日期清單。

`distinctWithNull(<listBoolean>)`

傳回布林值清單。

`distinctWithNull(<listDuration>)`

傳回持續時間清單。

## 範例

`distinctWithNull([10,2,10,null])`

傳回 [10, 2，空]
