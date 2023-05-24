---
product: journey optimizer
title: inNextHours
description: 瞭解NextHours中的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inNextHours，函式，表達式，旅程
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

如果給定日期或dateTime介於現在和現在之間+增量小時數，則返回true。

## 類別

日期

## 函式語法

`inNextHours(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inNextHours(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inNextHours(toDateTime('2010-12-12T01:11:00Z'), 4)`

返回true。
