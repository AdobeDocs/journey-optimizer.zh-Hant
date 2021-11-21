---
product: adobe campaign
title: replaceAll
description: 了解函式replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

---

# replaceAll {#replaceAll}

以基字串中的取代字串取代所有符合目標字串的發生次數。

替換從字串的開頭到結尾，例如，將字串&quot;aaa&quot;中的&quot;aa&quot;取代為&quot;b&quot;將產生&quot;ba&quot;而非&quot;ab&quot;。

## 類別

字串

## 函式語法

`replaceAll(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基礎 | 字串 |
| Target | 字串 |
| 更換 | 字串 |

## 簽名和返回類型

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

傳回字串。

## 範例

`replaceAll("Hello World", "l", "x")`

返回&quot;Hexxo Worxd&quot;。
