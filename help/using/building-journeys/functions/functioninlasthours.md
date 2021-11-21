---
product: adobe campaign
title: inLastHours
description: 了解inLastHours的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---

# inLastHours {#inLastHours}

如果指定的日期時間介於現在和現在之間 — 差值小時，則傳回true。

## 類別

Date

## 函式語法

`inLastHours(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽名和返回類型

`inLastHours(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

傳回true。

`inLastHours(@{MyEvent.timestamp}, 4)`

傳回true。
