---
product: adobe campaign
title: now
description: 立即了解函式
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 18%

---

# now {#now}

以日期時間格式傳回目前日期。 如需資料類型的詳細資訊，請參閱 [本頁](../expression/data-types.md).

## 類別

Date

## 函式語法

`now(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 字串 |  |

## 簽名和返回類型

`now()`

`now("<timeZone id>")`

傳回dateTime。

## 範例

`now()`

傳回2019-06-03T06:30Z。

`toString(now())`

傳回「2019-06-03T06:30Z」

`now("Europe/Paris")`

傳回2019-06-03T08:30+02:00。
