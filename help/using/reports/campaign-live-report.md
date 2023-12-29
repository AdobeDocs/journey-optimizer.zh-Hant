---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動即時報告
description: 瞭解如何使用Campaign即時報告的資料
feature: Reporting, Campaigns
topic: Content Management
role: User
level: Intermediate
exl-id: 925494b6-e08a-4bd3-8a2f-96a5d9cbc387
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '2095'
ht-degree: 40%

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

## 行銷活動標籤 {#campaign-live}

### 傳遞 {#delivery-live}

此 **[!UICONTROL 行銷活動統計資料]** widget會詳細說明與行銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**：開始歷程的設定檔數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件標籤 {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="電子郵件 - 傳送統計資料"
>abstract="「電子郵件 - 傳送統計資料」圖表總結有關你的電子郵件的基本資料，例如過去 24 小時內的指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="電子郵件 - 統計資料"
>abstract="「電子郵件 - 統計資料」表格提供過去 24 小時內你的電子郵件的設定檔活動資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="電子郵件 - 退回類別"
>abstract="「電子郵件 - 退回類別」圖表和表格提供有關過去 24 小時內暫時性和永久錯誤的資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="電子郵件 - 依日期劃分的效能"
>abstract="「電子郵件 - 依日期劃分的效能」圖表顯示過去 24 小時內有關已傳送電子郵件的綜合資料，提供關鍵量度例如送達和退回郵件的深入分析，從而對電子郵件傳送過程進行詳細分析。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="電子郵件 - 退回原因"
>abstract="「電子郵件 - 退回原因」圖表和表格包含與過去 24 小時內退回郵件相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="電子郵件 - 錯誤原因"
>abstract="「電子郵件 - 錯誤原因」圖表和表格讓你能夠確認過去 24 小時內發送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="電子郵件 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="電子郵件 - 最佳收件者網域"
>abstract="「電子郵件 - 最佳收件者」網域圖表和表格提供收件者開啟電子郵件時最常使用網域的詳細劃分，針對過去 24 小時內的收件者行為提供重要的深入分析。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 電子郵件]** 索引標籤會詳細說明與行銷活動中傳送之電子郵件相關的主要資訊。

![](assets/campaign_report_live_1.png)

+++進一步瞭解可用於電子郵件報告的不同量度和Widget。

此 **[!UICONTROL 電子郵件傳送統計資料]** widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 依電子郵件傳送量度]** 表格和 **[!UICONTROL 電子郵件摘要]** 圖表會詳細說明您的電子郵件是否成功：

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容被點按的次數。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 退回原因]** 和 **[!UICONTROL 退信類別]** Widget包含與退信相關的可用資料，例如：

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。

此 **[!UICONTROL 電子郵件 — 最佳收件者網域]** 圖表和表格詳細說明收件者最常用來開啟電子郵件的網域。
+++

## 應用程式內標籤 {#inapp-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_performance"
>title="應用程式內效能"
>abstract="應用程式內效能 KPI 提供有關訪客在過去 24 小時內參與應用程式內訊息的互動情況的重要分析。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="依類型劃分的互動"
>abstract="「依類型劃分的互動」圖表和表格透過追蹤過去 24 小時內的任何點選、關閉或互動，詳細說明使用者如何與應用程式內訊息進行互動。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表顯示過去 24 小時內應用程式內曝光與互動的進展。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 應用程式內]** 索引標籤詳細說明與在您的行銷活動中傳送的應用程式內訊息相關的主要資訊。

+++進一步瞭解應用程式內報表可用的不同量度和Widget。

此 **[!UICONTROL 應用程式內績效]** KPI會詳細說明與訪客與您應用程式內訊息的參與度相關的主要資訊，例如：

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

此 **[!UICONTROL 應用程式內摘要]** 圖表會顯示相關期間應用程式內曝光次數和互動的演變。

此 **[!UICONTROL 依型別的互動]** 圖表和表格會詳細說明使用者如何透過追蹤任何點選、解除或互動來與您的應用程式內訊息互動。

+++

## 推播通知標籤 {#push-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_performance"
>title="推播通知 - 傳送效能"
>abstract="「推播通知傳送效能」圖表總結有關推播通知的基本資料，例如過去 24 小時內的錯誤或已送達的訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="推播通知 - 統計資料"
>abstract="「推播統計資料」表格提供過去 24 小時內推播通知的收件者活動相關資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="推播通知 - 傳送摘要"
>abstract="「推播通知發送摘要」圖表顯示過去 24 小時內已發送的推播通知的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="推播通知 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="推播通知 - 錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認過去 24 小時內傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="推播通知 - 依平台劃分"
>abstract="「依平台劃分」圖表和表格根據收件人的作業系統提供過去 24 小時內成功傳送的推播通知的劃分資料。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 推播通知]** 索引標籤會詳細說明與行銷活動中傳送之推播通知相關的主要資訊。

![](assets/campaign_report_live_2.png)

+++進一步瞭解推送報表可用的不同量度和Widget。

**[!UICONTROL 推播通知傳送績效]**， **[!UICONTROL 推播通知摘要]** 和 **[!UICONTROL 推播通知 — 統計資料]** Widget會詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 參與]**：此推播通知的開啟和動作總數，也就是設定檔是否已開啟推播，或按鈕是否已點按。

此 **[!UICONTROL 錯誤原因]** 和 **[!UICONTROL 排除原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。

此 **[!UICONTROL 傳送統計資料 — 失敗]** widget可讓您檢視發生多少錯誤和退信。

此 **[!UICONTROL 依據平台的追蹤]**， **[!UICONTROL 由平台傳送]** 和 **[!UICONTROL 依平台劃分]** 圖表和表格會根據作業系統詳細描述推播通知的成功情況。
+++

## 簡訊標籤 {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="簡訊 - 統計資料"
>abstract="「簡訊傳送統計資料」表格總結有關簡訊的基本資料，例如過去 24 小時內指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="簡訊 - 依日期劃分的效能"
>abstract="「依日期劃分的簡訊效能」介面工具透過圖形呈現方式提供過去 24 小時內有關你的簡訊的重要資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="簡訊 - 錯誤原因"
>abstract="「簡訊 - 錯誤原因」圖表和表格讓你能夠確認過去 24 小時內傳送過程中發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="簡訊 - 排除原因"
>abstract="「排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="簡訊 - 退回原因"
>abstract="「退回原因」圖表和表格包含過去 24 小時內與退回郵件相關的可用資料。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 簡訊]** 索引標籤會詳細說明與行銷活動中傳送之SMS訊息相關的主要資訊。

![](assets/campaign_report_live_3.png)

+++進一步瞭解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL 簡訊 — 統計資料]** 表格詳細說明您的SMS訊息是否成功：

* **[!UICONTROL 已鎖定目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 點按次數]**：URL造訪總數。

此 **[!UICONTROL 依日期的SMS效能]** Widget會以圖表詳細列出與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 跳出數]**：傳送流程和自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

此 **[!UICONTROL 排除原因]**， **[!UICONTROL 退回原因]** 和 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。
+++

## 網頁標籤 {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_performance"
>title="網頁效能"
>abstract="Web 效能 KPI 提供有關過去 24 小時內訪客參與 Web 體驗相關情形的綜合資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="網頁摘要"
>abstract="「網頁摘要」圖表說明過去 24 小時內你的 Web 體驗的進展情況，包括曝光、唯一曝光和互動次數。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="依元素劃分的互動"
>abstract="「依元素劃分的互動」表格提供過去 24 小時內訪客參與網頁上不同元素之互動的重要資訊。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL Web]** 標籤會詳細說明與網頁相關的主要資訊。

+++進一步瞭解可用於網頁報表的不同量度和Widget。

此 **[!UICONTROL 網頁效能]** KPI會詳細說明與訪客對您網站體驗的參與度相關的主要資訊，例如：

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

此 **[!UICONTROL 網頁摘要]** 圖表顯示過去24小時您網站體驗的演變（曝光數、不重複曝光數和互動數）。

此 **[!UICONTROL 依元素的互動]** 此表格詳細說明與您的訪客與您網頁上各種元素的參與度相關的主要資訊。
+++

## 直接郵件標籤 {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="直接郵件 - 傳送統計資料"
>abstract="「直接郵件傳送統計資料」表格總結過去 24 小時內有關直接郵件的基本資料，例如指定對象或已送達的郵件。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="直接郵件 - 錯誤原因"
>abstract="「直接郵件 - 錯誤原因」圖表和表格讓你確認過去 24 小時內發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="直接郵件 - 排除原因"
>abstract="「直接郵件排除原因」圖表和表格說明在過去 24 小時內導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL 直接郵件]** 標籤詳細說明與直接郵件相關的主要資訊。

![](assets/direct-mail-report_2.png)

+++進一步瞭解直接郵件報表可用的不同量度和Widget。

此 **[!UICONTROL 直接郵件 — 傳送統計資料]** 表格詳細說明直接郵件成功與否：

* **[!UICONTROL 已鎖定目標]**：符合目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到直接郵件的使用者設定檔數。

此 **[!UICONTROL 直接郵件 — 排除的原因]** 和 **[!UICONTROL 直接郵件 — 錯誤原因]** 圖表和表格可讓您檢視傳送程式期間發生哪些錯誤和排除。
+++

## 其他資源

* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md)
* [建立行銷活動](../campaigns/create-campaign.md)
* [建立API觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [修改或停止行銷活動](../campaigns/modify-stop-campaign.md)
* [行銷活動全域報告](campaign-global-report.md)
