---
product: adobe campaign
title: serializeList
description: 瞭解函式serializeList
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 7ead9fa1-59b3-4960-818c-fe6321422952
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 20%

---

# 序列化清單 {#serializeList}

將第一個參數中給定的清單（任何類型）轉換為字串。 第二個參數表示要使用的分隔符。 第三個參數是一個布爾值，指示表達式的每個元素是否應包含引號。

## 類別

清單

## 函式語法

`serializeList(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 布爾型 | 布爾型 |
| 僅日期時間 | 僅日期時間 |
| 清單 | 清單字串 |
| 清單 | list布爾 |
| 清單 | 清單點 |
| 清單 | 清單十進位 |
| 清單 | listDuration（持續時間） |
| 清單 | 清單日期時間 |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

## 簽名和返回的類型

`serializeList(<listInteger>,<string>,<boolean>)`

`serializeList(<listDecimal>,<string>,<boolean>)`

`serializeList(<listString>,<string>,<boolean>)`

`serializeList(<listBoolean>,<string>,<boolean>)`

`serializeList(<listDateTimeOnly>,<string>,<boolean>)`

`serializeList(<listDateTime>,<string>,<boolean>)`

`serializeList(<listDateOnly>,<string>,<boolean>)`

`serializeList(<listDuration>,<string>,<boolean>)`

`serializeList(<listPoint>,<string>,<boolean>)`

返回字串。

## 範例

`serializeList(["Hello","World"], " ", false)`

返回「Hello World」。

`serializeList(["Hello", "World"], ",", true)`

返回「Hello」、「World」。
