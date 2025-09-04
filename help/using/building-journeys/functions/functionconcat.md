---
product: journey optimizer
title: concat
description: 瞭解函式內容
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: concat，函式，運算式，歷程
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# concat {#concat}

串連兩個字串引數或字串清單。

## 類別

字串

## 函式語法

`concat(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單 | listString |
| 字串 | 字串 |

## 簽章與傳回的型別

`concat(<string>,<string>)`

`concat(<listString>)`

傳回字串。

## 範例

`concat("Hello","World")`

傳回「HelloWorld」。

`concat(["Hello"," ","World"])`

傳回「Hello World」。
