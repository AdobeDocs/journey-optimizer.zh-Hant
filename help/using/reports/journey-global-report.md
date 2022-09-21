---
title: 歷程全域報告
description: 了解如何使用歷程全域報表中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: aecbf0f8bcfb8f6747ee072d891029a38f8f2ed1
workflow-type: tm+mt
source-wordcount: '1977'
ht-degree: 0%

---

# 歷程全域報告 {#journey-global-report}

您可以直接從歷程存取歷程全域報表，其中包含 **[!UICONTROL 檢視報表]** 按鈕。

![](assets/report_journey.png)

歷程 **[!UICONTROL 全域報表]** 頁面中顯示以下索引標籤：

* [歷程](#journey-global)
* [電子郵件](#email-global)
* [推播](#push-global)
* [SMS](#sms-global)

歷程 **[!UICONTROL 全域報表]** 會分為不同的Widget，詳述您歷程的成功與錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 有關詳細資訊，請參閱 [節](global-report.md#modify-dashboard).

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [本頁](global-report.md#list-of-components-global).

## 歷程標籤 {#journey-global}

從您的歷程 **[!UICONTROL 全域報表]**, **[!UICONTROL 歷程]** 索引標籤可讓您清楚檢視歷程的最重要追蹤資料。

![](assets/journey_global_1.png)

+++進一步了解「歷程」報表可用的不同量度和Widget。

此 **[!UICONTROL 歷程績效]** 介面工具集可讓您逐步查看目標設定檔的路徑，以完成歷程。

此 **[!UICONTROL 歷程統計]** 介面工具集顯示下列KPI:

* **[!UICONTROL 輸入的設定檔]**:到達歷程進入事件的個人總數。

* **[!UICONTROL 退出設定檔]**:離開歷程的個人總數。

* **[!UICONTROL 個別歷程失敗]**:未成功執行的個別歷程總數。

此 **[!UICONTROL 按事件接收的事件]**, **[!UICONTROL 各來源事件]** 和 **[!UICONTROL 熱門事件]** 介面工具集可讓您查看 **[!UICONTROL 事件]** 已通過圖形和表成功執行。

**[!UICONTROL 動作效能]**, **[!UICONTROL 動作錯誤原因]** 和 **[!UICONTROL 排名在前的動作]** 介面工具集代表最成功的動作，以及您 **[!UICONTROL 動作]** 已觸發。

此 **[!UICONTROL 排名在前的動作]** 表格包含可用於 **[!UICONTROL 動作]**，例如：

* **[!UICONTROL 已成功執行操作]**:總數 **[!UICONTROL 動作]** 成功執行歷程。

* **[!UICONTROL 操作錯誤]**:發生的錯誤總數 **[!UICONTROL 動作]**.

此 **[!UICONTROL 同意原則]** 表格和圖表顯示自訂動作中從每個原則排除的設定檔數量。
如需自訂動作的詳細資訊，請參閱 [詳細檔案](../action/about-custom-action-configuration.md).

請注意，若要讓這些Widget出現在您的歷程報表中，您需要重設控制面板。 若要這麼做，請按一下 **[!UICONTROL 修改]** then **[!UICONTROL 重設]** 在報表頂端。
+++

## 電子郵件索引標籤 {#email-global}

從您的歷程 **[!UICONTROL 全域報表]**, **[!UICONTROL 電子郵件]** 索引標籤會詳細列出與歷程中傳送之電子郵件相關的主要資訊。

![](assets/journey_global_2.png)

+++進一步了解「電子郵件」報表中可用的不同量度和小工具。

此 **[!UICONTROL 電子郵件傳送統計資料]** 圖表會詳細說明您的傳送是否成功：

* **[!UICONTROL 已鎖定]**:AdobeJourney Orchestration針對任何動作（例如傳送電子郵件或簡訊）的設定檔數目。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 傳送率]**:已成功發送的消息的百分比。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 反彈率]**:跳出的電子郵件與傳送的電子郵件的百分比。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 錯誤率]**:傳送期間發生、無法傳送的錯誤百分比，與已傳送的電子郵件相比。

此 **[!UICONTROL 電子郵件 — 追蹤統計資料]** 包含您傳送的收件者活動可用資料：

* **[!UICONTROL 開啟]**:傳送中開啟傳送的次數。

* **[!UICONTROL 不重複開啟次數]**:已開啟傳遞的百分比。

* **[!UICONTROL 不重複開放率]**:已開啟電子郵件的總數與已傳送電子郵件的總數相比。

* **[!UICONTROL 點按次數]**:電子郵件中內容被點按的次數。

* **[!UICONTROL 不重複點按次數]**：按一下電子郵件內容的收件者人數。

* **[!UICONTROL 點進率]**:與歷程互動的使用者百分比。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結的點按次數。

* **[!UICONTROL 垃圾郵件投訴]**:宣告郵件為垃圾郵件或垃圾郵件的次數。

此 **[!UICONTROL 傳送統計資料]** 圖表包含可用於傳送電子郵件的資料，例如：

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

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

>[!NOTE]
>
>只有在電子郵件中插入決策時，選件小工具和量度才可供使用。 有關「決策管理」的詳細資訊，請參閱 [頁面](../offers/get-started/starting-offer-decisioning.md).

此 **[!UICONTROL 優惠方案統計資料]** 和 **[!UICONTROL 選件統計資料]** 一段時間後，Widget會測量選件的成功，以及對目標對象的影響。 它會使用KPI詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送選件]**:選件的傳送總數。

* **[!UICONTROL 選件曝光]**:傳遞中開啟選件的次數。

* **[!UICONTROL 選件點按次數]**:傳送中點按選件的次數。

此 **[!UICONTROL 提供詳細統計資訊]** 表格包含您選件中收件者活動的可用資料：

* **[!UICONTROL 版位名稱]**:用來顯示優惠方案的版位名稱。 有關投放位置的詳細資訊，請參閱 [頁面](../offers/offer-library/creating-placements.md).

* **[!UICONTROL 選件名稱]**:傳送中新增的選件名稱。 有關投放位置的詳細資訊，請參閱 [頁面](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL 已傳送選件]**:選件的傳送總數。

* **[!UICONTROL 選件曝光率]**:已開啟選件與已傳送選件數量的百分比。

* **[!UICONTROL 選件點按率]**:與優惠方案互動的使用者百分比。
+++

## 推播通知標籤 {#push-global}

從您的歷程 **[!UICONTROL 全域報表]**, **[!UICONTROL 推播通知]** 索引標籤會詳細說明與歷程中傳送的推送傳送相關的主要資訊。

![](assets/journey_global_3.png)

+++進一步了解「推送」報表可用的不同量度和Widget。

此 **[!UICONTROL 推播通知 — 傳送統計資料]** 表格會透過圖表和KPI，詳細說明與推播通知相關的主要資訊：

* **[!UICONTROL 已鎖定]**:AdobeJourney Orchestration針對任何動作（例如傳送電子郵件或簡訊）的設定檔數目。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 傳送率]**:已成功發送的消息的百分比。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 反彈率]**:跳出的推播通知與傳送的推播通知的百分比。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

* **[!UICONTROL 錯誤率]**:與傳送的推播通知相比，傳送期間發生而無法傳送的錯誤百分比。

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

簡訊 **[!UICONTROL 全域報表]** 會分為不同的小工具，詳述傳送的成功和錯誤。 如有需要，可對每個介面工具集調整大小並加以刪除。 如需詳細資訊，請參閱 [節](global-report.md#modify-dashboard).
+++

## SMS標籤 {#sms-global}

![](assets/journey_global_4.png)

+++進一步了解SMS報表可用的不同量度和Widget。

此 **[!UICONTROL SMS — 傳送統計資料]** 表格會詳細說明傳送的成功：

* **[!UICONTROL 已鎖定]**:符合此傳送目標設定檔資格的使用者設定檔數目。

* **[!UICONTROL 已排除]**:未接收訊息的使用者設定檔數目，已從目標設定檔中排除。

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 簡訊摘要]** 介面工具集會透過圖表詳細說明與訊息相關的主要資訊：

* **[!UICONTROL 已傳送]**:傳送的傳送總數。

* **[!UICONTROL 傳遞]**:已成功傳送的訊息數，與已傳送的訊息總數相關。

* **[!UICONTROL 跳出數]**:傳送和自動回傳處理期間累積的錯誤總數，與已傳送訊息的總數相關。

* **[!UICONTROL 錯誤]**:傳送期間發生的錯誤總數，使其無法傳送至設定檔。

此 **[!UICONTROL 排除原因]** 圖形和表格可讓您查看在傳送期間發生的錯誤和排除。
+++
