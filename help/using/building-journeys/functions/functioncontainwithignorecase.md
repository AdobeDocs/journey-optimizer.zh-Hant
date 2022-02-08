---
product: adobe campaign
title: containIgnoreCase
description: 瞭解包含IgnoreCase的函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# 包含IgnoreCase {#containIgnoreCase}

檢查第二個參數字串是否包含在第一個參數字串中，而不考慮大小寫。

## 類別

字串

## 函式語法

`containIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 字串搜索 | 字串 |

## Signature and returned type

`containIgnoreCase(<string>,<string>)`

返回布爾值。

## 範例

`containIgnoreCase("rowing is great", "GREAT")`

返回true。
