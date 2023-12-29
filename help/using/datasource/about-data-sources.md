---
solution: Journey Optimizer
product: journey optimizer
title: 關於資料來源
description: 瞭解如何設定資料來源
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 資料，來源，歷程，平台
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 72%

---

# 關於資料來源 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="關於資料來源"
>abstract="資料來源設定一律會由技術使用者執行。資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊，例如：條件定義、動作中的參數和個人化資料、自訂等待定義、自訂時區定義。"

資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊，例如：

* [條件定義](../building-journeys/condition-activity.md)
* [動作](../action/action.md)中的參數和個人化資料
* [自訂等待定義](../building-journeys/wait-activity.md#custom)
* [時區定義](../building-journeys/timezone-management.md)

➡️ [在影片中探索此功能](#video)

如果您的歷程僅運用來自事件裝載的本機資料，則不需要進行此設定。例如，如果您的歷程由事件組成，之後僅會使用來自事件資料的管道動作活動，則不需要設定資料來源。

資料來源有兩種類型：

* 預先設定的 Adobe Experience Platform 資料來源可定義「即時客戶個人檔案服務」的連線，這是內建的資料來源。請參閱[此頁面](../datasource/adobe-experience-platform-data-source.md)。
* 外部資料來源可讓您定義外部系統的連線，這些是您可以建立的資料來源。請參閱[此頁面](../datasource/external-data-sources.md)。

對於每個資料來源，您會使用欄位群組來定義要擷取的資訊。欄位群組是可從資料來源擷取的欄位集。請參閱[此頁面](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>資料來源不支援結構描述關係。

如需如何設定Adobe Experience Platform資料來源和外部資料來源，以及如何在歷程中尋找和使用資料的詳細資訊，請觀看此影片 [教學課程影片](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}.

## 操作說明影片 {#video}

了解資料來源為何，以及如何設定 Experience Platform 和外部資料來源。

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

