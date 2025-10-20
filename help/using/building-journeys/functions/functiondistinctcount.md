---
product: journey optimizer
title: distinctCount
description: 瞭解函式distinctCount
feature: Journeys
role: Engineer
level: Experienced
keywords: distinctCount，函式，運算式，歷程
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 7%

---

# distinctCount{#distinctCount}

計算不同值的數目，忽略null值。

## 類別

彙總

## 函式語法

`distinctCount(<listAny>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數是選用專案，且僅適用於listObject。 如果未提供引數，如果所有屬性的值都相同，則會將物件視為重複。 否則，如果給定的屬性具有相同的值，則會將物件視為重複。 |

## 簽章與傳回的型別

`distinctCount(<listAny>)`

傳回整數。

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

傳回物件清單。


## 範例

`distinctCount([10,2,10,null])`

傳回2。

`distinctCount(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中完全不同的物件數目。

`distinctCount(@event{my_event.productListItems}, "SKU")`

傳回具有不同「SKU」屬性值{}的物件數目。
