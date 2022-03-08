---
product: adobe campaign
title: inNextDays
description: 瞭解NextDays中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 0cb3e0db-dc5b-4d4e-a057-af030d9bdb21
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# 在下一天 {#inNextDays}

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
