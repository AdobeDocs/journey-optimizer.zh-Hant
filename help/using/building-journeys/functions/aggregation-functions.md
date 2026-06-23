---
product: journey optimizer
title: 彙總函式
description: 瞭解彙總函式
feature: Journeys
role: Developer
level: Experienced
keywords: 彙總，函式，運算式，歷程，平均，計數，最大值，最小值，總和
version: Journey Orchestration
exl-id: 871a5212-5b94-4a54-bf1d-276022be3c95
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1105
ht-degree: 5%

---

# 彙總函式 {#aggregation-functions}

彙總函式會針對一組值執行計算，並傳回單一摘要結果。 這些函式可讓您透過計算平均值、尋找最小值和最大值、計數元素以及加總數值，來分析歷程運算式中的資料。

當您需要以下動作時，請使用彙總函式：

* 從清單或陣列計算統計值([avg](#avg)，[sum](#sum)，[min](#min)，[max](#max))
* 集合中的計數元素([count](#count)， [countOnlyNull](#countOnlyNull)， [countWithNull](#countWithNull))，包含或排除null值的選項
* 決定資料集內的唯一值([distinctCount](#distinctCount)， [distinctCountWithNull](#distinctCountWithNull))
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

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;本頁會記錄AJO歷程運算式中可用的所有彙總函式，包括如何計算清單與陣列上的平均值、總和、最小值/最大值、計數及相異計數。

**意圖：**
* 使用`avg`計算數值清單的平均值
* 使用`sum`加總清單或事件欄位中的數值
* 使用`min`或`max`尋找清單中的最小值或最大值
* 使用`count`、`countOnlyNull`或`countWithNull`計算清單中的非null、僅限null或所有元素
* 使用`distinctCount`或`distinctCountWithNull`計算清單中不同的值（無論有無null）
* 使用`distinctCount`搭配索引鍵引數，依特定索引鍵屬性篩選listObject中的唯一物件

**字彙表：**
* **listObject**：複雜物件的清單（欄位參考）；不能包含Null物件&#x200B;*（產品特定）*
* **listAny**：任何支援的純量型別（字串、布林值、整數、小數、持續時間、dateTime、dateTimeOnly、dateOnly）清單&#x200B;*（產品特定）*
* **Null值**：清單中有不存在或未定義的專案；大多數彙總函式會忽略null，除非函式明確處理它們（例如，`countOnlyNull`、`countWithNull`、`distinctCountWithNull`）

**護欄：**
* `countOnlyNull`、`countWithNull`和`distinctCountWithNull`不支援`<listObject>`引數型別
* `listObject`上的`distinctCount`要求清單是欄位參考，而非內嵌常值
* `listObject`上的`count`需要清單為欄位參考；listObject不能包含null物件

**術語：**
* 正式名稱：彙總函式 — 首字母縮寫：none — 變體：彙總函式、集合函式
* 同義字： &quot;count&quot; = &quot;count non-null elements&quot;； &quot;countWithNull&quot; = &quot;count all elements include null&quot;
* 請勿混淆：「distinctCount」（忽略null）≠「distinctCountWithNull」（包含null作為不同值）

**常見問題集：**
* **問： `avg`是否在計算中包含Null值？**  — 否，`avg`會自動忽略null值。
* **問：`count`與`countWithNull`之間有何差異？** — `count`會從總計中排除null值，而`countWithNull`會計算每個元素（包括null）。
* **問：我可以在listObject上使用`countOnlyNull`嗎？**  — 否，`countOnlyNull`、`countWithNull`或`distinctCountWithNull`不支援`<listObject>`。
* **問：我如何根據特定屬性計算陣列中不同的物件？**  — 使用`distinctCount(@event{...}, "attributeName")`提供索引鍵屬性名稱做為第二個引數。
* **問：當清單包含null時，`max`會傳回什麼？** — `max`會忽略null值，並傳回非null元素中的最大值。

+++
