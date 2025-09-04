---
product: journey optimizer
title: countWithNull
description: 瞭解函式countWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countWithNull，函式，運算式，歷程
exl-id: 8d53b6d8-f00f-4d1a-b6df-951f84a15430
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# countWithNull {#countWithNull}

計算清單的所有元素，包括null值。

請注意，此函式不支援引數`<listObject>`。

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
