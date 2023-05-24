---
solution: Journey Optimizer
product: journey optimizer
title: 歷程全域報告
description: 瞭解如何使用旅程全球報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: e851646e-4cef-45e8-97c2-a8f4c9d2cc08
source-git-commit: 4f3d22c9ce3a5b77969a2a04dafbc28b53f95507
workflow-type: tm+mt
source-wordcount: '2044'
ht-degree: 2%

---

# 歷程全域報告 {#journey-global-report}

>[!CONTEXTUALHELP]
>id="ajo_journey_global_report"
>title="歷程全域報告"
>abstract="歷程全域報告可讓您測量您的歷程在選取時段內的影響。您的報告會分為不同的 Widget，詳細說明您的歷程的成功和錯誤。每個報告儀表板都可以透過調整大小或移除 Widget 來修改。"

您可以直接通過 **[!UICONTROL 查看報表]** 按鈕

![](assets/report_journey.png)

旅程 **[!UICONTROL 全局報告]** 的子菜單。

* [歷程](#journey-global)
* [電子郵件](#email-global)
* [推播](#push-global)
* [簡訊](#sms-global)

旅程 **[!UICONTROL 全局報告]** 被分成不同的小部件，詳細描述你旅途的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此的詳細資訊，請參閱此 [節](global-report.md#modify-dashboard)。

有關Adobe Journey Optimizer可用的每個指標的詳細清單，請參閱 [此頁](global-report.md#list-of-components-global)。

## 行程頁籤 {#journey-global}

從你的旅程 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 旅程]** 頁籤可讓您清楚地查看有關行程的最重要跟蹤資料。

![](assets/journey_global_1.png)

+++瞭解「旅程」報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 旅程效能]** 構件允許您逐步查看目標配置檔案的路徑。

的 **[!UICONTROL 旅程統計]** 小部件顯示以下KPI:

* **[!UICONTROL 輸入的配置檔案]**:到達旅程的入門事件的個人總數。

* **[!UICONTROL 退出配置檔案]**:離開旅程的個人總數。

* **[!UICONTROL 單程失敗]**:未成功執行的單個行程的總數。

的 **[!UICONTROL 按事件接收的事件]**。 **[!UICONTROL 按來源列出的事件]** 和 **[!UICONTROL 熱門事件]** 小部件可讓您查看 **[!UICONTROL 事件]** 已通過圖形和表成功執行。

**[!UICONTROL 操作效能]**。 **[!UICONTROL 操作錯誤原因]** 和 **[!UICONTROL 頂級操作]** 小部件代表您在 **[!UICONTROL 操作]** 觸發。

的 **[!UICONTROL 頂級操作]** 表包含可用於 **[!UICONTROL 操作]**，例如：

* **[!UICONTROL 已成功執行操作]**:總數 **[!UICONTROL 操作]** 成功執行。

* **[!UICONTROL 操作中出錯]**:發生的錯誤總數 **[!UICONTROL 操作]**。

的 **[!UICONTROL 同意策略]** 表和圖形顯示自定義操作中從每個策略中排除的配置檔案數。
有關自定義操作的詳細資訊，請參閱 [詳細文檔](../action/about-custom-action-configuration.md)。

請注意，要使這些小部件顯示在您的「行程」報表中，您需要重置儀表板。 為此，請按一下 **[!UICONTROL 修改]** 然後 **[!UICONTROL 重置]** 在報告的頂部。
+++

## 電子郵件頁籤 {#email-global}

從你的旅程 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 電子郵件]** 頁籤，詳細列出與在旅途中發送的電子郵件遞送相關的主要資訊。

![](assets/journey_global_2.png)

+++瞭解電子郵件報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 電子郵件發送統計資訊]** 圖表詳細說明了您交付的成功：

* **[!UICONTROL 目標]**:AdobeJourney Orchestration針對任何操作（如發送電子郵件或SMS）的配置檔案數

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 交貨率]**:成功發送的郵件百分比。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 彈跳率]**:與發送的電子郵件相比，已跳轉的電子郵件的百分比。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 錯誤率]**:與發送的電子郵件相比，在發送過程中發生的阻止發送錯誤的百分比。

的 **[!UICONTROL 電子郵件 — 跟蹤統計]** 包含您交貨的收件人活動的可用資料：

* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。

* **[!UICONTROL 唯一開啟]**:已開啟交貨的百分比。

* **[!UICONTROL 唯一開啟率]**:已開啟電子郵件的總數與已發送電子郵件的數量相比。

* **[!UICONTROL 按一下]**:在電子郵件中按一下內容的次數。

* **[!UICONTROL 唯一按一下]**：按一下電子郵件內容的收件人數。

* **[!UICONTROL 按一下瀏覽率]**:與旅程互動的用戶百分比。

* **[!UICONTROL 取消訂閱]**:取消訂閱連結上的按一下次數。

* **[!UICONTROL 垃圾郵件投訴]**:將郵件聲明為垃圾郵件或垃圾郵件的次數。

的 **[!UICONTROL 正在發送統計資訊]** 圖形包含可用於已發送電子郵件的資料，如：

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 彈出原因]** 和 **[!UICONTROL 彈出類別]** 小部件包含與已恢復消息相關的可用資料，如：

* **[!UICONTROL 硬彈]**:永久錯誤（如錯誤的電子郵件地址）的總數。 這涉及一條錯誤消息，該錯誤消息明確指出地址無效，如「未知用戶」。

* **[!UICONTROL 軟彈跳]**:臨時錯誤（如完整收件箱）的總數。

* **[!UICONTROL 已忽略]**:臨時（如「外出」）或技術錯誤（例如，如果發件人類型是郵遞員）的總數。

有關退貨的詳細資訊，請參閱 [隱藏清單](../reports/suppression-list.md) 的子菜單。

的 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL 排除的原因]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL 電子郵件 — 頂部URL]** 圖表和表詳細資訊，您傳遞的URL訪問量最大。

的 **[!UICONTROL 電子郵件 — 頂級收件人域]** 圖表和表詳細資訊，哪些域是收件人開啟電子郵件時最常用的域。

>[!NOTE]
>
>的 **[!UICONTROL 優化與未優化]** 和 **[!UICONTROL 發送時間優化]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱 [此頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL 優化與未優化]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL 已發送]**:交貨的發送總數。
* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。
* **[!UICONTROL 按一下]**:在電子郵件中按一下內容的次數。

的 **[!UICONTROL 發送時間優化]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

>[!NOTE]
>
>只有在電子郵件中插入了決定時，「提供」小部件和度量才可用。 有關決策管理的詳細資訊，請參閱 [頁](../offers/get-started/starting-offer-decisioning.md)。

的 **[!UICONTROL 提供統計資訊]** 和 **[!UICONTROL 提供統計資訊]** 隨著時間推移，小部件可衡量您的產品的成功程度以及對目標受眾的影響。 它使用KPI詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已發送優惠]**:發送要約的總數。

* **[!UICONTROL 提供印象]**:在交貨中開啟要約的次數。

* **[!UICONTROL 提供點擊]**:在交貨中按一下要約的次數。

的 **[!UICONTROL 提供詳細統計資訊]** 表包含與您的優惠一起用於收件人活動的可用資料：

* **[!UICONTROL 放置名稱]**:用於顯示優惠的位置的名稱。 有關放置的詳細資訊，請參閱 [頁](../offers/offer-library/creating-placements.md)。

* **[!UICONTROL 優惠名稱]**:在交貨中添加的要約的名稱。 有關放置的詳細資訊，請參閱 [頁](../offers/offer-library/creating-personalized-offers.md)。

* **[!UICONTROL 已發送優惠]**:發送要約的總數。

* **[!UICONTROL 提供印象率]**:已開啟的優惠與已發送的優惠數目相比的百分比。

* **[!UICONTROL 服務點擊率]**:與報價互動的用戶百分比。
+++

## 推送通知頁籤 {#push-global}

從你的旅程 **[!UICONTROL 全局報告]**，也請參見Wiki頁。 **[!UICONTROL 推送通知]** 頁籤詳細列出與在行程中發送的推送交貨相關的主要資訊。

![](assets/journey_global_3.png)

+++瞭解有關「推送」報告可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL 推送通知 — 發送統計資訊]** 表詳細列出了與使用圖表和KPI的推送通知相關的主要資訊：

* **[!UICONTROL 目標]**:AdobeJourney Orchestration針對任何操作（如發送電子郵件或SMS）的配置檔案數

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 交貨率]**:成功發送的郵件百分比。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 彈跳率]**:與發送的推送通知相比，已跳轉的推送通知的百分比。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

* **[!UICONTROL 錯誤率]**:與發送的推送通知相比，在發送過程中發生的錯誤阻止發送的百分比。

的 **[!UICONTROL 推送 — 跟蹤統計資訊]** 包含您交貨的收件人活動的可用資料：

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 開啟速率]**:開啟的推送通知百分比。

* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL 預訂]**:此推送通知的開啟和操作總數，即，如果配置檔案開啟了推送或按一下了按鈕。

* **[!UICONTROL 訂約率]**:此推送通知的開啟和操作的百分比，即，如果配置檔案開啟了推送或按一下了按鈕。

的 **[!UICONTROL 推送通知摘要]** 圖形包含可用於發送推送通知的資料，如：

* **[!UICONTROL 開啟]**:在傳遞中開啟消息的次數。

* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

>[!NOTE]
>
>的 **[!UICONTROL 優化與未優化]** 和 **[!UICONTROL 發送時間優化]**  只有在為您的交貨激活「發送時間優化」選項時，小部件才可用。 有關發送時間優化的詳細資訊，請參閱 [此頁](../building-journeys/journeys-message.md#send-time-optimization)。

的 **[!UICONTROL 優化與未優化]** 圖表詳細列出了與消息相關的主要資訊，這些資訊是否已優化：

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 開啟]**:在交貨中開啟交貨的次數。
* **[!UICONTROL 操作]**:已傳遞的推送通知操作總數，例如按一下按鈕或解除按鈕。

的 **[!UICONTROL 發送時間優化]** 根據發送方法詳細說明您的交付成功：已優化或正常。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。
* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

的 **[!UICONTROL 錯誤原因]** 圖形和表格允許您查看在交付期間發生的錯誤。

的 **[!UICONTROL 排除的原因]** 圖形和表顯示阻止從目標配置檔案中排除的用戶配置檔案接收消息的不同原因。

的 **[!UICONTROL 按平台跟蹤]**。 **[!UICONTROL 按平台發送]** 和 **[!UICONTROL 按平台細分]** 圖表和表格根據收件人的作業系統詳細說明推送通知的成功。

簡訊 **[!UICONTROL 全局報告]** 被分成不同的小部件，詳細列出交付的成功和錯誤。 如果需要，可以調整每個小部件的大小並將其刪除。 有關此項的詳細資訊，請參閱 [節](global-report.md#modify-dashboard)。
+++

## SMS頁籤 {#sms-global}

![](assets/journey_global_4.png)

+++瞭解SMS報告中可用的不同度量和小部件的詳細資訊。

的 **[!UICONTROL SMS — 正在發送統計資訊]** 表詳細列出了您交付的成功：

* **[!UICONTROL 目標]**:符合此傳遞目標配置檔案的用戶配置檔案數。

* **[!UICONTROL 已排除]**:未接收消息的從目標配置檔案中排除的用戶配置檔案數。

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 簡訊摘要]** 小部件使用圖表詳細列出與消息相關的主要資訊：

* **[!UICONTROL 已發送]**:交貨的發送總數。

* **[!UICONTROL 已交付]**:成功發送的消息數，與已發送的消息總數相關。

* **[!UICONTROL 邊界]**:在傳遞和自動返回處理期間累積的與已發送消息總數有關的錯誤總數。

* **[!UICONTROL 錯誤]**:在傳遞期間發生的錯誤總數，使其無法發送到配置檔案。

的 **[!UICONTROL 排除原因]** 圖形和表格允許您查看在交付期間發生的錯誤和排除。

的 **[!UICONTROL SMS — 按連結按一下]** 和 **[!UICONTROL SMS — 跟蹤統計資訊]** 小部件詳細列出與訪問者與URL的約定有關的主要資訊。

+++
