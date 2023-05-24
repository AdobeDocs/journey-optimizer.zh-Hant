---
product: journey optimizer
title: inLastYears
description: 瞭解LastYears中的功能
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inLastYears，函式，表達式，旅程
exl-id: cdf653d2-967e-4a1b-92e5-37dd22f379f9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inLastYears {#inLastYears}

如果給定日期或dateTime介於現在和現在之間 — 增量年，則返回true。

## 類別

日期

## 函式語法

`inLastYears(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inLastYears(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inLastYears(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
