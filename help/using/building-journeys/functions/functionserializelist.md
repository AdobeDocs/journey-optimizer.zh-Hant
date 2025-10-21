---
product: journey optimizer
title: serializeList
description: 瞭解函式serializeList
feature: Journeys
role: Developer
level: Experienced
keywords: serializeList，函式，運算式，歷程
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

---

# serializeList {#serializeList}

將指定清單（listObject以外的任何型別）轉換為字串。

## 類別

清單

## 函式語法

`serializeList(<parameters>)`

## 參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly | 要轉換為字串的清單。 |
| 分隔符號 | 字串 | 輸出字串中每個清單元素之間的分隔符號。 |
| addQuotes | 布林值 | 此引數指出輸出字串中的每個元素是否應該包含引號(true)。 |

## 簽章與傳回的型別

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

傳回字串。

## 範例

`serializeList(["Hello","World"], " ", false)`

傳回「Hello World」。

`serializeList(["Hello", "World"], ",", true)`

傳回&quot;Hello&quot;、&quot;World&quot;。
