---
product: adobe campaign
title: inLastMonths
description: 了解LastMonths中的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 4933ef43-66b8-462d-867c-03edd4c34947
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---

# inLastMonths {#inLastMonths}

如果指定的date或dateTime介於now與now - now - delta months之間，則傳回true。

## 類別

Date

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
