---
product: adobe campaign
title: inNextMonths
description: 了解NextMonths中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

如果指定的日期或dateTime介於現在和現在+差異月份之間，則傳回true。

## 類別

Date

## 函式語法

`inNextMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽名和返回類型

`inNextMonths(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextMonths(toDateTime('2020-01-12T01:11:00Z'), 4)`

傳回true。
