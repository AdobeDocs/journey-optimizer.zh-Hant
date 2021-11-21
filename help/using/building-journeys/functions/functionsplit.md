---
product: adobe campaign
title: split
description: 了解函式分割
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 2022b2c81738ae6d3e66280265948c5b88a117c8
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---

# split {#split}

使用分隔符字串（第二個引數字串，可以是規則運算式）來分割第一個引數字串，以產生字串清單（代號）。

## 類別

字串

## 函式語法

`split(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 輸入字串 | 字串 |
| 分隔字串 | 字串 |

## 簽名和返回類型

`split(<input string>, <separator string>)`

傳回listString。

## 範例

`split(["A_B_C"], "_")`

傳回 `["A","B","C"]`

事件欄位為「event.appVersion」且值為的範例：&quot;20.45.2.3434&quot;

`split(@{event.appVersion}, "\\.")`

傳回 `["20", "45", "2", "3434"]`
