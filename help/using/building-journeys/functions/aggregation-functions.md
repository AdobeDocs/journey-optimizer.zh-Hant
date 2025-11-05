---
product: journey optimizer
title: 聚合函式
description: 瞭解彙總函式
feature: Journeys
role: Developer
level: Experienced
keywords: 彙總，函式，運算式，歷程，平均，計數，最大值，最小值，總和
version: Journey Orchestration
source-git-commit: 6102fba3ba30b462654e218f08835be53b75e2cc
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 8%

---

# 聚合函式 {#aggregation-functions}

彙總函式會針對一組值執行計算，並傳回單一摘要結果。 這些函式可讓您透過計算平均值、尋找最小值和最大值、計數元素以及加總數值，來分析歷程運算式中的資料。

當您需要以下動作時，請使用彙總函式：

* 從清單或陣列計算統計值（平均、總計、最小值、最大值）
* 計算集合中的元素，包含或排除null值的選項
* 決定資料集中的唯一值
* 根據計算量度做出資料導向式決策

彙總函式會根據其特定行為自動處理null值，讓處理可能包含遺失或未定義值的真實資料更容易。


## avg {#avg}

傳回一組運算式中的平均值（以清單或兩個運算式形式提供）。 會忽略Null值。

+++語法

`avg(<parameter>)`

+++

+++參數

支援的型別：

* listInteger
* listDecimal
* 小數
* 整數

+++

+++簽章與傳回型別

`avg(<listInteger>)`

`avg(<listDecimal>)`

`avg(<decimal>,<decimal>)`

`avg(<decimal>,<integer>)`

`avg(<integer>,<decimal>)`

`avg(<integer>,<integer>)`

傳回小數。

+++

+++範例

`avg(@event{BarBeacon.inventory},5)`

`avg([10,3,8])`

傳回7.0。

`avg(10.2, 3)`

傳回6.6。

+++

## 計數 {#count}

計算清單的元素而不考慮null值。

+++語法

`count(<listAny>)`

`count(<listObject>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 listObject不能包含null物件。 |

+++

+++簽章與傳回型別

`count(<listAny>)`

傳回整數。

+++

+++範例

`count([10,2,10,null])`

傳回3。

`count(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中的物件數目。 備註：listObject不能包含null物件

+++

## countOnlyNull {#countOnlyNull}

計算清單中Null值的數量。

+++語法

`countOnlyNull(<listAny>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

+++

+++簽章與傳回型別

`countOnlyNull(<listAny>)`

傳回整數。

+++

+++範例

`countOnlyNull([10,2,10,null])`

傳回1。

+++

**注意：**&#x200B;此函式不支援引數`<listObject>`。

## countWithNull {#countWithNull}

計算清單的所有元素，包括null值。

+++語法

`countWithNull(<listAny>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

+++

+++簽章與傳回型別

`countWithNull(<listAny>)`

傳回整數。

+++

+++範例

`countWithNull([10,2,10,null])`

傳回4。

+++

**注意：**&#x200B;此函式不支援引數`<listObject>`。

## distinctCount {#distinctCount}

計算不同值的數目，忽略null值。

+++語法

`distinctCount(<listAny>)`

+++

+++參數

| 參數 | 類型 | 說明 |
|-----------|------------------|------------------|
| listToProcess | listString、listBoolean、listInteger、listDecimal、listDuration、listDateTime、listDateTimeOnly、listDateOnly或listObject | 要處理的清單。 對於listObject，它必須是欄位參考。 |
| keyAttributeName | 字串 | 此引數是選用專案，且僅適用於listObject。 如果未提供引數，如果所有屬性的值都相同，則會將物件視為重複。 否則，如果給定的屬性具有相同的值，則會將物件視為重複。 |

+++

+++簽章與傳回型別

`distinctCount(<listAny>)`

傳回整數。

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

傳回物件清單。

+++

+++範例

`distinctCount([10,2,10,null])`

傳回2。

`distinctCount(@event{my_event.productListItems})`

傳回給定物件陣列（listObject型別）中完全不同的物件數目。

`distinctCount(@event{my_event.productListItems}, "SKU")`

傳回具有不同「SKU」屬性值{}的物件數目。

+++

## distinctCountWithNull {#distinctCountWithNull}

計算不同值的數量，包括null值。

+++語法

`distinctCountWithNull(<listAny>)`

+++

+++參數

| 參數 | 類型 |
|-----------|------------------|
| listToProcess | listString， listBoolean， listInteger， listDecimal， listDuration， listDateTime， listDateTimeOnly， listDateOnly |

+++

+++簽章與傳回型別

`distinctCountWithNull(<listAny>)`

傳回整數。

+++

+++範例

`distinctCountWithNull([10,2,10,null])`

傳回3。

+++

**注意：**&#x200B;此函式不支援引數`<listObject>`。

## max {#max}

傳回一組運算式中的最大值，以清單或兩個運算式形式提供。 會忽略Null值。

+++語法

`max(<parameter>)`

+++

+++參數

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 期間
* 整數
* 小數
* dateTime
* dateTimeOnly

+++

+++簽章與傳回的型別

`max(<listDuration>)`

傳回持續時間。

`max(<listInteger>)`

傳回持續時間。

`max(<listDateTimeOnly>)`

傳回日期時間，不考慮時區。

`max(<listDateTime>)`

傳回日期時間。

`max(<listDateOnly>)`

傳回日期。

`max(<listDecimal>)`

傳回小數。

`max(<decimal>,<decimal>)`

傳回小數。

`max(<duration>,<duration>)`

傳回持續時間。

`max(<dateTime>,<dateTime>)`

傳回日期時間。

`max(<dateTimeOnly>,<dateTimeOnly>)`

傳回日期時間，不考慮時區。

`max(<integer>,<integer>)`

傳回整數。

+++

+++範例

`max(@event{BarBeacon.inventory},5)`

`max([10,3,8])`

傳回10。

`max([10,null,8])`

傳回10。

+++

## min {#min}

傳回一組運算式中的最小值，以清單或兩個運算式形式提供。 會忽略Null值。

+++語法

`min(<parameters>)`

+++

+++參數

* listDuration
* listInteger
* listDecimal
* listDateTime
* listDateTimeOnly
* listDateOnly
* 期間
* 整數
* 小數
* dateTime
* dateTimeOnly

+++

+++簽章與傳回的型別

`min(<listDuration>)`

傳回持續時間。

`min(<listInteger>)`

傳回持續時間。

`min(<listDateTimeOnly>)`

傳回日期時間，不考慮時區。

`min(<listDateTime>)`

傳回日期時間。

`min(<listDateOnly>)`

傳回日期。

`min(<listDecimal>)`

傳回小數。

`min(<decimal>,<decimal>)`

傳回小數。

`min(<duration>,<duration>)`

傳回持續時間。

`min(<dateTime>,<dateTime>)`

傳回日期時間。

`min(<dateTimeOnly>,<dateTimeOnly>)`

傳回日期時間，不考慮時區。

`min(<integer>,<integer>)`

傳回整數。

+++

+++範例

`min(@event{BarBeacon.inventory},5)`

`min([10,3,8])`

傳回3。

`min([10,null,8])`

傳回8。

+++

## sum {#sum}

傳回一組運算式的值總和。 會忽略Null值。

+++語法

`sum(<parameters>)`

+++

+++參數

* listInteger
* listDecimal
* 期間
* 整數
* 小數

+++

+++簽章與傳回的型別

`sum(<listDecimal>)`

傳回小數。

`sum(<listInteger>)`

傳回整數。

`sum(<integer>,<integer>)`

傳回整數。

`sum(<decimal>,<decimal>)`

傳回小數。

+++

+++範例

`sum(@event{BarBeacon.inventory},5)`

`sum([10,3,8])`

傳回21。

`sum([10.5,null,8.1])`

傳回18.6。

+++
