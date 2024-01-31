---
solution: Journey Optimizer
product: journey optimizer
title: 頻道層級報表
description: 瞭解如何使用管道報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ead9359b-cdab-43ed-a469-d98b0ca19a17
source-git-commit: d26dbebaf36241d0e91c36c95f83ce6cf712ecee
workflow-type: tm+mt
source-wordcount: '3683'
ht-degree: 25%

---

# 頻道報告 {#channel-report}

>[!CONTEXTUALHELP]
>id="ajo_channel_level_report"
>title="管道層級報告"
>abstract="管道報告提供所有管道的流量和參與量度的全面概述。您的報告會分為不同的介面工具，詳述行銷活動和歷程的成功和錯誤。每個報告儀表板都可以透過調整大小或移除介面工具來修改。"

>[!IMPORTANT]
>
> 若要存取 **報告** 功能表，您必須擁有 **[!UICONTROL 檢視管道報表]** 許可權。 [了解更多](channel-report-gs.md#before-starting-manage-reports-prereq)

管道報表為使用者提供管道層級流量和參與量度的完整概觀。 這些量度會經過彙總，針對來自所選頻道的動作（橫跨各種促銷活動和歷程）呈現彙總值。

您可以導覽至「 」以存取管道報表。 **報表** 功能表中的 **歷程管理** 區段。 由於是完全可自訂的，您可以根據報表日期或動作來篩選資料。 [了解更多](channel-report-gs.md)

報表頁面會顯示以下索引標籤：

* [電子郵件](#email)
* [推播通知](#push)
* [簡訊](#sms)
* [應用程式內](#inapp)
* [Web](#web)
* [直接郵件](#direct-mail)

➡️ [在影片中探索此功能](#channel-report-video)

## 電子郵件 {#email}

在管道報表中，電子郵件功能表會詳細說明與行銷活動和歷程中傳送之電子郵件相關的主要資訊。 量度詳情如下。

### 電子郵件 - 傳送統計資料總計 {#email-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics"
>title="電子郵件 - 傳送統計資料總計"
>abstract="電子郵件 — 總傳送統計資料KPI會摘要有關您電子郵件的基本資料，例如「已鎖定目標」或「已傳送」訊息。"

![](assets/channel_email_total_sending.png)

此 **[!UICONTROL 電子郵件總傳送統計資料]** Widget提供您電子郵件績效的完整總覽，顯示摘要有關您電子郵件之基本資料的關鍵績效指標(KPI)。

+++ 進一步瞭解電子郵件傳送總計統計量度

* **[!UICONTROL 已鎖定目標]**：已處理的電子郵件總數。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的電子郵件百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 跳出率]**：與已傳送電子郵件相比跳出的電子郵件百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的電子郵件比較無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

+++

### 電子郵件 - 追蹤統計資料總計 {#email-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics"
>title="電子郵件 - 追蹤統計資料總計"
>abstract="電子郵件 - 追蹤統計資料總計 KPI 提供有關你的電子郵件的設定檔活動的資料。"

![](assets/channel_email_total_tracking.png)

此 **[!UICONTROL 電子郵件追蹤統計資料總計]** widget提供與您的電子郵件相連結的個人資料活動的詳細快照，提供參與和電子郵件有效性的基本深入分析。

+++ 進一步瞭解電子郵件追蹤統計資料總計

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 開啟率]**：與已傳遞電子郵件數量相比較的已開啟電子郵件總數。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

* **[!UICONTROL 點按率]**：與電子郵件互動的使用者百分比。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

* **[!UICONTROL 垃圾訊息申訴率]**：與已傳送電子郵件數量相較之下，宣告為垃圾郵件或垃圾郵件的郵件百分比。

* **[!UICONTROL 取消訂閱]**：對訂閱連結的點按次數。

* **[!UICONTROL 取消訂閱率]**：與已傳送電子郵件數目相比的取消訂閱百分比。

+++

### 電子郵件 - 時間區間內傳送統計資料 {#email-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_statistics_overtime"
>title="電子郵件 - 時間區間內傳送統計資料"
>abstract="「電子郵件 - 時間區間內傳送統計資料」圖表顯示有關已傳送的電子郵件的資料，依每小時、每天、每週或每月進行劃分。"

![](assets/channel_email_sending_statistics.png)

此 **[!UICONTROL 電子郵件 — 傳送一段時間內的統計資料]** 圖表提供動態表示，顯示電子郵件活動的分析。 此圖形表示提供已傳送電子郵件的完整劃分，可讓您以每小時、每日、每週或每月規模觀察趨勢和模式。

+++ 進一步瞭解電子郵件 — 傳送一段時間量度的統計資料

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 跳出數]**：與已傳送電子郵件總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

+++

### 電子郵件 - 時間區間內追蹤統計資料 {#email-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_tracking_statistics_overtime"
>title="電子郵件 - 時間區間內追蹤統計資料"
>abstract="「電子郵件 - 時間區間內追蹤統計資料」圖表提供有關你的電子郵件的設定檔活動相關資料，依每小時、每天、每週或每月進行劃分。"

![](assets/channel_email_tracking_overtime.png)

此 **[!UICONTROL 電子郵件 — 追蹤一段時間內的統計資料]** 圖表提供與您的電子郵件相關之設定檔活動的詳細概觀。 此圖形表示法以每小時、每日、每週或每月為基準劃分資料，提供收件者參與度如何隨著不同時間間隔演變的寶貴見解。

+++ 進一步瞭解電子郵件 — 追蹤一段時間量度的統計資料

* **[!UICONTROL 開啟次數]**：訊息開啟的次數。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

+++

### 電子郵件 — 退回類別和原因 {#bounce-categories}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_categories"
>title="退回類別"
>abstract="「退回」類別的圖表和表格提供有關暫時性和永久錯誤的資料。"

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons"
>title="退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

![](assets/channel_email_bounce_categories.png)

此 **[!UICONTROL 退信類別]** 和 **[!UICONTROL 退回原因]** Widget會封裝與退信相關的資料，提供各種類別的完整概觀，以及訊息退信背後的具體原因

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

+++ 進一步瞭解跳出類別量度

* **[!UICONTROL 硬退信]**：永久錯誤的總數，例如錯誤的電子郵件地址。 這包含明確指出地址無效的錯誤訊息，例如「未知使用者」。

* **[!UICONTROL 軟退信]**：暫時性錯誤的總數，例如完整的收件匣。

* **[!UICONTROL 已忽略]**：暫時性總數，例如「不在辦公室」或技術錯誤，例如，如果傳送者型別是郵遞員。

+++

### 錯誤原因 {#error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/channel_email_error.png)

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您精確指出傳送過程中發生的精確錯誤，協助您清楚瞭解遇到的任何問題。

### 排除原因 {#excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/channel_email_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖表和表格可全面檢視導致從目標對象中排除使用者設定檔，從而導致未收到訊息的不同因素。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 依網域劃分的已傳送和已送達郵件 {#sent-delivered-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_sending_delivered_domains"
>title="依網域劃分的已傳送和已送達郵件"
>abstract="「依網域劃分的已傳送和已送達郵件」圖表和表格呈現依網域層級劃分的每封傳送資料的重要電子郵件。"

![](assets/channel_email_sent_domains.png)

此  **[!UICONTROL 依網域傳送和傳遞]** 表格和圖表提供網域層級電子郵件傳送的詳細劃分，提供電子郵件效能的完整深入分析。

+++ 進一步瞭解依網域進行之傳送和傳遞的量度

* **[!UICONTROL 已傳送]**：電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的訊息數，與已傳送訊息總數相關。

+++

### 依網域劃分的退回情形與錯誤 {#bounces-errors-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounces_errors_domains"
>title="依網域劃分的退回情形與錯誤"
>abstract="「依網域劃分的退回情形與錯誤」圖表和表格呈現依網域層級劃分的傳送過程中發生的特定錯誤。"

![](assets/channel_email_bounces_domain.png)

此  **[!UICONTROL 依網域區分的退回和錯誤]** 圖表和表格提供傳送程式期間所遇到特定錯誤的網域層級劃分，針對所發生的問題提供詳細分析。

+++ 進一步瞭解依網域量度的跳出和錯誤

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

+++

### 依網域劃分的開啟和點選動作 {#open-clicks-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_open_clicks_domains"
>title="依網域劃分的開啟和點選動作"
>abstract="「依網域劃分的開啟和點選動作」圖表和表格呈現依網域層級劃分的訪客參與電子郵件互動的情形。"

![](assets/channel_email_open_domains.png)

此  **[!UICONTROL 依網域開啟和點按]** 圖形和表格會顯示訪客與電子郵件互動的網域層級劃分，提供不同網域與內容互動方式的寶貴深入分析。

+++ 進一步瞭解依網域量度的開啟和點按次數

* **[!UICONTROL 開啟次數]**：電子郵件開啟的次數。

* **[!UICONTROL 點按次數]**：內容在電子郵件中的點按次數。

+++

### 依網域劃分的退回原因 {#bounce-reasons-domains}

>[!CONTEXTUALHELP]
>id="ajo_channel_email_bounce_reasons_domains"
>title="依網域劃分的退回原因"
>abstract="「依網域劃分的退回原因」圖表和表格呈現依網域層級劃分的暫時性錯誤和永久錯誤的資料。"

![](assets/channel_email_bounce_domain.png)

此  **[!UICONTROL 依網域區分的退回原因]** 圖表和表格提供有關暫時和永久錯誤的網域層級資料劃分，提供退回訊息背後原因的詳細深入分析。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

## 推播通知 {#push}

在管道報表中， **推播通知** 功能表會詳細說明與您的行銷活動和歷程中傳送的推播通知相關的主要資訊。 量度詳情如下。

### 推播通知 - 傳送統計資料總計 {#push-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics"
>title="推播通知 - 傳送統計資料總計"
>abstract="推播通知 - 傳送統計資料總計 KPI 總結有關推播通知的基本資料，例如指定對象或已送達的郵件。"

![](assets/channel_push_total_sending.png)

此 **[!UICONTROL 推播通知 — 傳送統計資料總數]** KPI可當作完整摘要，封裝與推播通知相關的基本資料。 這些量度包含目標對象和實際傳送狀態的詳細深入分析，讓您更全面地瞭解推播通知的有效性和觸及範圍。

+++ 深入瞭解推播通知 — 傳送統計資料量度總計

* **[!UICONTROL 已鎖定目標]**：已處理的推播通知總數。

* **[!UICONTROL 已傳送]**：已傳送推播通知的總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的推播通知百分比。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 跳出率]**：與已傳送的推播通知相比退回的推播通知百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的推播通知相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：Adobe Journey Optimizer已排除的設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

+++

### 推播通知 - 追蹤統計資料總計 {#push-total-tracking}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics"
>title="推播通知 - 追蹤統計資料總計"
>abstract="「推播通知 - 追蹤統計資料總計」提供有關推播通知的設定檔活動的資料。"

此 **[!UICONTROL 推播通知 — 追蹤統計資料總數]** widget提供與您的推播通知相連結的個人資料活動的詳細快照，提供參與和推播通知有效性的基本深入分析。

+++ 進一步瞭解推播通知 — 追蹤統計量度總計

* **[!UICONTROL 開啟次數]**：推播通知開啟的次數。

* **[!UICONTROL 開啟率]**：已開啟推播通知的百分比。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

* **[!UICONTROL 動作率]**：已傳送推播通知的動作相對於已傳送推播通知的百分比。

+++

### 推播通知 - 時間區間內的傳送統計資料 {#push-sending-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_overtime"
>title="推播通知 - 時間區間內的傳送統計資料"
>abstract="「推播通知時間區間內傳送統計資料」圖表呈有關已傳送推播通知的資料，依每小時、每天、每週或每月劃分顯示。"

![](assets/channel_push_sending_statistics.png)

此 **[!UICONTROL 推播通知 — 傳送一段時間內的統計資料]** 圖表提供動態表示，顯示推播通知活動的分析。 此圖形表示提供已傳送推播通知的完整劃分，可讓您以每小時、每日、每週或每月規模觀察趨勢和模式。

+++ 深入瞭解推播通知 — 傳送一段時間量度的統計資料

* **[!UICONTROL 已傳送]**：已傳送推播通知的總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 跳出數]**：與已傳送訊息總數相關的累計錯誤數和自動傳回處理總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

+++

### 推播通知 - 時間區間內追蹤統計資料 {#push-tracking-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_overtime"
>title="推播通知 - 時間區間內追蹤統計資料"
>abstract="「推播通知 - 時間區間內追蹤統計資料」圖表提供有關你的推播通知的設定檔活動相關資料，依每小時、每天、每週或每月劃分顯示。"

此 **[!UICONTROL 推播通知 — 追蹤一段時間內的統計資料]** 圖表提供與推播通知相關的設定檔活動的詳細總覽。 此圖形表示法以每小時、每日、每週或每月為基準劃分資料，提供收件者參與度如何隨著不同時間間隔演變的寶貴見解。

+++ 進一步瞭解推播通知 — 追蹤一段時間量度的統計資料

* **[!UICONTROL 開啟次數]**：您的推播通知開啟次數。

* **[!UICONTROL 動作]**：推播通知已傳送的動作總數，例如按鈕點選或解除。

+++

### 推播通知 — 排除的原因 {#push-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/channel_push_excluded.png)

此 **[!UICONTROL 排除的原因]** 圖形和表格會顯示從目標設定檔中排除的使用者設定檔無法接收推播通知的不同原因。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 推播通知 — 錯誤原因 {#push-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/channel_push_error.png)

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您識別在傳送推播通知的過程中發生的特定錯誤，針對過程中遇到的任何問題提供詳細的深入分析。

### 推播通知 — 依據平台的追蹤 {#push-tracking-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_tracking_statistics_platform"
>title="依平台劃分的追蹤統計資料"
>abstract="「依平台劃分的追蹤統計資料」圖表和表格根據你的設定檔的作業系統提供推播通知的設定檔活動相關資料。"

此 **[!UICONTROL 推播通知 — 依據平台的追蹤]** 圖表和表格會根據您的設定檔作業系統，詳細列出推播通知的收件者活動。

### 推播通知 — 依據平台的傳送 {#push-sending-platform}

>[!CONTEXTUALHELP]
>id="ajo_channel_push_sending_statistics_platform"
>title="依平台劃分傳送統計資料"
>abstract="「依平台劃分的傳送統計資料」圖表和表格顯示有關已傳送推播通知的資料。"

![](assets/channel_push_sending_platform.png)

此 **[!UICONTROL 推播通知 — 依據平台的傳送]** 圖表和表格會提供全方位的劃分，詳述推送通知相對於設定檔作業系統的成功情形。 這項全面分析針對不同平台的推播通知有效性提供寶貴見解。

## 簡訊 {#sms}

從您的 **頻道** 報告，簡訊功能表會詳細說明與行銷活動和歷程中傳送之簡訊相關的主要資訊。 量度詳情如下。

### 簡訊 - 傳送統計資料總計 {#sms-sending-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics"
>title="簡訊 - 傳送統計資料總計"
>abstract="簡訊 - 傳送統計資料總計 KPI 總結有關簡訊的基本資料，例如指定對象或已送達的簡訊。"

![](assets/channel_sms_total_sending.png)

此 **[!UICONTROL 簡訊 — 傳送統計資料總數]** KPI可做為完整的摘要，封裝與簡訊相關的重要資料。 這些量度包含目標對象和實際傳送狀態的詳細深入分析，提供您SMS訊息成效和觸及範圍的完整檢視。

+++ 深入瞭解推播通知 — 傳送統計資料量度總計

* **[!UICONTROL 已鎖定目標]**：符合SMS頻道目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：已傳送的SMS訊息總數。

* **[!UICONTROL 已傳遞]**：成功傳送的SMS訊息數，與已傳送的SMS訊息總數相關。

* **[!UICONTROL 傳遞率]**：成功傳送的SMS訊息百分比。

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 跳出率]**：與已傳送的SMS訊息相比跳出的簡訊百分比。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的SMS訊息相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

+++

### 簡訊 - 追蹤統計資料總計 {#sms-tracking-statistics}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics"
>title="簡訊 - 追蹤統計資料總計"
>abstract="「SMS - 追蹤統計資料總計」提供有關你的簡訊的設定檔活動相關資料。"

![](assets/channel_sms_tracking.png)

此 **[!UICONTROL 簡訊 — 追蹤統計資料總數]** Widget提供與訪客與您URL互動相關之關鍵資訊的詳細概觀，提供您SMS訊息有效性的深入分析：

* **[!UICONTROL 點按次數]**：內容在SMS訊息中被點按的次數。

### 簡訊 - 時間區間內傳送統計資料 {#sms-sending-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_sending_statistics_overtime"
>title="簡訊 - 時間區間內傳送統計資料"
>abstract="「簡訊- 時間區間內傳送統計資料」圖表顯示有關已傳送簡訊的資料，依每小時、每天、每週或每月劃分顯示。"

![](assets/channel_sms_sending_overtime.png)

此 **[!UICONTROL 簡訊 — 傳送一段時間內的統計資料]** 圖表提供已傳送SMS訊息的完整檢視，提供每小時、每日、每週或每月劃分的資料。 此圖形表示法可讓您追蹤和分析簡訊活動在不同時間間隔內的趨勢。

+++ 進一步瞭解簡訊 — 傳送一段時間量度內的統計資料

* **[!UICONTROL 已傳送]**：已傳送的SMS訊息總數。

* **[!UICONTROL 跳出數]**：與已傳送SMS訊息總數相關的累積和自動傳回處理的錯誤總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

+++

### 簡訊 - 時間區間內追蹤統計資料 {#sms-tracking-statistics-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_tracking_statistics_overtime"
>title="簡訊 - 時間區間內追蹤統計資料"
>abstract="「簡訊 - 時間區間內追蹤統計資料」圖表提供有關你的簡訊的設定檔活動相關資料，依每小時、每天、每週或每月劃分顯示。"

![](assets/channel_sms_tracking_overtime.png)

此 **[!UICONTROL 簡訊 — 追蹤一段時間內的統計資料]** 圖表會提供與您的SMS訊息相關的設定檔活動的資料，提供每小時、每日、每週或每月的詳細劃分。 此圖形表示法可讓您分析和瞭解使用者在不同時間間隔內的參與模式。

* **[!UICONTROL 點按次數]**：內容在SMS訊息中被點按的次數。

### 排除原因 {#sms-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/channel_sms_excluded.png)

此 **[!UICONTROL 排除原因]** 圖表和表格會以視覺化方式呈現導致目標對象中排除使用者設定檔的各種因素，以防止他們接收您的SMS訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 退回原因 {#sms-bounce-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_bounce_reasons"
>title="退回原因"
>abstract="「退回原因」圖表和表格包含與退回郵件相關的可用資料。"

![](assets/channel_sms_bounce_reasons.png)

此 **[!UICONTROL 退回原因]** 圖表和表格提供與彈回SMS訊息相關的完整資料概觀，針對SMS訊息彈回例項背後的特定原因提供有價值的深入分析。

### 錯誤原因 {#sms-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_sms_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

此 **[!UICONTROL 錯誤原因]** 圖表和表格可讓您識別SMS訊息傳送過程中發生的特定錯誤，促進對所遇到的任何問題進行徹底分析。

## 直接郵件 {#direct-mail}

從您的 **頻道** 報表， **直接郵件** 功能表詳細說明與中傳送之直接郵件訊息相關的主要資訊 **行銷活動** 和 **歷程**. 量度詳情如下。

### 直接郵件 - 傳送統計資料總計 {#direct-mail-total-sending}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_sending_statistics"
>title="直接郵件 - 傳送統計資料總計"
>abstract="直接郵件 - 傳送統計資料總計 KPI 總結有關直接郵件的基本資料，例如指定對象或已送達的郵件。"

![](assets/channel_direct_sending.png)

此 **[!UICONTROL 直接郵件 — 總傳送統計資料]** widget提供您直接郵件訊息績效的完整總覽，顯示關鍵績效指標(KPI)，彙總您直接郵件訊息的基本資料。

+++ 深入瞭解直接郵件 — 傳送統計量度總計

* **[!UICONTROL 已鎖定目標]**：符合直接郵件訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已傳送]**：傳送總數。

* **[!UICONTROL 錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 錯誤率]**：與已傳送的推播通知相比，無法傳送的錯誤百分比。

* **[!UICONTROL 已排除]**：從目標設定檔中排除且未收到訊息的使用者設定檔數。

* **[!UICONTROL 排除率]**：Adobe Journey Optimizer已排除的設定檔百分比。

+++

### 排除原因 {#direct-mail-excluded-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_excluded_reasons"
>title="排除原因"
>abstract="「排除原因」圖表和表格說明導致使用者設定檔被排除在目標對象之外而未能收到訊息的各項因素。"

![](assets/channel_direct_excluded.png)

此 **[!UICONTROL 直接郵件 — 排除的原因]** 圖表和表格會以視覺化方式說明導致目標對象中排除使用者設定檔的各種因素，以防止他們接收您的直接郵件訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 錯誤原因 {#direct-mail-error-reasons}

>[!CONTEXTUALHELP]
>id="ajo_channel_direct_error_reasons"
>title="錯誤原因"
>abstract="「錯誤原因」圖表和表格讓你能夠確認傳送過程中發生的特定錯誤。"

![](assets/channel_direct_error.png)

此 **[!UICONTROL 直接郵件 — 錯誤原因]** 提供識別直接郵件訊息傳送過程中發生的特定錯誤的方法，以便詳細分析遇到的任何問題。

## 應用程式內 {#in-app}

在管道報表中，應用程式內功能表會詳細說明與促銷活動和歷程中傳送之應用程式內訊息有關的主要資訊。 量度詳情如下。

### 應用程式內參與總數 {#inapp-total-engagement}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement"
>title="應用程式內 - 參與度總計"
>abstract="應用程式內 - 參與度總計 KPI 提供有關訪客參與應用程式內訊息的互動的綜合資訊，包括曝光和互動次數等量度。"

![](assets/channel_inapp_engagement.png)

此 **[!UICONTROL 應用程式內參與總數]** KPI可提供訪客與應用程式內訊息互動情況的全方位分析，包含關鍵量度，例如 **曝光數** 和 **互動**.

+++ 進一步瞭解應用程式內參與總計量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

### 應用程式內參與加班 {#inapp-engagement-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_inapp_engagement_overtime"
>title="應用程式 - 時間區間內參與情形"
>abstract="「應用程式內 - 時間區間內參與度」圖表追蹤應用程式內曝光和互動次數，提供依每小時、每日、每周和每月劃分的資料。"

![](assets/channel_inapp_engagement_overtime.png)

此 **[!UICONTROL 應用程式內參與加班]** 圖表會透過追蹤任何曝光、關閉或互動，顯示您應用程式內曝光次數和互動在相關期間內的演變。

+++ 進一步瞭解應用程式內參與超時量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的應用程式內訊息總數。

* **[!UICONTROL 互動]**：應用程式內訊息的參與總數。 這包括使用者所執行的任何動作，例如點選、解僱或任何其他互動。

+++

## Web {#web}

從您的 **頻道** 報表，網頁功能表會詳細說明與包含在您的報表中的網頁相關的主要資訊。 **行銷活動** 和 **歷程**. 量度詳情如下。

### 網站 - 參與度總計 {#web-engagement-total}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement"
>title="網站 - 參與度總計"
>abstract="網頁 - 參與度總計 KPI 提供有關訪客參與網頁互動的綜合資訊，包括曝光和互動次數等量度。"

![](assets/channel_web_engagement.png)

此 **[!UICONTROL 網站參與總數]** KPI可提供訪客與網頁互動情況的全方位分析，包含曝光數和互動數等關鍵量度。

+++ 進一步瞭解網站總參與量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網頁體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

### 網頁 - 時間區間內參與度總計 {#web-engagement-total-overtime}

>[!CONTEXTUALHELP]
>id="ajo_channel_web_engagement_overtime"
>title="網頁 - 時間區間內參與度總計"
>abstract="「網頁 - 時間區間內參與度」圖表追蹤你的網頁曝光和互動次數，提供依每小時、每天、每周和每月劃分的資料。"

![](assets/channel_web_engagement_overtime.png)

此 **[!UICONTROL Web參與加班]** 圖表監視 **曝光數** 和 **互動** 的詳細劃分，提供每小時、每日、每週和每月的詳細劃分。

+++ 進一步瞭解Web參與超時量度

* **[!UICONTROL 曝光數]**：傳送給所有使用者的網頁體驗總數。

* **[!UICONTROL 互動]**：與您的網頁互動的總次數。 這包括使用者所執行的任何動作，例如點按或任何其他互動。

+++

## 管道報表（影片） {#channel-report-video}

透過此影片瞭解如何在頻道層級存取、導覽和匯出報告

>[!VIDEO](https://video.tv.adobe.com/v/3424537?quality=12)
