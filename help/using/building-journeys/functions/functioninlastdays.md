---
product: journey optimizer
title: inLastDays
description: 瞭解函式inLastDays
feature: Journeys
role: Developer
level: Experienced
keywords: inLastDays，函式，運算式，歷程
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 19%

---

# inLastDays {#inLastDays}

如果指定的dateTime介於現在與現在 — 差異天數之間，則傳回true。

## 類別

日期

## 函式語法

`inLastDays(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inLastDays(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。
