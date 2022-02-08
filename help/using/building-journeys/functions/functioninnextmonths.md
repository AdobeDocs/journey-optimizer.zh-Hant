---
product: adobe campaign
title: inNextMonths
description: 瞭解NextMonths中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# 在下個月 {#inNextMonths}

如果給定日期或dateTime介於現在和現在+增量月份之間，則返回true。

## 類別

日期

## 函式語法

`inNextMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inNextMonths(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

返回true。
