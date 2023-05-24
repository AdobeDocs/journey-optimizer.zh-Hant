---
solution: Journey Optimizer
product: journey optimizer
title: 歷程即時報告
description: 瞭解如何使用行程即時報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e3781f79-7c8d-4512-b44f-835639b1471f
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 5%

---

# 歷程即時報告 {#journey-live-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_live_report"
>title="歷程即時報告"
>abstract="歷程即時報告可讓您僅在過去 24 小時內對歷程的影響和效能進行即時測量和視覺化。您的報告會分為不同的 Widget，詳細說明您的歷程的成功和錯誤。每個報告儀表板都可以透過調整大小或移除 Widget 來修改。"

您可以直接通過 **[!UICONTROL 查看報表]** 按鈕

![](assets/report_journey.png)

旅程 **[!UICONTROL 即時報告]** 的子菜單。

* [歷程](#journey-live)
* [電子郵件](#email-live)
* [推播](#push-live)
* [簡訊](#sms-live)

旅程 **[!UICONTROL 即時報告]** 被分成不同的小部件，詳細描述你旅途的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](live-report.md#modify-dashboard)。

有關Adobe Journey Optimizer可用的每個指標的詳細清單，請參閱 [此頁](live-report.md#list-of-components-live)。

## 行程頁籤 {#journey-live}

從你的旅程 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 旅程]** 頁籤可讓您清楚地查看有關行程的最重要跟蹤資料。

![](assets/journey_live_1.png)

+++瞭解有關「旅程」報告可用的不同度量和小部件的詳細資訊。

**[!UICONTROL 旅程效能]** 允許您逐步查看目標配置檔案的路徑。

的 **[!UICONTROL 旅程統計]** 小部件顯示以下KPI:

* **[!UICONTROL 輸入的配置檔案]**:到達旅程的入門事件的個人總數。

* **[!UICONTROL 退出配置檔案]**:離開旅程的個人總數。

* **[!UICONTROL 失敗的單個行程]**:未成功執行的單個行程的總數。

的 **[!UICONTROL 過去24小時內執行的事件]** 和 **[!UICONTROL 事件]** 通過小部件，您可以通過摘要編號、圖形和表來查看哪些事件已成功執行。

的 **[!UICONTROL 過去24小時內執行的操作]** 和 **[!UICONTROL 執行的操作和錯誤]** 小部件表示觸發操作時發生的最成功的操作和錯誤。 「操作」圖形、表和摘要編號包含可用於操作的資料，例如：

* **[!UICONTROL 已執行的操作]**:成功執行行程的操作總數。

* **[!UICONTROL 操作中出錯]**:為操作發生的錯誤總數。
+++

## 電子郵件頁籤 {#email-live}

從你的旅程 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 電子郵件]** 頁籤，詳細列出與在旅途中發送的電子郵件遞送相關的主要資訊。

![](assets/journey_live_2.png)

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

>[!NOTE]
>
>只有在電子郵件中插入了決定時，「提供」小部件和度量才可用。 有關決策管理的詳細資訊，請參閱 [頁](../offers/get-started/starting-offer-decisioning.md)。

的 **[!UICONTROL 提供統計資訊]** 和 **[!UICONTROL 提供統計資訊]** 隨著時間推移，小部件可衡量您的產品的成功程度以及對目標受眾的影響。 它使用KPI詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已發送優惠]**:發送要約的總數。

* **[!UICONTROL 提供印象]**:在交貨中開啟要約的次數。

* **[!UICONTROL 提供點擊]**:在交貨中按一下要約的次數。
+++

## 推送通知頁籤 {#push-live}

從你的旅程 **[!UICONTROL 即時報告]**，也請參見Wiki頁。 **[!UICONTROL 推送通知]** 頁籤詳細列出與在行程中發送的推送交貨相關的主要資訊。

![](assets/journey_live_3.png)

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

![](assets/journey_live_4.png)

+++瞭解SMS報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL SMS — 正在發送統計資訊]** 表詳細列出了您交付的成功：

* **[!UICONTROL 目標]**:符合此傳遞目標配置檔案的用戶配置檔案數。

* **[!UICONTROL 已排除]**:未接收消息的從目標配置檔案中排除的用戶配置檔案數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 按一下]**:在傳遞中按一下內容的次數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 簡訊摘要]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL 已交付]**:成功發送的消息數。

* **[!UICONTROL 邊界]**:在交貨和自動退貨處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 排除原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。
+++
