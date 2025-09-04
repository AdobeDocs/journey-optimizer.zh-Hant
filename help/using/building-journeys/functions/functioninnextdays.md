---
product: journey optimizer
title: inNextDays
description: 瞭解函式inNextDays
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays，函式，運算式，歷程
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

如果指定的日期或日期時間介於現在和現在+差異天數之間，則傳回true。

## 類別

日期

## 函式語法

`inNextDays(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inNextDays(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextDays(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。
