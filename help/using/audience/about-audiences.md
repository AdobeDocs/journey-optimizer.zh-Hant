---
solution: Journey Optimizer
product: journey optimizer
title: 關於 Adobe Experience Platform 客群
description: 了解如何使用 Adobe Experience Platform 客群
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: be05bb72ace2e2084675f4278501a520d592e304
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 17%

---


# 開始使用 Audiences {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="客群"
>abstract="透過使用即時客戶輪廓資料，Adobe Experience Platform 能讓您輕鬆建置區段定義，以建立能夠擷取客戶獨特行為與偏好的目標的客群。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="選取行銷活動的對象"
>abstract="此清單顯示所有可用的 Adobe Experience Platform 對象。為你的行銷活動選取目標對象。在行銷活動中設定的訊息將傳送給屬於所選對象的所有個人。[了解更多關於客群](../audience/about-audiences.md)"

對象是具有相同類似行為和/或特徵的人集合。 透過Adobe Experience Platform Segmentation Service，這些功能可在Adobe Experience Platform上集中設定和維護，並可在Journey Optimizer中輕鬆存取，以便在您的歷程和行銷活動中啟用。

Adobe Journey Optimizer提供強大的工具，用於建立、管理和豐富受眾，以強化行銷工作。 在與Adobe Real-Time Customer Data Platform結合時，Journey Optimizer可讓您針對更複雜的細分細分細分細分細分細分對象，並與其他Adobe Experience Cloud解決方案雙向共用對象。

As real-time data streams or batch uploads occur, datasets update, and Journey Optimizer dynamically moves individuals in and out of audiences and journeys in real time.

>[!BEGINSHADEBOX]

本檔案提供如何在[!DNL Adobe Journey Optimizer]內使用對象的資訊。 有關對象入口網站和對象的詳細資訊，請參閱Adobe Experience Platform細分服務檔案。 如需詳細資訊，請參閱以下章節：

* [Segmentation Service UI指南](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/ui/overview){target="_blank"}

* [分段服務 — 常見問題](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/faq){target="_blank"}

>[!ENDSHADEBOX]

## 瀏覽客群 {#browse}

可從&#x200B;**[!UICONTROL 客戶]** > **[!UICONTROL 對象]**&#x200B;功能表取得對象。

控制面板以視覺化方式顯示重要受眾之間的重疊，並支援探索有價值的受眾趨勢。 例如，指定時段內的對象人數變化或對象突然激增，可能會醒目顯示導致對象縮小或增大的事件或動作，例如成功的選件。

![](assets/audiences-overview.png)

從受眾入口網站，您可以透過標準標籤、治理控制、可搜尋資料夾和標籤輕鬆管理、尋找和探索受眾。

For more information on how to work with audiences in the Audience Portal, refer to the [Adobe Experience Platform Segmentation Service documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hant){target="_blank"}.

## Audiences types {#types}

Audiences can be generated using different methods:

* **區段定義**：使用Adobe Experience Platform Segmentation Service建立新的對象定義。 對象是從區段定義產生，並會根據其評估型別在不同時間重新整理：

   * 串流區段：隨著新資料流入，對象會即時更新，以確保根據使用者活動保持持續相關性。
   * 批次細分：對象每24小時重新整理一次，以固定間隔擷取設定檔快照。 在歷程中使用時，新限定的區段成員要等到下次快照時才會出現。 [進一步瞭解時間](../building-journeys/audience-qualification-events.md#timing-segment-membership)。
   * Edge區段：對象會在邊緣即時評估，以便即時個人化。

  [瞭解如何建立區段定義](creating-a-segment-definition.md)

* **自訂上傳**：使用CSV檔案匯入對象。 [Learn how to create Custom Upload audiences](custom-upload.md)

* **Audience composition**: Create a composition workflow to combine existing audiences into a visual canvas and apply actions such as rank, split, join to create new audiences. [Learn how to work with audience composition](get-started-audience-orchestration.md)

* **Federated Audience Composition**: Federate datasets directly from your existing data warehouse to build and enrich Adobe Experience Platform audiences and attributes all in one system. [Learn how to work with Federated Audience Composition](federated-audience-composition.md).

## 在歷程和行銷活動中鎖定對象 {#target-audiences}

一旦您的對象準備就緒後，您就可以在建立歷程或建立行銷活動時選取他們，讓您透過相關訊息在適當的時間聯絡適當的人。 [進一步瞭解Journey Optimizer中的Audience Activation](target-audiences.md)。

## 作法影片 {#video}

了解 Journey Optimizer 的統一客戶輪廓及客群。

>[!VIDEO](https://video.tv.adobe.com/v/3432671?quality=12)
