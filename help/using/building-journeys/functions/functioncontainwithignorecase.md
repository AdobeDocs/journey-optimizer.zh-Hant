---
product: journey optimizer
title: containIgnoreCase
description: 瞭解包含IgnoreCase的函式
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase，函式，表達式，journey
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

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

## 簽名和返回的類型

`containIgnoreCase(<string>,<string>)`

返回布爾值。

## 範例

`containIgnoreCase("rowing is great", "GREAT")`

返回true。
