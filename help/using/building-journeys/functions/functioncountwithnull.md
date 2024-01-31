---
product: journey optimizer
title: countWithNull
description: 瞭解函式countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函式，運算式，歷程
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

計算清單的所有元素，包括null值。

請注意，引數 `<listObject>` 不支援此函式。

## 類別

彙總

## 函式語法

`countWithNull(<listAny>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

## 簽章與傳回的型別

`countWithNull(<listAny>)`

傳回整數。

## 範例

`countWithNull([10,2,10,null])`

傳回4。
