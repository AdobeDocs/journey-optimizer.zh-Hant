---
title: 開始使用Helper函式
description: Journey Optimizer幫助程式函式館
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 9b0b0d8e-a819-4d2e-a241-f3c4d104eab9
source-git-commit: baa98afcc8e5e9be3062c8c16adc7f4ae17b15b7
workflow-type: tm+mt
source-wordcount: '1344'
ht-degree: 4%

---

# 開始使用Helper函式{#functionsL}

使用 [!DNL Journey Optimizer] 模板化語言，用於對資料執行操作，例如計算、資料格式化或轉換、條件，並在個性化的上下文中對它們進行操作。 瞭解中的個性化語法准則 [此頁](../personalization-syntax.md)。

➡️ [瞭解如何使用幫助程式函式](#video) （視頻）

模板化語言用於表達式編輯器個性化下拉清單中提供的幫助函式，如下所示：

![](../assets/access-helper-functions.png)

在 [!DNL Journey Optimizer] 表達式編輯器中，幫助程式函式分為三類： [函式](#functions-helper)。 [幫手](#helper-helper) 和 [運算子](#operators-helper)。

選擇一個類別，以訪問子類別和函式。

通過按一下 `>` 表徵圖 通過按一下 `+` 表徵圖：該功能自動添加到個性化螢幕。

按一下 `...` 表徵圖，查看函式的說明並將其添加到收藏夾。 [了解更多](../personalize.md#fav)

## 函式{#functions-helper}

### 陣列函式

<table>
    <tr>
        <td><a href="aggregation.md#average">平均</a></td><td>此函式返回陣列中所有選定值的算術平均值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">在</a></td><td>此函式用於確定項目是否是陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">最小</a></td><td>此函式返回陣列中所有選定值中最小值</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">計數</a></td><td>此函式返回給定陣列中的元素數</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">包括</a></td><td>此函式確定陣列或清單是否包含給定項</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">不在</a></td><td>此函式確定項目是否不是陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">獨特</a></td><td>此函式從陣列或刪除重複值的清單中獲取值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">交叉</a></td><td>此函式確定兩個陣列或清單是否至少有一個公用成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">子集</a></td><td>此函式確定特定陣列（陣列A）是否是另一陣列（陣列B）的子集，即陣列A中的所有元素是否都是陣列B的元素</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">第一項</a></td><td>此函式返回陣列或清單中的第一項</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">陣列中的最後一個n</a></td><td>此函式返回陣列中最後一個「N」項，當根據給定的數字表達式按升序排序時</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">和</a></td><td>此函式返回陣列內所有選定值的總和</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">陣列中的第一個n</a></td><td>此函式返回陣列中第一個「N」項，當根據給定的數字表達式按升序排序時</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">最大</a></td><td>此函式返回陣列中所有選定值中的最大值</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">超集</a></td><td>此函式確定特定陣列（陣列A）是否是另一陣列（陣列B）的超集，即該陣列A是否包含陣列B中的所有元素</td>
    </tr>
</table>

### 日期時間函式{#date-functions}

<table>
    <tr>
        <td><a href="dates.md#age">年齡</a></td><td>此函式檢索給定日期的年齡</td>
    </tr>
    <tr>
        <td><a href="dates.md#current">當前時間（毫秒）</a></td><td>此函式檢索當前時間（以新紀元毫秒為單位）</td>
    </tr>
    <tr>
        <td><a href="dates.md#date-diff">日期差異</a></td><td>此函式檢索兩個日期（天數）之間的差值</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-week">週中的日</a></td><td>此函式檢索星期幾</td>
    </tr>
    <tr>
        <td><a href="dates.md#day-year">年中的日</a></td><td>此函式檢索年中的某一天</td>
    </tr>
    <tr>
        <td><a href="dates.md#format-date">格式日期</a></td><td>此函式格式化日期時間值</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-days">設定天數</a></td><td>此函式設定給定日期時間的月份日期</td>
    </tr>
    <tr>
        <td><a href="dates.md#set-hours">設定天數</a></td><td>此函式設定日期 — 時間的小時</td>
    </tr>
    <tr>
        <td><a href="dates.md#to-utc">到UTC</a></td><td>此函式將日期時間轉換為UTC</td>
    </tr>
    <tr>
        <td><a href="dates.md#week-of-year">每年</a></td><td>此函式返回年中的周</td>
    </tr>
</table>
</table>

### 映射函式 {#map-functions}

<table>
    <tr>
        <td><a href="maps.md#get">取得</a></td><td>此函式用於檢索給定鍵的映射值</td>
    </tr>
    <tr>
        <td><a href="maps.md#keys">鍵</a></td><td>此函式用於檢索給定映射的所有鍵</td>
    </tr>
    <tr>
        <td><a href="maps.md#values">值</a></td><td>此函式檢索給定映射的所有值</td>
    </tr>
</table>

**對象函式**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">不為空</a></td><td>此函式用於確定是否存在對象引用</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">為空</a></td><td>此函式用於確定對象引用是否不存在</td>
    </tr>
</table>

### 字串函式 {#string-functions}

<table>
    <tr>
        <td><a href="string.md#camelCase">駝峰</a></td><td>此函式用於大寫字串中每個單詞的首字母</td>
    </tr>
    <tr>
        <td><a href="string.md#concat">孔卡</a></td><td>此函式用於將兩個字串組合為一個</td>
    </tr>
    <tr>
        <td><a href="string.md#contains">包含</a></td><td>此函式用於確定字串是否包含指定的子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotContain">不包含</a></td><td>此函式用於確定字串是否不包含指定的子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotEndWith">不以</a></td><td>此函式用於確定字串是否不以指定的子字串結尾</td>
    </tr>
    <tr>
        <td><a href="string.md#doesNotStartWith">不以開頭</a></td><td>此函式用於確定字串是否不以指定的子字串開頭</td>
    </tr>
    <tr>
        <td><a href="string.md#encode64">編碼64</a></td><td>此函式用於對字串進行編碼或解碼</td>
    </tr>
    <tr>
        <td><a href="string.md#endsWith">終止於</a></td><td>此函式用於確定字串是否以指定的子字串結尾</td>
    </tr>
        </tr>
    <tr>
        <td><a href="string.md#equals">等於</a></td><td>此函式用於確定字串是否不以指定的子字串開頭，區分大小寫</td>
    </tr>
    <tr>
        <td><a href="string.md#equalsIgnoreCase">等於忽略大小寫</a></td><td>此函式用於確定字串是否不以指定的子字串開頭，而不區分大小寫</td>
    </tr>
    <tr>
        <td><a href="string.md#extractEmailDomain">提取電子郵件域</a></td><td>此函式用於提取電子郵件地址的域</td>
    </tr>
    <tr>
        <td><a href="string.md#isEmpty">為空</a></td><td>此函式用於檢查字串或表達式是否為空。</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">左修剪</a></td><td>此函式從字串開頭刪除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>此函式用於獲取字串或表達式中的字元數</td>
    </tr>
    <tr>
        <td><a href="string.md#like">像</a></td><td>此函式用於確定字串是否與指定的模式匹配</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">小寫</a></td><td>此函式將字串轉換為小寫字母</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">符合</a></td><td>此函式用於確定字串是否與特定規則運算式匹配</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">不等於</a></td><td>此函式用於確定字串是否不等於指定的字串</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">規則運算式組</a></td><td>此函式用於根據所提供的規則運算式提取特定資訊</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>此函式用另一個子字串替換字串中的給定子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">全部替換</a></td><td>此函式將匹配"target"的文本的所有子字串替換為指定的文本"replacement"字串</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">右修剪</a></td><td>此函式從字串末尾刪除空格 </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>此函式用於按給定字元拆分字串</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">開始於</a></td><td>此函式用於確定字串是否以指定的子字串開頭</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">標題案例</a></td><td>此函式用於大寫字串中每個單詞的首字母</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">修剪</a></td><td>此函式從字串的開頭和結尾刪除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">大寫</a></td><td>此函式將字串轉換為大寫字母</td>
    </tr>
</table>


## 輔助程式{#helper-helper}

幫助程式詳見 [此頁](helpers.md)。


<table>
    <tr>
        <td><a href="helpers.md#each">每個</a></td><td>此函式用於在陣列上迭代</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">若  </a></td><td>此函式用於定義條件塊 — 如果表達式求值返回true，則呈現該塊</td>
    </tr>
    <tr>
        <td><a href="helpers.md#let">讓</a></td><td>此函式允許將表達式儲存為變數，以便稍後在查詢中使用</td>
    </tr>
   <tr>
        <td><a href="helpers.md#unless">除非</a></td><td>此函式用於定義條件塊 — 如果表達式計算返回false，則呈現該塊</td>
    </tr>
    <tr>
        <td><a href="helpers.md#with">與</a></td><td>此函式用於更改template-part的評估令牌</td>
    </tr>
</table>

## 操作者{#operators-helper}

### 算術函式 {#arithmetic-helper}

算術函式用於對值執行基本計算。

<table>
    <tr>
        <td><a href="arithmetic-functions.md#add">添加</a></td><td>此運算子用於查找兩個參數表達式的和</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#divide">除</a></td><td>此運算子用於查找兩個參數表達式的商</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#multiply">乘法</a></td><td>此運算子用於查找兩個參數表達式的乘積</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#remainder">余數</a> </td><td>此運算子用於在分割兩個參數表達式後查找余數</td>
    </tr>
    <tr>
        <td><a href="arithmetic-functions.md#substract">減法</a> </td><td>此運算子查找兩個表達式之間的差異</td>
    </tr>
</table>


### 布爾函式 {#boolean-functions}

布爾函式用於對不同的元素執行布爾邏輯。

<table>
    <tr>
        <td><a href="operators.md#and">和</a></td><td>此運算子建立邏輯連接</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">若  </a></td><td>此運算子根據指定的條件是否為true解析表達式</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Not</a></td><td>此運算子建立邏輯否定</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">或</a></td><td>此運算子建立邏輯斷開</td>
    </tr>
</table>


### 比較函式 {#comparison-functions}

比較函式用於比較不同的表達式和值，從而返回true或false。

<table>
    <tr>
        <td><a href="operators.md#and">等號</a></td><td>此操作檢查值是否相等</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>此運算子檢查第一個值是否大於第二個值</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">大於或等於</a></td><td>此運算子檢查第一值是否大於或等於第二值</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">不等於</a></td><td>此運算子檢查給定表達式是否不等於賦值</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">小於或等於</a> </td><td>此運算子檢查第一值是否小於或等於第二值</td>
    </tr>
</table>

## How-to視頻{#video}

瞭解如何使用個人化協助程式函式來轉換個人化值，並瞭解協助程式函式的不同使用案例。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)
