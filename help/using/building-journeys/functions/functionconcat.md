---
product: adobe campaign
title: concat
description: 了解函式概念
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 690c8aa9-f754-4720-b4ed-a338e5d3b79d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '40'
ht-degree: 27%

---

# concat {#concat}

串連兩個字串參數或字串清單。

## 類別

字串

## 函式語法

`concat(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 清單 | listString |
| 字串 | 字串 |

## 簽名和返回類型

`concat(<string>,<string>)`

`concat(<listString>)`

傳回字串。

## 範例

`concat("Hello","World")`

返回&quot;HelloWorld&quot;。

`concat(["Hello"," ","World"])`

返回&quot;Hello World&quot;。
