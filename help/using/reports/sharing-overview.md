---
title: 歷程步驟分享概覽
description: 歷程步驟分享概覽
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 4%

---

# 建立歷程報告 {#design-jo-reports}

除 [即時報告](live-report.md) 內置 [全局報告功能](global-report.md)。 [!DNL Journey Optimizer] 可以自動將行程效能資料發送到Adobe Experience Platform，以便與其他資料組合以便進行分析。

>[!NOTE]
>
>This feature is activated by default on all instances for journey steps events. For journey profile step events, the activation is upon request. 您不能修改或更新在為步驟事件設定期間建立的架構和資料集。 By default, these schemas and datasets are in read-only mode.

例如，您已設定了發送多個電子郵件的行程。 此功能允許您將 [!DNL Journey Optimizer] 與下游事件資料的資料，如發生了多少次轉換、網站上發生了多少項參與，或在儲存中發生了多少事務。 行程資訊可以與Adobe Experience Platform上的資料組合，或者從其他數字屬性或從離線屬性中組合，以提供更全面的效能視圖。

[!DNL Journey Optimizer] 自動為個人在旅途中採取的每一步建立必要的模式並將其流式傳輸到Adobe Experience Platform。 步驟事件對應於在行程中從一個節點移動到另一個節點的個人。 For example, in a journey that has an event, a condition and an action, three step events are sent to Adobe Experience Platform.

傳遞的XDM欄位清單是全面的。 有些包含系統生成的代碼，有些則具有可讀的友好名稱。 示例包括行程活動的標籤或步驟狀態：操作超時或錯誤結束的次數。

>[!CAUTION]
>
>無法為即時配置檔案服務開啟資料集。 Please make sure that the **[!UICONTROL Profile]** toggle is turned off.

Journeys sends data as it occurs, in a streaming way. 您可以使用查詢服務查詢此資料。 You can connect to Customer Journey Analytics or other BI tools to view data related to these steps.

The following schemas are created:

* 行程步驟配置檔案事件架構 [!DNL Journey Orchestration]  — 體驗事件，用於在行程中執行的步驟以及用於映射到單個行程參與者的身份映射。
* 行程步驟事件架構 [!DNL Journey Orchestration]  — 與行程元資料相關聯的行程步驟事件。
* Journey schema with Journey Fields for [!DNL Journey Orchestration] – Journey Metadata to describe Journeys.

![](assets/sharing1.png)

![](assets/sharing2.png)

傳遞了以下資料集：

* 行程步驟配置檔案事件架構 [!DNL Journey Orchestration]
* 旅程事件
* 歷程

![](assets/sharing3.png)

The lists of XDM fields passed to Adobe Experience Platform are detailed here:

* [步驟事件欄位清單](../reports/sharing-field-list.md)
* [舊版步驟事件欄位](../reports/sharing-legacy-fields.md)

有關向Adobe Experience Platform報告的步驟事件的詳細資訊，請觀看此 [教程視頻](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/reporting-step-events-to-adobe-experience-platform.html){target=&quot;_blank&quot;}。

## 與Customer Journey Analytics整合 {#integration-cja}

Journey Optimizer步驟事件可以連結到中的其他資料集 [AdobeCustomer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant)。 以下是一般工作流：

* Customer Journey Analytics ingests the &quot;Journey Step Event&quot; dataset.
* 的 **配置檔案ID** 關聯的「Journey Orchestration的行程步驟事件模式」中的欄位定義為「標識」欄位。 在Customer Journey Analytics中，然後可以將此資料集連結到與基於人員的標識符具有相同值的任何其他資料集。
* 如果要在Customer Journey Analytics中使用此資料集，請參閱此 [文檔](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html)。

