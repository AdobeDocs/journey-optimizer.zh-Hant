---
product: journey optimizer
title: distinctWithNull
description: 瞭解函式distinctWithNull
feature: Journeys
role: Engineer
level: Experienced
keywords: distinctWithNull，函式，運算式，歷程
exl-id: 73fa9837-d2e1-4f0a-a423-cf7728882eba
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---

# distinctWithNull {#distinctWithNull}

傳回給定清單的不同值或物件。 如果清單中至少有一個null專案，則傳回的清單中會出現null專案。

請注意，此函式不支援引數`<listObject>`。

## 類別

清單

## 函式語法

`distinctWithNull(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly | 要處理的清單。 |

## 簽章與傳回的型別

`distinctWithNull(<listInteger>)`

傳回整數清單。

`distinctWithNull(<listDecimal>)`

傳回小數點清單。

`distinctWithNull(<listString>)`

傳回字串清單。

`distinctWithNull(<listDateTimeOnly>)`

傳回日期時間清單，不考慮時區。

`distinctWithNull(<listDateTime>)`

傳回日期時間清單。

`distinctWithNull(<listDateOnly>)`

傳回日期清單。

`distinctWithNull(<listBoolean>)`

傳回布林值清單。

`distinctWithNull(<listDuration>)`

傳回持續時間清單。

## 範例

`distinctWithNull([10,2,10,null])`

傳回[10， 2， null]
