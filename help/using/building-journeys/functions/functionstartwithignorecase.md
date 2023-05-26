---
product: journey optimizer
title: startWithIgnoreCase
description: 瞭解函式startWithIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: startWithIgnoreCase，函式，運算式，歷程
exl-id: b6bd9f77-272f-4c2b-b085-20ab5f043793
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 22%

---

# startWithIgnoreCase {#startWithIgnoreCase}

如果第二個引數是第一個引數的前置詞，則傳回true，而不考慮大小寫。

## 類別

字串

## 函式語法

`startWithIgnoreCase(<parameters>)`

## 參數

| 參數 | 類型 |
|-------------|--------|
| 字串 | 字串 |
| 前置詞 | 字串 |

## 簽章和傳回的型別

`startWithIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`startWithIgnoreCase("rowing is great", "RO")`

傳回true。
