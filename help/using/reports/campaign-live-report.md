---
title: 行銷活動即時報告
description: 了解如何使用Campaign即時報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '870'
ht-degree: 3%

---

# 行銷活動即時報告 {#campaign-live-report}

您可以使用 **[!UICONTROL 即時檢視]** 按鈕。

行銷活動 **[!UICONTROL 即時報表]** 頁面中顯示以下索引標籤：

* [Campaign](#campaign-live)
* [電子郵件](#email-live)
* [推播](#push-live)
* [SMS](#sms-live)


行銷活動 **[!UICONTROL 即時報表]** 會分為不同的小工具，詳細說明促銷活動的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](../reports/live-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](live-report.md#list-of-components-live).

## 行銷活動標籤 {#campaign-global}

### 傳遞 {#delivery-global}

此 **[!UICONTROL 促銷活動統計資料]** 介面工具集詳細說明與促銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**:開始歷程的設定檔數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## 電子郵件索引標籤 {#email-live}

從您的行銷活動 **[!UICONTROL 即時報表]**, **[!UICONTROL 電子郵件]** 索引標籤會詳細列出與促銷活動中所傳送之電子郵件傳送相關的主要資訊。

![](assets/campaign_report_live_1.png)

+++進一步了解「電子郵件」報表中可用的不同量度和小工具。

此 **[!UICONTROL 電子郵件傳送統計資料]** 介面工具集詳細說明了與您的訊息相關的主要資訊：

* **[!UICONTROL 傳遞]**:已成功發送的消息數。

* **[!UICONTROL 跳出數]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 依電子郵件傳送量度]** 表格和 **[!UICONTROL 電子郵件摘要]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功發送的消息數。

* **[!UICONTROL 跳出數]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 開啟]**:傳送中開啟訊息的次數。

* **[!UICONTROL 點按次數]**:內容在傳送中被點按的次數。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴]**:宣告郵件為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 退回原因]**, **[!UICONTROL 跳出類別]** 和 **[!UICONTROL 硬式和彈回 — 依電子郵件]** 小工具包含與退信消息相關的可用資料，例如：

* **[!UICONTROL 硬跳出]**:永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知」使用者。

* **[!UICONTROL 軟跳出]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL 已忽略]**:臨時的總數，例如「不在辦公室」或技術錯誤，例如，如果發送者類型是郵遞區號。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。

此 **[!UICONTROL 電子郵件 — 最上層收件者網域]** 圖表和表格詳細說明收件者最常使用哪些網域來開啟電子郵件。
+++

## 推播通知標籤 {#push-live}

從您的行銷活動 **[!UICONTROL 即時報表]**, **[!UICONTROL 推播通知]** 索引標籤會詳細說明與促銷活動中傳送的推送傳送相關的主要資訊。

![](assets/campaign_report_live_2.png)

+++進一步了解「推送」報表可用的不同量度和Widget。

**[!UICONTROL 推播通知傳送效能]**, **[!UICONTROL 推播通知摘要]** 和 **[!UICONTROL 傳送量度 — 依推播]** widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功發送的消息數。

* **[!UICONTROL 跳出數]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 開啟]**:傳送中開啟訊息的次數。

* **[!UICONTROL 動作]**:已傳送推播通知的動作總數，例如按鈕點擊或解除。

* **[!UICONTROL 參與]**:此推播通知的開啟次數和動作總數，亦即設定檔開啟了推播或按了按鈕。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。

此 **[!UICONTROL 發送統計資訊 — 失敗]** 介面工具集可讓您查看發生了多少錯誤和彈回。

此 **[!UICONTROL 依平台追蹤]**, **[!UICONTROL 依平台傳送]** 和 **[!UICONTROL 依平台劃分]** 圖表和表格會根據作業系統，詳細說明推播通知的成功。
+++

## SMS標籤 {#sms-live}

從您的行銷活動 **[!UICONTROL 即時報表]**, **[!UICONTROL 簡訊]** 索引標籤會詳細說明與促銷活動中傳送的SMS傳送相關的主要資訊。

![](assets/campaign_report_live_3.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS — 傳送統計資料]** 表格會詳細說明傳送的成功：

* **[!UICONTROL 已鎖定]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功發送的消息數。

* **[!UICONTROL 跳出數]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 按日期的SMS效能]** 介面工具集會透過圖表詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功發送的消息數。

* **[!UICONTROL 跳出數]**:傳送和自動回訪處理期間累積的錯誤總數。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 排除原因]**, **[!UICONTROL 跳出原因]** 和 **[!UICONTROL 錯誤原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的促銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報告](campaign-global-report.md)
