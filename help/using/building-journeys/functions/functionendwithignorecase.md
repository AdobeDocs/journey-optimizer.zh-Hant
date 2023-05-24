---
product: journey optimizer
title: endWithIgnoreCase
description: 瞭解函式endWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWithIgnoreCase，函式，表達式，旅程
exl-id: 278ef1a4-571c-4b5f-b4de-0cfc644ac7d7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 17%

---

# endWithIgnoreCase {#endWithIgnoreCase}

檢查第一個參數字串是否以特定字串結尾（第二個參數字串），而不考慮大小寫。

## 類別

字串

## 函式語法

`endWithIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

## 簽名和返回的類型

`endWithIgnoreCase(<string>,<string>)`

返回布爾值。

## 範例

`endWithIgnoreCase("rowing is great", "AT")`

返回true。
