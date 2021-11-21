---
product: adobe campaign
title: startWith
description: 了解函式startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# startWith {#startWith}

如果第二個參數是第一個參數的前置詞，則傳回true。

## 類別

字串

## 函式語法

`startWith(<parameters>)`

## 參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

## 簽名和返回類型

`startWith(<string>,<string>)`

傳回布林值。

## 範例

`startWith("Hello World", "Hello")`

傳回true。

`startWith("Hello World", "World")`

傳回false。
