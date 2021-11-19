---
product: adobe campaign
title: replaceAll
description: 了解函式replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
source-git-commit: 23f4e8224ea5b00e8132b6a3f3e32f73b0cc993f
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
