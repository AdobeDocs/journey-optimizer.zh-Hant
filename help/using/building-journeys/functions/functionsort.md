---
product: journey optimizer
title: sort
description: 了解函式排序
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 9%

---

# 排序 {#sort}

按自然順序對值或對象清單進行排序。

## 類別

清單

## 函式語法

`sort(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | 清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此參數僅適用於listObject。 指定清單對象中的屬性名稱用作排序的鍵。 |
| sortingOrder | 布林值 | 遞增(true)或遞減(false) |

## 簽名和返回類型

`sort(<listInteger>,<boolean>)`

傳回整數清單。

`sort(<listDecimal>,<boolean>)`

傳回小數清單。

`sort(<listString>,<boolean>)`

傳回字串清單。

`sort(<listDateTimeOnly>,<boolean>)`

返回不考慮時區的datetimes清單。

`sort(<listDateTime>,<boolean>)`

返回datetimes清單。

`sort(<listDateOnly>,<boolean>)`

傳回日期清單。

`sort(<listBoolean>,<boolean>)`

傳回布林值清單。

`sort(<listObject>,<string>,<boolean>)`

返回對象清單。

## 範例

`sort(["A", "C", "B"], true)`

傳回 `["A","B","C"]`.

`sort([1, 3, 2], false)`

傳回 `[3, 2, 1]`.

