---
solution: Journey Optimizer
product: journey optimizer
title: 元件清單
description: 瞭解如何使用報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: 7945ab9369498f23685aa2f727542c7367c2d830
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 0%

---

# 指標清單 {#list-of-components-global}

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
<td>歷程參與</td> 
<td>收到透過歷程傳送之訊息的不重複個人總數，代表到達歷程中指定動作點的不同設定檔。</td> 
</tr> 
<tr> 
<td>歷程進入者</td> 
<td>到達歷程進入事件的個人總數。</td> 
</tr>
<tr> 
<td>歷程結束</td> 
<td>已退出歷程的個人總數。</td> 
</tr>
<tr> 
<td>歷程失敗次數</td> 
<td>未成功執行的個別歷程總數。</td> 
</tr>
<tr> 
<td>不重複歷程進入者</td> 
<td>到達歷程進入事件的個人總數，不考慮相同設定檔的多個互動。</td> 
</tr>
<tr> 
<td>不重複歷程結束</td> 
<td>退出歷程的個人總數，不考慮相同設定檔的多個互動。</td> 
</tr>
<tr> 
<td>不重複歷程失敗</td> 
<td>未成功執行的個別歷程總數，未考慮相同設定檔的多個互動。</td> 
</tr>
 </tbody> 
</table>

## 電子郵件量度 {#email-metrics}

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
   <td> 相對於已傳送電子郵件總數，造成退回的電子郵件百分比。<br/> </td> 
  </tr> 
  <tr> 
   <td> 點進開啟率(CTOR)<br/> </td> 
   <td> 電子郵件開啟的次數。<br/> </td> 
  </tr>
  <tr> 
   <td> 點進率(CTR)<br/> </td> 
   <td> 與電子郵件互動的使用者百分比。<br/> </td> 
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
   <td> 錯誤原因<br/> </td> 
   <td> 特定原始錯誤原因的名稱。 <a href="exclusion-list.md">進一步瞭解錯誤原因</a>。<br/> </td> 
  </tr>
  <tr> 
   <td>預估電子郵件開啟次數<br/> </td> 
   <td>預估由設定檔直接開啟和郵件伺服器觸發自動開啟帳戶的總電子郵件開啟次數。 此量度會套用由手動開啟電子郵件的收件者計算出的開啟率，調整郵件伺服器為隱私權或安全性掃描所觸發的開啟，並調整至僅由郵件伺服器開啟電子郵件的收件者。<br/> </td> 
  </tr>
  <tr> 
   <td> 選件點按率<br/> </td> 
   <td> 與優惠互動的使用者百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 優惠曝光率<br/> </td> 
   <td> 與已傳送之選件數目相較的已開啟選件百分比。<br/> </td> 
  </tr>
  <tr> 
   <td> 提案名稱<br/> </td> 
   <td> 在傳遞中新增的優惠方案名稱。 如需位置的詳細資訊，請參閱此<a href="../offers/offer-library/creating-personalized-offers.md">頁面</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> 已傳送提案<br/> </td> 
   <td> 優惠方案的傳送總數。<br/> </td> 
  </tr> 
  <tr> 
   <td> 開啟<br/> </td> 
   <td> 訊息開啟的次數。<br/> </td> 
  </tr> 
  <tr> 
   <td> 傳送錯誤<br/> </td> 
   <td> 在傳送過程中發生的錯誤總數，導致無法將其傳送至設定檔。<br/> </td> 
  </tr> 
  <tr> 
   <td> 傳送排除專案<br/> </td> 
   <td> Adobe Journey Optimizer已排除的設定檔數。 <a href="exclusion-list.md">進一步瞭解排除專案的計算方式</a>。<br/> </td> 
  </tr>
  <tr> 
   <td> 位置名稱<br/> </td> 
   <td> 用來顯示優惠方案的位置名稱。 如需位置的詳細資訊，請參閱此<a href="../offers/offer-library/creating-placements.md">頁面</a>。 </td> 
  </tr>
  <tr> 
   <td> 垃圾訊息申訴<br/> </td> 
   <td> 宣告郵件為垃圾郵件或垃圾郵件的次數。<br/> </td> 
  </tr> 
  <tr> 
   <td> 已鎖定目標<br/> </td> 
   <td> 在套用排除、隱藏或同意移除之前，符合對象資格的設定檔數。 在啟用重新進入的歷程中，設定檔可能會鎖定多次。<br/> </td> 
  </tr>
  <tr> 
   <td>不重複退回<br/> </td> 
   <td> 至少有一封電子郵件導致退回的不重複設定檔數。</td> 
  </tr>
  <tr> 
   <td>不重複跳出率<br/> </td> 
   <td>根據不重複傳送總數，電子郵件至少跳出一次的不重複設定檔百分比。</td> 
  </tr>
  <tr> 
   <td> 不重複點按<br/> </td> 
   <td> 在電子郵件中點按內容的設定檔數。<br>請注意，在計算不重複點按時，會將過去10天列入考量。 如果設定檔在10天內註冊了多次點按，則會計為不重複點按。 但是，如果設定檔相隔10天以上，有2次點按，則不會視為不重複點按。<br/> </td> 
  </tr>
  <tr> 
   <td>不重複點進開啟率<br/> </td> 
   <td> 根據不重複開啟次數，在開啟電子郵件後點按連結的不重複設定檔百分比。 </td> 
  </tr>
  <tr> 
   <td> 不重複點進率<br/> </td> 
   <td> 相對於不重複傳送電子郵件數量，按一下電子郵件中至少一個連結的不重複設定檔百分比。 </td> 
  </tr>
  <tr> 
   <td> 不重複傳遞<br/> </td> 
   <td> 成功收到至少一封電子郵件的不重複設定檔數。</td> 
  </tr>
  <tr> 
   <td> 不重複電子郵件取消訂閱<br/> </td> 
   <td> 取消訂閱您電子郵件的設定檔數目。<br/> </td> 
  </tr>
  <tr> 
   <td> 不重複的預估電子郵件開啟次數<br/> </td> 
   <td> 可能開啟電子郵件之不重複電子郵件收件者的預估人數。 此量度旨在套用從手動開啟電子郵件的不重複設定檔計算出的不重複開啟率，並將此不重複開啟率套用至僅由郵件伺服器開啟電子郵件的使用者，以提供由郵件伺服器觸發的隱私權或安全性掃描的更準確個人參與計數。<br/> </td> 
  </tr>
  <tr> 
   <td> 不重複開啟<br/> </td> 
   <td> 開啟傳送的設定檔數。 <br>請注意，計算唯一開啟次數時，會將過去10天列入考量。 如果設定檔在10天內註冊了多次開啟，則會計為不重複開啟。 但是，如果設定檔有2個開啟間隔超過10天，則不會視為唯一開啟。<br/> </td> 
  </tr> 
  <tr>
  <tr> 
   <td> 不重複傳送<br/> </td> 
   <td>至少嘗試傳送一封電子郵件的不重複設定檔數目。<br/> </td> 
  </tr>
  <tr> 
   <td> 不重複傳送錯誤<br/> </td> 
   <td>在傳出程式期間遇到至少一個傳送錯誤的不重複設定檔數目。<br/> </td> 
  </tr>
  <tr> 
   <td> 不重複傳送排除<br/> </td> 
   <td>因適用性規則、對象細分或設定檔狀態而排除無法接收訊息的不重複設定檔數目。 <a href="exclusion-list.md">進一步瞭解排除專案的計算方式</a>。<br/> </td> 
  </tr>
  <tr> 
   <td>唯一目標<br/> </td> 
   <td>在套用排除、隱藏或同意移除之前，符合對象資格的不重複設定檔數目。<br/> </td> 
  </tr> 
  <tr> 
   <td> 取消訂閱<br/> </td> 
   <td> 對取消訂閱連結的點按次數。<br/> </td> 
  </tr> 
 </tbody> 
</table>

## 簡訊量度

<table> 
  <thead> 
    <tr> 
      <th> 簡訊量度 </th> 
      <th> 定義 </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>已傳遞</td> 
      <td>成功傳送的SMS訊息數（與SMS訊息總數相關）。</td> 
    </tr>
    <tr> 
      <td>點按次數</td> 
      <td>SMS訊息中連結的點按次數。</td> 
    </tr>
    <tr> 
      <td>傳出SMS訊息的退信</td> 
      <td>與已傳送SMS訊息總數相關的傳送程式與自動傳回處理期間累積的錯誤總數。</td> 
    </tr>
    <tr> 
      <td>傳出簡訊錯誤</td> 
      <td>發生的總錯誤數，導致SMS訊息無法傳送給收件者。</td> 
    </tr>
    <tr> 
      <td>傳出簡訊排除</td> 
      <td>Adobe Journey Optimizer不接收SMS訊息的設定檔數。 <a href="exclusion-list.md">進一步瞭解排除專案的計算方式</a>。</td> 
    </tr>
    <tr> 
      <td>不重複點按</td> 
      <td>點選SMS訊息中連結的不重複收件者人數。</td> 
    </tr>
    <tr> 
      <td>展示次數</td> 
      <td>簡訊顯示或開啟的次數。</td> 
    </tr>
    <tr> 
      <td>不重複顯示</td> 
      <td>開啟SMS訊息（排除來自相同使用者的多個互動）的不重複收件者人數。</td> 
    </tr>
    <tr> 
      <td>人員</td> 
      <td>接收或與SMS訊息互動的不重複使用者設定檔數目。</td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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
   <td>與應用程式內訊息所含按鈕互動的設定檔總數。<br/> </td> 
  </tr>
  <tr> 
   <td>點按率<br/> </td> 
   <td>與已看到訊息的使用者相比，與應用程式內訊息中所包含按鈕互動的使用者百分比。<br/> </td> 
  </tr>
  <tr> 
   <td>解除率<br/> </td> 
   <td>設定檔已解除的應用程式內訊息百分比。<br/> </td> 
  </tr>
  <tr> 
   <td>曝光次數<br/> </td> 
   <td>傳遞給所有使用者的應用程式內訊息總數。<br/> </td>
  </tr>
  <tr> 
   <td>不重複曝光次數<br/> </td> 
   <td>已向其傳遞應用程式內訊息的不重複使用者人數。<br/> </td>
  </tr>
  <tr> 
   <td>顯示<br/> </td>
   <td>應用程式內訊息開啟的次數。<br/> </td>
  </tr>
  <tr> 
   <td>唯一顯示區<br/> </td>
   <td>應用程式內訊息的開啟次數，排除來自相同設定檔的多個互動。<br/> </td>
  </tr>
  <tr> 
   <td>不重複點按<br/> </td>
   <td>在您的應用程式內訊息中點按內容的設定檔數目。<br/> </td>
  </tr>
  <tr> 
   <td>點按<br/> </td>
   <td>在您的應用程式內訊息中，內容被點按的次數。<br/> </td>
  </tr>
  <tr> 
   <td>點進率(CTR)<br/> </td>
   <td>與應用程式內訊息互動的使用者百分比。<br/> </td>
  </tr>
  <tr> 
   <td>點進開啟率(CTOR)<br/> </td>
   <td>應用程式內訊息開啟的次數。<br/> </td>
  </tr>
  <tr> 
   <td>傳送<br/> </td>
   <td>已傳送的應用程式內訊息總數。<br/> </td>
  </tr>
  <tr> 
   <td>傳入已觸發<br/> </td>
   <td>使用者互動或預先定義事件觸發應用程式內訊息的次數。<br/> </td>
  </tr>
  <tr> 
   <td>傳入解除次數<br/> </td>
   <td>使用者未與應用程式內訊息互動即解除訊息的次數。<br/> </td>
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
   <td> 推播自訂動作<br/> </td> 
   <td>設定檔回應推播通知所採取的自訂動作數目。<br/> </td> 
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
   <td>跳出率<br/> </td> 
   <td>已檢視登入頁面但未互動或訂閱的使用者相對於造訪總數的百分比。<br/> </td> 
</tr>
 <tr> 
   <td>點按<br/> </td> 
   <td>內容在登入頁面中被點按的次數。<br/> </td> 
</tr>

<tr> 
   <td>登陸頁面轉換<br/> </td> 
   <td>與登入頁面互動的人數，例如，訂閱表單的人數。<br/> </td> 
</tr>
<tr> 
   <td>登陸頁面轉換率<br/> </td> 
   <td>與登入頁面互動（例如訂閱了表單）的人員相對於造訪總數的百分比。<br/> </td> 
</tr>
 <tr> 
   <td>登陸頁面檢視<br/> </td> 
   <td>從歷程和外部來源造訪您的登入頁面總數，包括來自相同設定檔的多次造訪。<br/> </td> 
</tr>
<tr> 
   <td>不重複登陸頁面轉換<br/> </td> 
   <td>與登入頁面互動的不重複人數，不包括來自相同設定檔的多個互動。<br/> </td> 
</tr>
 <tr> 
   <td>不重複登陸頁面檢視<br/> </td> 
   <td>造訪您登陸頁面的不重複人員數量，不包括來自相同設定檔的多次造訪。<br/> </td> 
</tr>
 </tbody> 
</table>

## 直接郵件 {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>已傳遞<br/> </td> 
   <td>成功傳遞給收件者的直接郵件訊息數目。<br/> </td> 
</tr>
<tr> 
   <td>傳出錯誤<br/> </td> 
   <td>處理或傳送期間發生錯誤，無法成功傳遞的直接郵件訊息數目。<br/> </td> 
</tr>
<tr> 
   <td>傳出排除專案<br/> </td> 
   <td>由於預先定義的條件或Adobe Journey Optimizer的篩選而從接收直接郵件中排除的設定檔數。 <a href="exclusion-list.md">進一步瞭解排除專案的計算方式</a>。<br/> </td> 
</tr>
<tr> 
   <td>輪廓<br/> </td> 
   <td>識別為直接郵件行銷活動目標對象的使用者設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>已傳送<br/> </td> 
   <td>作為行銷活動的一部分成功傳送的直接郵件訊息總數。<br/> </td> 
</tr>
<tr> 
   <td>已鎖定目標<br/> </td> 
   <td>準備並處理的直接郵件傳送總數。<br/> </td> 
</tr>
 </tbody> 
</table>


## 內容卡量度 {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> 量度<br/> </th> 
   <th> 定義<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>點進率(CTR)<br/> </td> 
   <td>與內容卡互動的使用者百分比。<br/> </td> 
</tr>
<tr> 
   <td>點按<br/> </td> 
   <td>內容卡中內容被點按的次數。<br/> </td> 
</tr>
<tr> 
   <td>顯示<br/> </td> 
   <td>訊息開啟的次數。<br/> </td> 
</tr>
<tr> 
   <td>人員<br/> </td> 
   <td>符合內容卡目標設定檔資格的使用者設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>不重複點按<br/> </td> 
   <td>按一下內容卡中內容的設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>唯一顯示區<br/> </td> 
   <td>訊息開啟的次數，一個設定檔的多個互動不會被列入考量。<br/> </td> 
</tr>
 </tbody> 
</table>

## 網頁量度 {#web}

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
   <td>內容在您網頁中的點按次數。<br/> </td> 
</tr>
<tr> 
   <td>點進率(CTR)<br/> </td> 
   <td>與網頁互動的使用者百分比。<br/> </td> 
</tr>
<tr> 
   <td>顯示<br/> </td> 
   <td>網頁開啟的次數。<br/> </td> 
</tr>
<tr> 
   <td>人員<br/> </td> 
   <td>符合網頁目標設定檔資格的設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>不重複點按<br/> </td> 
   <td>在您網頁中點按內容的設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>唯一顯示區<br/> </td> 
   <td>開啟網頁的次數，一個設定檔的多個互動未列入考量。<br/> </td> 
</tr>
 </tbody> 
</table>

## 程式碼型體驗量度 {#code-based}

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
   <td>使用者點按顯示給他們之個人化體驗的總次數。<br/> </td> 
</tr>
<tr> 
   <td>點進率(CTR)<br/> </td> 
   <td>與連結、廣告或建議顯示次數相較之下，按一下連結的使用者百分比。<br/> </td> 
</tr>
<tr> 
   <td>轉換率<br/> </td> 
   <td>導致使用者動作（例如點按）的顯示百分比，表示模型成功吸引使用者。<br/> </td> 
</tr>
<tr> 
   <td>決定專案績效<br/> </td> 
   <td>評估每個專案在吸引使用者及推動所需動作（例如購買、點按或其他回應）方面的執行狀況。<br/> </td> 
</tr>
<tr> 
   <td>決策KPI<br/> </td> 
   <td>訪客與體驗互動的關鍵深入分析，包括專案總計、點按總計、顯示總計和遞補率。<br/> </td> 
</tr>
<tr> 
   <td>顯示<br/> </td> 
   <td>在各種接觸點之間，向使用者顯示或呈現個人化體驗的總次數。<br/> </td> 
</tr>
<tr> 
   <td>參與Funnel<br/> </td> 
   <td>透過評估funnel每個階段驅動使用者互動的效能來監視個人化體驗的效能。<br/> </td> 
</tr>
<tr> 
   <td>依選擇策略參與Funnel<br/> </td> 
   <td>監視和分析不同的選取策略如何有效地吸引具有個人化體驗的使用者。<br/> </td> 
</tr>
<tr> 
   <td>人員<br/> </td> 
   <td>符合程式碼型體驗目標設定檔資格的使用者設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>排名策略<br/> </td> 
   <td>比較兩種流量型別的AI驅動排名模型效能的深入分析：模型驅動和維持。<br/> </td> 
</tr>
<tr> 
   <td>按CTR<br/>排名最前的決定專案 </td> 
   <td>根據個別專案的點進率(CTR)，強調其效能，協助評估哪些專案最能有效吸引使用者。<br/> </td> 
</tr>
<tr> 
   <td>不重複點按<br/> </td> 
   <td>在您的程式碼型體驗中按一下內容的設定檔數目。<br/> </td> 
</tr>
<tr> 
   <td>唯一顯示區<br/> </td> 
   <td>開啟體驗的次數，一個設定檔的多個互動不會被列入考量。<br/> </td> 
</tr>
 </tbody> 
</table>
