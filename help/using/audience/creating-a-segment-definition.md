---
solution: Journey Optimizer
product: journey optimizer
title: 建立區段定義
description: 瞭解如何透過區段定義建立對象
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 11%

---

# 建立區段定義 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="建立規則"
>abstract="建置規則建立方法可讓您使用 Adobe Experience Platform 對象分段服務建立新的對象定義。"

在此範例中，我們將建立受眾，以鎖定居住在亞特蘭大、舊金山或西雅圖且出生於1980年後的所有客戶。 所有這些客戶應在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買。

➡️ [透過此影片瞭解如何建立對象](#video-segment)

1. 存取 **[!UICONTROL 受眾]** 功能表，然後按一下 **[!UICONTROL 建立對象]** 按鈕。

   ![](assets/create-segment.png)

   區段定義畫面可讓您設定定義對象的所有必要欄位。 瞭解如何在中設定對象 [Segment Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html){target="_blank"}.

   ![](assets/segment-builder.png)

1. 在 **[!UICONTROL 對象屬性]** 窗格，提供對象的名稱和說明（選用）。

   ![](assets/segment-properties.png)

1. 將所需欄位從左窗格拖放至中央工作區，然後視需要加以設定。

   >[!NOTE]
   >
   >請注意，左窗格中可用的欄位會依以下方式而有所不同： **XDM個別設定檔** 和 **XDM ExperienceEvent** 已為貴組織設定結構描述。  進一步瞭解 [Experience Data Model (XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}.

   ![](assets/drag-fields.png)

   在此範例中，我們需要仰賴 **屬性** 和 **事件** 建立對象的欄位：

   * **屬性**：1980年後出生且生活在亞特蘭大、舊金山或西雅圖的設定檔

     ![](assets/add-attributes.png)

   * **事件**：在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買的使用者設定檔。

     ![](assets/add-events.png)

1. 當您在工作區中新增及設定新欄位時， **[!UICONTROL 對象屬性]** 窗格會自動更新屬於對象的預估設定檔資訊。

   ![](assets/segment-estimate.png)

1. 對象準備好後，按一下 **[!UICONTROL 儲存]**. 它會顯示在Adobe Experience Platform受眾清單中。 請注意，搜尋列可協助您搜尋清單中的特定對象。

對象現在可用於您的歷程。 如需詳細資訊，請參閱[本章節](../audience/about-audiences.md)。

## 操作說明影片{#video-segment}

瞭解如何建立對象。

>[!VIDEO](https://video.tv.adobe.com/v/334281?quality=12)
