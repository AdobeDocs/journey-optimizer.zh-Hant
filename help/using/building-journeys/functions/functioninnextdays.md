---
product: journey optimizer
title: inNextDays
description: 瞭解NextDays中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextDays，函式，表達式， journey
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextDays {#inNextDays}

如果給定日期或dateTime介於現在和現在+增量天之間，則返回true。

## 類別

日期

## 函式語法

`inNextDays(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inNextDays(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inNextDays(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
