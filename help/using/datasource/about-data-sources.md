---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用資料來源
description: 瞭解如何開始使用資料來源
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: 資料，來源，歷程，平台
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 36f8224b33411f23f23985c55bdb6cebbcdf5712
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 37%

---

# 開始使用資料來源 {#about-data-sources}

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

* **預先設定的** Adobe Experience Platform資料來源定義與即時客戶個人檔案服務的連線。 這是內建的資料來源。請參閱[此頁面](../datasource/adobe-experience-platform-data-source.md)。
* 允許您定義外部系統連線的&#x200B;**外部**&#x200B;資料來源。 這些是您可以建立的資料來源。請參閱[此頁面](../datasource/external-data-sources.md)。

>[!NOTE]
>
>現在支援回應，因此您應該針對外部資料來源使用案例使用自訂動作，而非資料來源。 如需回應的詳細資訊，請參閱此[區段](../action/action-response.md)

對於每個資料來源，您會使用欄位群組來定義要擷取的資訊。欄位群組是可從資料來源擷取的欄位集。請參閱[此頁面](../datasource/configure-data-sources.md#define-field-groups)。

>[!NOTE]
>
>資料來源不支援結構描述關係。

## 選擇您的資料存取策略 {#data-access-strategy}

在設定資料來源之前，請先考慮哪個方法最適合您的使用案例。 有三種選項可供使用，每種選項在持續性、設定檔擴充及重複使用性方面都有不同的權衡。 如需這些選項的詳細討論，請參閱[Journey Optimizer中進階歷程的最佳實務](https://experienceleague.adobe.com/en/perspectives/best-practices-for-advanced-journeys-in-journey-optimizer){target="_blank"}。

**選項1 — 透過自訂動作（無資料湖）存取外部資料**

在歷程執行階段直接連線到外部API，而不將資料儲存在Experience Platform資料湖中。 最適合下列情況：

* 資料僅在歷程內容中才有用，其他地方並不需要。
* 可透過傳回所需屬性的API端點存取外部系統。

深入瞭解[自訂動作](../action/action.md)和[自訂動作回應](../action/action-response.md)。

**選項2 — 資料湖中的資料集，未針對設定檔**&#x200B;啟用

將資料擷取至資料集，以根據情境式事件資料觸發並個人化歷程，而不會對即時客戶個人檔案有所貢獻。 最適合下列情況：

* 記錄中包含可用於存取已儲存在Experience Platform中的設定檔的身分欄位。
* 在Journey Optimizer外部建立受眾或拼接身分時不需要資料。

**選項3 — 在資料湖**&#x200B;中啟用設定檔的資料集

將資料內嵌至啟用[設定檔的資料集](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"}中，以建立對象、豐富身分圖表，並跨多個歷程和RT-CDP目的地運用資料。 最適合下列情況：

* 此資料可用於Journey Optimizer以外的管道中使用的受眾定義。
* 資料包含多個身分，這些身分有助於提供更豐富的拼接設定檔片段。

| | 資料持續存在資料湖中 | 為設定檔啟用的資料集 |
| --- | --- | --- |
| **選項1** — 透過自訂動作的外部資料 | 無 | 無 |
| **選項2** — 未針對設定檔啟用資料集 | 是 | 無 |
| **選項3** — 啟用設定檔的資料集 | 是 | 是 |

如需如何設定 Adobe Experience Platform 資料來源和外部資料來源，以及如何在歷程中尋找和使用資料的詳細資訊，請觀看此[教學課程影片](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target="_blank"}。

## 作法影片 {#video}

了解資料來源為何，以及如何設定 Experience Platform 和外部資料來源。

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

