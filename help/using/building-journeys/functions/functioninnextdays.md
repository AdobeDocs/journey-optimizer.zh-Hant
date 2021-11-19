---
product: adobe campaign
title: inNextDays
description: 了解NextDays中的函式
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inNextDays {#inNextDays}

如果指定的日期或dateTime介於現在和現在+差異天之間，則傳回true。

## 類別

Date

## 函式語法

`inNextDays(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽名和返回類型

`inNextDays(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回true。
