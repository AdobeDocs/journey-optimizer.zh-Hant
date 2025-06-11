---
solution: Journey Optimizer
product: journey optimizer
title: 編輯運算式
description: 瞭解如何編輯運算式。
badge: label="Alpha"
hide: true
exl-id: bf0a905f-00af-4ed7-9e4f-bf8cb0af9ea9
source-git-commit: 38d4cc896414fce2e8453940fb4674ce7e60fd2b
workflow-type: tm+mt
source-wordcount: '2035'
ht-degree: 30%

---


# 編輯運算式 {#edit-expressions}

>[!NOTE]
>
>下節提供如何使用運算式編輯器建立規則的資訊。 請記住，用來建置規則的語法與用來新增個人化的語法不同。

## 使用運算式編輯器 {#edit}

編輯運算式需要手動輸入條件以形成規則。 此模式可讓您使用進階函式，這些函式可讓您控制用於執行特定查詢的值，例如控制日期、字串、數值欄位和排序。

設定自訂條件時，可從規則產生器&#x200B;**[!UICONTROL 編輯運算式]**&#x200B;按鈕取得運算式編輯器，適用於&#x200B;**[!UICONTROL 屬性]**&#x200B;和&#x200B;**[!UICONTROL 值]**&#x200B;欄位。

| 從&#x200B;**屬性**&#x200B;欄位存取 | 從&#x200B;**值**&#x200B;欄位存取 |
| --- | --- |
| 屬性欄位![&#128279;](assets/rule-builder-expression-access-attribute.png){zoomable="yes"}{width="200" align="center" zoomable="yes"}的![運算式編輯器 | 值欄位](assets/rule-builder-expression-access-value.png){zoomable="yes"}{width="200" align="center" zoomable="yes"}的運算式編輯器 |

運算式編輯器提供：

* 定義運算式的&#x200B;**輸入欄位(1)**。
* 可用的&#x200B;**欄位(2)**&#x200B;清單，可用於運算式中，並對應至查詢的目標維度。
* **協助程式函式(3)**，依類別排序。

直接在輸入欄位中輸入運算式以編輯運算式。 若要新增欄位或協助程式函式，請將游標置於要新增的運算式中，然後按一下+按鈕。

![運算式編輯器介面](assets/rule-builder-expression-editor.png){zoomable="yes"}

## 協助程式功能

查詢編輯工具可讓您使用進階功能，根據所需結果和操作資料的型別執行複雜的篩選。 可使用下列函式：

### 彙總

彙總函式會針對一組值執行計算。

<table>
<tbody>
<tr>
<td><strong>名稱</strong></td>
<td><strong>說明</strong></td>
<td><strong>語法</strong></td>
</tr>
<tr>
<td><strong>平均</strong></td>
<td>傳回數字型別欄的平均值</td>
<td>Avg(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>計數</strong></td>
<td>計算資料行的非空值</td>
<td>Count(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>全部計數</strong></td>
<td>計算傳回的值（所有欄位）</td>
<td>CountAll()</td>
</tr>
<tr>
<td><strong>Countdistinct</strong></td>
<td>計算資料行的不同非空值</td>
<td>Countdistinct(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>最大</strong></td>
<td>傳回數字、字串或日期型別欄的最大值</td>
<td>Max(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>最小</strong></td>
<td>傳回數字、字串或日期型別欄的最小值</td>
<td>Min(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>StdDev</strong></td>
<td>傳回數字、字串或日期欄的標準差</td>
<td>stdev(&lt;value&gt;)</td>
</tr>
<tr>
<td><strong>StringAgg</strong></td>
<td>傳回字串型別欄值的串連，以第二個引數中的字元分隔</td>
<td>StringAgg(&lt;Value&gt;， &lt;String&gt;)</td>
</tr>
<tr>
<td><strong>總和</strong></td>
<td>傳回數字、字串或日期型別欄的值總和</td>
<td>Sum(&lt;value&gt;)</td>
</tr>
</tbody>
</table>

### 日期

日期函式會操控日期或時間值。

<table>
<tbody>
<tr>
<td><strong>名稱</strong></td>
<td><strong>說明</strong></td>
<td><strong>語法</strong></td>
</tr>
<tr>
<td><strong>AddDays</strong></td>
<td>新增日期的天數</td>
<td>AddDays(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddHours</strong></td>
<td>將小時數新增至日期</td>
<td>AddHours(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddMinutes</strong></td>
<td>將分鐘數新增至日期</td>
<td>AddMinutes(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddMonths</strong></td>
<td>新增月份至日期</td>
<td>AddMonths(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddSeconds</strong></td>
<td>新增秒數至日期</td>
<td>AddSeconds(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>AddYears</strong></td>
<td>在日期中新增多年</td>
<td>AddYears(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>ConvertNTZ</strong></td>
<td>套用定義的工作階段TZ，將時間戳記NTZ （沒有時區的時間戳記）轉換為TZ （有時區的時間戳記）</td>
<td>ConvertNTZ(&lt;date+time&gt;)</td>
</tr>
<tr>
<td><strong>DateCmp</strong></td>
<td>比較兩個日期</td>
<td>DateCmp(&lt;date&gt;， &lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Dateonly</strong></td>
<td>僅傳回日期（時間為00:00）</td>
<td>DateOnly(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>日</strong></td>
<td>傳回代表日期的數字</td>
<td>Day(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>DayOfYear</strong></td>
<td>傳回日期當年的日數</td>
<td>DayOfYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>幾天前</strong></td>
<td>傳回與目前日期對應的日期減去n天</td>
<td>DaysAgo(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>DaysAgoInt</strong></td>
<td>傳回與目前日期對應的日期（整數yyyymmdd）減去n天</td>
<td>DaysAgoInt(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>DaysDiff</strong></td>
<td>傳回兩個日期之間的天數</td>
<td>DaysDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>DaysOld</strong></td>
<td>傳回日期的年齡（以天為單位）</td>
<td>DaysOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>GetDate</strong></td>
<td>傳回伺服器的目前系統日期</td>
<td>GetDate()</td>
</tr>
<tr>
<td><strong>小時</strong></td>
<td>傳回日期的小時數</td>
<td>Hour(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>HoursDiff</strong></td>
<td>傳回兩個日期之間的小時數</td>
<td>HoursDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>分鐘</strong></td>
<td>傳回日期的分鐘數</td>
<td>Minute(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>MinutesDiff</strong></td>
<td>傳回兩個日期之間的分鐘數</td>
<td>MinutesDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>月</strong></td>
<td>傳回代表日期月份的數字</td>
<td>Month(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>MonthsAgo</strong></td>
<td>傳回與目前日期對應的日期減去n個月</td>
<td>MonthsAgo(&lt;number&gt;)</td>
</tr>
<tr>
<td><strong>MonthsDiff</strong></td>
<td>傳回兩個日期之間的月數</td>
<td>MonthsDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>MonthsOld</strong></td>
<td>傳回日期的年齡（月數）</td>
<td>MonthsOld(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>Oldest</strong></td>
<td>傳回範圍中最早的日期</td>
<td>Oldest(&lt;date， date&gt;)</td>
</tr>
<tr>
<td><strong>秒</strong></td>
<td>傳回日期的秒數</td>
<td>Second(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>SecondsDiff</strong></td>
<td>傳回兩個日期之間的秒數</td>
<td>SecondsDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>subdays</strong></td>
<td>從日期減去天數</td>
<td>SubDays(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>subhours</strong></td>
<td>從日期減去數小時</td>
<td>SubHours(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>subminutes</strong></td>
<td>從日期減去分鐘數</td>
<td>SubMinutes(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>submonths</strong></td>
<td>從日期減去幾個月</td>
<td>SubMonths(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>subseconds</strong></td>
<td>從日期減去秒數</td>
<td>SubSeconds(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>subyears</strong></td>
<td>從日期減去數年</td>
<td>SubYears(&lt;date&gt;， &lt;number&gt;)</td>
</tr>
<tr>
<td><strong>ToDate</strong></td>
<td>將日期+時間轉換為日期</td>
<td>ToDate(&lt;date + time&gt;)</td>
</tr>
<tr>
<td><strong>ToDateTime</strong></td>
<td>將字串轉換為日期+時間</td>
<td>ToDateTime(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimestamp</strong></td>
<td>將字串轉換為時間戳記</td>
<td>ToTimestamp(&lt;string&gt;)</td>
</tr>
<tr>
<td><strong>ToTimeZone</strong></td>
<td>將日期+時間轉換為時區</td>
<td>ToTimeZone(&lt;date&gt;， &lt;time zone&gt;)</td>
</tr>
<tr>
<td><strong>TruncDate</strong></td>
<td>將日期+時間舍入至最接近的秒數</td>
<td>TruncDate(@lastModified， &lt;number of seconds&gt;)</td>
</tr>
<tr>
<td><strong>TruncDateTZ</strong></td>
<td>將日期+時間四捨五入為以秒為單位的指定精確度</td>
<td>TruncDateTZ(&lt;date&gt;， &lt;number of seconds&gt;， &lt;time zone&gt;)</td>
</tr>
<tr>
<td><strong>TruncQuarter</strong></td>
<td>將日期舍入為季度</td>
<td>TruncQuarter(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncTime</strong></td>
<td>將時間部分捨入到最接近的秒數</td>
<td>TruncTime(&lt;date&gt;， &lt;number of seconds&gt;)</td>
</tr>
<tr>
<td><strong>TruncWeek</strong></td>
<td>將日期舍入為一週</td>
<td>TruncWeek(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>TruncYear</strong></td>
<td>將日期+時間舍入至年度的1月1日</td>
<td>TruncYear(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>WeekDay</strong></td>
<td>傳回代表日期當週中某天的數字（0=星期一，6=星期日）</td>
<td>WeekDay(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>年</strong></td>
<td>傳回代表日期年份的數字</td>
<td>Year(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearAndMonth</strong></td>
<td>傳回代表日期的年份和月份的數字</td>
<td>YearAndMonth（&lt;日期&gt;）</td>
</tr>
<tr>
<td><strong>YearAgo</strong></td>
<td>傳回指定日期與目前日期之間的年數</td>
<td>YearsAgo(&lt;date&gt;)</td>
</tr>
<tr>
<td><strong>YearsDiff</strong></td>
<td>傳回兩個日期之間的年數</td>
<td>YearsDiff(&lt;end date&gt;， &lt;start date&gt;)</td>
</tr>
<tr>
<td><strong>YearsOld</strong></td>
<td>傳回日期的年齡</td>
<td>YearsOld(&lt;date&gt;)</td>
</tr>
</tbody>
</table>

>[!NOTE]
>
>請注意，**DateOnly**&#x200B;函式會考量伺服器的時區，而非運運算元的時區。


### 地理行銷

地理行銷函式用於操縱地理值。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名稱</strong><br /> </td> 
   <td> <strong>說明</strong><br /> </td> 
   <td> <strong>語法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>距離</strong><br /> </td> 
   <td> 傳回由經度和緯度定義的兩點之間的距離，以度表示。<br /> </td> 
   <td> 距離（&lt;Longitude A&gt;, &lt;Latitude A&gt;, &lt;Longitude B&gt;, &lt;Latitude B&gt;）<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 數值

數值函式用於將文字轉換為數字。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名稱</strong><br /> </td> 
   <td> <strong>說明</strong><br /> </td> 
   <td> <strong>語法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Abs</strong><br /> </td> 
   <td> 返回數字的絕對值<br /> </td> 
   <td> Abs(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Ceil</strong><br /> </td> 
   <td> 傳回大於或等於數字的最小整數<br /> </td> 
   <td> Ceil(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Floor</strong><br /> </td> 
   <td> 傳回大於或等於數字<br />的最大整數 </td> 
   <td> Floor(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Greatest</strong><br /> </td> 
   <td> 傳回兩個數字中的較大值<br /> </td> 
   <td> Greatest(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Least</strong><br /> </td> 
   <td> 傳回兩個數字中的較小者<br /> </td> 
   <td> Least(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Mod</strong><br /> </td> 
   <td> 傳回n1除以n2<br />的整數除法的餘數 </td> 
   <td> Mod(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Percent</strong><br /> </td> 
   <td> 傳回兩個數字的比率，以百分比表示<br /> </td> 
   <td> Percent(&lt;number 1&gt;, &lt;number 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Random</strong><br /> </td> 
   <td> 傳回隨機值<br /> </td> 
   <td> Random()<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Round</strong><br /> </td> 
   <td> 將數字四捨五入為n個小數<br /> </td> 
   <td> Round(&lt;number&gt;, &lt;number of decimals&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Sign</strong><br /> </td> 
   <td> 傳回數字元號<br /> </td> 
   <td> Sign(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToDouble</strong><br /> </td> 
   <td> 將整數轉換為浮點數<br /> </td> 
   <td> ToDouble(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInt64</strong><br /> </td> 
   <td> 將浮點數轉換為　64　位整數<br /> </td> 
   <td> ToInt64(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToInteger</strong><br /> </td> 
   <td> 將浮點數轉換為整數<br /> </td> 
   <td> ToInteger(&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Trunc</strong><br /> </td> 
   <td> 截斷　n1　到　n2　小數<br /> </td> 
   <td> Trunc(&lt;n1&gt;, &lt;n2&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 其他

此表格包含剩餘的可用函式。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名稱</strong><br /> </td> 
   <td> <strong>說明</strong><br /> </td> 
   <td> <strong>語法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AESEncrypt</strong><br /> </td> 
   <td> 加密引數<br />中提供的字串 </td> 
   <td> AESEncrypt(&lt;value&gt;)<br /> </td> 
  </tr>
  <tr> 
   <td> <strong>案例</strong><br /> </td> 
   <td> 若條件為true，則傳回值1。 如果沒有，則傳回值2.<br /> </td> 
   <td> Case(When(&lt;condition&gt;, &lt;value 1&gt;), Else(&lt;value 2&gt;))<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>ClearBit</strong><br /> </td> 
   <td> 刪除值中的旗標<br /> </td> 
   <td> ClearBit(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>合併</strong><br /> </td> 
   <td> 如果值　1　為　零或　null，則傳回值　2，否則傳回值　1<br /> </td> 
   <td> Coalesce(&lt;value 1&gt;, &lt;value 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Decode</strong><br /> </td> 
   <td> 如果值1 =值2，則傳回值3。 如果未傳回值4.<br /> </td> 
   <td> Decode(&lt;value 1&gt;, &lt;value 2&gt;, &lt;value 3&gt;, &lt;value 4&gt;)<br /> </td>  
  </tr>

<tr> 
   <td> <strong>Else</strong><br /> </td> 
   <td> 傳回值　1（只能用作　case　函式的參數）<br /> </td> 
   <td> Else(&lt;value 1&gt;， &lt;value 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetEmailDomain</strong><br /> </td> 
   <td> 從電子郵件地址中擷取網域<br /> </td> 
   <td> GetEmailDomain(&lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>GetMirrorURL</strong><br /> </td> 
   <td> 檢索鏡像頁面伺服器的URL<br /> </td> 
   <td> GetMirrorURL(&lt;value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Iif</strong><br /> </td> 
   <td> 如果運算式為true，則傳回值1。 如果沒有，則傳回值2<br /> </td> 
   <td> Iif(&lt;condition&gt;, &lt;value 1&gt;, &lt;value 2&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsBitSet</strong><br /> </td> 
   <td> 指出旗標是否在值中<br /> </td> 
   <td> IsBitSet(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>IsEmptyString</strong><br /> </td> 
   <td> 如果字串1為空，則傳回值2，否則傳回值3<br /> </td> 
   <td> IsEmptyString(&lt;value 1&gt;， &lt;value 2&gt;， &lt;value 3&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NewUUID</strong><br /> </td> 
   <td> 傳回唯一識別碼<br /> </td> 
   <td> NewUUID()<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>NoNull</strong><br /> </td> 
   <td> 如果引數為　NULL，則返回空字串<br /> </td> 
   <td> NoNull(&lt;value&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>RowId</strong><br /> </td> 
   <td> 返回行號<br /> </td> 
   <td> RowId<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>SetBit</strong><br /> </td> 
   <td> 強制值中的旗標<br /> </td> 
   <td> SetBit(&lt;identifier&gt;, &lt;flag&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToBoolean</strong><br /> </td> 
   <td> 將數字轉換為布林值<br /> </td> 
   <td> ToBoolean(&lt;number&gt;)<br /> </td>   
  </tr> 
  <tr> 
   <td> <strong>When</strong><br /> </td> 
   <td> 如果運算式為true，則傳回值1。 如果沒有，則傳回值2 （只能用作case函式的引數）<br /> </td> 
   <td> When(&lt;condition&gt;, &lt;value 1&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 字串

字串函式可用來控制一組字串。

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名稱</strong><br /> </td> 
   <td> <strong>說明</strong><br /> </td> 
   <td> <strong>語法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull2</strong><br /> </td> 
   <td> 指示所有參數是否為非空值且非空白<br /> </td> 
   <td> AllNonNull2(&lt;string&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>AllNonNull3</strong><br /> </td> 
   <td> 指示所有參數是否為非空值且非空白<br /> </td> 
   <td> AllNonNull3(&lt;string&gt;， &lt;string&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ascii</strong><br /> </td> 
   <td> 傳回字串中第一個字元的ASCII值。<br /> </td> 
   <td> Ascii(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Char</strong><br /> </td> 
   <td> 傳回與　'n' ASCII　代碼對應的字元<br /> </td> 
   <td> 字元(&lt;number&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Charindex</strong><br /> </td> 
   <td> 傳回字串1.<br />中字串2的位置 </td> 
   <td> Charindex(&lt;string&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>資料長度</strong><br /> </td> 
   <td> 傳回字串<br />的大小（位元組） </td> 
   <td> dataLength(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>GetLine</strong><br /> </td> 
   <td> 傳回字串的第　n　行（從　1　到　n）<br /> </td> 
   <td> GetLine(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IfEquals</strong><br /> </td> 
   <td> 如果前兩個引數相等，則傳回第三個引數。 如果不是，則傳回最後一個引數<br /> </td> 
   <td> IfEquals(&lt;string&gt;， &lt;string&gt;， &lt;string&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>IsMemoNull</strong><br /> </td> 
   <td> 指示作為參數傳遞的備忘錄是否為空<br /> </td> 
   <td> IsMemoNull(&lt;memo&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords</strong><br /> </td> 
   <td> 串連以引數形式傳遞的字串。 如有必要，在字串之間新增空格。<br /> </td> 
   <td> JuxtWords(&lt;string&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>JuxtWords3</strong><br /> </td> 
   <td> 串連以引數形式傳遞的字串。 如有必要，在字串之間新增空格<br /> </td> 
   <td> JuxtWords3(&lt;string&gt;， &lt;string&gt;， &lt;string&gt;)<br /></td>  
  </tr> 
  <tr> 
   <td> <strong>Left</strong><br /> </td> 
   <td> 傳回字串的前　n　個字元<br /> </td> 
   <td> Left(&lt;string&gt;， &lt;number&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Length</strong><br /> </td> 
   <td> 傳回字串<br />的長度 </td> 
   <td> Length(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>行</strong><br /> </td> 
   <td> 從字串<br />擷取行n </td> 
   <td> Line(&lt;string&gt;，&lt;number&gt;)<br /></td> 
  </tr>
  <tr> 
   <td> <strong>Lower</strong><br /> </td> 
   <td> 傳回小寫字串<br /> </td> 
   <td> Lower(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>LPad</strong><br /> </td> 
   <td> 傳回左側的已完成字串<br /> </td> 
   <td> LPad (&lt;String&gt;， &lt;Number&gt;， &lt;Char&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Ltrim</strong><br /> </td> 
   <td> 移除字串左側的空格<br /> </td> 
   <td> Ltrim(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Md5Digest</strong><br /> </td> 
   <td> 返回字串　MD5　鍵的十六進位表示<br /> </td> 
   <td> Md5Digest(&lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>MemoContains</strong><br /> </td> 
   <td> 指定備忘錄是否包含作為參數傳遞的字串<br /> </td> 
   <td> MemoContains(&lt;memo&gt;， &lt;string&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>節點值</strong><br /> </td> 
   <td> 從其XPath和欄位資料中擷取XML欄位的值<br /> </td> 
   <td> NodeValue (&lt;String&gt;， &lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Replace</strong><br /> </td> 
   <td> 以其他字串值取代指定字串值的所有出現次數。<br /> </td> 
   <td> Replace(&lt;String&gt;，&lt;String&gt;，&lt;String&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Right</strong><br /> </td> 
   <td> 傳回字串的最後　n　個字元<br /> </td> 
   <td> Right(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>RPad</strong><br /> </td> 
   <td> 傳回右側的已完成字串<br /> </td> 
   <td> RPad(&lt;string&gt;， &lt;number&gt;， &lt;character&gt;)<br /></td> 
  </tr> 
  <tr> 
   <td> <strong>Rtrim</strong><br /> </td> 
   <td> 移除字串右側的空格<br /> </td> 
   <td> Rtrim(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha256Digest</strong><br /> </td> 
   <td> 字串SHA256鍵的十六進位表示。<br /> </td> 
   <td> Sha256Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Sha512Digest</strong><br /> </td> 
   <td> 字串SHA512鍵的十六進位表示。<br /> </td> 
   <td> Sha512Digest (&lt;String&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Smart</strong><br /> </td> 
   <td> 傳回字串，每個字詞的首字母以大寫表示<br /> </td> 
   <td> Smart(&lt;string&gt;)<br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>Substring</strong><br /> </td> 
   <td> 從字串的字元n1開始提取長度為n2<br />的子字串 </td> 
   <td> Substring(&lt;string&gt;, &lt;offset&gt;, &lt;length&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>ToString</strong><br /> </td> 
   <td> 將數字轉換為字串<br /> </td> 
   <td> ToString(&lt;number&gt;， &lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Upper</strong><br /> </td> 
   <td> 以大寫傳回字串<br /> </td> 
   <td> Upper(&lt;string&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLink</strong><br /> </td> 
   <td> 傳回連結的外鍵，如果其他兩個參數相等，則傳遞為參數<br /> </td> 
   <td> VirtualLink(&lt;number&gt;、&lt;number&gt;、&lt;number&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>VirtualLinkStr</strong><br /> </td> 
   <td> 傳回連結的外鍵（文字）索引鍵，如果其他兩個參數相等，則傳回該連結的外鍵　(text)　<br /> </td> 
   <td> VirtualLinkStr(&lt;string&gt;, &lt;number&gt;, &lt;number&gt;)<br /> </td>  
  </tr> 
 </tbody> 
</table>

### 視窗

<table> 
 <tbody> 
  <tr> 
   <td> <strong>名稱</strong><br /> </td> 
   <td> <strong>說明</strong><br /> </td> 
   <td> <strong>語法</strong><br /> </td> 
  </tr> 
  <tr> 
   <td> <strong>_超過__</strong><br /> </td> 
   <td> 執行以第1個引數輸入的SQL函式呼叫，透過Partition或Order By輸入為第2個引數的欄位<br /> </td> 
   <td> _超過_ (&lt;Value&gt;， &lt;Value&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>Desc</strong><br /> </td> 
   <td> 套用遞減排序<br /> </td> 
   <td> Desc(&lt;value 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>OrderBy</strong><br /> </td> 
   <td> 對分區內的結果進行排序<br /> </td> 
   <td> OrderBy(&lt;value 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>PartitionBy</strong><br /> </td> 
   <td> 對表上的查詢結果進行分區<br /> </td> 
   <td> PartitionBy(&lt;value 1&gt;)<br /> </td>  
  </tr> 
  <tr> 
   <td> <strong>RowNum</strong><br /> </td> 
   <td> 根據資料表分割和排序順序產生行號。<br /> </td> 
   <td> RowNum(PartitionBy(&lt;value 1&gt;), OrderBy(&lt;value 1&gt;))<br /> </td> 
  </tr> 
 </tbody> 
</table>
