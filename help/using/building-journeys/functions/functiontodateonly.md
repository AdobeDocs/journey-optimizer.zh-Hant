---
product: journey optimizer
title: toDateOnly
description: 瞭解函式toDateOnly
feature: Journeys
role: Developer
level: Experienced
keywords: toDateOnly，函式，運算式，歷程
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

將引數轉換為dateOnly型別值。 若要深入瞭解資料型別，請參閱此[區段](../expression/data-types.md)。

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 以「YYYY-MM-DD」（XDM格式）表示日期的字串表示法。 也支援ISO-8601格式：只考慮&#x200B;**完整日期**&#x200B;部分（請參閱[RFC 3339，第5.6](https://www.rfc-editor.org/rfc/rfc3339#section-5.6)節） | 字串 |
| 日期時間 | dateTime |
| 沒有時區的日期時間 | dateTimeOnly |
| 紀元的整數值（以毫秒為單位） | 整數 |

## 簽章與傳回的型別

`toDateOnly(<dateTime>)`

`toDateOnly(<dateTimeOnly>)`

`toDateOnly(<string>)`

`toDateOnly(<integer>, <integer>, <integer>)`

傳回dateOnly型別值。

## 範例

`toDateOnly("2023-08-18")`

`toDateOnly("2023-08-18T00:00:00.000Z")`

`toDateOnly("2023-08-18T00:00:00")`

所有傳回代表2023-08-18的dateOnly物件。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

傳回dateOnly。
