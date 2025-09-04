---
product: journey optimizer
title: substr
description: 瞭解函式子字串
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: substr，函式，運算式，歷程
exl-id: 58a3107a-b4f3-43da-b454-5ce597515847
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 17%

---

# substr {#substr}

傳回開始索引和結束索引之間的字串運算式的子字串。 如果未定義結束索引，則它介於開始索引和結束索引之間。

## 類別

字串

## 函式語法

`substr(<parameters>)`

## 參數

| 參數 | 類型 |
|-------------|----------|
| 字串 | 字串 |
| beginindex | 整數 |
| endIndex | 整數 |

## 簽章與傳回的型別

`substr(<string>,<beginIndex>)`

`substr(<string>,<beginIndex>,<endIndex>)`

傳回字串。

## 範例

`substr("Hello World",6)`

傳回「World」。

`substr("Hello World", 0, 5)`

傳回「Hello」。
