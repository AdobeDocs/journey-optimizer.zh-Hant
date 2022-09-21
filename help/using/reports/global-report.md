---
title: 全域報告
description: 了解如何使用全域報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 開始使用全域報表 {#global-report}

>[!NOTE]
>
> 如果使用查詢服務時透過API進行自訂查詢，報表可能會延遲一些。

使用 **[!UICONTROL 全域報表]** 以測量您在所選時段內的歷程和傳送的影響。

* 如果您想要定位歷程內容中的歷程或傳送，請從 **[!UICONTROL 歷程]** 功能表，存取您的歷程，然後按一下 **[!UICONTROL 檢視報表]** 按鈕。 接著，您就可以找到歷程、電子郵件、簡訊及推播全域報表。

   ![](assets/report_journey.png)

* 如果您想定位促銷活動，請從 **[!UICONTROL 行銷活動]** 功能表，存取您的促銷活動，然後按一下 **[!UICONTROL 報表]** 按鈕。

   ![](assets/report_campaign.png)

* 如果您想從 **[!UICONTROL 即時報表]** 到 **[!UICONTROL 全域報表]** 若要傳送，請按一下 **[!UICONTROL 所有時間]** 切換器。

   ![](assets/report_5.png)

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](#list-of-components-global)

## 自訂控制面板 {#modify-dashboard}

每個報表控制面板都可透過變更時段、調整大小或移除小工具來修改。 變更介面工具集只會影響目前使用者的控制面板。 其他使用者會看到自己的控制面板或預設設定的控制面板。

1. 從「全域」報表中，選取「開始」和「結束」時間來鎖定特定資料。

   ![](assets/report_modify_1.png)

1. 選擇是否要使用切換列從報表中排除測試事件。 如需測試事件的詳細資訊，請參閱 [本頁](../building-journeys/testing-the-journey.md).

   請注意， **[!UICONTROL 排除測試事件]** 選項僅適用於歷程報表。

   ![](assets/report_modify_2.png)

1. 按一下 **[!UICONTROL 修改]** 開始自訂控制面板。

   ![](assets/report_modify_3.png)

1. 拖曳介面工具集的右下角來調整介面工具集大小。

   ![](assets/report_modify_4.png)

1. 按一下 **[!UICONTROL 移除]** 移除您不需要的任何小工具集。

   ![](assets/report_modify_5.png)

1. 對顯示順序和小部件的大小感到滿意後，按一下 **[!UICONTROL 儲存]**.

您的控制面板現在已儲存。 您的不同變更將會重新套用，以供稍後使用您的即時報表。 如有需要，請使用 **[!UICONTROL 重設]** 選項，以還原預設小工具和小工具的順序。

## 元件清單 {#list-of-components-global}

下表提供報表中使用的量度清單及其定義（視傳送類型而定）。

### 歷程量度 {#journey-metrics}

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
   <td> 成功執行歷程之動作的總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 輸入的設定檔<br/> </td> 
   <td> 到達歷程進入事件的個人總數。<br/> </td> 
</tr>
  <tr> 
   <td> 操作錯誤<br/> </td> 
   <td>為動作發生的錯誤總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 退出設定檔<br/> </td> 
   <td> 離開歷程的個人總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 個別歷程失敗<br/> </td> 
   <td> 未成功執行的個別歷程總數。<br/> </td> 
</tr> 
 </tbody> 
</table>

### 電子郵件和簡訊量度 {#email-and-sms-metrics}

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
   <td> 傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 跳出的電子郵件與傳送的電子郵件的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 點擊次數<br/> </td> 
   <td> 電子郵件中內容被點按的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳遞 <br/> </td> 
   <td> 已成功傳送的訊息數，與已傳送的訊息總數相關。<br/></td> 
</tr> 
  <tr> 
   <td> 傳送率<br/> </td> 
   <td> 已成功發送的消息的百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳送期間發生的錯誤總數，使其無法傳送至設定檔。<br/> </td> 
</tr> 
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 傳送期間發生、無法傳送的錯誤百分比，與已傳送的電子郵件相比。<br/> </td> 
</tr>
  <tr> 
   <td> 已排除<br/> </td> 
   <td> 已由Adobe Journey Optimizer排除的設定檔數目。<br/> </td> 
</tr>
  <tr> 
   <td> 硬跳出<br/> </td> 
   <td> 永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。<br/> </td>
</tr>
  <tr> 
   <td> 已忽略<br/> </td> 
   <td> 臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。<br/> </td> 
</tr>
   <tr> 
   <td>選件點按率<br/> </td> 
   <td>與優惠方案互動的使用者百分比。<br/> </td> 
</tr>
   <tr> 
   <td>選件曝光率<br/> </td> 
   <td>已開啟選件與已傳送選件數量的百分比。<br/> </td> 
</tr>
   <tr> 
   <td>優惠方案名稱<br/> </td> 
   <td> 傳送中新增的選件名稱。 有關投放位置的詳細資訊，請參閱 <a href="../offers/offer-library/creating-personalized-offers.md">頁面</a>.<br/> </td> 
</tr>
   <tr> 
   <td>已傳送選件<br/> </td> 
   <td>選件的傳送總數。<br/> </td> 
</tr> 
  <tr>
   <td>開啟數<br/> </td> 
   <td> 訊息開啟的次數。<br/> </td> 
</tr> 
  <tr> 
   <td> 開放率<br/> </td> 
   <td> 已開啟電子郵件的總數與已傳送電子郵件的總數相比。<br/> </td> 
</tr>
  <tr> 
   <td>版位名稱<br/> </td> 
   <td> 用來顯示優惠方案的版位名稱。 有關投放位置的詳細資訊，請參閱 <a href="../offers/offer-library/creating-placements.md">頁面</a>. </td> 
</tr> 
  <tr> 
   <td> 重試次數<br/> </td> 
   <td> 佇列中重試的電子郵件數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳送的傳送總數。<br/> </td> 
</tr>
  <tr> 
   <td> 軟跳出<br/> </td> 
   <td> 臨時錯誤（如完整收件箱）的總數。<br/> </td> 
</tr>
  <tr> 
   <td> 垃圾郵件投訴<br/> </td> 
   <td> 宣告郵件為垃圾郵件或垃圾郵件的次數。<br/> </td> 
</tr>
  <tr> 
   <td> 已鎖定<br/> </td> 
   <td> 傳送分析期間處理的訊息總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 不重複點按次數<br/> </td> 
   <td> 按一下電子郵件中內容的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td>不重複點按率<br/> </td> 
   <td> 與傳送互動的使用者百分比。<br/> </td> 
</tr>
  <tr> 
   <td> 不重複開啟次數<br/> </td> 
   <td>開啟傳遞的收件者人數。<br/> </td> 
</tr> 
  <tr> 
   <td> 取消訂閱<br/> </td> 
   <td> 取消訂閱連結的點按次數。<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
### Experimentation metrics {#experimentation-metrics}
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

### 推播通知量度 {#push-notification-metrics}

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
   <td> 已傳送推播通知的動作總數，例如按鈕點擊或解除。<br/> </td> 
</tr>
  <tr> 
   <td>跳出<br/> </td> 
   <td> 傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。<br/> </td> 
</tr> 
  <tr> 
   <td> 跳出率<br/> </td> 
   <td> 跳出的推播通知與傳送的推播通知的百分比。<br/> </td>
</tr>
  <tr> 
   <td> 已傳遞<br/> </td> 
   <td> 已成功傳送的訊息數，與已傳送的訊息總數相關。<br/> </td> 
</tr> 
  <tr> 
   <td> 傳送率<br/> </td> 
   <td> 成功傳送推播通知的百分比。<br/> </td> 
</tr>
  <tr> 
   <td>參與<br/> </td> 
   <td> 此推播通知的開啟次數和動作總數，亦即設定檔開啟了推播或按了按鈕。<br/> </td> 
</tr> 
  <tr> 
   <td> 參與率<br/> </td> 
   <td> 此推播通知的開啟次數和動作百分比，亦即設定檔開啟了推播或按鈕被點按時。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤<br/> </td> 
   <td> 傳送期間發生的錯誤總數，使其無法傳送至設定檔。<br/> </td> 
</tr>
  <tr> 
   <td> 錯誤率<br/> </td> 
   <td> 與傳送的推播通知相比，傳送期間發生而無法傳送的錯誤百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已排除<br/> </td> 
   <td> 已由Adobe Journey Optimizer排除的設定檔數目。<br/> </td> 
</tr>
  <tr> 
   <td> 開啟數<br/> </td> 
   <td> 傳送至裝置並由使用者點按以開啟應用程式的推播通知總數。 這類似於推播點擊，但若關閉通知，則不會觸發推播開啟。<br/> </td> 
</tr> 
  <tr> 
   <td> 開放率<br/> </td> 
   <td> 已開啟推播通知的百分比。<br/> </td> 
</tr> 
  <tr> 
   <td> 已傳送<br/> </td> 
   <td> 傳送的傳送總數。<br/> </td> 
</tr> 
  <tr> 
   <td> 已鎖定<br/> </td> 
   <td> 傳送分析期間處理的推送訊息總數。<br/> </td> 
</tr>  
 </tbody> 
</table>

### 登陸頁面量度 {#landing-page-metrics}

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
   <td>未與登錄頁面互動且未完成訂閱動作的人數。<br/> </td> 
</tr>
 <tr> 
   <td>跳出率<br/> </td> 
   <td>未與登錄頁面互動且未完成訂閱動作的人數，與瀏覽總數相關。<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>點擊次數<br/> </td> 
   <td>登陸頁面中內容被點按的次數。<br/> </td> 
</tr>
 <tr> 
   <td>點按率<br/> </td> 
   <td>登錄頁面中的點按百分比。<br/> </td>
</tr>
<tr>
<td>轉換<br/> </td> 
   <td>與登錄頁面互動的人數，例如訂閱表單。<br/> </td> 
</tr>
<tr>
   <td>轉換率<br/> </td> 
   <td>與登錄頁面互動的人數（例如訂閱表單），與瀏覽總數相關。<br/> </td> 
</tr>
 <tr> 
   <td>歷程<br/> </td> 
   <td>來自歷程的登錄頁面造訪次數。<br/> </td> 
</tr>
 <tr> 
   <td>其他來源<br/> </td> 
   <td>來自外部來源而非歷程的著陸頁面造訪次數。<br/> </td> 
</tr>
 <tr> 
   <td>瀏覽總數<br/> </td> 
   <td> 來自歷程和外部來源對您登陸頁面的瀏覽總數，包括一個收件者的多次瀏覽。<br/> </td> 
</tr>
 <tr> 
   <td>不重複訪客<br/> </td> 
   <td>瀏覽您的登錄頁面的人數，不會考慮一個收件者的多次瀏覽。<br/> </td> 
</tr>
 <tr> 
   <td>造訪數<br/> </td> 
   <td>對登錄頁面的瀏覽次數，包括一個收件者的多次瀏覽。<br/> </td> 
</tr>
 </tbody> 
</table>

