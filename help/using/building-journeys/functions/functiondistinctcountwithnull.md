---
product: journey optimizer
title: distinctCountWithNull
description: 瞭解函式distinctCountWithNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: distinctCountWithNull，函式，運算式，歷程
exl-id: 2c3f629f-2220-44a4-9b0c-8aa602301098
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---

# distinctCountWithNull {#distinctCountWithNull}

計算不同值的數量，包括null值。

請注意，此函式不支援引數`<listObject>`。

## 類別

彙總

## 函式語法

`distinctCountWithNull(<listAny>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

## 簽章與傳回的型別

`distinctCountWithNull(<listAny>)`

傳回整數。

## 範例

`distinctCountWithNull([10,2,10,null])`

傳回3。
