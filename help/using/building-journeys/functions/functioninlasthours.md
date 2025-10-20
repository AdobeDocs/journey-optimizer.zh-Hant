---
product: journey optimizer
title: inLastHours
description: 瞭解函式inLastHours
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastHours，函式，運算式，歷程
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# inLastHours {#inLastHours}

如果指定的日期時間介於現在和現在之間 — 差異小時，則傳回true。

## 類別

日期

## 函式語法

`inLastHours(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inLastHours(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。

`inLastHours(@event{MyEvent.timestamp}, 4)`

傳回true。
