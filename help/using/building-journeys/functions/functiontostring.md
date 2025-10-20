---
product: journey optimizer
title: toString
description: 瞭解函式toString
feature: Journeys
role: Engineer
level: Experienced
keywords: toString，函式，運算式，歷程
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# toString {#toString}

根據其型別，將引數值轉換為字串值。 如需資料型別的詳細資訊，請參閱[此頁面](../expression/data-types.md)。

## 類別

轉換

## 函式語法

`toString(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| dateTime | 將日期轉換為UTC日期格式 |
| dateTimeOnly | 將日期轉換為UTC日期格式 |
| 期間 | 轉換為字串形式的對應毫秒數 |
| 整數 | 轉換為值的字串表示法（1會變成「1」） |
| 小數 | 轉換為值的字串表示法（1.5會變成&quot;1.5&quot;） |
| 布林值 | 將布林值轉換為&#39;true&#39; （如果為true），&#39;false&#39; （如果為false） |

## 簽章與傳回型別

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

傳回字串。

## 範例

`toString(4)`

傳回「4」。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

傳回給定dateOnly欄位（XDM日期欄位）的字串表示法，例如「2023-08-18」。

`toString(toDuration(1520))`

傳回「PT1.52S」。
