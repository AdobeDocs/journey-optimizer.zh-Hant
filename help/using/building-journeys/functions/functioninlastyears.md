---
product: journey optimizer
title: inLastYears
description: 瞭解函式inLastYears
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears，函式，運算式，歷程
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

如果指定的日期或dateTime介於現在和現在之間 — 差異年份，則傳回true。

## 類別

日期

## 函式語法

`inLastYears(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inLastYears(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastYears(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。
