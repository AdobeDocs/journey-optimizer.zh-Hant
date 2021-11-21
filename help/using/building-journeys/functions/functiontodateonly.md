---
product: adobe campaign
title: toDateOnly
description: 了解函式toDateOnly
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 21%

---

# toDateOnly{#toDateOnly}

將引數值轉換為僅限日期的值。

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 日期格式（XDM日期格式） | 字串 |
| 日期 | 日期 |

## 簽名和返回的類型

`toDateOnly(<date>)`

`toDateOnly(<string>)`

不考慮時區而返回日期時間。

## 範例

`toDateOnly("2016-08-18")`

傳回代表2016-08-18的dateOnly物件。
