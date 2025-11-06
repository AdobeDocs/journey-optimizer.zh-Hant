---
solution: Journey Optimizer
product: journey optimizer
title: 函式
description: 瞭解歷程運算式中的函式
feature: Journeys
role: Developer
level: Experienced
keywords: 函式，運算式，編輯器，歷程，資料，操作
exl-id: 5b978eef-7d3e-41fe-bb08-0cf37c3b125d
version: Journey Orchestration
source-git-commit: 99053c6c1327818645adc4ab9a5d3dd30eb96b87
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 9%

---

# 函式 {#functions}

函式是Adobe Journey Optimizer中動態歷程運算式的建置組塊。 它們可讓您即時轉換、計算、驗證和操控資料，以建立個人化的客戶體驗。 有了60多種以直覺式類別組織的功能，您就能在客戶歷程的每個步驟中建立複雜的條件、執行複雜的計算，以及做出資料導向式決策。

## 瞭解函式

歷程運算式中的函式遵循一致的語法模式：

`<function name>`(`<expression as param 1>`， `<expression as param 2>`， ... ，`<expression as param N>`)

**主要特性：**

* **多重簽章**：函式可以有不同的簽章（不同的有序引數集），以因應不同的使用案例
* **型別特定的傳回**：每個函式都有特定的傳回型別（字串、整數、布林值、日期、清單等）
* **Zero到N引數**：函式可以接受0-N運算式做為排序引數，提供您使用它們的彈性

## 為何使用函式？

函式可讓您：

* **建立動態條件** — 根據即時資料評估的分支歷程路徑
* **大規模個人化** — 使用客戶資料和行為分析量身打造內容和體驗
* **自動化決策** — 無需手動介入即可建置智慧型邏輯
* **轉換資料** — 轉換、格式化及操控資料型別，以確保相容性
* **執行計算** — 執行數學運算和統計分析
* **驗證輸入** — 在採取行動之前檢查資料品質和完整性

## 函式（依類別）

瀏覽依主要目的組織的功能，以快速找到符合您需求的適當工具。

### Adobe Experience Platform {#aep-functions}

**對象細分與目標定位**

評估對象成員資格，以根據Adobe Experience Platform中定義的客戶區段建立個人化歷程路徑。

| 函數 | 說明 |
|----------|-------------|
| [inAudience](../functions/functioninaudience.md) | 檢查個人是否屬於特定對象 |

[檢視Adobe Experience Platform函式詳細資料→](../functions/functioninaudience.md)

### 聚合函式 {#aggregation-functions}

**統計計算和資料摘要**

對值集執行計算，以得出平均值、計數、總和以及最小/最大值等見解。 對於資料導向式決策至關重要。

| 函數 | 說明 |
|----------|-------------|
| [avg](../functions/aggregation-functions.md#avg) | 計算平均值 |
| [count](../functions/aggregation-functions.md#count) | 計算非空元素 |
| [countOnlyNull](../functions/aggregation-functions.md#countOnlyNull) | 只計算null值 |
| [countWithNull](../functions/aggregation-functions.md#countWithNull) | 計算所有元素，包括Null |
| [distinctCount](../functions/aggregation-functions.md#distinctCount) | 計算不重複的非空值 |
| [distinctCountWithNull](../functions/aggregation-functions.md#distinctCountWithNull) | 計算包括Null的不重複值 |
| [max](../functions/aggregation-functions.md#max) | 尋找最大值 |
| [min](../functions/aggregation-functions.md#min) | 尋找最小值 |
| [sum](../functions/aggregation-functions.md#sum) | 計算總和 |

[檢視所有彙總函式→](../functions/aggregation-functions.md)

### 轉換函式 {#conversion-functions}

**資料型別轉換**

在不同型別（字串、整數、小數、布林值、日期、持續時間）之間轉換資料，以確保跨作業和資料來源的相容性。

| 函數 | 說明 |
|----------|-------------|
| [toBool](../functions/conversion-functions.md#toBool) | 轉換為布林值 |
| [toDateOnly](../functions/conversion-functions.md#toDateOnly) | 僅轉換為日期（無時間） |
| [toDateTime](../functions/conversion-functions.md#toDateTime) | 轉換為日期（含時間） |
| [toDateTimeOnly](../functions/conversion-functions.md#toDateTimeOnly) | 轉換為不含時區的日期時間 |
| [toDecimal](../functions/conversion-functions.md#toDecimal) | 轉換為十進位數字 |
| [toDuration](../functions/conversion-functions.md#toDuration) | 轉換為持續時間 |
| [toInteger](../functions/conversion-functions.md#toInteger) | 轉換為整數 |
| [toString](../functions/conversion-functions.md#toString) | 轉換為字串 |

[檢視所有轉換函式→](../functions/conversion-functions.md)

### 日期函式 {#date-functions}

**日期與時間操控**

使用日期、時間和時區來建立以時間為基礎的條件、排程動作並執行暫時性計算。

| 函數 | 說明 |
|----------|-------------|
| [currentTimeInMillis](../functions/date-functions.md#currentTimeInMillis) | 取得目前時間（以毫秒為單位） |
| [inLastDays](../functions/date-functions.md#inLastDays) | 檢查日期是否在過去的N天內 |
| [inLastHours](../functions/date-functions.md#inLastHours) | 檢查日期是否在過去N小時內 |
| [inLastMonths](../functions/date-functions.md#inLastMonths) | 檢查日期是否在過去的N個月內 |
| [inLastYears](../functions/date-functions.md#inLastYears) | 檢查日期是否在過去N年內 |
| [inNextDays](../functions/date-functions.md#inNextDays) | 檢查日期是否在未來N天內 |
| [inNextHours](../functions/date-functions.md#inNextHours) | 檢查日期是否在N小時內 |
| [inNextMonths](../functions/date-functions.md#inNextMonths) | 檢查日期是否在未來N個月內 |
| [inNextYears](../functions/date-functions.md#inNextYears) | 檢查日期是否在未來N年內 |
| [now](../functions/date-functions.md#now) | 取得目前的日期時間 |
| [nowWithDelta](../functions/date-functions.md#nowWithDelta) | 取得目前時間（含位移） |
| [setHours](../functions/date-functions.md#setHours) | 在日期時間中設定特定時數 |
| [setDays](../functions/date-functions.md#setDays) | 在日期時間中設定特定天數 |
| [updateTimeZone](../functions/date-functions.md#updateTimeZone) | 更新日期時間的時區 |

[檢視所有日期函式→](../functions/date-functions.md)

### 清單函式 {#list-functions}

**集合操作和分析**

篩選、排序、轉換和分析陣列和清單，以處理複雜的資料結構並執行設定作業。

| 函數 | 說明 |
|----------|-------------|
| [distinct](../functions/list-functions.md#distinct) | 取得唯一值（不包括Null） |
| [distinctWithNull](../functions/list-functions.md#distinctWithNull) | 取得唯一值（包括空值） |
| [篩選器](../functions/list-functions.md#filter) | 根據條件篩選清單 |
| [getListItem](../functions/list-functions.md#getListItem) | 取得位於特定索引的專案 |
| [in](../functions/list-functions.md#in) | 檢查值是否存在於清單中 |
| [相交](../functions/list-functions.md#intersect) | 尋找清單之間的共同元素 |
| [限制](../functions/list-functions.md#limit) | 限制傳回的專案數 |
| [listSize](../functions/list-functions.md#listSize) | 取得清單大小 |
| [serializeList](../functions/list-functions.md#serializeList) | 將清單轉換為字串 |
| [sort](../functions/list-functions.md#sort) | 排序清單元素 |

[檢視所有清單函式→](../functions/list-functions.md)

### 數學函式 {#math-functions}

**數學運算**

針對資料處理和商業邏輯執行數值計算和轉換。

| 函數 | 說明 |
|----------|-------------|
| [random](../functions/math-functions.md#random) | 產生隨機數字(0-1) |
| [round](../functions/math-functions.md#round) | 四捨五入到最近的整數 |

[檢視所有數學函式→](../functions/math-functions.md)

### 字串函式 {#string-functions}

**文字操作與驗證**

處理、轉換、搜尋及驗證文字資料，以建立動態內容與條件式邏輯。

| 函數 | 說明 |
|----------|-------------|
| [concat](../functions/string-functions.md#concat) | 串連字串 |
| [contain](../functions/string-functions.md#contain) | 檢查字串是否包含子字串 |
| [containIgnoreCase](../functions/string-functions.md#containIgnoreCase) | 檢查包含（不區分大小寫） |
| [endWith](../functions/string-functions.md#endWith) | 檢查字串結尾是否為尾碼 |
| [endWithIgnoreCase](../functions/string-functions.md#endWithIgnoreCase) | 檢查結尾為（不區分大小寫） |
| [equalIgnoreCase](../functions/string-functions.md#equalIgnoreCase) | 比較字串（不區分大小寫） |
| [indexOf](../functions/string-functions.md#indexOf) | 尋找第一個出現位置 |
| [isEmpty](../functions/string-functions.md#isEmpty) | 檢查字串是否為空 |
| [isNotEmpty](../functions/string-functions.md#isNotEmpty) | 檢查字串是否非空白 |
| [lastIndexOf](../functions/string-functions.md#lastIndexOf) | 尋找最後一個發生位置 |
| [length](../functions/string-functions.md#length) | 取得字串長度 |
| [lower](../functions/string-functions.md#lower) | 轉換為小寫 |
| [matchRegExp](../functions/string-functions.md#matchRegExp) | 符合規則運算式 |
| [notEqualIgnoreCase](../functions/string-functions.md#notEqualIgnoreCase) | 檢查不等於（不區分大小寫） |
| [replace](../functions/string-functions.md#replace) | 取代第一個專案 |
| [replaceAll](../functions/string-functions.md#replaceAll) | 取代所有出現位置 |
| [split](../functions/string-functions.md#split) | 將字串分割為陣列 |
| [startWith](../functions/string-functions.md#startWith) | 檢查字串的開頭是否為前置詞 |
| [startWithIgnoreCase](../functions/string-functions.md#startWithIgnoreCase) | 檢查開頭為（不區分大小寫） |
| [substr](../functions/string-functions.md#substr) | 擷取子字串 |
| [trim](../functions/string-functions.md#trim) | 移除前置/尾端空格 |
| [upper](../functions/string-functions.md#upper) | 轉換為大寫 |
| [uuid](../functions/string-functions.md#uuid) | 產生UUID |

[檢視所有字串函式→](../functions/string-functions.md)

## 後續步驟

現在您已瞭解可用的功能，請探索：

* **[進階運算式編輯器](expressionadvanced.md)** — 瞭解如何使用進階編輯器建立複雜的運算式
* **[運算式語法](generalities.md)** — 掌握撰寫歷程運算式的語法規則
* **[運運算元](operators.md)** — 探索您可以與函式搭配使用以建置邏輯的運運算元
* **[欄位參考](field-references.md)** — 瞭解如何在運算式中參考資料欄位
