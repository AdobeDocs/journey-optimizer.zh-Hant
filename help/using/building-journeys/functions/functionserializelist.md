---
product: journey optimizer
title: serializeList
description: 瞭解函式serializeList
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: serializeList，函式，運算式，歷程
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 21%

---

# serializeList {#serializeList}

將第一個引數中指定的清單（任何型別）轉換為字串。 第二個引數代表要使用的分隔符號。 第三個引數是布林值，指出運算式的每個元素是否應該包含引號。

## 類別

清單

## 函式語法

`serializeList(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 布林值 | 布林值 |
| DateTimeOnly | DateTimeOnly |
| 清單 | listString |
| 清單 | listBoolean |
| 清單 | listPoint |
| 清單 | listDecimal |
| 清單 | listDuration |
| 清單 | listDateTime |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

## 簽章和傳回的型別

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

傳回字串。

## 範例

`serializeList(["Hello","World"], " ", false)`

傳回「Hello World」。

`serializeList(["Hello", "World"], ",", true)`

傳回「Hello」、「World」。
