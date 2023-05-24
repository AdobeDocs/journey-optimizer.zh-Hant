---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動即時報告
description: 瞭解如何使用市場活動即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 7%

---

# 行銷活動即時報告 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="行銷活動即時報告"
>abstract="行銷活動即時報告可讓您僅在過去 24 小時內對行銷活動的影響和效能進行即時測量和視覺化。您的報告會分為不同的 Widget，詳細說明您的行銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除 Widget 來修改。"

您可以通過 **[!UICONTROL 即時視圖]** 按鈕

市場活動 **[!UICONTROL 即時報告]** 的子菜單。

* [Campaign](#campaign-live)
* [電子郵件](#email-live)
* [推播](#push-live)
* [簡訊](#sms-live)
* [Web](#web-tab)

市場活動 **[!UICONTROL 即時報告]** 被分成不同的小部件，詳細列出您的活動的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](../reports/live-report.md#modify-dashboard)。

有關Adobe Journey Optimizer可用的每個指標的詳細清單，請參閱 [此頁](live-report.md#list-of-components-live)。

## 市場活動頁籤 {#campaign-global}

### 傳送 {#delivery-global}

的 **[!UICONTROL 市場活動統計]** 小部件詳細列出與市場活動相關的主要資訊：

* **[!UICONTROL 輸入的配置檔案]**:開始此行程的配置檔案數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件頁籤 {#email-live}

從您的活動 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 電子郵件]** 頁籤詳細列出與市場活動中發送的電子郵件交貨相關的主要資訊。

![](assets/campaign_report_live_1.png)

+++瞭解電子郵件報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 電子郵件發送統計資訊]** 小部件詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 通過電子郵件發送度量]** 表格 **[!UICONTROL 電子郵件摘要]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 按一下]**:在傳遞中按一下內容的次數。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL 垃圾郵件投訴]**:將郵件聲明為垃圾郵件或垃圾郵件的次數。

的 **[!UICONTROL 彈出原因]**。 **[!UICONTROL 彈出類別]** 和 **[!UICONTROL 硬體和彈出 — 通過電子郵件]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL 硬彈]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL 軟彈跳]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL 已忽略]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

的 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL 電子郵件 — 頂級收件人域]** 圖表和表詳細資訊，哪些域是收件人開啟電子郵件時最常用的域。
+++

## 推送通知頁籤 {#push-live}

從您的活動 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 推送通知]** 頁籤詳細列出與市場活動中發送的推送交貨相關的主要資訊。

![](assets/campaign_report_live_2.png)

+++瞭解有關「推送」報告可用的不同度量和小部件的詳細資訊。

**[!UICONTROL 推送通知發送效能]**。 **[!UICONTROL 推送通知摘要]** 和 **[!UICONTROL 發送度量 — 按推送]** 小部件詳細列出與您的消息相關的主要資訊：

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL 預訂]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL 發送統計資訊 — 失敗]** 小部件允許您查看發生了多少個錯誤和彈出。

的 **[!UICONTROL 按平台跟蹤]**。 **[!UICONTROL 按平台發送]** 和 **[!UICONTROL 按平台細分]** 圖表和表根據作業系統詳細說明了推送通知的成功。
+++

## SMS頁籤 {#sms-live}

從您的活動 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 簡訊]** 頁籤詳細列出與市場活動中發送的SMS遞送相關的主要資訊。

![](assets/campaign_report_live_3.png)

+++瞭解SMS報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL SMS — 統計]** 表詳細列出了您交付的成功：

* **[!UICONTROL 目標]**:符合此傳遞目標配置檔案的用戶配置檔案數。

* **[!UICONTROL 已排除]**:未接收消息的從目標配置檔案中排除的用戶配置檔案數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 按一下]**:URL訪問總數。

的 **[!UICONTROL 按日期顯示的SMS效能]** 小部件使用圖表詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 排除原因]**。 **[!UICONTROL 彈出原因]** 和 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。
+++

## Web頁籤 {#web-tab}

從您的活動 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL Web]** 頁籤詳細列出與網頁相關的主要資訊。

+++瞭解有關Web報告可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL Web效能]** KPI將詳細列出與訪問者的Web體驗相關的主要資訊，例如：

* **[!UICONTROL 獨特印象]**:向其提供Web體驗的唯一用戶數。

* **[!UICONTROL 印象]**:提供給所有用戶的Web體驗總數。

* **[!UICONTROL 按一下]**:URL訪問總數。

的 **[!UICONTROL Web摘要]** 圖形顯示了您在相關期間的Web體驗（印象、獨特印象和點擊）的演變。

的 **[!UICONTROL 按元素按一下]** 表詳細列出了與訪問者參與網頁中各種元素相關的主要資訊。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的市場活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報告](campaign-global-report.md)
