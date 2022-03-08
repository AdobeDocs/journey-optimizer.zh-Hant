---
product: adobe campaign
title: replaceAll
description: 瞭解函式replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 16%

---

# 全部替換 {#replaceAll}

用基本字串中的替換字串替換與目標字串匹配的所有匹配項。

替換從字串的開頭到結尾，例如，在字串&quot;aaa&quot;中將&quot;aa&quot;替換為&quot;b&quot;將導致&quot;ba&quot;而不是&quot;ab&quot;。

## 類別

字串

## 函式語法

`replaceAll(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基礎 | 字串 |
| Target | 字串 |
| 替換 | 字串 |

## 簽名和返回的類型

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

返回字串。

## 範例

`replaceAll("Hello World", "l", "x")`

返回&quot;Hexxo Worxd&quot;。
