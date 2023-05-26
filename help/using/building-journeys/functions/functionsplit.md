---
product: journey optimizer
title: split
description: 瞭解函式分割
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: split， function， expression， journey
exl-id: 37bcdf98-203c-4f82-8d8a-be2b2c45c4e7
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 17%

---

# split {#split}

以分隔字串分割第一個引數字串（第二個引數字串，可以是規則運算式），以產生字串清單（代號）。

## 類別

字串

## 函式語法

`split(<parameters>)`

## 參數

| 參數 | 類型 |
|-----------|------------------|
| 輸入字串 | 字串 |
| 分隔符號字串 | 字串 |

## 簽章和傳回型別

`split(<input string>, <separator string>)`

傳回listString。

## 範例

`split(["A_B_C"], "_")`

傳回 `["A","B","C"]`

具有值「20.45.2.3434」的事件欄位「event.appVersion」的範例

`split(@{event.appVersion}, "\\.")`

傳回 `["20", "45", "2", "3434"]`
