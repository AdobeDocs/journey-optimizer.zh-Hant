---
solution: Journey Optimizer
product: journey optimizer
title: 元件清單
description: 瞭解如何使用全域報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: c487bb38-49ce-4238-8e94-8364f994cedd
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 1%

---

# 元件清單 {#list-of-components-global}

>[!AVAILABILITY]
>
>目前的報告體驗將於2025年1月淘汰。 在此日期之後，新的報告體驗將成為標準體驗。建議您熟悉新功能，以確保順利轉換。 [開始使用Journey Optimizer的新報告介面。](report-gs-cja.md)

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
   <td> 在傳送程式期間累計的錯誤總數，以及相對於已傳送訊息總數的自動傳回處理。<br/> </td> 
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
   <td> 成功傳送的訊息數（與已傳送訊息總數相關）。<br/></td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 已成功傳送的訊息百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 在傳送過程中發生的錯誤總數，導致無法將其傳送至設定檔。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的電子郵件相比，在傳送過程中發生而無法傳送的錯誤百分比。<br/> </td> 
</tr>
</tr> 
  <tr> 
   <td> 錯誤原因<br/> </td> 
   <td> 特定原始錯誤原因的名稱。 <a href="exclusion-list.md">進一步瞭解錯誤原因</a>。<br/> </td> 
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
   <td> 點按電子郵件中內容的收件者人數。<br>請注意，在計算不重複點按時，會將過去10天列入考量。 如果設定檔在10天內註冊了多次點按，則會計為不重複點按。 但是，如果設定檔相隔10天以上，有2次點按，則不會視為不重複點按。<br/> </td> 
</tr> 
  <tr> 
   <td>不重複點按率<br/> </td> 
   <td> 與傳遞互動的使用者百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 不重複開啟<br/> </td> 
   <td>開啟傳遞的收件者人數。 <br>請注意，計算唯一開啟次數時，會將過去10天列入考量。 如果設定檔在10天內註冊了多次開啟，則會計為不重複開啟。 但是，如果設定檔有2個開啟間隔超過10天，則不會視為唯一開啟。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消訂閱<br/> </td> 
   <td> 對取消訂閱連結的點按次數。<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../content-management/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../content-management/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../content-management/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td>Number of recipients who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of recipients who clicked on the unsubscription link.<br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## 應用程式內量度 {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>點按<br/> </td> 
   <td>與應用程式內訊息所含按鈕互動的收件者總數。<br/> </td> 
</tr>
  <tr> 
   <td>點按率<br/> </td> 
   <td>與已看到訊息的使用者相比，與應用程式內訊息中所包含按鈕互動的使用者百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>解除率<br/> </td> 
   <td> 收件者已解除的應用程式內訊息百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>曝光次數<br/> </td> 
   <td> 傳遞給所有使用者的應用程式內訊息總數。<br/> </td>
</tr>
  <tr> 
   <td>不重複曝光次數<br/> </td> 
   <td>已向其傳遞應用程式內訊息的不重複使用者人數。<br/> </td>
</tr>
 </tbody> 
</table>

## 推播通知量度

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
   <td> 傳遞期間累計的錯誤總數與自動傳回處理相對於已傳送訊息的總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與已傳送的推播通知相比退回的推播通知百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 成功傳送的訊息數，與已傳送的訊息總數相關。<br/> </td> 
</tr> 
  <tr> 
   <td> 傳遞率<br/> </td> 
   <td> 已成功傳送的推播通知百分比。<br/> </td> 
</tr>
  <tr> 
   <td>參與<br/> </td> 
   <td> 此推播通知的開啟和動作總數，亦即，設定檔是否已開啟推播，或按鈕是否已點按。<br/> </td> 
</tr> 
  <tr> 
   <td> 參與率<br/> </td> 
   <td> 此推播通知的開啟和動作百分比，亦即，設定檔是否開啟推播或按鈕是否已點按。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳遞期間發生的錯誤總數，導致無法將其傳送至設定檔。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與已傳送的推播通知相比，傳遞期間發生且無法傳送的錯誤百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤原因<br/> </td> 
   <td> 特定原始錯誤原因的名稱。 <a href="exclusion-list.md">進一步瞭解錯誤原因</a>。<br/> </td> 
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
   <td> 開啟率<br/> </td> 
   <td> 已開啟推播通知的百分比。<br/> </td> 
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
   <td>跳出率<br/> </td> 
   <td>未與登入頁面互動且未完成訂閱動作的人數（相對於造訪總數）。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>點按<br/> </td> 
   <td>內容在登入頁面中被點按的次數。<br/> </td> 
</tr>
 <tr> 
   <td>點按率<br/> </td> 
   <td>登陸頁面中的點按百分比。<br/> </td>
</tr>
<tr>
<td>轉換<br/> </td> 
   <td>與登入頁面互動（例如訂閱表單）的人數。<br/> </td> 
</tr>
<tr>
   <td>轉換率<br/> </td> 
   <td>與登入頁面互動的人數，例如訂閱的表單，與造訪總數相關。<br/> </td> 
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
