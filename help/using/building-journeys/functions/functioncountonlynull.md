---
product: journey optimizer
title: countOnlyNull
description: 瞭解函式countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull，函式，運算式，歷程
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 14%

---

# countOnlyNull {#countOnlyNull}

計算清單中Null值的數量。

請注意，此函式不支援引數`<listObject>`。

## 類別

彙總

## 函式語法

`countOnlyNull(<listAny>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

## 簽章與傳回的型別

`countOnlyNull(<listAny>)`

傳回整數。

## 範例

`countOnlyNull([10,2,10,null])`

傳回1。
