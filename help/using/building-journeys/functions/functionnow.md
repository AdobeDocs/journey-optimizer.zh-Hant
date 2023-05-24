---
product: journey optimizer
title: now
description: 立即瞭解該功能
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: 現在，函式，表達，旅程
exl-id: 16dcc772-e48d-4f10-be75-62dd39473556
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 16%

---

# now {#now}

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
