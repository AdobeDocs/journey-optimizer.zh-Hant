---
product: journey optimizer
title: startWithIgnoreCase
description: 了解函式startWithIgnoreCase
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 25%

---

# startWithIgnoreCase {#startWithIgnoreCase}

如果第二個參數是第一個參數的前置詞，而不考慮大小寫，則傳回true。

## 類別

字串

## 函式語法

`startWithIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

## 簽名和返回類型

`startWithIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`startWithIgnoreCase("rowing is great", "RO")`

傳回true。
