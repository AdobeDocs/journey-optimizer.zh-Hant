---
product: journey optimizer
title: '在 '
description: 瞭解中的函式
feature: Journeys
role: Engineer
level: Experienced
keywords: in，函式，運算式，歷程
exl-id: 629b7aa3-8904-453b-ba3c-c6a333b13c81
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 23%

---

# 在  {#in}

檢查第一個引數值是否在清單中。 檢查會透過每個引數值上的「等於」來執行。 如果找到引數值，則傳回true，否則傳回false。

`<expression>`的型別必須與清單的專案相符。 提醒清單的專案型別必須彼此相符。

## 類別

清單

## 函式語法

`in(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 字串 | 字串 |
| 布林值 | 布林值 |
| 整數 | 整數 |
| 小數 | 小數 |
| 持續時間 | 持續時間 |
| 日期時間 | 日期時間 |
| DateTimeOnly | DateTimeOnly |
| 清單 | listString |
| 清單 | listBoolean |
| 清單 | listInteger |
| 清單 | listDecimal |
| 清單 | listDuration |
| 清單 | listDateTime |
| 清單 | listDateTimeOnly |
| 清單 | listDateOnly |

## 簽章與傳回的型別

`in(<integer>,<listInteger>)`

`in(<decimal>,<listDecimal>)`

`in(<string>,<listString>)`

`in(<boolean>,<listBoolean>)`

`in(<dateTimeOnly>,<listDateTimeOnly>)`

`in(<dateTime>,<listDateTime>)`

`in(<dateOnly>,<listDateOnly>)`

`in(<duration>,<listDuration>)`

傳回布林值。

## 範例

`in(4,[4,5,3,4])`

傳回true。

`in(8,[4,5,3,4])`

傳回false。

`in(#{ExperiencePlatform.ProfileFieldGroup.profile.person.gender}, ["male"])`
