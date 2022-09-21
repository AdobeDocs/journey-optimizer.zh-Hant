---
title: 行銷活動全域報告
description: 了解如何使用Campaign全域報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '1660'
ht-degree: 1%

---

# 行銷活動全域報告 {#campaign-global-report}

您可以使用 **[!UICONTROL 所有時間]** 按鈕。

![](assets/campaign_report_global_5.png)

行銷活動 **[!UICONTROL 全域報表]** 頁面中顯示以下索引標籤：

* [Campaign](#campaign-global)
* [電子郵件](#email-global)
* [推播](#push-global)
* [SMS](#sms-global)

行銷活動 **[!UICONTROL 全域報表]** 會分為不同的小工具，詳細說明促銷活動的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](../reports/global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](global-report.md#list-of-components-global.md)

## 行銷活動標籤 {#campaign-global}

### 傳遞 {#delivery-global}

![](assets/campaign_report_global_1.png)

此 **[!UICONTROL 促銷活動的統計資料]** 介面工具集詳細說明與促銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**:開始歷程的設定檔數。

* **[!UICONTROL 已傳遞的動作]**:歷程中某個動作已傳送的不重複總次數。

* **[!UICONTROL 操作在%中失敗]**:歷程中某個動作失敗的不重複次數總計，與已傳送動作的不重複次數總計相比。

## 電子郵件索引標籤 {#email-global}

![](assets/campaign_report_global_2.png)

從您的行銷活動 **[!UICONTROL 全域報表]**, **[!UICONTROL 電子郵件]** 索引標籤會詳細說明與在促銷活動中傳送的電子郵件傳送相關的主要資訊。

+++進一步了解「電子郵件」報表中可用的不同量度和小工具。

此 **[!UICONTROL 電子郵件傳送統計資料]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL 已鎖定]**:傳送分析期間處理的訊息總數。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 傳送率]**:已成功發送的消息的百分比。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 反彈率]**:跳出的電子郵件與傳送的電子郵件的百分比。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 錯誤率]**:傳送期間發生、無法傳送的錯誤百分比，與已傳送的電子郵件相比。

* **[!UICONTROL 重試]**:佇列中重試的電子郵件數。

* **[!UICONTROL 已排除]**:已由Adobe Journey Optimizer排除的設定檔數目。

此 **[!UICONTROL 電子郵件 — 追蹤統計資料]** 介面工具集包含您傳送之收件者活動的可用資料：

* **[!UICONTROL 開啟]**:傳送中開啟傳送的次數。

* **[!UICONTROL 不重複開啟次數]**:已開啟傳遞的百分比。

* **[!UICONTROL 開放率]**:已開啟電子郵件的總數與已傳送電子郵件的總數相比。

* **[!UICONTROL 點按次數]**:電子郵件中內容被點按的次數。

* **[!UICONTROL 不重複點按次數]**：按一下電子郵件內容的收件者人數。

* **[!UICONTROL 不重複點按率]**:與傳送互動的使用者百分比。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴]**:宣告郵件為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 傳送統計資料]** 圖表包含可用於傳送電子郵件的資料，例如：

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 重試]**:佇列中重試的電子郵件數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 跳出類別]** 小工具包含與退信消息相關的可用資料，例如：

* **[!UICONTROL 硬跳出]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL 軟跳出]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL 已忽略]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

如需退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

此 **[!UICONTROL 錯誤原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

此 **[!UICONTROL 排除的原因]** 圖表和表格顯示阻止從目標設定檔排除的使用者設定檔接收訊息的不同原因。

此 **[!UICONTROL 電子郵件 — 頂端Url]** 圖表和表格會詳細說明哪些URL最常被瀏覽。

此 **[!UICONTROL 電子郵件 — 最上層收件者網域]** 圖表和表格詳細說明收件者最常使用哪些網域來開啟電子郵件。

>[!NOTE]
>
>此 **[!UICONTROL 最佳化與非最佳化]** 和 **[!UICONTROL 傳送時間最佳化]**  只有在為您的傳送啟動「傳送時間最佳化」選項時，介面工具集才可用。 如需傳送時間最佳化的詳細資訊，請參閱 [本頁](../messages/send-time-optimization.md).

此 **[!UICONTROL 最佳化與非最佳化]** 圖表詳細說明了與訊息相關的主要資訊（無論訊息是否已最佳化）:

* **[!UICONTROL 已傳送]**:傳送的傳送總數。
* **[!UICONTROL 開啟]**:傳送中開啟傳送的次數。
* **[!UICONTROL 點按次數]**:電子郵件中內容被點按的次數。

此 **[!UICONTROL 傳送時間最佳化]** 根據傳送方法，詳細說明傳送是否成功：優化或正常。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。
+++

## 推播通知標籤 {#push-global}

從您的行銷活動 **[!UICONTROL 全域報表]**, **[!UICONTROL 推播通知]** 索引標籤會詳細說明與促銷活動中傳送的推送傳送相關的主要資訊。

![](assets/campaign_report_global_3.png)

+++進一步了解「推送」報表可用的不同量度和Widget。

此 **[!UICONTROL 推播通知 — 傳送統計資料]** 表格會透過圖表和KPI，詳細說明與推播通知相關的主要資訊：

* **[!UICONTROL 已鎖定]**:傳送分析期間處理的訊息總數。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 傳送率]**:已成功發送的消息的百分比。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 反彈率]**:跳出的推播通知與傳送的推播通知的百分比。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 錯誤率]**:與傳送的推播通知相比，傳送期間發生而無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**:已由Adobe Journey Optimizer排除的設定檔數目。

此 **[!UICONTROL 推播 — 追蹤統計資料]** 包含您傳送的收件者活動可用資料：

* **[!UICONTROL 開啟]**:傳送中開啟訊息的次數。

* **[!UICONTROL 開放率]**:已開啟推播通知的百分比。

* **[!UICONTROL 動作]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL 參與]**:此推播通知的開啟次數和動作總數，亦即設定檔開啟了推播或按了按鈕。

* **[!UICONTROL 參與率]**:此推播通知的開啟次數和動作百分比，亦即設定檔開啟了推播或按鈕被點按時。

此 **[!UICONTROL 推播通知摘要]** 圖形包含可用於傳送推播通知的資料，例如：

* **[!UICONTROL 開啟]**:傳送中開啟訊息的次數。

* **[!UICONTROL 動作]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

>[!NOTE]
>
>此 **[!UICONTROL 最佳化與非最佳化]** 和 **[!UICONTROL 傳送時間最佳化]**  只有在為您的傳送啟動「傳送時間最佳化」選項時，介面工具集才可用。 如需傳送時間最佳化的詳細資訊，請參閱 [本頁](../messages/send-time-optimization.md).

此 **[!UICONTROL 最佳化與非最佳化]** 圖表詳細說明了與訊息相關的主要資訊（無論訊息是否已最佳化）:

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL 開啟]**:傳送中開啟傳送的次數。
* **[!UICONTROL 動作]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

此 **[!UICONTROL 傳送時間最佳化]** 根據傳送方法，詳細說明傳送是否成功：優化或正常。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。
* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

此 **[!UICONTROL 錯誤原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤。

此 **[!UICONTROL 排除的原因]** 圖表和表格顯示阻止從目標設定檔排除的使用者設定檔接收訊息的不同原因。

此 **[!UICONTROL 依平台追蹤]**, **[!UICONTROL 依平台傳送]** 和 **[!UICONTROL 依平台劃分]** 圖形和表格會根據收件者的作業系統，詳細說明推播通知的成功。
+++

## SMS標籤 {#sms-global}

從您的行銷活動 **[!UICONTROL 全域報表]**, **[!UICONTROL 簡訊]** 索引標籤會詳細說明與促銷活動中傳送的SMS傳送相關的主要資訊。

![](assets/campaign_report_global_4.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS — 傳送統計資料]** 表格會詳細說明傳送的成功：

* **[!UICONTROL 已鎖定]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 按日期的SMS效能]** 介面工具集會透過圖表詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 排除原因]**, **[!UICONTROL 跳出原因]** 和 **[!UICONTROL 錯誤原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的促銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動即時報告](campaign-live-report.md)
