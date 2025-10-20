---
product: journey optimizer
title: 計數
description: 瞭解函式計數
feature: Journeys
role: Engineer
level: Experienced
keywords: 計數，函式，運算式，歷程
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 10%

---

# 計數 {#count}

計算清單的元素而不考慮null值。

## 類別

彙總

## 函式語法

`count(<listAny>)`

`count(<listObject>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 listObject不能包含null物件。 |

## 簽章與傳回型別

`count(<listAny>)`

傳回整數。

## 範例

`count([10,2,10,null])`

傳回3。

`count(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中的物件數目。 備註：listObject不能包含null物件
