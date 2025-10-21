---
product: journey optimizer
title: split
description: 瞭解函式分割
feature: Journeys
role: Developer
level: Experienced
keywords: 分割，函式，運算式，歷程
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 14%

---

# split {#split}

以分隔字串分割第一個引數字串（第二個引數字串，可以是規則運算式），以產生字串（代號）清單。

## 類別

字串

## 函式語法

`split(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 輸入字串 | 字串 |
| 分隔符號字串 | 字串 |

## 簽章與傳回型別

`split(<input string>, <separator string>)`

傳回listString。

## 範例

`split("A_B_C", "_")`

傳回`["A","B","C"]`

具有下列值的事件欄位「event.appVersion」範例：「20.45.2.3434」

`split(@event{event.appVersion}, "\\.")`

傳回`["20", "45", "2", "3434"]`
