---
product: journey optimizer
title: toDateOnly
description: 瞭解函式toDateOnly
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: toDateOnly，函式，運算式，歷程
exl-id: 1929644f-8b51-4f95-aea5-627fc1dd115d
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 10%

---

# toDateOnly{#toDateOnly}

將引數轉換為dateOnly型別值。 如需瞭解資料型別的詳細資訊，請參閱本節 [區段](../expression/data-types.md).

## 類別

轉換

## 函式語法

`toDateOnly(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 以「YYYY-MM-DD」（XDM格式）表示日期的字串表示法。 也支援ISO-8601格式：僅限 **完整日期** 部分已列入考量(請參閱 [RFC 3339,5.6節](https://www.rfc-editor.org/rfc/rfc3339#section-5.6) | 字串 |
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

`toDateOnly("2016-08-18")`

`toDateOnly("2016-08-18T00:00:00.000Z")`

`toDateOnly("2016-08-18T00:00:00")`

所有傳回代表2016-08-18的dateOnly物件。

`toDateOnly(#{ExperiencePlatform.ProfileFieldGroup.person.birthDate})`

傳回dateOnly。
