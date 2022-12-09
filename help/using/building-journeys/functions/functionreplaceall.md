---
product: journey optimizer
title: replaceAll
description: 了解函式replaceAll
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5543e123-a5f4-4153-8709-97eeb9be83ba
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

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
| 目標 | 字串(RegExp) |
| 更換 | 字串 |

## 簽名和返回類型

`replaceAll(<baseString>,<sourceString>,<replacementString>)`

傳回字串。

## 範例{#example}

`replaceAll("Hello World", "l", "x")`

返回&quot;Hexxo Worxd&quot;。

由於目標參數是RegExp，因此根據您要取代的字串，您可能需要逸出某些字元。 請參閱 [本頁](../functions/functionreplace.md#example_2).
