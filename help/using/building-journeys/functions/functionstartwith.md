---
product: adobe campaign
title: startWith
description: 瞭解函式startWith
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '43'
ht-degree: 25%

---

# 開頭 {#startWith}

如果第二個參數是第一個參數的前置詞，則返回true。

## 類別

字串

## 函式語法

`startWith(<parameters>)`

## 參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

## 簽名和返回的類型

`startWith(<string>,<string>)`

返回布爾值。

## 範例

`startWith("Hello World", "Hello")`

返回true。

`startWith("Hello World", "World")`

返回false。
