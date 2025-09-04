---
product: journey optimizer
title: inNextYears
description: 瞭解函式inNextYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears，函式，運算式，歷程
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

如果指定的日期或dateTime介於現在和現在+差異年度之間，則傳回true。

## 類別

日期

## 函式語法

`inNextYears(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inNextYears(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

傳回true。
