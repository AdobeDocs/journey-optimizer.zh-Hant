---
product: journey optimizer
title: endWith
description: 瞭解函式endWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: endWith，函式，運算式，歷程
exl-id: ae54c127-9de2-42fd-942c-664d2cfe66d2
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# endWith {#endWith}

如果第二個引數是第一個引數的尾碼，則傳回true。

## 類別

字串

## 函式語法

`endWith(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 尾碼 | 字串 |

## 簽章與傳回的型別

`endWith(<string>,<string>)`

傳回布林值。

## 範例

`endWith("Hello World", "World")`

傳回true。

`endWith("Hello World", "Hello")`

傳回false。
