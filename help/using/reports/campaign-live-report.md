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
source-git-commit: 6bceccc561daac594f5c84d3d3250d887a349b7b
workflow-type: tm+mt
source-wordcount: '2063'
ht-degree: 3%

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

### 傳送 {#delivery-live}

此 **[!UICONTROL 行銷活動統計資料]** widget會詳細說明與行銷活動相關的主要資訊：

* **[!UICONTROL 輸入的設定檔]**：開始歷程的設定檔數。

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->

## 電子郵件索引標籤 {#email-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_sending_statistics"
>title="電子郵件 — 傳送統計資料"
>abstract="電子郵件 — 傳送統計資料圖表會摘要有關電子郵件的基本資料，例如過去24小時已鎖定或傳送。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_statistics"
>title="電子郵件 — 統計資料"
>abstract="「電子郵件 — 統計資料」表格提供過去24小時您電子郵件的設定檔活動資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_categories"
>title="電子郵件 — 退回類別"
>abstract="電子郵件 — 退回類別圖表和表格提供過去24小時內的暫時和永久錯誤資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_performance_bydate"
>title="電子郵件 — 依據日期的績效"
>abstract="電子郵件 — 依日期效能圖表顯示過去24小時已傳送電子郵件的全面資料，提供關鍵量度（例如傳送和跳出）的深入分析，允許電子郵件傳送流程的詳細分析。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_bounce_reasons"
>title="電子郵件 — 退回原因"
>abstract="「電子郵件 — 退信原因」圖表和表格包含與過去24小時內退信相關的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_error_reasons"
>title="電子郵件 — 錯誤原因"
>abstract="電子郵件 — 錯誤原因圖表和表格可讓您識別過去24小時內傳送程式期間發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_excluded_reasons"
>title="電子郵件 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除，以及在過去24小時內未收到訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_email_best_recipient"
>title="電子郵件 — 最佳收件者網域"
>abstract="電子郵件 — 最佳收件者網域圖表和表格提供收件者最常用來開啟電子郵件的網域詳細劃分，提供過去24小時內收件者行為的寶貴見解。"

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
>title="應用程式內績效"
>abstract="應用程式內績效KPI可針對訪客過去24小時內與應用程式內訊息的互動程度，提供重要的深入分析。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_interactions"
>title="依型別的互動"
>abstract="「依型別的互動」圖表和表格會追蹤過去24小時內的任何點按、解除或互動，以詳細說明使用者如何與您的應用程式內訊息互動。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_inapp_summary"
>title="應用程式內摘要"
>abstract="應用程式內摘要圖表會說明應用程式內曝光次數和互動在過去24小時內的進展情況。"

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
>title="推播通知 — 傳送績效"
>abstract="「推播通知傳送績效」圖表會摘要推播通知的相關基本資料，例如「錯誤」或過去24小時的已傳送訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_statistics"
>title="推播通知 — 統計資料"
>abstract="「推播統計資料」表格提供過去24小時內推播通知的收件者活動資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_sending_summary"
>title="推播通知 — 傳送摘要"
>abstract="「推播通知傳送摘要」圖表顯示過去24小時內已傳送推播通知的可用資料。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_excluded_reasons"
>title="推播通知 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除，以及在過去24小時內未收到訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_error_reasons"
>title="推播通知 — 錯誤原因"
>abstract="「錯誤原因」圖表和表格可讓您識別在傳送過程中最近24小時發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_push_breakdown_platform"
>title="推播通知 — 依據平台的劃分"
>abstract="「依平台劃分」圖表和表格會根據收件者的作業系統，提供過去24小時內推播通知成功的劃分。"

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

## 簡訊索引標籤 {#sms-live}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_statistics"
>title="簡訊 — 統計資料"
>abstract="SMS傳送統計資料表格會摘要有關SMS訊息的基本資料，例如過去24小時內的已鎖定目標或已傳送訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_performance"
>title="簡訊 — 依據日期的績效"
>abstract="依日期的SMS效能Widget透過圖形化呈現方式，提供過去24小時有關您訊息的重要資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_error_reasons"
>title="簡訊 — 錯誤原因"
>abstract="SMS — 錯誤原因圖表和表格可讓您識別在傳送過程中過去24小時內發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_excluded_reasons"
>title="簡訊 — 排除的原因"
>abstract="「排除的原因」圖表和表格說明導致使用者設定檔從目標對象中排除，以及在過去24小時內未收到訊息的各種因素。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_sms_bounces_reasons"
>title="簡訊 — 退回原因"
>abstract="「退信原因」圖表和表格包含與退信相關的過去24小時可用資料。"

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
>abstract="網站績效KPI提供關於訪客與過去24小時您網站體驗互動情況的完整資訊。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_summary"
>title="網頁摘要"
>abstract="「網站摘要」圖表會說明網站體驗從過去24小時的進展情況，包括曝光數、不重複曝光數和互動數。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_web_interactions"
>title="依元素的互動"
>abstract="「依元素的互動」表格提供關於訪客在過去24小時內與您的網頁上不同元素的互動的關鍵資訊。"

從您的行銷活動 **[!UICONTROL 即時報告]**，則 **[!UICONTROL Web]** 標籤會詳細說明與網頁相關的主要資訊。

+++進一步瞭解可用於網頁報表的不同量度和Widget。

此 **[!UICONTROL 網頁效能]** KPI會詳細說明與訪客對您網站體驗的參與度相關的主要資訊，例如：

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網站體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

此 **[!UICONTROL 網頁摘要]** 圖表顯示過去24小時您網站體驗的演變（曝光數、不重複曝光數和互動數）。

此 **[!UICONTROL 依元素的互動]** 此表格詳細說明與您的訪客與您網頁上各種元素的參與度相關的主要資訊。
+++

## 直接郵件索引標籤 {#direct-mail-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_sending_statistics"
>title="直接郵件 — 傳送統計資料"
>abstract="「直接郵件傳送統計資料」表格會摘要過去24小時有關直接郵件訊息的基本資料，例如「已鎖定目標」或「已傳遞」訊息。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_error_reasons"
>title="直接郵件 — 錯誤原因"
>abstract="「直接郵件 — 錯誤原因」圖表和表格可讓您識別過去24小時內發生的特定錯誤。"

>[!CONTEXTUALHELP]
>id="ajo_campaign_live_direct_excluded_reasons"
>title="直接郵件 — 排除的原因"
>abstract="「直接郵件排除的原因」圖表和表格說明了導致使用者設定檔從目標對象排除，以及在過去24小時內未收到訊息的各種因素。"

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
