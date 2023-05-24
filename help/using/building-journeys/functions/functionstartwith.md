---
product: journey optimizer
title: startWith
description: 瞭解函式startWith
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWith，函式，表達式，journey
exl-id: 1abdf947-2873-4e45-a26c-cb895980e76a
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 23%

---

# startWith {#startWith}

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
