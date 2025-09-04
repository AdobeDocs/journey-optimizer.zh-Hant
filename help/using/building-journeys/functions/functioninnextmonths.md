---
product: journey optimizer
title: inNextMonths
description: 瞭解函式inNextMonths
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextMonths，函式，運算式，歷程
exl-id: e2e520ec-ae9e-4ed6-b50d-606fc6861d56
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextMonths {#inNextMonths}

如果指定的日期或dateTime介於現在和現在+差異月份之間，則傳回true。

## 類別

日期

## 函式語法

`inNextMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inNextMonths(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextMonths(toDateTime('2023-01-12T01:11:00Z'), 4)`

傳回true。
