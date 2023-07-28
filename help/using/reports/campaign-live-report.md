---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動即時報告
description: 瞭解如何使用Campaign即時報告的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 96d90ff8c4ef29328810b3146d1e9a2aa3c25f2a
workflow-type: tm+mt
source-wordcount: '1342'
ht-degree: 6%

---

# 行銷活動即時報告 {#campaign-live-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_report"
>title="行銷活動即時報告"
>abstract="行銷活動即時報告可讓您僅在過去 24 小時內對行銷活動的影響和效能進行即時測量和視覺化。您的報表會分為不同的介面工具，詳述促銷活動的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

從「最近24小時」索引標籤存取的即時報告，會顯示過去24小時內發生的事件，從事件發生起的最短時間間隔為兩分鐘。 相較之下，全域報表著重於至少兩小時前發生的事件，並涵蓋選定時段內的事件。

行銷活動即時報告可直接從您的行銷活動存取，使用 **[!UICONTROL 即時檢視]** 按鈕。

行銷活動 **[!UICONTROL 即時報告]** 頁面會顯示以下索引標籤：

* [Campaign](#campaign-live)
* [電子郵件](#email-live)
* [應用程式內](#inapp-live)
* [推播](#push-live)
* [簡訊](#sms-live)
* [Web](#web-tab)
* [直接郵件](#direct-mail-tab)

行銷活動 **[!UICONTROL 即時報告]** 分成不同的Widget，詳細說明行銷活動的成功和錯誤。 如有需要，可以調整每個Widget的大小並將其刪除。 如需詳細資訊，請參閱此 [區段](../reports/live-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](live-report.md#list-of-components-live).

## 行銷活動標籤 {#campaign-global}

### 傳送 {#delivery-global}

此 **[!UICONTROL 行銷活動統計資料]** widget會詳細說明與行銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**：開始歷程的設定檔數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件索引標籤 {#email-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 電子郵件]** 索引標籤詳細說明與在您的行銷活動中傳送的電子郵件傳遞相關的主要資訊。

![](assets/campaign_report_live_1.png)

+++進一步瞭解可用於電子郵件報告的不同量度和Widget。

此 **[!UICONTROL 電子郵件傳送統計資料]** widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送期間和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 依電子郵件傳送量度]** 表格和 **[!UICONTROL 電子郵件摘要]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL 已傳送]**：傳遞的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送期間和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：在傳遞中開啟訊息的次數。

* **[!UICONTROL 點按次數]**：內容在傳遞中的點按次數。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 退回原因]**， **[!UICONTROL 退信類別]** 和 **[!UICONTROL 硬退信 — 透過電子郵件]** Widget包含與退信相關的可用資料，例如：

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖表和表格可讓您檢視傳送期間發生哪些錯誤和排除。

此 **[!UICONTROL 電子郵件 — 熱門收件者網域]** 圖表和表格詳細說明收件者最常用來開啟電子郵件的網域。
+++

## 應用程式內標籤 {#inapp-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤會詳細說明與行銷活動中傳送之應用程式內傳遞相關的主要資訊。

+++進一步瞭解應用程式內報表可用的不同量度和Widget。

此 **[!UICONTROL 應用程式內績效]** KPI會詳細說明與訪客與您應用程式內訊息的參與度相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：應用程式內訊息已傳送給的不重複使用者人數。

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

此 **[!UICONTROL 應用程式內摘要]** 圖表會顯示相關期間您應用程式內曝光次數的演變。

此 **[!UICONTROL 依據按鈕的點按]** 圖形和表格包含每個按鈕的收件者行為可用資料：

* **[!UICONTROL 點按次數]**：與應用程式內訊息所含按鈕互動的收件者總數。

+++

## 推播通知標籤 {#push-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 推播通知]** 索引標籤會詳細說明與行銷活動中傳送之推播傳遞相關的主要資訊。

![](assets/campaign_report_live_2.png)

+++進一步瞭解推送報表可用的不同量度和Widget。

**[!UICONTROL 推播通知傳送績效]**， **[!UICONTROL 推播通知摘要]** 和 **[!UICONTROL 傳送量度 — 透過推播]** Widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：傳遞的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送期間和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：在傳遞中開啟訊息的次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 參與]**：此推播通知的開啟和動作總數，也就是設定檔是否已開啟推播，或按鈕是否已點按。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖表和表格可讓您檢視傳送期間發生哪些錯誤和排除。

此 **[!UICONTROL 傳送統計資料 — 失敗]** widget可讓您檢視發生多少錯誤和退信。

此 **[!UICONTROL 依據平台的追蹤]**， **[!UICONTROL 由平台傳送]** 和 **[!UICONTROL 依平台劃分]** 圖表和表格會根據作業系統詳細描述推播通知的成功情況。
+++

## 簡訊索引標籤 {#sms-live}

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 簡訊]** 索引標籤會詳細說明與行銷活動中傳送之SMS傳遞相關的主要資訊。

![](assets/campaign_report_live_3.png)

+++進一步瞭解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL 簡訊 — 統計資料]** 表格詳細說明您的傳送是否成功：

* **[!UICONTROL 已鎖定目標]**：符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：傳遞的傳送總數。

* **[!UICONTROL 跳出數]**：傳送期間和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 點按次數]**：URL造訪總數。

此 **[!UICONTROL 依日期的SMS效能]** Widget會以圖表詳細列出與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：傳遞的傳送總數。

* **[!UICONTROL 跳出數]**：傳送期間和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視傳送期間發生哪些錯誤和排除。
+++

## 網頁標籤 {#web-tab}

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL Web]** 標籤會詳細說明與網頁相關的主要資訊。

+++進一步瞭解可用於網頁報表的不同量度和Widget。

此 **[!UICONTROL 網頁效能]** KPI會詳細說明與訪客對您網站體驗的參與度相關的主要資訊，例如：

* **[!UICONTROL 不重複曝光次數]**：提供網頁體驗的不重複使用者人數。

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 點按次數]**：URL造訪總數。

此 **[!UICONTROL 網頁摘要]** 圖表會顯示相關期間您網站體驗（曝光數、不重複曝光數和點按數）的演變。

此 **[!UICONTROL 依據元素的點按]** 此表格詳細說明與您的訪客與您網頁上各種元素的參與度相關的主要資訊。
+++

## 直接郵件索引標籤 {#direct-mail-tab}

從您的行銷活動 **[!UICONTROL 全域報告]**，則 **[!UICONTROL 直接郵件]** 索引標籤會詳細說明與直接郵件傳送相關的主要資訊。

![](assets/direct-mail-report_2.png)

+++進一步瞭解直接郵件報表可用的不同量度和Widget。

此 **[!UICONTROL 直接郵件 — 傳送統計資料]** 表格詳細說明您的傳送是否成功：

* **[!UICONTROL 已鎖定目標]**：符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：傳遞的傳送總數。

* **[!UICONTROL 錯誤]**：在傳送期間發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到傳送的使用者設定檔數。

此 **[!UICONTROL 直接郵件 — 排除的原因]** 和 **[!UICONTROL 直接郵件 — 錯誤原因]** 圖表和表格可讓您檢視傳送期間發生哪些錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報告](campaign-global-report.md)
