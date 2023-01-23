---
product: journey optimizer
title: distinctWithNull
description: 了解函式distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull，函式，運算式，歷程
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---

# distinctWithNull {#distinctWithNull}

傳回指定清單的不同值或物件。 如果清單至少包含一個空條目，則返回的清單中將存在一個空條目。

## 類別

清單

## 函式語法

`distinctWithNull(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此參數為選用，且僅適用於listObject。 如果未提供參數，如果所有屬性具有相同值，則會將物件視為重複項目。 否則，如果給定的屬性具有相同值，則會將物件視為重複。 |

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

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

返回對象清單。

## 範例

`distinctWithNull([10,2,10,null])`

傳回 [10, 2，空]
