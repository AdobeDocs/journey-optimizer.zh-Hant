---
product: journey optimizer
title: notEqualIgnoreCase
description: 瞭解函式notEqualIgnoreCase
feature: Journeys
role: Developer
level: Experienced
keywords: notEqualIgnoreCase，函式，運算式，歷程
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

檢查第一個引數字串是否與第二個引數字串不同，忽略大小寫考量。

## 類別

字串

## 函式語法

`notEqualIgnoreCase(<parameters>)`

## 參數

* 字串

## 簽章與傳回的型別

`notEqualIgnoreCase(<string>,<string>)`

傳回布林值。

## 範例

`notEqualIgnoreCase(@event{iOSPushPermissionAllowed.device.model}, "iPad")`
