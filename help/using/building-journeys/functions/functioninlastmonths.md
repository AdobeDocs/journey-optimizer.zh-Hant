---
product: journey optimizer
title: inLastMonths
description: 瞭解函式inLastMonths
feature: Journeys
role: Engineer
level: Experienced
keywords: inLastMonths，函式，運算式，歷程
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

如果指定的日期或dateTime介於現在和現在 — 差異月份之間，則傳回true。

## 類別

日期

## 函式語法

`inLastMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inLastMonths(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastMonths(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。
