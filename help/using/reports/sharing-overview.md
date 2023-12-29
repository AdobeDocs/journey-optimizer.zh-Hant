---
solution: Journey Optimizer
product: journey optimizer
title: 歷程步驟分享概覽
description: 歷程步驟分享概覽
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 3%

---

# 建立歷程報告 {#design-jo-reports}

除了 [即時報表](live-report.md) 和內建 [全域報告功能](global-report.md)， [!DNL Journey Optimizer] 可以自動將歷程績效資料傳送至Adobe Experience Platform，以便與其他資料結合而進行分析。

>[!NOTE]
>
>此功能預設會在歷程步驟事件的所有執行個體上啟動。 您無法修改或更新在布建步驟事件期間建立的結構描述和資料集。 預設情況下，這些結構描述和資料集處於唯讀模式。

例如，您已設定傳送多封電子郵件的歷程。 此功能可讓您結合 [!DNL Journey Optimizer] 含有下游事件資料的資料，例如已發生轉換的數量、網站上發生的參與度或是商店中發生的交易數。 歷程資訊可與Adobe Experience Platform上的資料結合，結合方式為來自其他數位屬性或離線屬性，以提供更完整的效能檢視。

[!DNL Journey Optimizer] 自動建立必要的結構描述，並針對個人在歷程中採取的每個步驟，將資料集串流至Adobe Experience Platform。 步驟事件對應於在歷程中從某個節點移動到另一個節點的個人。 例如，在包含事件、條件和動作的歷程中，會將三個步驟事件傳送至Adobe Experience Platform。

傳遞的XDM欄位清單是完整的。 有些包含系統產生的程式碼，有些則有人類看得懂的易記名稱。 範例包括歷程活動的標籤或步驟狀態：動作逾時或錯誤結束的次數。

>[!CAUTION]
>
>無法為即時設定檔服務開啟資料集。 請確定 **[!UICONTROL 個人資料]** 切換功能已關閉。

[!DNL Journey Optimizer] 會在資料發生時以串流方式傳送資料。 您可以使用查詢服務來查詢此資料。 您可以連線至Customer Journey Analytics或其他BI工具，以檢視與這些步驟相關的資料。

將建立下列結構描述：

* 的歷程步驟事件結構描述 [!DNL Journey Orchestration]  — 繫結至歷程中繼資料的歷程步驟事件。
* 歷程結構描述及其歷程欄位 [!DNL Journey Orchestration]  — 說明歷程的歷程中繼資料。

![](assets/sharing1.png)

![](assets/sharing2.png)

會傳遞下列資料集：

* 歷程步驟事件
* 歷程

![](assets/sharing3.png)

傳遞至Adobe Experience Platform的XDM欄位清單詳細說明：

* [步驟事件欄位清單](../reports/sharing-field-list.md)
* [舊版步驟事件欄位](../reports/sharing-legacy-fields.md)

## 與Customer Journey Analytics整合 {#integration-cja}

[!DNL Journey Optimizer] 步驟事件可以連結到中的其他資料集 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant){target="_blank"}.

一般工作流程為：

* [!DNL Customer Journey Analytics] 內嵌「歷程步驟事件」資料集。
* 此 **profileID** 相關聯「用於Journey Orchestration的歷程步驟事件結構描述」中的欄位定義為身分欄位。 在 [!DNL Customer Journey Analytics]，然後您可以將此資料集連結至與以人員為基礎的識別碼具有相同值的任何其他資料集。
* 若要在中使用此資料集 [!DNL Customer Journey Analytics]，如需跨管道歷程分析，請參閱 [Customer Journey Analytics檔案](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"}.

