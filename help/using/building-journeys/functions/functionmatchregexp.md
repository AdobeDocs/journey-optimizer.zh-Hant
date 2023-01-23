---
product: journey optimizer
title: matchRegExp
description: 了解函式matchRegExp
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: matchRegExp，函式，運算式，歷程
exl-id: 24cf362c-f390-4bb1-be82-a079bc27fa1f
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 17%

---

# matchRegExp {#matchRegExp}

如果第一個參數中的字串符合第二個參數中的規則運算式，則傳回true。 如需詳細資訊，請參閱 [本頁](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html).

## 類別

字串

## 函式語法

`matchRegExp(<parameters>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 字串 | 字串 |
| regexp | 字串 |

## 簽名和返回類型

`matchRegExp(<string>,<string>)`

傳回布林值。

## 範例

`matchRegExp("username@adobe.com", "*adobe")`

傳回true。
