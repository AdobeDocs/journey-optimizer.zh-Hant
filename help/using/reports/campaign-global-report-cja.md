---
solution: Journey Optimizer
product: journey optimizer
title: 行銷活動全域報告
description: 瞭解如何使用Campaign全域報告的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 51cbe27f-3f3f-471e-a5d9-e3a88fcfdd68
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '4251'
ht-degree: 2%

---

# 行銷活動報告 {#campaign-global-report-cja}

此 **行銷活動報告** 作為完整儀表板，提供與行銷活動相關之關鍵量度的詳細分析。 其中包含點按計數、傳送的訊息、設定檔編號和所採取的動作等資料。 透過提供行銷活動成效和參與等級的完整概觀，報告可確保全面瞭解行銷活動的整體成效。

行銷活動報表可以直接從您的行銷活動存取，使用 **[!UICONTROL 報表]** 按鈕。

![](assets/gs-cja-report-2.png)

此 **行銷活動報告** 根據所選的頻道，頁面將顯示以下索引標籤：

* [Campaign](#campaign-global)
* [實驗](#experimentation)
* [電子郵件](#email-global)
* [簡訊](#sms)
* [推播通知](#push-notification)
* [直接郵件](#direct-mail)
* [Web](#web)

若要瞭解有關Customer Journey Analytics工作區以及如何篩選和分析資料的詳細資訊，請參閱 [此頁面](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

## Campaign {#campaign-global}

### 行銷活動KPI {#campaign-kpis}

![](assets/cja-email-kpis.png)

此 **[!UICONTROL Campaign]** 關鍵績效指標(KPI)可做為全方位的控制面板，提供與行銷活動相關之基本量度的分析。 其中包含點按次數和已傳送訊息數量等詳細資訊，可全面分析您的行銷活動的成效和參與程度。

KPI會因行銷活動中使用的管道而有所不同。

+++ 進一步瞭解行銷活動KPI量度

* **[!UICONTROL 點進率]**：與訊息互動的使用者百分比。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

+++

### Campaign 概觀 {#delivery-global}

![](assets/cja-campaign-overview.png)

此 **[!UICONTROL Campaign概覽]** 此表格可做為完整的儀表板，提供與您的行銷活動相關之關鍵量度的詳細劃分。 這包括基本資訊，例如已傳送的設定檔數和動作，讓您透徹瞭解行銷活動的績效和參與。

請注意，量度會因行銷活動中使用的管道而有所不同。

+++ 進一步瞭解Campaign概觀量度

* **[!UICONTROL 人員]**：符合訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 點進率]**：與訊息互動的使用者百分比。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

* **[!UICONTROL 不重複點按]**：點按訊息中內容的設定檔數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 傳出頻道的跳出數]**：在傳送過程中累積的錯誤總數以及自動傳回處理與已傳送訊息總數相關的數量。

* **[!UICONTROL 傳出錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++

### Campaign 漏斗結果 {#campaign-funnel}

![](assets/cja-campaign-funnel.png)

此 **[!UICONTROL 行銷活動漏斗結果]** 圖表提供設定檔與訊息互動的詳細分析，提供各種設定檔與內容互動方式的寶貴見解。

+++ 深入瞭解Campaign漏斗結果量度

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。
+++

### 追蹤的連結標籤 {#campaign-track}

![](assets/cja-campaign-tracked-link.png)

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供訪客與訊息中所包含URL互動的基本深入分析，提供關於哪些連結吸引最多互動的寶貴資訊。

+++ 深入瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：點按訊息中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在訊息中被點按的次數。

+++

## 實驗 {#experimentation}

此 **[!UICONTROL 實驗]** Tab提供每個變體績效的關鍵分析，並識別最成功的變體。

請注意，定義績效最佳者可能需要一些時間。 如果您的實驗不成功，則會將其設為 **尚無結果**.

![](assets/cja-experimentation-1.png)

### 實驗KPI {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

此 **[!UICONTROL 實驗]** 關鍵績效指標(KPI)可作為全方位的控制面板，提供與您的實驗相關之基本量度的分析。

+++ 進一步瞭解實驗KPI量度

* **[!UICONTROL 提升度]**：測量指定處理的轉換率相對於基線的增進百分比。

* **[!UICONTROL 信賴度]**：指定處理與基線處理相同的證據。 [了解更多](../content-management/experiment-calculations.md#understand-confidence)

+++

### 依傳入點按次數區分的變體 {#variant-inbound}

![](assets/cja-experimentation-variants.png)

此 **[!UICONTROL 依傳入點按次數區分的變體]** widget詳細說明每個變體的效能。
如需這些結果的深入瞭解以及如何解讀，請參閱 [此頁面](../content-management/get-started-experiment.md#interpret-results).

+++ 進一步瞭解依據傳入點按量度的變體

* **[!UICONTROL 人員]**：符合訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 傳入點按次數]**：跨傳出頻道的點按總數。

* **[!UICONTROL 轉換率]**：建立實驗時先前選取的成功量度總值除以設定檔數量。

* **[!UICONTROL 提升度]**：測量指定處理的轉換率相對於基線的增進百分比。

* **[!UICONTROL 信賴度]**：指定處理與基線處理相同的證據。 [了解更多](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:
* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### 傳入點按的轉換率 {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

此 **[!UICONTROL 信賴區間]** 圖表會測量改善的不確定性。 它詳細說明基準線和最佳執行處理之間的效能百分比差異。 [了解更多](../content-management/experiment-calculations.md#confidence-intervals)。

## 電子郵件 {#email-global}

### 已傳遞vs點選趨勢 {#delivered-click}

![](assets/cja-email-delivered-click.png)

此 **[!UICONTROL 已傳遞vs點選趨勢]** 圖表提供設定檔與電子郵件互動的詳細分析，提供設定檔與內容互動方式的寶貴見解。

+++ 深入瞭解傳遞與點選趨勢量度

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

+++


### 傳遞狀態 {#delivery-status}

![](assets/cja-email-delivery-status.png)

此 **[!UICONTROL 傳遞狀態]** graph提供促銷活動中已傳送電子郵件相關資料的完整檢視，深入分析關鍵量度，例如傳送和跳出。 這可啟用電子郵件傳送流程的詳細分析，提供關於行銷活動效率和績效的寶貴資訊。

+++ 進一步瞭解傳遞狀態量度

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 傳出頻道的跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 傳出錯誤]**：傳送程式期間發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 正在傳送統計數據 {#sending-statistics-email}

![](assets/cja-email-sending-stat.png)

此 **[!UICONTROL 傳送統計資料]** 表格提供有關行銷活動中電子郵件之基本資料的完整摘要。 它詳細說明關鍵量度，例如與您的電子郵件的互動和成功傳送的電子郵件數量，提供對您的電子郵件和行銷活動的成效和觸及範圍的寶貴見解。

+++ 進一步瞭解如何傳送統計資料

* **[!UICONTROL 人員]**：符合訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已鎖定目標]**：傳送過程中處理的電子郵件總數。

* **[!UICONTROL 傳送]**：電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數量，與已傳送訊息總數相關。

* **[!UICONTROL 傳出頻道的跳出數]**：與已傳送訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 傳出錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 追蹤統計資料 {#tracking-statistics-email}

![](assets/cja-email-track-stat.png)

此 **[!UICONTROL 電子郵件 — 追蹤統計資料]** 表格提供與行銷活動中所包含電子郵件相關的設定檔活動的詳細帳戶。 其中包括開啟次數、點按次數和其他相關的參與指標，以提供設定檔與電子郵件內容互動方式的完整檢視。

+++ 進一步瞭解追蹤統計量度

* **[!UICONTROL 點進率(CTR)]**：與電子郵件互動的使用者百分比。

* **[!UICONTROL 點進開啟率(CTOR)]**：電子郵件開啟的次數。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

* **[!UICONTROL 不重複點按]**：點按電子郵件中內容的設定檔數。

* **[!UICONTROL 電子郵件開啟次數]**：您的電子郵件在行銷活動中開啟的次數。

* **[!UICONTROL 不重複電子郵件開啟次數]**：已開啟電子郵件的百分比。

* **[!UICONTROL 垃圾郵件投訴數]**：訊息被宣告為垃圾郵件或垃圾郵件的次數。

* **[!UICONTROL 取消訂閱]**：對取消訂閱連結的點按次數。

+++


### 電子郵件網域 {#email-domains}

![](assets/cja-email-email-domains.png)

此 **[!UICONTROL 電子郵件網域]** 表格提供依網域分類的電子郵件深入劃分，讓您深入瞭解電子郵件行銷活動的效能量度。 這項全方位的分析可讓您瞭解不同網域在回應電子郵件內容時的行為。

+++ 進一步瞭解電子郵件網域量度

* **[!UICONTROL 傳送]**：電子郵件的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的電子郵件數，與已傳送電子郵件總數相關。

* **[!UICONTROL 電子郵件開啟次數]**：您的電子郵件在行銷活動中開啟的次數。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

* **[!UICONTROL 傳出頻道的跳出數]**：與已傳送電子郵件總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 傳出錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。
+++

### 追蹤的連結標籤 {#track-link-label}

![](assets/cja-email-tracked-link.png)

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供電子郵件中連結標籤的完整總覽，重點說明產生最高訪客流量的連結。 此功能可讓您識別最熱門的連結並加以優先處理。

+++ 進一步瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：點按電子郵件中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

+++

### 追蹤的連結 URL {#track-link-url}

![](assets/cja-journey-tracked-link-urls.png)

此 **[!UICONTROL 追蹤的連結URL]** 表格提供電子郵件中吸引最高訪客流量之URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解電子郵件中特定內容的設定檔參與情形。

+++ 深入瞭解追蹤的連結URL量度

* **[!UICONTROL 不重複點按]**：點按電子郵件中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在您的電子郵件中被點按的次數。

* **[!UICONTROL 顯示區]**：電子郵件開啟的次數。

* **[!UICONTROL 不重複顯示]**：電子郵件的開啟次數，不會將一個設定檔的多個互動計算在內。

+++

### 電子郵件主旨 {#email-subjects}

![](assets/cja-email-subject.png)

此 **[!UICONTROL 電子郵件主題]** 此表格提供吸引最多訪客流量的電子郵件主題的完整概觀。 此資源提供受眾參與動態的寶貴見解。

+++ 進一步瞭解電子郵件主題量度

* **[!UICONTROL 人員]**：符合電子郵件目標設定檔資格的使用者設定檔數目。

+++

### 排除原因 {#excluded-reasons}

此 **[!UICONTROL 排除的原因]** 此表格提供導致從目標對象中排除使用者設定檔，導致未收到訊息之不同因素的完整檢視。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

### 退回原因 {#bounce-reasons-email}

此 **[!UICONTROL 退回原因]** 表格會編譯與退回訊息相關的可用資料，提供電子郵件退回背後特定原因的詳細深入分析。

有關退信的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 頁面。

### 錯誤原因 {#error-reasons-email}

此 **[!UICONTROL 錯誤原因]** 表格可讓您檢視傳送程式期間發生的特定錯誤，並提供有關錯誤性質和發生次數的寶貴資訊。

## 簡訊 {#sms}

### 已傳遞vs點選趨勢 {#delivered-click-sms}

此 **[!UICONTROL 已傳遞vs點選趨勢]** 圖表提供設定檔與電子郵件互動的詳細分析，提供設定檔與內容互動方式的寶貴見解。

+++ 深入瞭解傳遞與點選趨勢量度

* **[!UICONTROL 已傳遞]**：成功傳送的SMS訊息數，與SMS訊息總數相關。

* **[!UICONTROL 點按次數]**：內容在您的SMS訊息中被點按的次數。

+++

### 傳遞狀態 {#delivery-status-sms}

此 **[!UICONTROL 傳遞狀態]** 表格提供與您的SMS行銷活動相關的設定檔活動的詳細帳戶。 這包括已傳送的量度、點按次數和其他相關的參與指標，以提供設定檔與簡訊內容互動方式的完整檢視。

+++ 進一步瞭解傳遞狀態量度

* **[!UICONTROL 已傳遞]**：成功傳送的SMS訊息數，與SMS訊息總數相關。

* **[!UICONTROL 傳出頻道的跳出數]**：與已傳送SMS訊息總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 傳出錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 追蹤的連結標籤 {#track-link-label-sms}

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供SMS訊息中連結標籤的完整概觀，醒目顯示產生最高訪客流量的連結。 此功能可讓您識別最熱門的連結並加以優先處理。

+++ 進一步瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：點選SMS訊息中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在您的SMS訊息中被點按的次數。

+++

### 追蹤的連結 URL {#track-link-url-sms}

此 **[!UICONTROL 追蹤的連結URL]** 表格提供您的SMS訊息中吸引最高訪客流量的URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，讓您更瞭解簡訊訊息中特定內容的設定檔參與情形。

+++ 深入瞭解追蹤的連結URL量度

* **[!UICONTROL 不重複點按]**：點選SMS訊息中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在您的SMS訊息中被點按的次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++

### 簡訊傳入訊息 {#sms-inbound}

此 **[!UICONTROL SMS傳入訊息]** 表格提供哪些SMS訊息吸引最多訪客流量的完整概觀。 此資源提供受眾參與動態的寶貴見解。

+++ 進一步瞭解簡訊傳入訊息量度

* **[!UICONTROL 人員]**：符合簡訊訊息目標設定檔資格的使用者設定檔數目。

+++

### 簡訊型別 {#sms-message-type}

此 **[!UICONTROL 簡訊型別]** 表格提供哪種SMS訊息型別吸引最多訪客流量的完整概觀。 此資源提供受眾參與動態的寶貴見解。

+++ 進一步瞭解簡訊型別量度

* **[!UICONTROL 人員]**：符合簡訊訊息目標設定檔資格的使用者設定檔數目。

+++

### 簡訊提供者 {#sms-providers}

此 **[!UICONTROL 簡訊提供者]** 此表格提供哪些SMS提供者吸引最多訪客流量的完整概觀。 此資源提供受眾參與動態的寶貴見解。

+++ 進一步瞭解簡訊提供者量度

* **[!UICONTROL 人員]**：符合簡訊訊息目標設定檔資格的使用者設定檔數目。

+++

### 退回原因 {#bounce-reasons-sms}

此 **[!UICONTROL 退回原因]** 表格提供與彈回SMS訊息相關的完整資料概觀，針對SMS訊息彈回例項背後的特定原因提供寶貴的見解。

### 錯誤原因 {#error-reasons-sms}

此 **[!UICONTROL 錯誤原因]** 表格可讓您識別SMS訊息傳送過程中發生的特定錯誤，協助徹底分析遇到的任何問題。

### 排除原因 {#excluded-reasons-sms}

此 **[!UICONTROL 排除原因]** 該表格會以視覺化方式呈現導致目標對象中排除使用者設定檔，進而阻止他們接收您SMS訊息的各種因素。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

## 推播通知 {#push-notification}

### 正在傳送統計數據 {#sending-statistics-push}

![](assets/cja-campaign-push-sending-stat.png)

此 **[!UICONTROL 傳送統計資料]** 表格提供有關推播通知行銷活動的完整基本資料摘要。 它會詳細說明關鍵量度，例如目標對象的大小和成功傳送的推播通知的數量，為您的推播通知提供有效性和觸及範圍的寶貴見解。

+++ 進一步瞭解如何傳送統計資料

* **[!UICONTROL 人員]**：符合推播通知目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已鎖定目標]**：分析期間處理的推播通知總數。

* **[!UICONTROL 傳送]**：推播通知的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的推播通知數，與已傳送推播通知總數相關。

* **[!UICONTROL 傳出頻道的跳出數]**：與推播通知總數相關的傳送程式與自動傳回處理期間累計的錯誤總數。

* **[!UICONTROL 傳出錯誤]**：發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 追蹤統計資料 {#tracking-statistics-push}

![](assets/cja-campaign-push-track-stat.png)

此 **[!UICONTROL 追蹤統計資料]** 表格提供與您的推播通知相連結的個人資料活動的詳細快照，提供參與和推播通知有效性的基本深入分析。

+++ 進一步瞭解追蹤統計量度

* **[!UICONTROL 點進率(CTR)]**：與推播通知互動的使用者百分比。

* **[!UICONTROL 點進開啟率(CTOR)]**：推播通知開啟的次數。

* **[!UICONTROL 點按次數]**：在推播通知中點按內容的次數。

* **[!UICONTROL 不重複點按]**：點按推播通知中內容的設定檔數。

<!--
* **[!UICONTROL Push custom actions]**: 
-->
+++

### 追蹤的連結標籤 {#track-link-label-push}

![](assets/cja-campaign-push-link-labels.png)

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供推播通知中連結標籤的完整總覽，重點顯示產生最高訪客流量的連結。 此功能可讓您識別最熱門的連結並加以優先處理。

+++ 進一步瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：點按推播通知中內容的設定檔數。

* **[!UICONTROL 點按次數]**：在推播通知中點按內容的次數。

+++

### 追蹤的連結 URL {#track-link-url-push}

![](assets/cja-campaign-push-link-urls.png)

此 **[!UICONTROL 追蹤的連結URL]** 表格提供推播通知中吸引最高訪客流量的URL完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解推播通知中特定內容的設定檔參與情形。

+++ 深入瞭解追蹤的連結URL量度

* **[!UICONTROL 不重複點按]**：點按推播通知中內容的設定檔數。

* **[!UICONTROL 點按次數]**：在推播通知中點按內容的次數。

+++

### 退回原因 {#bounce-reasons-push}

此 **[!UICONTROL 退回原因]** 表格提供與推播通知跳出的相關資料的完整總覽，針對推播通知跳出的例項背後的特定原因提供寶貴的見解。

### 錯誤原因 {#error-reasons-push}

此 **[!UICONTROL 錯誤原因]** 表格可讓您識別在傳送推播通知的過程中發生的特定錯誤，協助徹底分析遇到的任何問題。

### 排除原因 {#exclude-reasons-push}

![](assets/cja-campaign-push-excluded.png)

此 **[!UICONTROL 排除原因]** 表格會以視覺化方式呈現導致目標對象中排除使用者設定檔的各種因素，以防止他們收到您的推播通知。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

## 應用程式內 {#in-app}

### 曝光與點按趨勢 {#impression-click-trend}

![](assets/cja-inapp-impressions-click.png)

此 **[!UICONTROL 曝光與點選趨勢]** 圖表提供設定檔與應用程式內訊息互動的詳細分析，提供設定檔與內容互動方式的寶貴見解。

+++ 進一步瞭解「曝光與點選」趨勢量度

* **[!UICONTROL 點按次數]**：在您的應用程式內訊息中點按內容的次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

+++

### 點按次數 {#clicks-inapp}

此 **[!UICONTROL 點按次數]** 圖形會顯示應用程式內的點選量度，說明內容點選總數以及點選內容的不重複設定檔數量。

+++ 進一步瞭解點按量度

* **[!UICONTROL 不重複點按]**：在您的應用程式內訊息中點按內容的設定檔數

* **[!UICONTROL 點按次數]**：在您的應用程式內訊息中點按內容的次數。

+++

### 顯示 {#display-inapp}

此 **[!UICONTROL 顯示區]** 圖表可協助您瞭解訊息的整體觸及範圍和與其互動的不重複設定檔數量。

+++ 深入瞭解顯示量度

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++

### 追蹤資料 {#tracking-data-inapp}

此 **[!UICONTROL 追蹤資料]** 表格提供與應用程式內訊息繫結的設定檔活動詳細快照，提供參與和應用程式內訊息有效性方面的基本深入分析。

+++ 進一步瞭解追蹤資料量度

* **[!UICONTROL 人員]**：符合應用程式內訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 點進率(CTR)]**：與應用程式內訊息互動的使用者百分比。

* **[!UICONTROL 點進開啟率(CTOR)]**：應用程式內訊息的開啟次數。

* **[!UICONTROL 點按次數]**：在您的應用程式內訊息中點按內容的次數。

* **[!UICONTROL 不重複點按]**：在您的應用程式內訊息中按一下內容的設定檔數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

* **[!UICONTROL 傳送]**：應用程式內訊息的傳送總數。

<!--
* **[!UICONTROL Inbound triggered]**: 

* **[!UICONTROL Inbound dismisses]**: 
-->
+++

### 追蹤的連結標籤 {#track-link-label-inapp}

![](assets/cja-inapp-tracked-link-labels.png)

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供應用程式內訊息中連結標籤的完整概述，重點說明產生最高訪客流量的連結。 此功能可讓您識別最熱門的連結並加以優先處理。

+++ 進一步瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：在您的應用程式內訊息中按一下內容的設定檔數。

* **[!UICONTROL 點按次數]**：在您的應用程式內訊息中點按內容的次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++

### 追蹤的連結 URL {#track-link-url-inapp}

![](assets/cja-inapp-tracked-link-urls.png)

此 **[!UICONTROL 追蹤的連結URL]** 表格提供應用程式內訊息中，吸引最高訪客流量之URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解應用程式內訊息中特定內容的設定檔參與情形。

+++ 深入瞭解追蹤的連結URL量度

* **[!UICONTROL 不重複點按]**：在您的應用程式內訊息中按一下內容的設定檔數。

* **[!UICONTROL 點按次數]**：在您的應用程式內訊息中點按內容的次數。

+++

## 直接郵件 {#direct-mail}

### 正在傳送統計數據 {#sending-statistics-directmail}

![](assets/cja-direct-sending-stat.png)

此 **[!UICONTROL 傳送統計資料]** 表格提供有關直接郵件行銷活動之基本資料的完整摘要。 它會詳細說明關鍵量度，例如目標對象的大小和成功傳送的直接郵件數量，提供您直接郵件訊息的有效性和觸及範圍的寶貴見解。

+++ 進一步瞭解如何傳送統計資料

* **[!UICONTROL 人員]**：符合訊息目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已鎖定目標]**：傳送過程中處理的直接郵件訊息總數。

* **[!UICONTROL 傳送]**：直接郵件訊息的傳送總數。

* **[!UICONTROL 已傳遞]**：成功傳送的直接郵件訊息數，與已傳送訊息總數相關。

* **[!UICONTROL 傳出錯誤]**：在傳送過程中發生且無法傳送至設定檔的錯誤總數。

* **[!UICONTROL 傳出排除專案]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 傳遞狀態 {#delivery-status-directmail}

![](assets/cja-direct-delivery-status.png)

此 **[!UICONTROL 傳遞狀態]** graph提供促銷活動中與已傳送直接郵件訊息相關之資料的完整檢視，提供關鍵量度的深入分析，例如傳送和錯誤。 這可讓您詳細分析直接郵件訊息傳送流程，提供行銷活動的效率和成效的寶貴資訊。

+++ 進一步瞭解傳遞狀態量度

* **[!UICONTROL 已傳遞]**：成功傳送的直接郵件訊息數，與已傳送的直接郵件訊息總數相關。

* **[!UICONTROL 傳出錯誤]**：在傳送過程中發生且阻止您的直接郵件訊息傳送至設定檔的錯誤總數。

* **[!UICONTROL 未繫結排除]**：Adobe Journey Optimizer已排除的設定檔數。

+++

### 錯誤原因 {#error-reasons-directmail}

此 **[!UICONTROL 錯誤原因]** 表格可讓您識別直接郵件訊息傳送過程中發生的特定錯誤，以便深入分析所遇到的任何問題。

### 排除原因 {#exclude-reasons-directmail}

[](assets/cja-direct-excluded.png)

此 **[!UICONTROL 排除原因]** 表格會以視覺化方式呈現導致目標對象中排除使用者設定檔的各種因素，以防止他們接收您的直接郵件訊息。

請參閱 [此頁面](exclusion-list.md) 以取得排除原因的完整清單。

## Web {#web}

### 曝光與點按趨勢 {#impressions-web}

![](assets/cja-web-impression.png)

此 **[!UICONTROL 曝光與點選趨勢]** 圖表提供設定檔與網頁互動的詳細分析，提供設定檔與內容互動方式的寶貴見解。

+++ 進一步瞭解「曝光與點選」趨勢量度

* **[!UICONTROL 點按次數]**：內容在網頁中的點按次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

+++

### 點按次數 {#clicks-web}

![](assets/cja-web-clicks.png)

此 **[!UICONTROL 點按次數]** 圖表會顯示網頁點選量度，說明內容點選總數和點選內容的不重複設定檔數量。

+++ 進一步瞭解點按量度

* **[!UICONTROL 不重複點按]**：點按您網頁中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在網頁中的點按次數。

+++

### 展示次數 {#displays-web}

![](assets/cja-web-displays.png)

此 **[!UICONTROL 顯示區]** 圖表可協助您瞭解訊息的整體觸及範圍和與其互動的不重複設定檔數量。

+++ 深入瞭解顯示量度

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++


### 追蹤資料 {#track-data-web}

![](assets/cja-web-tracking-data.png)

此 **[!UICONTROL 追蹤資料]** 表格提供與您的網頁相連結的個人資料活動的詳細快照，提供參與和網頁效益的基本深入分析。

+++ 進一步瞭解追蹤資料量度

* **[!UICONTROL 人員]**：符合資格成為網頁目標設定檔的使用者設定檔數目。

* **[!UICONTROL 點進率(CTR)]**：與網頁互動的使用者百分比。

* **[!UICONTROL 點按次數]**：內容在網頁中的點按次數。

* **[!UICONTROL 不重複點按]**：點按您網頁中內容的設定檔數。

* **[!UICONTROL 顯示區]**：網頁開啟的次數。

* **[!UICONTROL 不重複顯示]**：網頁開啟的次數，一個設定檔的多個互動不會考慮在內。

+++

### 追蹤的連結標籤 {#track-link-web}

![](assets/cja-web-tracked-link-labels.png)

此 **[!UICONTROL 追蹤的連結標籤]** 表格提供您網頁內連結標籤的完整概觀，醒目顯示產生最高訪客流量的連結。 此功能可讓您識別最熱門的連結並加以優先處理。

+++ 進一步瞭解追蹤的連結標籤量度

* **[!UICONTROL 不重複點按]**：點按您網頁中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在網頁中的點按次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++

### 追蹤的連結 URL {#track-url-web}

![](assets/cja-web-tracked-link-urls.png)

此 **[!UICONTROL 追蹤的連結URL]** 表格提供您網頁中吸引最高訪客流量之URL的完整概觀。 這可讓您識別最熱門的連結並排定其優先順序，進而更瞭解個人檔案參與網頁中特定內容的情形。

+++ 深入瞭解追蹤的連結URL量度

* **[!UICONTROL 不重複點按]**：點按您網頁中內容的設定檔數。

* **[!UICONTROL 點按次數]**：內容在網頁中的點按次數。

* **[!UICONTROL 顯示區]**：訊息開啟的次數。

* **[!UICONTROL 不重複顯示]**：訊息的開啟次數，一個設定檔的多個互動不會考慮在內。

+++
