---
solution: Journey Optimizer
product: journey optimizer
title: 元件清單
description: 瞭解如何使用全局報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a41e82db-1fa4-478d-a5a2-324d1df1f8ee
source-git-commit: 26456f7c2d879843eb533209377b83fc0ccb5617
workflow-type: tm+mt
source-wordcount: '972'
ht-degree: 5%

---

# 元件清單 {#list-of-components-global}

下表根據交付類型為您提供報告中使用的度量及其定義的清單。

## 行程度量 {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>已成功執行操作<br/> </td> 
   <td> 成功執行行程的活動總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 輸入的配置檔案<br/> </td> 
   <td> 到達旅程的入門事件的個人總數。<br/> </td> 
</tr>
  <tr> 
   <td> 操作中出錯<br/> </td> 
   <td>為操作發生的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 退出配置檔案<br/> </td> 
   <td> 離開旅程的個人總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 單程失敗<br/> </td> 
   <td> 未成功執行的單個行程的總數。<br/> </td> 
</tr> 
 </tbody> 
</table>

## 電子郵件和SMS維度和度量 {#email-and-sms-metrics}

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
   <td> 在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與發送的電子郵件相比，已跳轉的電子郵件的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 點擊次數<br/> </td> 
   <td> 在電子郵件中按一下內容的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞 <br/> </td> 
   <td> 成功發送的消息數，與已發送的消息總數相關。<br/></td> 
</tr> 
  <tr> 
   <td> 交貨率<br/> </td> 
   <td> 成功發送的郵件百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與發送的電子郵件相比，在發送過程中發生的阻止發送錯誤的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> 被Adobe Journey Optimizer排除的檔案數。<br/> </td> 
</tr>
  <tr> 
   <td> 硬彈<br/> </td> 
   <td> 永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。<br/> </td> 
</tr>
   <tr> 
   <td>服務點擊率<br/> </td> 
   <td>與報價互動的用戶百分比。<br/> </td> 
</tr>
   <tr> 
   <td>提供印象率<br/> </td> 
   <td>已開啟的優惠與已發送的優惠數目相比的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠方案名稱<br/> </td> 
   <td> 在交貨中添加的要約的名稱。 有關放置的詳細資訊，請參閱 <a href="../offers/offer-library/creating-personalized-offers.md">頁</a>。<br/> </td> 
</tr>
   <tr> 
   <td>已發送優惠<br/> </td> 
   <td>發送要約的總數。<br/> </td> 
</tr> 
  <tr>
   <td>開啟數<br/> </td> 
   <td> 消息開啟的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟速率<br/> </td> 
   <td> 已開啟電子郵件的總數與已發送電子郵件的數量相比。<br/> </td> 
</tr>
  <tr> 
   <td>放置名稱<br/> </td> 
   <td> 用於顯示優惠的位置的名稱。 有關放置的詳細資訊，請參閱 <a href="../offers/offer-library/creating-placements.md">頁</a>。 </td> 
</tr> 
  <tr> 
   <td> 重試次數<br/> </td> 
   <td> 隊列中重試的電子郵件數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 交貨的發送總數。<br/> </td> 
</tr>
  <tr> 
   <td> 軟彈跳<br/> </td> 
   <td> 臨時錯誤（如完整收件箱）的總數。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾郵件投訴數<br/> </td> 
   <td> 將郵件聲明為垃圾郵件或垃圾郵件的次數。<br/> </td> 
</tr>
  <tr> 
   <td> 目標<br/> </td> 
   <td> 在傳遞分析期間處理的郵件總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 不重複點按次數<br/> </td> 
   <td> 按一下電子郵件內容的收件人數。<br/> </td> 
</tr> 
  <tr> 
   <td>唯一按一下率<br/> </td> 
   <td> 與遞送互動的用戶百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 不重複開啟次數<br/> </td> 
   <td>開啟交貨的收件人數。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消訂閱<br/> </td> 
   <td> 取消訂閱連結上的按一下次數。<br/> </td> 
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
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td><br/> </td> 
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
   <td><br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td><br/> </td>
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

## 應用內度量 {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>點擊次數<br/> </td> 
   <td>與In-app消息中包含的按鈕交互的收件人總數。<br/> </td> 
</tr>
  <tr> 
   <td>按一下率<br/> </td> 
   <td>與看到In-app消息的用戶相比，與In-app消息中包含的按鈕交互的用戶的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>消除率<br/> </td> 
   <td> 接收者拒絕的應用內郵件的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td>曝光數<br/> </td> 
   <td> 傳遞給所有用戶的應用內消息總數。<br/> </td>
</tr>
  <tr> 
   <td>獨特印象<br/> </td> 
   <td>將In-app消息傳遞給的唯一用戶數。<br/> </td>
</tr>
 </tbody> 
</table>

## 推送通知度量

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
   <td> 已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。<br/> </td> 
</tr>
  <tr> 
   <td>跳出<br/> </td> 
   <td> 在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 與發送的推送通知相比，已跳轉的推送通知的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 成功發送的消息數，與已發送的消息總數相關。<br/> </td> 
</tr> 
  <tr> 
   <td> 交貨率<br/> </td> 
   <td> 已成功發送推送通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td>預訂<br/> </td> 
   <td> 此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。<br/> </td> 
</tr> 
  <tr> 
   <td> 訂約率<br/> </td> 
   <td> 此推送通知的開啟和操作的百分比，即，如果配置檔案開啟了推送或按一下了按鈕。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與發送的推送通知相比，在發送過程中發生的錯誤阻止發送的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已排除<br/> </td> 
   <td> 被Adobe Journey Optimizer排除的檔案數。<br/> </td> 
</tr>
  <tr> 
   <td> 開啟數<br/> </td> 
   <td> 用戶通過點擊將推送通知發送到設備並開啟應用的總數。 這與「推式按一下」類似，但「推式開啟」在通知被撤消時不會觸發。<br/> </td> 
</tr> 
  <tr> 
   <td> 開啟率<br/> </td> 
   <td> 開啟的推送通知百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 交貨的發送總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 目標<br/> </td> 
   <td> 在傳遞分析期間處理的推送消息總數。<br/> </td> 
</tr>  
 </tbody> 
</table>

### 登錄頁度量 {#landing-page-metrics}

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
   <td>未與登錄頁交互且未完成訂閱操作的人數。<br/> </td> 
</tr>
 <tr> 
   <td>跳出率<br/> </td> 
   <td>未與登錄頁互動且未完成訂閱行動的人數，與訪問總數相比。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>點擊次數<br/> </td> 
   <td>在登錄頁中按一下內容的次數。<br/> </td> 
</tr>
 <tr> 
   <td>按一下率<br/> </td> 
   <td>登錄頁中的按一下百分比。<br/> </td>
</tr>
<tr>
<td>轉換<br/> </td> 
   <td>與登錄頁互動的人數，例如訂閱表格。<br/> </td> 
</tr>
<tr>
   <td>轉換率<br/> </td> 
   <td>與登錄頁互動的人數，例如訂閱表格，與訪問總數相比。<br/> </td> 
</tr>
 <tr> 
   <td>旅程<br/> </td> 
   <td>從旅程訪問登錄頁的次數。<br/> </td> 
</tr>
 <tr> 
   <td>其他來源<br/> </td> 
   <td>從外部來源而不是旅程訪問登錄頁的次數。<br/> </td> 
</tr>
 <tr> 
   <td>訪問總數<br/> </td> 
   <td> 來自行程和外部來源（包括一個收件人的多次訪問）的登錄頁訪問總數。<br/> </td> 
</tr>
 <tr> 
   <td>不重複訪客<br/> </td> 
   <td>訪問登錄頁的人數，不考慮一個收件人的多次訪問。<br/> </td> 
</tr>
 <tr> 
   <td>造訪數<br/> </td> 
   <td>訪問登錄頁的次數，包括一個收件人的多次訪問。<br/> </td> 
</tr>
 </tbody> 
</table>
