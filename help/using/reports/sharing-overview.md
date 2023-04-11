---
solution: Journey Optimizer
product: journey optimizer
title: 歷程步驟分享概覽
description: 歷程步驟分享概覽
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 5%

---

# 建立歷程報告 {#design-jo-reports}

除 [即時報表](live-report.md) 和內建 [全域報告功能](global-report.md), [!DNL Journey Optimizer] 可自動將歷程績效資料傳送至Adobe Experience Platform，以便與其他資料結合以進行分析。

>[!NOTE]
>
>此功能預設會在歷程步驟事件的所有執行個體上啟用。 您無法修改或更新在布建步驟事件期間建立的結構和資料集。 這些結構和資料集預設為唯讀模式。

例如，您已設定可傳送多封電子郵件的歷程。 此功能可讓您結合 [!DNL Journey Optimizer] 具有下游事件資料的資料，例如發生了多少次轉換、網站上發生了多少參與，或商店中發生了多少交易。 歷程資訊可與Adobe Experience Platform上的資料結合，不論是來自其他數位屬性或來自離線屬性，以提供更全面的效能檢視。

[!DNL Journey Optimizer] 針對個人在歷程中執行的每個步驟，自動將必要的結構描述和資料流建立至資料集Adobe Experience Platform。 步驟事件對應至歷程中從一個節點移至另一個節點的個人。 例如，在具有事件、條件和動作的歷程中，會將三個步驟事件傳送至Adobe Experience Platform。

傳遞的XDM欄位清單為完整。 有些包含系統產生的程式碼，有些則有人類看得懂的易記名稱。 範例包括歷程活動的標籤或步驟狀態：動作逾時或因錯誤而結束的次數。

>[!CAUTION]
>
>無法為即時設定檔服務開啟資料集。 請確定 **[!UICONTROL 設定檔]** 切換為關閉。

[!DNL Journey Optimizer] 以串流方式在資料發生時傳送。 您可以使用查詢服務查詢此資料。 您可以連線至Customer Journey Analytics或其他BI工具，以檢視與這些步驟相關的資料。

會建立下列結構：

* 適用於的歷程步驟事件結構 [!DNL Journey Orchestration]  — 系結至歷程中繼資料的歷程步驟事件。
* 具有歷程欄位的歷程結構 [!DNL Journey Orchestration]  — 描述歷程的歷程中繼資料。

![](assets/sharing1.png)

![](assets/sharing2.png)

會傳遞下列資料集：

* 歷程步驟事件
* 歷程

![](assets/sharing3.png)

傳遞至Adobe Experience Platform的XDM欄位清單詳列於此處：

* [步驟事件欄位清單](../reports/sharing-field-list.md)
* [舊版步驟事件欄位](../reports/sharing-legacy-fields.md)

## 與Customer Journey Analytics整合 {#integration-cja}

[!DNL Journey Optimizer] 步驟事件可連結至 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant){target="_blank"}.

一般工作流程為：

* [!DNL Customer Journey Analytics] 內嵌「歷程步驟事件」資料集。
* 此 **profileID** 相關「Journey Orchestration的歷程步驟事件結構」中的欄位定義為「身分」欄位。 在 [!DNL Customer Journey Analytics]，您就可以將此資料集連結至任何其他與人員型識別碼具有相同值的資料集。
* 若要在 [!DNL Customer Journey Analytics]，如需跨頻道歷程分析，請參閱 [Customer Journey Analytics檔案](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"}.

