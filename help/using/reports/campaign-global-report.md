---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報告
description: 瞭解如何使用「市場活動全局」報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '2036'
ht-degree: 3%

---

# 行銷活動全域報告 {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="行銷活動全域報告"
>abstract="行銷活動全域報告可測量您的行銷活動在選取時段內的影響。您的報告會分為不同的 Widget，詳細說明您的行銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除 Widget 來修改。"

您可以直接從市場活動訪問市場活動全局報告， **[!UICONTROL 查看報表]** 按鈕

![](assets/campaign_report_global_5.png)

市場活動 **[!UICONTROL 全局報告]** 的子菜單。

* [Campaign](#campaign-global)
* [電子郵件](#email-global)
* [應用程式內](#inapp-global)
* [推播](#push-global)
* [簡訊](#sms-global)
* [Web](#web-tab)

市場活動 **[!UICONTROL 全局報告]** 被分成不同的小部件，詳細列出您的活動的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](../reports/global-report.md#modify-dashboard)。

有關Adobe Journey Optimizer可用的每個指標的詳細清單，請參閱 [此頁](global-report.md#list-of-components-global.md)

## 市場活動頁籤 {#campaign-global}

### 傳送 {#delivery-global}

![](assets/campaign_report_global_1.png)

的 **[!UICONTROL 市場活動統計]** 小部件詳細列出與市場活動相關的主要資訊：

* **[!UICONTROL 輸入的配置檔案]**:開始此行程的配置檔案數。

* **[!UICONTROL 已交付的操作]**:在行程中執行操作的唯一時間總數。

* **[!UICONTROL 操作在%中失敗]**:在行程中某個操作失敗的唯一次數與已傳遞操作的唯一次數之和。

## 電子郵件頁籤 {#email-global}

![](assets/campaign_report_global_2.png)

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 電子郵件]** 頁籤詳細列出與「市場活動」中發送的電子郵件交貨相關的主要資訊。

+++瞭解電子郵件報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 電子郵件發送統計資訊]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL 目標]**:在傳遞分析期間處理的郵件總數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 交貨率]**:成功發送的郵件百分比。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 彈跳率]**:與發送的電子郵件相比，已跳轉的電子郵件的百分比。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 錯誤率]**:與發送的電子郵件相比，在發送過程中發生的阻止發送錯誤的百分比。

* **[!UICONTROL 重試次數]**:隊列中重試的電子郵件數。

* **[!UICONTROL 已排除]**:被Adobe Journey Optimizer排除的檔案數。

的 **[!UICONTROL 電子郵件 — 跟蹤統計]** 小部件包含用於您遞送的收件人活動的可用資料：

* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。

* **[!UICONTROL 唯一開啟]**:已開啟交貨的百分比。

* **[!UICONTROL 開啟速率]**:已開啟電子郵件的總數與已發送電子郵件的數量相比。

* **[!UICONTROL 按一下]**:在電子郵件中按一下內容的次數。

* **[!UICONTROL 唯一按一下]**：按一下電子郵件內容的收件人數。

* **[!UICONTROL 唯一按一下率]**:與遞送互動的用戶百分比。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL 垃圾郵件投訴]**:將郵件聲明為垃圾郵件或垃圾郵件的次數。

的 **[!UICONTROL 正在發送統計資訊]** 圖形包含可用於已發送電子郵件的資料，如：

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 重試次數]**:隊列中重試的電子郵件數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 彈出原因]** 和 **[!UICONTROL 彈出類別]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL 硬彈]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL 軟彈跳]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL 已忽略]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

有關退貨的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 的子菜單。

的 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL 排除的原因]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL 電子郵件 — 頂部URL]** 圖表和表詳細資訊，您傳遞的URL訪問量最大。

的 **[!UICONTROL 電子郵件 — 頂級收件人域]** 圖表和表詳細資訊，哪些域是收件人開啟電子郵件時最常用的域。

>[!NOTE]
>
>的 **[!UICONTROL 優化與未優化]** 和 **[!UICONTROL 發送時間優化]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱 [此頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL 優化與未優化]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL 已發送]**:交貨的發送總數。
* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。
* **[!UICONTROL 按一下]**:在電子郵件中按一下內容的次數。

的 **[!UICONTROL 發送時間優化]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。
+++

## 應用程式內頁籤 {#inapp-global}

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 應用程式內]** 頁籤詳細列出與市場活動中發送的In-app交貨相關的主要資訊。

![](assets/campaign_report_global_6.png)

+++瞭解有關應用程式內報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 應用內效能]** KPI將詳細列出與訪問者與應用內消息的約定相關的主要資訊，例如：

* **[!UICONTROL 獨特印象]**:向其傳遞In-app消息的唯一用戶數。

* **[!UICONTROL 印象]**:傳遞給所有用戶的應用內消息總數。

* **[!UICONTROL 按一下率]**:與看到該消息的用戶相比，與In-app消息中包含的按鈕交互的用戶百分比。

* **[!UICONTROL 消除率]**:接收者拒絕的應用內郵件百分比。

的 **[!UICONTROL 應用內摘要]** 圖形顯示了您在有關期間的應用內印象的演變。

的 **[!UICONTROL 按一下按鈕]** 圖形和表包含每個按鈕的收件人行為的可用資料：

* **[!UICONTROL 按一下]**:與In-app消息中包含的按鈕交互的收件人總數。

* **[!UICONTROL 按一下率]**:與看到該消息的用戶相比，與In-app消息中包含的按鈕交互的用戶百分比。
+++

## 推送通知頁籤 {#push-global}

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 推送通知]** 頁籤詳細列出與市場活動中發送的推送交貨相關的主要資訊。

![](assets/campaign_report_global_3.png)

+++瞭解有關「推送」報告可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 推送通知 — 發送統計資訊]** 表詳細列出了與使用圖表和KPI的推送通知相關的主要資訊：

* **[!UICONTROL 目標]**:在傳遞分析期間處理的郵件總數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 交貨率]**:成功發送的郵件百分比。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 彈跳率]**:與發送的推送通知相比，已跳轉的推送通知的百分比。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 錯誤率]**:與發送的推送通知相比，在發送過程中發生的錯誤阻止發送的百分比。

* **[!UICONTROL 已排除]**:被Adobe Journey Optimizer排除的檔案數。

的 **[!UICONTROL 推送 — 跟蹤統計資訊]** 包含您交貨的收件人活動的可用資料：

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 開啟速率]**:開啟的推送通知百分比。

* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL 預訂]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

* **[!UICONTROL 訂約率]**:此推送通知的開啟和操作的百分比，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL 推送通知摘要]** 圖形包含可用於發送推送通知的資料，如：

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

>[!NOTE]
>
>的 **[!UICONTROL 優化與未優化]** 和 **[!UICONTROL 發送時間優化]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱 [此頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL 優化與未優化]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。
* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

的 **[!UICONTROL 發送時間優化]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

的 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL 排除的原因]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL 按平台跟蹤]**。 **[!UICONTROL 按平台發送]** 和 **[!UICONTROL 按平台細分]** 圖表和表格根據收件人的作業系統詳細說明推送通知的成功。
+++

## SMS頁籤 {#sms-global}

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 簡訊]** 頁籤詳細列出與市場活動中發送的SMS遞送相關的主要資訊。

![](assets/campaign_report_global_4.png)

+++瞭解SMS報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL SMS — 正在發送統計資訊]** 表詳細列出了您交付的成功：

* **[!UICONTROL 目標]**:符合此傳遞目標配置檔案的用戶配置檔案數。

* **[!UICONTROL 已排除]**:未接收消息的從目標配置檔案中排除的用戶配置檔案數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 按日期顯示的SMS效能]** 小部件使用圖表詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 排除原因]**。 **[!UICONTROL 彈出原因]** 和 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL SMS — 按連結按一下]** 和 **[!UICONTROL SMS — 跟蹤統計資訊]** 小部件詳細列出與訪問者與URL的約定有關的主要資訊。

+++

## Web頁籤 {#web-tab}

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL Web]** 頁籤詳細列出與網頁相關的主要資訊。

![](assets/web-report.png)

+++瞭解有關Web報告可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL Web效能]** KPI將詳細列出與訪問者的Web體驗相關的主要資訊，例如：

* **[!UICONTROL 獨特印象]**:向其提供Web體驗的唯一用戶數。

* **[!UICONTROL 印象]**:提供給所有用戶的Web體驗總數。

* **[!UICONTROL 按一下率]**:與網頁上的各種元素進行互動的訪問者的百分比。

的 **[!UICONTROL Web摘要]** 圖形顯示了您在相關期間的Web體驗（印象、獨特印象和點擊）的演變。

的 **[!UICONTROL 按元素按一下]** 表詳細列出了與訪問者參與網頁中各種元素相關的主要資訊。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的市場活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
