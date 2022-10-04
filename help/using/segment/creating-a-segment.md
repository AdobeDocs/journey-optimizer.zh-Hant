---
title: 建立區段
description: 了解如何建立區段
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: a51b41ddbb562137dc1f6cf15160ce326cc0564a
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 5%

---

# 建立區段 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="建立規則"
>abstract="建置規則建立方法可讓您使用Adobe Experience Platform分段服務建立新的區段定義。"

在此範例中，我們將建立一個區段來鎖定居住在亞特蘭大、舊金山或西雅圖且在1980年後出生的所有客戶。 所有這些客戶應在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買。

➡️ [了解如何在此影片中建立區段](#video-segment)

1. 存取 **[!UICONTROL 區段]** ，然後按一下 **[!UICONTROL 建立區段]** 按鈕。

   ![](assets/create-segment.png)

   區段定義畫面可讓您設定所有必填欄位來定義區段。 了解如何在 [區段服務檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target=&quot;_blank&quot;}。

   ![](assets/segment-builder.png)

1. 在 **[!UICONTROL 區段屬性]** 窗格，請提供區段的名稱和說明（選用）。

   ![](assets/segment-properties.png)

1. 將需要的欄位從左窗格拖曳至中央工作區，然後根據您的需求進行設定。

   >[!NOTE]
   >
   >請注意，左窗格中可用的欄位會依 **XDM個別設定檔** 和 **XDM ExperienceEvent** 已為貴組織配置結構。  了解更多 [Experience Data Model(XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

   ![](assets/drag-fields.png)

   在此範例中，我們需要 **屬性** 和 **事件** 要建立區段的欄位：

   * **屬性**:1980年後出生在亞特蘭大、舊金山或西雅圖的個人檔案

      ![](assets/add-attributes.png)

   * **事件**:過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買的設定檔。

      ![](assets/add-events.png)

1. 當您新增和設定工作區中的新欄位時， **[!UICONTROL 區段屬性]** 窗格會自動更新，其中包含屬於區段之估計設定檔的資訊。

   ![](assets/segment-estimate.png)

1. 區段準備就緒後，按一下 **[!UICONTROL 儲存]**. 它會顯示在Adobe Experience Platform區段清單中。 請注意，搜尋列可協助您搜尋清單中的特定區段。

區段現在可用於您的歷程。 如需詳細資訊，請參閱[本章節](../segment/about-segments.md)。

## 作法影片{#video-segment}

了解如何建立區段。

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
