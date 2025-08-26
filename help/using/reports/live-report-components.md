---
solution: Journey Optimizer
product: journey optimizer
title: 元件清單
description: 瞭解如何使用即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 12168cdf-f517-49b5-958b-ba689ade6982
source-git-commit: c9505b482d2dedc10c4025574cccb662fe149510
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

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
   <td> 已成功為歷程執行的動作總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已輸入的設定檔<br/> </td> 
   <td> 到達歷程進入事件的個人總數。<br/> </td> 
</tr>
  <tr> 
   <td> 動作<br/>發生錯誤 </td> 
   <td>動作發生的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已退出的設定檔<br/> </td> 
   <td> 退出歷程的個人總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 失敗的個別歷程<br/> </td> 
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
   <td> 退回<br/> </td> 
   <td> 傳遞與自動傳回處理期間累積的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與已傳送的電子郵件相比退回的電子郵件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 點按<br/> </td> 
   <td> 電子郵件中內容被點按的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 成功傳送的訊息數。<br/></td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 已成功傳送的訊息百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳遞期間發生的錯誤總數，導致無法將其傳送至設定檔。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的電子郵件相較之下，在傳遞期間發生且無法傳送的錯誤百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 硬退回<br/> </td> 
   <td> 永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 暫時的總數，例如「不在辦公室」，或技術錯誤，例如，寄件者型別是郵遞員。<br/> </td> 
</tr>
   <tr> 
   <td>選件點按率<br/> </td> 
   <td>與優惠互動的使用者百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠曝光率<br/> </td> 
   <td>與已傳送之選件數目相較的已開啟選件百分比。<br/> </td> 
</tr>
   <tr> 
   <td>提案名稱<br/> </td> 
   <td> 在傳遞中新增的優惠方案名稱。 如需位置的詳細資訊，請參閱此<a href="../offers/offer-library/creating-personalized-offers.md">頁面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已傳送提案<br/> </td> 
   <td>優惠方案的傳送總數。<br/> </td> 
</tr> 
  <tr>
   <td>開啟<br/> </td> 
   <td> 訊息開啟的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟率<br/> </td> 
   <td> 與傳遞的電子郵件數目相較的已開啟電子郵件總數。<br/> </td> 
</tr>
  <tr> 
   <td>位置名稱<br/> </td> 
   <td> 用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此<a href="../offers/offer-library/creating-placements.md">頁面</a>。 </td> 
</tr> 
  <tr> 
   <td> 重試<br/> </td> 
   <td> 重試佇列中的電子郵件數目。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr>
  <tr> 
   <td> 軟退信<br/> </td> 
   <td> 暫存錯誤總數，例如完整的收件匣。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾訊息申訴<br/> </td> 
   <td> 宣告郵件為垃圾郵件或垃圾郵件的次數。<br/> </td> 
</tr>
  <tr> 
   <td> 已鎖定目標<br/> </td> 
   <td> 傳遞分析期間處理的訊息總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 不重複點按<br/> </td> 
   <td> 按一下電子郵件中內容的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td>不重複點按率<br/> </td> 
   <td> 與傳遞互動的使用者百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 不重複開啟<br/> </td> 
   <td>開啟傳遞的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消訂閱<br/> </td> 
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
  <td>退回<br/> </td> 
   <td>未與登入頁面互動且未完成訂閱動作的人數。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>點按<br/> </td> 
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
   <td>瀏覽總數<br/> </td> 
   <td> 來自歷程和外部來源的登入頁面造訪總數，包括一個收件者的多次造訪。<br/> </td> 
</tr>
 <tr> 
   <td>不重複訪客<br/> </td> 
   <td>造訪您登陸頁面的人員數量，未考慮一位收件者的多次造訪。<br/> </td> 
</tr>
 <tr> 
   <td>造訪<br/> </td> 
   <td>對登入頁面的瀏覽次數，包括一位收件者的多次瀏覽。<br/> </td> 
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
   <td> 推播通知已傳遞的動作總數，例如按鈕點選或解除。<br/> </td> 
</tr>
  <tr> 
   <td>退回<br/> </td> 
   <td> 傳遞與自動傳回處理期間累積的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 已成功傳送的訊息數。<br/> </td> 
</tr> 
  <tr> 
   <td>參與<br/> </td> 
   <td> 此推播通知的開啟和動作總數，亦即，設定檔是否已開啟推播，或按鈕是否已點按。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳遞期間發生的錯誤總數，導致無法將其傳送至設定檔。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。<br/> </td> 
</tr>
  <tr> 
   <td> 開啟<br/> </td> 
   <td> 傳遞到裝置且使用者因此開啟應用程式而點按的推播通知總數。 這類似於「推送點按」，但如果通知已關閉，則不會觸發「推送開啟」。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳遞的傳送總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已鎖定目標<br/> </td> 
   <td> 傳遞分析期間處理的推播訊息總數。<br/> </td> 
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
