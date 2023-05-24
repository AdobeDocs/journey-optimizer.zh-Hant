---
product: journey optimizer
title: matchRegExp
description: 瞭解函式matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp，函式，表達式， journey
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 17%

---

# matchRegExp {#matchRegExp}

如果第一個參數中的字串與第二個參數中的規則運算式匹配，則返回true。 有關詳細資訊，請參見 [此頁](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html)。

## 類別

字串

## 函式語法

`matchRegExp(<parameters>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 字串 | 字串 |
| regexp | 字串 |

## 簽名和返回的類型

`matchRegExp(<string>,<string>)`

返回布爾值。

## 範例

`matchRegExp("username@adobe.com", "*adobe")`

返回true。
