---
product: journey optimizer
title: limit
description: 了解函式限制
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7fa1e393-2912-4392-b759-e54d08d5635a
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 8%

---

# 限制 {#limit}

傳回清單的第一個或最後一個N個元素。

## 類別

清單

## 函式語法

`limit(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | 清單。 對於listObject，它必須是欄位參考。 |
| numberOfItems | 整數 | 要從給定清單返回的項目數。 |
| firstOrLastItems | 布林值 | 此參數為選用項目（預設為true）。 true會傳回第一個項目。 false會傳回最後一個項目。 |

## 簽名和返回類型

`limit(<listString>,<integer>)`
`limit(<listString>,<integer>,<boolean>)`

傳回字串清單。

`limit(<listInteger>,<integer>)`
`limit(<listInteger>,<integer>,<boolean>)`

傳回整數清單。

`limit(<listDecimal>,<integer>)`
`limit(<listDecimal>,<integer>,<boolean>)`

傳回小數清單。

`limit(<listBoolean>,<integer>)`
`limit(<listBoolean>,<integer>,<boolean>)`

傳回布林值清單。

`limit(<listDateOnly>,<integer>)`
`limit(<listDateOnly>,<integer>,<boolean>)`

傳回日期清單。

`limit(<listDateTimeOnly>,<integer>)`
`limit(<listDateTimeOnly>,<integer>,<boolean>)`

返回不考慮時區的datetimes清單。

`limit(<listDateTime>,integer>)`
`limit(<listDateTime>,<integer>,<boolean>)`

返回datetimes清單。

`limit(<listDuration>,<integer>)`
`limit(<listDuration>,<integer>,<boolean>)`

傳回持續時間清單。

`limit(<listObject>,<integer>)`
`limit(<listObject>,<integer>,<boolean>)`

返回對象清單。

## 範例

`limit(["A", "B", "C", "D", "E"], 3)`

傳回 `["A","B","C"]`.

`limit(["A", "B", "C", "D", "E"], 3, false)`

傳回 `["C","D","E"]`.
