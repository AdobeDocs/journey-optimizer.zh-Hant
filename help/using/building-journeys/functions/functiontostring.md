---
product: adobe campaign
title: toString
description: 瞭解函式toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 7%

---

# 到字串 {#toString}

根據參數值的類型將參數值轉換為字串值。 有關資料類型的詳細資訊，請參閱 [此頁](../expression/data-types.md)。

## 類別

轉換

## 函式語法

`toString(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| 日期時間 | 轉換UTC日期格式的日期 |
| 日期僅時間 | 轉換UTC日期格式的日期 |
| 持續時間 | 轉換為字串形式的相應毫秒數 |
| 時區 | 轉換為時區ID字串表示(JODA id) |
| 整數 | 轉換為值的字串表示形式（1變為&quot;1&quot;） |
| 小數 | 轉換為值的字串表示形式（1.5變為&quot;1.5&quot;） |
| 布林值 | 如果為true，則將布爾值轉換為「true」；如果為false，則將布爾值轉換為「false」 |

## 簽名和返回的類型

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<timeZone>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

返回字串。

## 範例

`toString(4)`

返回&quot;4&quot;。
