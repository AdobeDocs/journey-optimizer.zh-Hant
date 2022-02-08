---
product: adobe campaign
title: now
description: 立即瞭解該功能
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# 現在 {#now}

以日期時間格式返回當前日期。 有關資料類型的詳細資訊，請參閱 [此頁](../expression/data-types.md)。

## 類別

日期

## 函式語法

`now(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 |  |

## 簽名和返回的類型

`now()`

`now("<timeZone id>")`

返回dateTime。

## 範例

`now()`

返回2019-06-03T06:30Z。

`toString(now())`

返回「2019-06-03T06:30Z」

`now("Europe/Paris")`

返回2019-06-03T08:30+02:00。
