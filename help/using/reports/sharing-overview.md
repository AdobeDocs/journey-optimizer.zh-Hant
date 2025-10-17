---
solution: Journey Optimizer
product: journey optimizer
title: 歷程步驟分享概觀
description: 歷程步驟分享概觀
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: efae7f7d366690af71430bb9eb62523d1881c50e
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 3%

---

# 建立歷程報告 {#design-jo-reports}

除了[即時報表](live-report.md)和內建[報告功能](report-gs-cja.md)之外，[!DNL Journey Optimizer]還可以自動將歷程績效資料傳送至Adobe Experience Platform，以便與其他資料結合以進行分析。

>[!NOTE]
>
>此功能預設會在歷程步驟事件的所有執行個體上啟動。 您無法修改或更新在布建步驟事件期間建立的結構描述和資料集。 預設情況下，這些結構描述和資料集處於唯讀模式。

例如，您已設定傳送多封電子郵件的歷程。 此功能可讓您將[!DNL Journey Optimizer]資料與下游事件資料結合，例如發生轉換數、網站上發生的參與數，或商店中發生的交易數。 歷程資訊可與Adobe Experience Platform上的資料結合，結合方式為來自其他數位屬性或離線屬性，以提供更完整的效能檢視。

[!DNL Journey Optimizer]會自動建立必要的結構描述，並針對個人在歷程中執行的每個步驟，將資料集串流至Adobe Experience Platform。 步驟事件對應於在歷程中從某個節點移動到另一個節點的個人。 例如，在包含事件、條件和動作的歷程中，會將三個步驟事件傳送至Adobe Experience Platform。

>[!NOTE]
>
>除了設定檔層級步驟事件之外，系統也會產生&#x200B;**讀取對象**&#x200B;活動的內部事件。 這些稱為`segmentExportJob`事件的事件會記錄「讀取對象」節點的生命週期（例如匯出工作建立、佇列、完成和錯誤），而且是根據「讀取對象」活動（而非個別設定檔）產生。 因此，這些事件可能沒有相關的設定檔識別碼(UPMID)。 這些內部事件對於監視和疑難排解讀取對象效能非常有用，可以使用[serviceEvents區段](../reports/sharing-field-list.md#servicevents-field)中記錄的欄位進行查詢。 如需有關如何使用segmentExportJob事件的查詢範例，請參閱與讀取對象相關的[查詢](../reports/query-examples.md#read-segment-queries)。

在某些情況下，可以為同一節點建立多個事件。 例如，在等待活動的案例中：

* 當設定檔進入wait （journeyNodeProcessed屬性等於false）時，會產生一個事件
* 當設定檔退出時會產生一個事件（journeyNodeProcessed屬性等於true）

傳遞的XDM欄位清單是完整的。 有些包含系統產生的程式碼，有些則有人類看得懂的易記名稱。 範例包括歷程活動的標籤或步驟狀態：動作逾時或錯誤結束的次數。

>[!CAUTION]
>
>無法為即時設定檔服務開啟資料集。 請確定&#x200B;**[!UICONTROL 設定檔]**&#x200B;切換功能已關閉。

[!DNL Journey Optimizer]會在資料發生時傳送資料，以串流方式進行。 您可以使用查詢服務來查詢此資料。 您可以連線至Customer Journey Analytics或其他BI工具，以檢視與這些步驟相關的資料。

將建立下列結構描述：

* [!DNL Journey Orchestration]的歷程步驟事件結構描述 — 繫結至歷程中繼資料的歷程步驟事件。
* 具有[!DNL Journey Orchestration]的歷程欄位的歷程結構描述 — 描述歷程的歷程中繼資料。

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

[!DNL Journey Optimizer]個步驟事件可以連結到[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant){target="_blank"}中的其他資料集。

一般工作流程為：

* [!DNL Customer Journey Analytics]內嵌「歷程步驟事件」資料集。
* 關聯的「Journey Orchestration的歷程步驟事件結構描述」中的&#x200B;**profileID**&#x200B;欄位定義為身分欄位。 在[!DNL Customer Journey Analytics]中，您可以將此資料集連結至與以人員為基礎的識別碼具有相同值的任何其他資料集。
* 若要在[!DNL Customer Journey Analytics]中使用此資料集，如需進行跨管道歷程分析，請參閱[Customer Journey Analytics檔案](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html?lang=zh-Hant){target="_blank"}。

➡️ [使用Customer Journey Analytics](cja-ajo.md){target="_blank"}
