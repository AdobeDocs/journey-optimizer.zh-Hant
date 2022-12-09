---
title: 開始使用Helper函式
description: Journey Optimizer Helper函式程式庫
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: 315c3e8c04b2e3944d0d5b2befb205acbe0ef7c9
workflow-type: tm+mt
source-wordcount: '1744'
ht-degree: 0%

---

# 開始使用Helper函式{#functions}

使用 [!DNL Journey Optimizer] 範本語言，可對資料執行操作，例如計算、資料格式或轉換、條件，以及在個人化內容中處理。 了解個人化語法准則，位於 [本頁](../personalization-syntax.md).

➡️ [了解如何在此影片中使用協助程式功能](#video)

在運算式編輯器的個人化下拉式清單中可用的協助函式中，會運用範本語言，如下所示：

![](../assets/access-helper-functions.png)

在 [!DNL Journey Optimizer] 運算式編輯器、協助程式函式分為三個類別： [函式](#functions-helper), [Helpers](#helper-helper) 和 [運算子](#operators-helper).

選擇類別以訪問子類別和函式。

按一下 `>` 表徵圖。 按一下 `+` 圖示：函式會自動新增至個人化畫面。

按一下 `...` 表徵圖，查看函式的說明並將其添加到收藏夾中。 [深入了解](../personalize.md#fav)

## 函式{#functions-helper}

### 聚合和陣列函式

<table>
    <tr>
        <td><a href="aggregation.md#average">平均</a></td><td>此函式返回陣列內所有選定值的算術平均值</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">計數</a></td><td>此函式會傳回指定陣列中的元素數</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-only-null">僅計數Null</a></td><td>此函式會計算清單中的空值數。</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count-with-null">計數為空</a></td><td>此函式會計算清單中的所有元素，包括空值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">不重複</a></td><td>此函式會從陣列或清單中取得值，且清單中會移除重複值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct-count-with-null">包含Null的不重複計數</a></td><td>此函式會計算包含空值的不同值數</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">第一項</a></td><td>此函式會傳回陣列或清單中的第一個項目</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">陣列中的第一個n</a></td><td>此函式會根據指定的數值運算式，以遞增順序排序時，傳回陣列中的前N個項目</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">在</a></td><td>此函式用於確定項目是否為陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">包含</a></td><td>此函式確定陣列或清單是否包含指定項目</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">相交</a></td><td>此函式確定兩個陣列或清單是否至少具有一個公共成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">陣列中的最後n個</a></td><td>此函式會根據指定的數值運算式，以遞增順序排序時，傳回陣列中的最後一個「N」項目</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">最大值</a></td><td>此函式會傳回陣列中所有選取值中最大的值</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">最低</a></td><td>此函式會傳回陣列中所有選取值的最小值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">不在</a></td><td>此函式確定項目是否不是陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">子集</a></td><td>此函式確定特定陣列（陣列A）是否是另一個陣列（陣列B）的子集，即陣列A中的所有元素是否是陣列B的元素</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">總和</a></td><td>此函式會傳回陣列內所有選取值的總和</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">超集</a></td><td>此函式確定特定陣列（陣列A）是否是另一個陣列（陣列B）的超集，即陣列A是否包含陣列B中的所有元素</td>
    </tr>
</table>

### 日期時間函式{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">年齡</a></td><td>此函式會從指定日期擷取年齡</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">當前時間（以毫秒為單位）</a></td><td>此函式以每秒的時間擷取目前時間</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">日期差異</a></td><td>此函式會擷取兩個日期之間的差異（以天為單位）</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">星期</a></td><td>此函式會擷取一週中的某天</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">一年當中的第幾天</a></td><td>此函式會擷取一年當中的某天</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">日期格式</a></td><td>此函式會格式化日期時間值</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">設定天數</a></td><td>此函式會設定指定日期時間的月份日</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">設定小時數</a></td><td>此函式會設定日期時間的小時數</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">到UTC</a></td><td>此函式將日期時間轉換為UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">一年中的第一週</a></td><td>此函式會傳回一年中的第一週</td>
    </tr>
</table>
</table>

### 映射函式 {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">取得</a></td><td>此函式可用來擷取指定索引鍵之對應的值</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">金鑰</a></td><td>此函式用於檢索給定映射的所有鍵</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">值</a></td><td>此函式會擷取指定地圖的所有值</td>
    </tr>
</table>

### 數學函式 {#math-functions}

<table>
    <tr>
        <td><a href="objects.md#absolute">絕對</a></td><td>此函式會轉換其絕對值的數字</td>
    </tr>
    <tr>
        <td><a href="objects.md#random">隨機</a></td><td>此函式會傳回0到1之間的隨機值</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-down">向下捨入</a></td><td>此函式會捨入數字</td>
    </tr>
    <tr>
        <td><a href="objects.md#round-up">向上</a></td><td>此函式會四捨五入數字</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-percentage">結束百分比</a></td><td>此函式將數字轉換為百分比</td>
    </tr>
    <tr>
        <td><a href="objects.md#to-precision">精準</a></td><td>此函式將數字轉換為所需的精度</td>
    </tr>
</table>

### 物件函式 {#object-functions}

<table>
    <tr>
        <td><a href="objects.md#isNotNull">非空</a></td><td>此函式用於確定對象引用是否存在</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">為null</a></td><td>此函式用於確定對象引用是否不存在</td>
    </tr>
</table>

### 字串函式 {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">駝峰</a></td><td>此函式用於大寫字串每個字詞的首字母</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">Concat</a></td><td>此函式用於將兩個字串合併為一個</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">包含</a></td><td>此函式用於確定字串是否包含指定的子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">不包含</a></td><td>此函式用於判斷字串是否不包含指定的子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">結尾並非為</a></td><td>此函式用於判斷字串是否未以指定的子字串結尾</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">開頭非為</a></td><td>此函式用於判斷字串是否未以指定的子字串開頭</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">編碼64</a></td><td>此函式用於對字串進行編碼或解碼</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">結尾為</a></td><td>此函式用於判斷字串結尾是否為指定的子字串</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">等於</a></td><td>此函式用於判斷字串是否不以指定的子字串開頭，且區分大小寫</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">等於忽略大小寫</a></td><td>此函式用於判斷字串是否不以指定的子字串開頭，且不區分大小寫</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">擷取電子郵件網域</a></td><td>此函式可用來擷取電子郵件地址的網域</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-host">取得url主機</a></td><td>此函式用於取得url主機。</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-path">取得url路徑</a></td><td>此函式用於取得url路徑</td>
    </tr>
    <tr>
        <td><a href="string.md#get-url-protocol">取得URL通訊協定</a></td><td>此函式用於取得URL通訊協定</td>
    </tr>
    <tr>
        <td><a href="string.md#index-of">索引</a></td><td>此函式會傳回第二個參數首次出現的位置（在第一個引數中）。 如果不匹配，則返回–1</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>此函式用於檢查字串或運算式是否為空。</td>
    </tr>
    <tr>
        <td><a href="string.md#is-not-empty">非空白</a></td><td>如果參數中的字串不為空，則此函式會傳回true。</td>
    </tr>
    <tr>
        <td><a href="string.md#last-index-of">上次索引</a></td><td>此函式會傳回第二個參數最後出現次數的位置（在第一個引數中）。 如果不匹配，則返回–1。</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">左修剪</a></td><td>此函式會從字串的開頭移除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#length">長度</a></td><td>此函式用於獲取字串或表達式中的字元數</td>
    </tr>
    <tr>
        <td><a href="string.md#like">贊</a></td><td>此函式用於判斷字串是否符合指定的模式</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">小寫</a></td><td>此函式將字串轉換為小寫字母</td>
    </tr>
    <tr>
        <td><a href="string.md#mask">遮色片</a></td><td>此函式可用來將字串的一部分取代為「X」字元。</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">符合</a></td><td>此函式用於判斷字串是否符合特定規則運算式</td>
    </tr>
    <tr>
        <td><a href="string.md#md5">MD5</a></td><td>此函式會傳回輸入字串的md5雜湊。</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">不等於</a></td><td>此函式用於判斷字串是否不等於指定的字串</td>
    </tr>
    <tr>
        <td><a href="string.md#not-equal-with-ignore-case">不等於忽略大小寫</a></td><td>此函式會比較兩個字串忽略大小寫。</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">規則運算式群組</a></td><td>此函式用於根據提供的規則運算式擷取特定資訊</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">取代</a></td><td>此函式會將字串中的指定子字串取代為另一個子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">全部替換</a></td><td>此函式會以指定的常值「取代」字串，取代符合「目標」之文字的所有子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">右修剪</a></td><td>此函式會從字串的結尾移除空格 </td>
    </tr>
    <tr>
        <td><a href="string.md#split">分割</a></td><td>此函式可用來依指定字元分割字串</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">開頭為</a></td><td>此函式用於判斷字串是否以指定的子字串開頭</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-date">至今的字串</a></td><td>此函式用於將字串轉換為日期。 它會傳回紀元日期作為無效輸入的輸出。</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-integer">從字串轉換為整數</a></td><td>此函式會將字串值轉換為整數值。</td>
    </tr>
    <tr>
        <td><a href="string.md#string-to-number">字串至數字</a></td><td>此函式用於將字串轉換為數字。 它會傳回與無效輸入的輸出相同的字串。</td>
    </tr>
    <tr>
        <td><a href="string.md#sub-string">子字串</a></td><td>此函式返回起始索引和結束索引之間的字串表達式的子字串。</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">標題案例</a></td><td>此函式用於大寫字串每個單詞的前字母</td>
    </tr>
    <tr>
        <td><a href="string.md#to-bool">到布爾</a></td><td>此函式根據參數值的類型將參數值轉換為布爾值。</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time">結束日期時間</a></td><td>此函式用於將字串轉換為日期。 它會傳回紀元日期作為無效輸入的輸出。</td>
    </tr>
    <tr>
        <td><a href="string.md#to-date-time-only">僅截止日期時間</a></td><td>此函式會將引數值轉換為僅限日期時間的值。 它會傳回紀元日期作為無效輸入的輸出。</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">修剪</a></td><td>此函式會從字串的開頭和結尾移除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">大寫</a></td><td>此函式將字串轉換為大寫字母</td>
    </tr>
    <tr>
        <td><a href="string.md#url-decode">Url解碼</a></td><td>此函式可用來將URL編碼字串解碼。</td>
    </tr>
    <tr>
        <td><a href="string.md#url-encode">Url編碼</a></td><td>此函式用於將字串編碼為URL。</td>
    </tr>
</table>


## Helpers{#helper-helper}

Helpers在 [本頁](helpers.md).


<table>
    <tr>
        <td><a href="helpers.md#default">預設後援值</a></td><td>此函式可讓呈現預設的變數</td>
    </tr>
    <tr>
        <td><a href="helpers.md#each">每個</a></td><td>此函式用於迭代過陣列</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">若</a></td><td>此函式用於定義條件塊 — 如果運算式計算傳回true，則會呈現區塊</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">讓</a></td><td>此函式可讓運算式儲存為變數，以供稍後在查詢中使用</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">除非</a></td><td>此函式用於定義條件區塊 — 如果運算式評估傳回false，則會轉譯區塊</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">使用</a></td><td>此函式用於更改template-part的評估令牌</td>
    </tr>
</table>

## 運算子{#operators-helper}

### 算術函式 {#arithmetic-helper}

算術函式用於對值執行基本計算。

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">新增</a></td><td>此運算子用於尋找兩個引數運算式的總和</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">除</a></td><td>此運算子用於查找兩個參數表達式的商</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">乘法</a></td><td>此運算子用於查找兩個參數表達式的乘積</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">余數</a> </td><td>此運算子用於在將兩個引數運算式除以後尋找余數</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">減法</a> </td><td>此運算子會找出兩個運算式之間的差異</td>
    </tr>
</table>


### 布林函式 {#boolean-functions}

布林函式用於對不同元素執行布林邏輯。

<table>
    <tr>
        <td><a href="operators.md#and">和</a></td><td>此運算子建立邏輯連接</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">或</a></td><td>此運算子會建立邏輯分離</td>
    </tr>
</table>


### 比較函式 {#comparison-functions}

比較函式可用來比較不同運算式和值，並據以傳回true或false。

<table>
    <tr>
        <td><a href="operators.md#equals">等於</a></td><td>此操作檢查值是否相等</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">大於</a></td><td>此運算子會檢查第一個值是否大於第二個值</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">大於或等於</a></td><td>此運算子會檢查第一值是否大於或等於第二值</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">小於或等於</a> </td><td>此運算子會檢查第一個值是否小於或等於第二個值</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">不等於</a></td><td>此運算子會檢查給定運算式是否不等於給定值</td>
    </tr>
</table>

## 作法影片{#video}

了解如何使用個人化協助程式函式來轉換個人化值，並了解協助程式函式的不同使用案例。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
