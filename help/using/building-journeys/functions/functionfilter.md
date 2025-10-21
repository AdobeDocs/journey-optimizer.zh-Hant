---
product: journey optimizer
title: 篩選
description: 瞭解函式篩選器
feature: Journeys
role: Developer
level: Experienced
keywords: 篩選器，函式，運算式，歷程
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 9%

---

# 篩選{#filter}

傳回listObject，其中物件的索引鍵屬性符合其中一個指定的索引鍵值。

## 類別

清單

## 函式語法

`filter(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToFilter | listObject | 要篩選的物件清單。 它必須是欄位參考。 |
| keyAttributeName | 字串 | 指定清單物件中的屬性名稱，用來作為篩選的索引鍵 |
| keyValueList | list | 用於篩選的索引鍵值陣列 |

## 簽章與傳回的型別

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

傳回listObject。

## 範例

以下是在傳入事件「myevent」中傳遞的裝載範例：

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

您可以使用下列運算式：

```json
filter(
 @event{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

傳回listObject，其中包含以&quot;product2&quot;和&quot;product3&quot;作為ID的兩個物件。
