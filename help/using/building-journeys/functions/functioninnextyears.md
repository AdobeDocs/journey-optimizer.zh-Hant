---
product: journey optimizer
title: inNextYears
description: 了解NextYears中的功能
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextYears，函式，運算式，歷程
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextYears {#inNextYears}

如果指定的date或dateTime介於現在和現在+ delta年之間，則返回true。

## 類別

日期

## 函式語法

`inNextYears(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽名和返回類型

`inNextYears(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

傳回true。
