---
product: journey optimizer
title: distinct
description: 了解不同的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 6%

---

# distinct {#distinct}

傳回指定清單的不同值或物件。 忽略Null項。

>[!NOTE]
>
>如果目標清單為listObject，則此函式只能用於自訂動作運算式。

## 類別

清單

## 函式語法

`distinct(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此參數為選用，且僅適用於listObject。 如果未提供參數，如果所有屬性具有相同值，則會將物件視為重複項目。 否則，如果給定的屬性具有相同值，則會將物件視為重複。 |

## 簽名和返回的類型

`distinct(<listInteger>)`

傳回整數清單。

`distinct(<listDecimal>)`

傳回小數清單。

`distinct(<listString>)`

傳回字串清單。

`distinct(<listDateTimeOnly>)`

返回不考慮時區的datetimes清單。

`distinct(<listDateTime>)`

返回datetimes清單。

`distinct(<listDateOnly>)`

傳回日期清單。

`distinct(<listBoolean>)`

傳回布林值清單。

`distinct(<listDuration>)`

傳回持續時間清單。

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

返回對象清單。


## 範例

`distinct([10,2,10,null])`

傳回 `[10, 2]`.
