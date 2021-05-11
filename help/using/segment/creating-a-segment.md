---
title: 建立區段
description: 瞭解如何建立細分
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 5%

---

# 建立區段 {#build-segments}

![](../assets/do-not-localize/badge.png)

在此範例中，我們將建立一個區段，以定位所有居住在亞特蘭大、舊金山或西雅圖且出生於1980年以後的客戶。 所有這些客戶都應該在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內完成購買。

1. 訪問&#x200B;**[!UICONTROL Segments]**&#x200B;菜單，然後按一下&#x200B;**[!UICONTROL Create segment]**&#x200B;按鈕。

   ![](../assets/create-segment.png)

   區段定義螢幕可讓您設定所有必要欄位，以定義區段。 瞭解如何在[區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)中設定區段。

   ![](../assets/segment-builder.png)

1. 在&#x200B;**[!UICONTROL Segment properties]**&#x200B;窗格中，提供區段的名稱和說明（選用）。

   ![](../assets/segment-properties.png)

1. 將所需欄位從左窗格拖放至中心工作區，然後根據您的需求進行設定。

   >[!NOTE]
   >
   >請注意，左窗格中的可用欄位會依組織的&#x200B;**XDM個別設定檔**&#x200B;和&#x200B;**XDM ExperienceEvent**&#x200B;結構設定而有所不同。  進一步瞭解[體驗資料模型(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant)。

   ![](../assets/drag-fields.png)

   在此範例中，我們需要仰賴&#x200B;**屬性**&#x200B;和&#x200B;**事件**&#x200B;欄位來建立區段：

   * **屬性**:1980年後出生在亞特蘭大、舊金山或西雅圖的個人檔案，
   * **事件**:描述檔，這些描述檔會在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內進行購買。

      ![](../assets/add-attributes.png)

      ![](../assets/add-events.png)

1. 當您在工作區中新增和設定新欄位時，**[!UICONTROL Segment Properties]**&#x200B;窗格會自動更新為區段的估計描述檔資訊。

   ![](../assets/segment-estimate.png)

1. 區段準備就緒後，按一下&#x200B;**[!UICONTROL Save]**。 它會顯示在Adobe Experience Platform區段清單中。 請注意，搜尋列可協助您搜尋清單中的特定區段。

此區段現在可用於您的歷程中。 如需詳細資訊，請參閱[本章節](../segment/about-segments.md)。
