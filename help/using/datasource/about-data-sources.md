---
title: 關於資料來源
description: 瞭解如何設定資料來源
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: d9f7c64358be3c3355337ba0db12e5b8c17bba4c
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 74%

---

# 關於資料來源 {#about-data-sources}

>[!CONTEXTUALHELP]
>id="jo_datasources"
>title="關於資料來源"
>abstract="資料來源設定一律會由技術使用者執行。資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊，例如：條件定義、動作中的參數和個人化資料、自訂等待定義、自訂時區定義。"

資料來源設定可讓您定義系統連線，以擷取將用於歷程的其他資訊，例如：

* [條件定義](../building-journeys/condition-activity.md)
* [動作](../action/action.md)中的參數和個人化資料
* [自定等待定義](../building-journeys/wait-activity.md#custom)
* [時區定義](../building-journeys/timezone-management.md)

➡️ [在影片中探索此功能](#video)

如果您的歷程僅運用來自事件裝載的本機資料，則不需要進行此設定。例如，如果行程由一個事件組成，然後是一個僅使用事件資料的消息活動，則無需配置資料源。

資料來源有兩種類型：

* 預先設定的 Adobe Experience Platform 資料來源可定義「即時客戶個人檔案服務」的連線，這是內建的資料來源。請參閱[此頁面](../datasource/adobe-experience-platform-data-source.md)。
* 外部資料來源可讓您定義外部系統的連線，這些是您可以建立的資料來源。請參閱[此頁面](../datasource/external-data-sources.md)。

對於每個資料來源，您會使用欄位群組來定義要擷取的資訊。欄位群組是可從資料來源擷取的欄位集。請參閱[此頁面](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>現在，資料源支援架構關係。

有關如何配置Adobe Experience Platform資料源和外部資料源以及如何查找和使用行程中的資料的詳細資訊，請觀看此資訊 [教程視頻](https://experienceleague.adobe.com/docs/journey-orchestration-learn/tutorials/configure-data-sources.html){target=&quot;_blank&quot;}。

## How-to視頻 {#video}

了解資料來源為何，以及如何設定 Experience Platform 和外部資料來源。

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

