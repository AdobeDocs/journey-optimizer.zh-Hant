---
product: journey optimizer
title: endWithIgnoreCase
description: 瞭解函式endWithIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: endWithIgnoreCase，函式，運算式，歷程
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

檢查第一個引數字串是否以特定字串（第二個引數字串）結尾，並未考慮大小寫。

## 類別

字串

## 函式語法

`endWithIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

## 簽章與傳回的型別

`endWithIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`endWithIgnoreCase("rowing is great", "AT")`

傳回true。
