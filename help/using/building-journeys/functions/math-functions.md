---
product: journey optimizer
title: 數學函式
description: 瞭解數學函式
feature: Journeys
role: Developer
level: Experienced
keywords: 數學，函式，運算式，歷程，計算，數字
version: Journey Orchestration
source-git-commit: bb47ca4957129a4d05aa3d7286409eef0cb62143
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 7%

---

# 數學函式 {#math-functions}

數學函式為歷程運算式中的數值計算提供基本的數學運算。 這些函式可讓您對資料執行精確數值計算和轉換。

當您需要以下作業時使用數學函式：

* 產生測試、抽樣或隨機化的隨機值([random](#random))
* 將十進位數字四捨五入為最接近的整數，以便呈現較乾淨的資料（[四捨五入](#round)）
* 對數值欄位執行數學計算
* 轉換商業邏輯和決策的數值

數學函式會處理十進位和整數型別，並自動管理型別轉換，以確保歷程運算式中的結果準確。

## random {#random}

產生介於0和1之間的隨機數字。

+++語法

`random()`

+++

+++簽章與傳回的型別

`random()`

傳回小數。

+++

## round {#round}

傳回引數最接近的整數值，並會將四捨五入連結至正無限。

+++語法

`round(<parameters>)`

+++

+++參數

* 小數
* 整數

+++

+++簽章與傳回型別

`round(<decimal>)`

`round(<integer>)`

傳回整數。

+++

+++範例

`round(3.14)`

傳回3。

`round(3.54)`

傳回4。

`round(-3.14)`

傳回–3。

`round(3)`

傳回3。

+++

