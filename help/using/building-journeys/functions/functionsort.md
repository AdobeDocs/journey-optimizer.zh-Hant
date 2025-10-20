---
product: journey optimizer
title: sort
description: 瞭解函式排序
feature: Journeys
role: Engineer
level: Experienced
keywords: 排序，函式，運算式，歷程
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 7%

---

# sort {#sort}

以自然順序排序值或物件清單。

## 類別

清單

## 函式語法

`sort(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToSort | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要排序的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數僅適用於listObject。 指定清單物件中的屬性名稱會作為排序的索引鍵。 |
| sortingOrder | 布林值 | 遞增(true)或遞減(false) |

## 簽章與傳回的型別

`sort(<listInteger>,<boolean>)`

傳回整數清單。

`sort(<listDecimal>,<boolean>)`

傳回小數點清單。

`sort(<listString>,<boolean>)`

傳回字串清單。

`sort(<listDateTimeOnly>,<boolean>)`

傳回日期時間清單，不考慮時區。

`sort(<listDateTime>,<boolean>)`

傳回日期時間清單。

`sort(<listDateOnly>,<boolean>)`

傳回日期清單。

`sort(<listBoolean>,<boolean>)`

傳回布林值清單。

`sort(<listObject>,<string>,<boolean>)`

傳回物件清單。

## 範例

`sort(["A", "C", "B"], true)`

傳回`["A","B","C"]`。

`sort([1, 3, 2], false)`

傳回`[3, 2, 1]`。

`sort(@event{my_event.productListItems}, "SKU", true)`

傳回依SKU屬性排序的listObject （遞增順序）

