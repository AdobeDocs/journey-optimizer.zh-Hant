---
product: journey optimizer
title: inLastDays
description: 瞭解LastDays中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastDays，函式，表達式， journey
exl-id: 1b150568-17c2-454d-847e-17bac3d0b35d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastDays {#inLastDays}

如果給定日期或dateTime介於現在和現在之間 — 增量天，則返回true。

## 類別

日期

## 函式語法

`inLastDays(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inLastDays(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inLastDays(toDateTime('2019-12-12T01:11:00Z'), 4)`

返回true。
