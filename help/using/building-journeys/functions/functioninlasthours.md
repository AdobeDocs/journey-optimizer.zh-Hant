---
product: adobe campaign
title: inLastHours
description: 瞭解LastHours中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: c648d711-c81b-403b-9adb-792c7e79e4e2
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 17%

---

# 在最後時間 {#inLastHours}

如果給定日期時間介於現在和現在之間 — 增量小時數，則返回true。

## 類別

日期

## 函式語法

`inLastHours(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | 日期時間 |
| 三角 | 整數 |

## 簽名和返回的類型

`inLastHours(<dateTime>,<integer>)`

返回布爾值。

## 範例

`inLastHours(toDateTime('2019-12-12T01:11:00Z'), 4)`

返回true。

`inLastHours(@{MyEvent.timestamp}, 4)`

返回true。
