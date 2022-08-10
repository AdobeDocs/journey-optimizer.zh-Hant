---
title: 歷程步驟分享概覽
description: 歷程步驟分享概覽
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 1fa91a841d4f941f2c5bd1efd4a06ac8a9938bc7
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 5%

---

# 建立歷程報告 {#design-jo-reports}

除 [即時報告](live-report.md) 內置 [全局報告功能](global-report.md)。 [!DNL Journey Optimizer] 可以自動將行程效能資料發送到Adobe Experience Platform，以便與其他資料組合以便進行分析。

>[!NOTE]
>
>預設情況下，在所有實例上都會激活此功能，用於行程步驟事件。 您不能修改或更新在為步驟事件設定期間建立的架構和資料集。 預設情況下，這些架構和資料集處於只讀模式。

例如，您已設定了發送多個電子郵件的行程。 此功能允許您將 [!DNL Journey Optimizer] 與下游事件資料的資料，如發生了多少次轉換、網站上發生了多少項參與，或在儲存中發生了多少事務。 行程資訊可以與Adobe Experience Platform上的資料組合，或者從其他數字屬性或從離線屬性中組合，以提供更全面的效能視圖。

[!DNL Journey Optimizer] 自動為個人在旅途中採取的每一步建立必要的模式並將其流式傳輸到Adobe Experience Platform。 步驟事件對應於在行程中從一個節點移動到另一個節點的個人。 例如，在具有事件、條件和動作的旅程中，三步事件被發送到Adobe Experience Platform。

傳遞的XDM欄位清單是全面的。 有些包含系統生成的代碼，有些則具有可讀的友好名稱。 示例包括行程活動的標籤或步驟狀態：操作超時或錯誤結束的次數。

>[!CAUTION]
>
>無法為即時配置檔案服務開啟資料集。 請確保 **[!UICONTROL Profile]** 切換被關閉。

[!DNL Journey Optimizer] 以流方式在資料發生時發送資料。 您可以使用查詢服務查詢此資料。 您可以連接到Customer Journey Analytics或其他BI工具，以查看與這些步驟相關的資料。

將建立以下架構：

* 行程步驟事件架構 [!DNL Journey Orchestration]  — 與行程元資料相關聯的行程步驟事件。
* 帶行程欄位的行程架構 [!DNL Journey Orchestration]  — 描述旅程的旅程元資料。

![](assets/sharing1.png)

![](assets/sharing2.png)

傳遞了以下資料集：

* 旅程事件
* 歷程

![](assets/sharing3.png)

傳遞給Adobe Experience Platform的XDM欄位清單如下：

* [步驟事件欄位清單](../reports/sharing-field-list.md)
* [舊版步驟事件欄位](../reports/sharing-legacy-fields.md)

## 與Customer Journey Analytics整合 {#integration-cja}

[!DNL Journey Optimizer] 步驟事件可以連結到中的其他資料集 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant){target=&quot;_blank&quot;}。

一般工作流是：

* [!DNL Customer Journey Analytics] 接收「行程步驟事件」資料集。
* 的 **配置檔案ID** 關聯的「Journey Orchestration的行程步驟事件模式」中的欄位定義為「標識」欄位。 在 [!DNL Customer Journey Analytics]，然後可以將此資料集連結到與基於人員的標識符具有相同值的任何其他資料集。
* 在 [!DNL Customer Journey Analytics]，有關跨通道行程分析，請參閱 [Customer Journey Analytics文檔](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}。

