---
product: journey optimizer
title: inLastMonths
description: 了解LastMonths中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 0%

---

# inLastMonths {#inLastMonths}

如果指定的date或dateTime介於now與now - now - delta months之間，則返回true。

## 類別

日期

## 函式語法

`inLastMonths(<dateTime>,<delta>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期時間 | dateTime |
| delta | 整數 |

## 簽名和返回類型

`inLastMonths(<dateTime>,<integer>)`

傳回布林值。

## 範例

`inLastMonths(toDateTime('2010-12-12T01:11:00Z'), 4)`

傳回true。
