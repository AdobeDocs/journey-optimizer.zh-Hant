---
product: journey optimizer
title: notEqualIgnoreCase
description: 瞭解函式notEqualIgnoreCase
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: notEqualIgnoreCase，函式，表達式，journey
exl-id: 74f8cae0-7d2f-4f5e-bc13-837c9bc69ad9
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '41'
ht-degree: 12%

---

# notEqualIgnoreCase {#notEqualIgnoreCase}

檢查帶有第二個參數字串的第一個參數字串是否不同，忽略大小寫注意事項。

## 類別

字串

## 函式語法

`notEqualIgnoreCase(<parameters>)`

## 參數

* 字串

## 簽名和返回的類型

`notEqualIgnoreCase(<string>,<string>)`

返回布爾值。

## 範例

`notEqualIgnoreCase(@{iOSPushPermissionAllowed.device.model}, "iPad")`
