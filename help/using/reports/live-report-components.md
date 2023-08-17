---
solution: Journey Optimizer
product: journey optimizer
title: 元件清單
description: 瞭解如何使用即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d6ec55e5-e44e-4773-a561-d1bc0919ea04
source-git-commit: 26456f7c2d879843eb533209377b83fc0ccb5617
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 7%

---

# 元件清單 {#list-of-components-live}

下表提供報表中使用的量度清單，以及量度定義（視傳送型別而定）。

## 歷程量度 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>動作已成功執行<br/> </td> 
   <td> 為歷程成功執行的動作總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 輸入的設定檔<br/> </td> 
   <td> 到達歷程進入事件的個人總數。<br/> </td> 
</tr>
  <tr> 
   <td> 動作中的錯誤<br/> </td> 
   <td>動作發生的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已退出的設定檔<br/> </td> 
   <td> 已退出歷程的個人總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 失敗的個人歷程<br/> </td> 
   <td> 未成功執行的個別歷程總數。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 電子郵件和簡訊維度與量度 {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> 跳出<br/> </td> 
   <td> 傳遞與自動退貨處理期間累計的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與已傳送電子郵件相比跳出的電子郵件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 點擊次數<br/> </td> 
   <td> 在電子郵件中點按內容的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞 <br/> </td> 
   <td> 成功傳送的訊息數。<br/></td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 已成功傳送的訊息百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳遞期間發生且無法傳送至設定檔的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的電子郵件相較之下，在傳送期間發生且無法傳送的錯誤百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 硬退信<br/> </td> 
   <td> 永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 暫時的總數，例如「不在辦公室」或技術錯誤（例如，如果寄件者型別是郵遞員）。<br/> </td> 
</tr>
   <tr> 
   <td>優惠點按率<br/> </td> 
   <td>與選件互動的使用者百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠曝光率<br/> </td> 
   <td>已開啟選件相對於已傳送選件數量的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠方案名稱<br/> </td> 
   <td> 在傳遞中新增的優惠方案名稱。 如需位置的詳細資訊，請參閱此 <a href="../offers/offer-library/creating-personalized-offers.md">頁面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已傳送的優惠<br/> </td> 
   <td>優惠方案的傳送總數。<br/> </td> 
</tr> 
  <tr>
   <td>開啟數<br/> </td> 
   <td> 訊息開啟的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟率<br/> </td> 
   <td> 與已傳遞電子郵件數量相較的已開啟電子郵件總數。<br/> </td> 
</tr>
  <tr> 
   <td>位置名稱<br/> </td> 
   <td> 用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此 <a href="../offers/offer-library/creating-placements.md">頁面</a>. </td> 
</tr> 
  <tr> 
   <td> 重試次數<br/> </td> 
   <td> 重試佇列中的電子郵件數目。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr>
  <tr> 
   <td> 軟退信<br/> </td> 
   <td> 暫時性錯誤總數，例如完整收件匣。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾郵件投訴數<br/> </td> 
   <td> 訊息宣告為垃圾郵件或垃圾郵件的次數。<br/> </td> 
</tr>
  <tr> 
   <td> 已鎖定目標<br/> </td> 
   <td> 傳遞分析期間處理的訊息總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 不重複點按次數<br/> </td> 
   <td> 點按電子郵件中內容的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td>不重複點按率<br/> </td> 
   <td> 與傳遞互動的使用者百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 不重複開啟次數<br/> </td> 
   <td>開啟傳遞的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消訂閱次數<br/> </td> 
   <td> 對取消訂閱連結的點按次數。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 登陸頁面量度 {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>跳出<br/> </td> 
   <td>未與登入頁面互動且未完成訂閱動作的人數。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>點擊次數<br/> </td> 
   <td>內容在登入頁面中被點按的次數。<br/> </td> 
</tr>
<tr>
<td>轉換<br/> </td> 
   <td>與登入頁面互動（例如訂閱表單）的人數。<br/> </td> 
</tr>
 <tr> 
   <td>歷程<br/> </td> 
   <td>來自歷程的登陸頁面造訪次數。<br/> </td> 
</tr>
 <tr> 
   <td>其他來源<br/> </td> 
   <td>來自外部來源而非歷程的登陸頁面造訪次數。<br/> </td> 
</tr>
 <tr> 
   <td>造訪總數<br/> </td> 
   <td> 來自歷程和外部來源的登入頁面造訪總數，包括一位收件者的多次造訪。<br/> </td> 
</tr>
 <tr> 
   <td>不重複訪客<br/> </td> 
   <td>造訪您登陸頁面的人員數量，系統不會考慮一位收件者的多次造訪。<br/> </td> 
</tr>
 <tr> 
   <td>造訪數<br/> </td> 
   <td>造訪您的登陸頁面的次數，包括一位收件者的多次造訪。<br/> </td> 
</tr>
 </tbody> 
</table>

## 推播通知量度 {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>動作<br/> </td> 
   <td> 推播通知已傳送的動作總數，例如按鈕點選或解除。<br/> </td> 
</tr>
  <tr> 
   <td>跳出<br/> </td> 
   <td> 傳遞與自動退貨處理期間累計的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 成功傳送的訊息數。<br/> </td> 
</tr> 
  <tr> 
   <td>參與<br/> </td> 
   <td> 此推播通知的開啟和動作總數，也就是設定檔是否已開啟推播，或按鈕是否已點按。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳遞期間發生且無法傳送至設定檔的錯誤總數。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 開啟數<br/> </td> 
   <td> 傳遞到裝置且使用者因此開啟應用程式而點按的推播通知總數。 這類似於「推送點按」，但如果通知已關閉，則不會觸發「推送開啟」。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已鎖定目標<br/> </td> 
   <td> 傳遞分析期間處理的推送訊息總數。<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
## In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->
