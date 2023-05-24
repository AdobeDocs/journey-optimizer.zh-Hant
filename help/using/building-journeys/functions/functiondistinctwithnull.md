---
product: journey optimizer
title: distinctWithNull
description: 瞭解函式distinctWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctWithNull，函式，表達式，journey
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---

# distinctWithNull {#distinctWithNull}

返回給定清單的不同值或對象。 如果清單至少有一個空項，則返回的清單中將存在一個空項。

## 類別

清單

## 函式語法

`distinctWithNull(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| 清單至進程 | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位引用。 |
| keyAttributeName | 字串 | 此參數是可選的，且僅適用於listObject。 如果未提供該參數，則如果所有屬性具有相同的值，則對象被視為重複對象。 否則，如果給定屬性具有相同的值，則對象被視為重複對象。 |

## 簽名和返回的類型

`distinctWithNull(<listInteger>)`

返回整數清單。

`distinctWithNull(<listDecimal>)`

返回小數位清單。

`distinctWithNull(<listString>)`

返回字串清單。

`distinctWithNull(<listDateTimeOnly>)`

返回不考慮時區的日期時間清單。

`distinctWithNull(<listDateTime>)`

返回日期時間清單。

`distinctWithNull(<listDateOnly>)`

返回日期清單。

`distinctWithNull(<listBoolean>)`

返回布爾值清單。

`distinctWithNull(<listDuration>)`

返回持續時間清單。

`distinctWithNull(<listObject>)`

`distinctWithNull(<listObject>,<string>)`

返回對象清單。

## 範例

`distinctWithNull([10,2,10,null])`

返回 [10, 2，空]
