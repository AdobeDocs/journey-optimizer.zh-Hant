---
product: adobe campaign
title: inLastMonths
description: 瞭解LastMonths中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# 在最後一個月 {#inLastMonths}

如果給定日期或dateTime介於現在和現在之間 — 增量月份，則返回true。

## 類別

日期

## 函式語法

`inLastMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inLastMonths(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
