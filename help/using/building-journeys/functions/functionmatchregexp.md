---
product: journey optimizer
title: matchRegExp
description: 瞭解函式matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp，函式，運算式，歷程
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 9e6b3fc5c91e360a9bd7e727949ac5445cd79654
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 19%

---

# matchRegExp {#matchRegExp}

如果第一個引數中的字串符合第二個引數中的規則運算式，則傳回true。 如需詳細資訊，請參閱[此頁面](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)。

## 類別

字串

## 函式語法

`matchRegExp(<parameters>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 字串 | 字串 |
| regexp | 字串 |

## 簽章與傳回的型別

`matchRegExp(<string>,<string>)`

傳回布林值。

## 範例

`matchRegExp("12345", "\\d+")`

傳回true。
