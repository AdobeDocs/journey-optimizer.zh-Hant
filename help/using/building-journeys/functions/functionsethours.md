---
product: journey optimizer
title: setHours
description: 瞭解函式setHours
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: setHours，函式，運算式，歷程
exl-id: ed78c2a9-d83a-4fac-a2e9-7383da131a1f
source-git-commit: 4e7c4e7e6fcf488f572ccf3e9037e597dde06510
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 9%

---

# setHours {#setHours}

僅設定日期時間或日期時間的小時。 例如，如果您要等到明天的特定小時，則可以強制該小時。

## 類別

日期

## 函式語法

`setHours(<parameter>)`

## 參數

| 參數 | 類型 |
|--- |--- |
| 日期時間 | dateTime |
| 不考慮時區的日期時間 | dateTimeOnly |
| 小時 | 整數 |

## 簽章與傳回型別

`setHours(<dateTime>,<hours>)`

傳回日期時間。

`setHours(<dateTimeOnly>,<hours>)`

傳回日期時間，不考慮時區。

## 範例

`setHours(toDateTime('2023-12-12T01:11:00Z'), 4)`

傳回2023-12-12T04:11:00Z。

`setHours(nowWithDelta(1, "days"), 20)`

傳回明天晚上8:XY，XY是目前時間評估的分鐘數。 如果評估發生在上午2:45，則傳回的時間將會是晚上8:45。
