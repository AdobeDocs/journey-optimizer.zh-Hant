---
product: adobe campaign
title: toDateOnly
description: 瞭解函式toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# toDateOnly{#toDateOnly}

將參數值轉換為僅日期值。

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| ISO-8601或「YYYY-MM-DD」格式的日期（XDM日期格式） | 字串 |
| 日期 | 日期 |

## 簽名和返回的類型

`toDateOnly(<date>)`

`toDateOnly(<string>)`

返回不考慮時區的日期時間。

## 範例

`toDateOnly("2016-08-18")`

返回表示2016-08-18的dateOnly對象。
