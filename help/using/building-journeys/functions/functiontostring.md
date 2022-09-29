---
product: adobe campaign
title: toString
description: 了解函式toString
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 06727146-2a44-4b74-aac4-be60e9e0e37c
source-git-commit: cca94d15da5473aa9890c67af7971f2e745d261e
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 7%

---

# toString {#toString}

根據參數值的類型，將參數值轉換為字串值。 如需資料類型的詳細資訊，請參閱 [本頁](../expression/data-types.md).

## 類別

轉換

## 函式語法

`toString(<parameter>)`

## 參數

| 參數 | 說明 |
|--- |--- |
| dateTime | 轉換UTC日期格式的日期 |
| dateTimeOnly | 轉換UTC日期格式的日期 |
| 持續時間 | 轉換為字串形式的對應毫秒數 |
| 整數 | 轉換為值的字串表示（1變成&quot;1&quot;） |
| 小數 | 轉換為值的字串表示（1.5變成&quot;1.5&quot;） |
| 布林值 | 若為true，則將布林值轉換為&#39;true&#39;；若為false，則將布林值轉換為&#39;false&#39; |

## 簽名和返回類型

`toString(<dateTimeOnly>)`

`toString(<dateTime>)`

`toString(<duration>)`

`toString(<boolean>)`

`toString(<integer>)`

`toString(<decimal>)`

傳回字串。

## 範例

`toString(4)`

傳回&quot;4&quot;。

`toString(#{ExperiencePlatform.test_date.person.birthDate}))`

傳回指定dateOnly欄位（XDM日期欄位）的字串表示法，例如&quot;2016-08-18&quot;。
