---
product: journey optimizer
title: distinct
description: 瞭解不同的函式
feature: Journeys
role: Engineer
level: Experienced
keywords: distinct，函式，運算式，歷程
exl-id: f4e2dd34-b634-4a91-af53-60be155a65d0
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 6%

---

# distinct {#distinct}

傳回給定清單的不同值或物件。 會忽略Null專案。

## 類別

清單

## 函式語法

`distinct(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數是選用專案，且僅適用於listObject。 如果未提供引數，如果所有屬性的值都相同，則會將物件視為重複。 否則，如果給定的屬性具有相同的值，則會將物件視為重複。 |

## 簽章與傳回的型別

`distinct(<listInteger>)`

傳回整數清單。

`distinct(<listDecimal>)`

傳回小數點清單。

`distinct(<listString>)`

傳回字串清單。

`distinct(<listDateTimeOnly>)`

傳回日期時間清單，不考慮時區。

`distinct(<listDateTime>)`

傳回日期時間清單。

`distinct(<listDateOnly>)`

傳回日期清單。

`distinct(<listBoolean>)`

傳回布林值清單。

`distinct(<listDuration>)`

傳回持續時間清單。

`distinct(<listObject>)`

`distinct(<listObject>,<string>)`

傳回物件清單。


## 範例

`distinct([10,2,10,null])`

傳回`[10, 2]`。
