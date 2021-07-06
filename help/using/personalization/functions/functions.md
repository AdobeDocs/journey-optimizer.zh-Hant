---
title: 幫助程式函式庫
description: Journey Optimizer Helper函式庫
feature: 個性化
topic: 個性化
role: Data Engineer
level: Experienced
source-git-commit: d09eedce833b41037452bb46bc748e7e9f477d0a
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 2%

---


# 幫助程式函式庫{#functionsL}

使用[!DNL Journey Optimizer]範本語言對資料執行操作，例如計算、資料格式或轉換、條件，以及在個人化內容中處理這些操作。 在[本頁面](../personalization-syntax.md)中了解個人化語法准則。

➡️ [探索如何使用協助函式](#video)（影片）

範本語言會運用在運算式編輯器的個人化下拉式清單中可用的協助函式中，如下所示：

![](../assets/access-helper-functions.png)



在[!DNL Journey Optimizer]運算式編輯器中，協助程式函式分為三個類別：[函式](#functions-helper)、[Helpers](#helper-helper)和[操作符](#operators-helper)。

## 函數{#functions-helper}

**陣列函式**

<table>
    <tr>
        <td><a href="aggregation.md#average">平均</a></td><td>此函式返回陣列內所有選定值的算術平均值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#in">在</a></td><td>此函式用於確定項目是否為陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#min">最小</a></td><td>此函式會傳回陣列中所有選取值的最小值</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#count">計數</a></td><td>此函式會傳回指定陣列中的元素數</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#includes">包含</a></td><td>此函式確定陣列或清單是否包含指定項目</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#notin">不在</a></td><td>此函式確定項目是否不是陣列或清單的成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#distinct">不重複</a></td><td>此函式會從陣列或清單中取得值，且清單中會移除重複值</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#intersects">相交</a></td><td>此函式確定兩個陣列或清單是否至少具有一個公共成員</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#subset">子集</a></td><td>此函式確定特定陣列（陣列A）是否是另一個陣列（陣列B）的子集，即陣列A中的所有元素是否是陣列B的元素</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#head">第一項</a></td><td>此函式會傳回陣列或清單中的第一個項目</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#last-n">陣列中的最後n個</a></td><td>此函式會根據指定的數值運算式，以遞增順序排序時，傳回陣列中的最後一個「N」項目</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#sum">總和</a></td><td>此函式會傳回陣列內所有選取值的總和</td>
    </tr>
    <tr>
        <td><a href="arrays-list.md#first-n">陣列中的第一個n</a></td><td>此函式會根據指定的數值運算式，以遞增順序排序時，傳回陣列中的前N個項目</td>
    </tr>
    <tr>
        <td><a href="aggregation.md#max">最大</a></td><td>此函式會傳回陣列中所有選取值中最大的值</td>
    </tr>
    <tr>
    <td><a href="arrays-list.md#superset">超集</a></td><td>此函式確定特定陣列（陣列A）是否是另一個陣列（陣列B）的超集，即陣列A是否包含陣列B中的所有元素</td>
    </tr>
</table>


**映射函式**

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

**物件函式**

<table>
    <tr>
        <td><a href="objects.md#isNotNull">非空</a></td><td>此函式用於確定對象引用是否存在</td>
    </tr>
    <tr>
        <td><a href="objects.md#isNull">為null</a></td><td>此函式用於確定對象引用是否不存在</td>
    </tr>
</table>

**字串函式**

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
        <td><a href="string.md#endsWith">終止於</a></td><td>此函式用於判斷字串結尾是否為指定的子字串</td>
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
        <td><a href="string.md#isEmpty">IsEmpty</a></td><td>此函式用於檢查字串或運算式是否為空。</td>
    </tr>
    <tr>
        <td><a href="string.md#leftTrim">左修剪</a></td><td>此函式會從字串的開頭移除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#length">Length</a></td><td>此函式用於獲取字串或表達式中的字元數</td>
    </tr>
    <tr>
        <td><a href="string.md#like">贊</a></td><td>此函式用於判斷字串是否符合指定的模式</td>
    </tr>
    <tr>
        <td><a href="string.md#lower">小寫</a></td><td>此函式將字串轉換為小寫字母</td>
    </tr>
    <tr>
        <td><a href="string.md#matches">符合</a></td><td>此函式用於判斷字串是否符合特定規則運算式</td>
    </tr>
    <tr>
        <td><a href="string.md#notEqualTo">不等於</a></td><td>此函式用於判斷字串是否不等於指定的字串</td>
    </tr>
    <tr>
        <td><a href="string.md#regexGroup">規則運算式群組</a></td><td>此函式用於根據提供的規則運算式擷取特定資訊</td>
    </tr>
    <tr>
        <td><a href="string.md#replace">Replace</a></td><td>此函式會將字串中的指定子字串取代為另一個子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#replaceAll">全部替換</a></td><td>此函式會以指定的常值「取代」字串，取代符合「目標」之文字的所有子字串</td>
    </tr>
    <tr>
        <td><a href="string.md#rightTrim">右修剪</a></td><td>此函式會從字串的結尾移除空格 </td>
    </tr>
    <tr>
        <td><a href="string.md#split">Split</a></td><td>此函式可用來依指定字元分割字串</td>
    </tr>
    <tr>
        <td><a href="string.md#startsWith">開始於</a></td><td>此函式用於判斷字串是否以指定的子字串開頭</td>
    </tr>
    <tr>
        <td><a href="string.md#titleCase">標題案例</a></td><td>此函式用於大寫字串每個單詞的前字母</td>
    </tr>
    <tr>
        <td><a href="string.md#trim">修剪</a></td><td>此函式會從字串的開頭和結尾移除空格</td>
    </tr>
    <tr>
        <td><a href="string.md#upper">大寫</a></td><td>此函式將字串轉換為大寫字母</td>
    </tr>
</table>


## 輔助程式{#helper-helper}

[本頁](helpers.md)中有詳細的幫助程式。


<table>
    <tr>
        <td><a href="helpers.md#each">每個</a></td><td>此函式用於迭代過陣列</td>
    </tr>
    <tr>
        <td><a href="helpers.md#if-function">若  </a></td><td>此函式用於定義條件塊 — 如果運算式計算傳回true，則會呈現區塊</td>
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

## 操作者{#operators-helper}

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


### 布林函式

布林函式用於對不同元素執行布林邏輯。

<table>
    <tr>
        <td><a href="operators.md#and">和</a></td><td>此運算子建立邏輯連接</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">若  </a></td><td>此運算子會根據指定的條件是否為true來解析運算式</td>
    </tr>
    <tr>
        <td><a href="operators.md#not">Not</a></td><td>此運算子會建立邏輯否定</td>
    </tr>
    <tr>
        <td><a href="operators.md#or">或</a></td><td>此運算子會建立邏輯分離</td>
    </tr>
</table>


### 比較函式

比較函式可用來比較不同運算式和值，並據以傳回true或false。

<table>
    <tr>
        <td><a href="operators.md#and">等號</a></td><td>此操作檢查值是否相等</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthan">Greater than</a></td><td>此運算子會檢查第一個值是否大於第二個值</td>
    </tr>
    <tr>
        <td><a href="operators.md#greaterthanorequal">大於或等於</a></td><td>此運算子會檢查第一值是否大於或等於第二值</td>
    </tr>
    <tr>
        <td><a href="operators.md#notequal">不等於</a></td><td>此運算子會檢查給定運算式是否不等於給定值</td>
    </tr>
    <tr>
        <td><a href="operators.md#lessthanorequal">小於或等於</a> </td><td>此運算子會檢查第一個值是否小於或等於第二個值</td>
    </tr>
</table>

## 作法影片{#video}

了解如何使用個人化協助程式函式來轉換個人化值，並了解協助程式函式的不同使用案例。

>[!VIDEO](https://video.tv.adobe.com/v/334244?quality=12)