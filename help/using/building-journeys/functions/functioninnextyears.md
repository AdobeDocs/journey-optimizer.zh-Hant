---
product: adobe campaign
title: inNextYears
description: 瞭解下一年的功能
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e4597772-d53c-4e15-8237-b2460ce31170
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# 下一年 {#inNextYears}

如果給定日期或dateTime介於現在和現在+增量年間，則返回true。

## 類別

日期

## 函式語法

`inNextYears(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inNextYears(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inNextYears(toDateTime('2021-12-12T01:11:00Z'), 4)`

返回true。
