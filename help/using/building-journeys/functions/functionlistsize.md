---
product: journey optimizer
title: listSize
description: 瞭解函式listSize
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: listSize，函式，運算式，歷程
exl-id: dd378e4d-f65a-495c-ac10-b4209d6b6b88
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 10%

---

# listSize {#listSize}

計算清單中的元素數量。

## 類別

清單

## 函式語法

`listSize(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 listObject不能包含null物件。 |

## 簽章與傳回型別

`listSize(<listInteger>)`

`listSize(<listDecimal>)`

`listSize(<listString>)`

`listSize(<listBoolean>)`

`listSize(<listDateTimeOnly>)`

`listSize(<listDateTime>)`

`listSize(<listDateOnly>)`

`listSize(<listDuration>)`

傳回整數。

`listSize(<listObject>)`

## 範例

`listSize([10,2,3])`

傳回3。

`listSize(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中的物件數目。
