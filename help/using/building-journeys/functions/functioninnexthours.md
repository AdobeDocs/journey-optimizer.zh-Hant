---
product: journey optimizer
title: inNextHours
description: 瞭解inNextHours函式
feature: Journeys
role: Developer
level: Experienced
keywords: inNextHours，函式，運算式，歷程
exl-id: 079a91b6-49c5-4e68-a240-358ed0cded92
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# inNextHours {#inNextHours}

如果指定的日期或日期時間介於現在和現在+差異小時之間，則傳回true。

## 類別

日期

## 函式語法

`inNextHours(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽章與傳回型別

`inNextHours(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inNextHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回true。
