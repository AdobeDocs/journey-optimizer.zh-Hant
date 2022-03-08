---
product: adobe campaign
title: replace
description: 瞭解函式替換
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---

# 替換 {#replace}

用基本字串中的替換字串替換與目標字串匹配的第一個匹配項。

替換從字串的開頭到結尾，例如，在字串&quot;aaa&quot;中將&quot;aa&quot;替換為&quot;b&quot;將導致&quot;ba&quot;而不是&quot;ab&quot;。

## 類別

字串

## 函式語法

`replace(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|--------------|
| 基礎 | 字串 |
| Target | 字串 |
| 替換 | 字串 |

## 簽名和返回的類型

`replace(<base>,<target>,<replacement>)`

返回字串。

## 範例

`replace("Hello World", "l", "x")`

返回&quot;Hexlo World&quot;。
