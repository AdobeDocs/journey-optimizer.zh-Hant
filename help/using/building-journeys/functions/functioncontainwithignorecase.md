---
product: journey optimizer
title: containIgnoreCase
description: 瞭解函式containIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: containIgnoreCase，函式，運算式，歷程
exl-id: 26074584-a215-4515-8a61-7460bd9d4447
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# containIgnoreCase {#containIgnoreCase}

檢查第二個引數字串是否包含在第一個引數字串中，而不考慮大小寫。

## 類別

字串

## 函式語法

`containIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 搜尋的字串 | 字串 |

## 簽章與傳回的型別

`containIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`containIgnoreCase("rowing is great", "GREAT")`

傳回true。
