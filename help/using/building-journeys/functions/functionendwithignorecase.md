---
product: adobe campaign
title: endWithIgnoreCase
description: 了解函式endWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 18%

---

# endWithIgnoreCase {#endWithIgnoreCase}

檢查第一個引數字串結尾是否為特定字串（第二個引數字串），不考慮大小寫。

## 類別

字串

## 函式語法

`endWithIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

## 簽名和返回類型

`endWithIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`endWithIgnoreCase("rowing is great", "AT")`

傳回true。
