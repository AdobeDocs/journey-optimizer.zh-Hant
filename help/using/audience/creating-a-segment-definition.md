---
solution: Journey Optimizer
product: journey optimizer
title: 建置區段定義
description: 瞭解如何透過區段定義建立對象
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 289aac5d-6cdb-411f-985e-3acef58050a8
source-git-commit: b9d70bf2b3e16638a03b59fd4036771ad959a631
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 16%

---

# 建置區段定義 {#build-segments}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_rule"
>title="建立規則"
>abstract="建置規則建立方法讓您可以使用 Adobe Experience Platform Segmentation Service 建立新的對象定義。"

在此範例中，我們將建立受眾，鎖定生活在亞特蘭大、舊金山或西雅圖且出生於1980年之後的所有客戶。 這些客戶應在過去7天內開啟Luma應用程式，然後在開啟應用程式後2小時內購買。

➡️[在此影片中瞭解如何建立對象](#video-segment)

1. 從&#x200B;**[!UICONTROL 對象]**&#x200B;功能表，按一下&#x200B;**[!UICONTROL 建立對象]**&#x200B;按鈕並選取&#x200B;**[!UICONTROL 建置規則]**。

   ![](assets/create-segment.png)

   區段定義畫面可讓您設定定義對象的所有必要欄位。 在[Segmentation Service檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant){target="_blank"}中瞭解如何設定對象。

   ![](assets/segment-builder.png)

1. 在&#x200B;**[!UICONTROL 對象屬性]**&#x200B;窗格中，提供對象的名稱和說明（選擇性）。

   ![](assets/segment-properties.png)

1. 將所需欄位從左窗格拖放至中央工作區，然後視需要加以設定。

   >[!NOTE]
   >
   >請注意，左窗格中可用的欄位會依貴組織已設定的&#x200B;**XDM Individual Profile**&#x200B;和&#x200B;**XDM ExperienceEvent**&#x200B;結構描述而有所不同。  在[Experience Data Model (XDM)檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解。

   ![](assets/drag-fields.png)

   在此範例中，我們需要依賴&#x200B;**屬性**&#x200B;和&#x200B;**事件**&#x200B;欄位來建置對象：

   * **屬性**：在1980年後出生的亞特蘭大、舊金山或西雅圖的設定檔

     ![](assets/add-attributes.png)

   * **事件**：在過去7天內開啟Luma應用程式的設定檔，然後在開啟應用程式後2小時內進行購買。

     ![](assets/add-events.png)

     >[!NOTE]
     >
     >Adobe建議不要對串流細分使用開啟和傳送事件。 請改用真正的使用者活動訊號，例如點選、購買或信標資料。 針對頻率或隱藏邏輯，請使用商業規則而非傳送事件。 [了解更多](about-audiences.md#open-and-send-event-guardrails)

1. 當您在工作區中新增及設定新欄位時，**[!UICONTROL 對象屬性]**&#x200B;窗格會自動更新，內含屬於該對象的預估設定檔資訊。

   ![](assets/segment-estimate.png)

1. 對象準備就緒後，按一下&#x200B;**[!UICONTROL 儲存]**。 它會顯示在Adobe Experience Platform對象清單中。 請注意，搜尋列可協助您搜尋清單中的特定對象。

對象現在可用於您的歷程。 如需詳細資訊，請參閱[本章節](../audience/about-audiences.md)。

## 操作說明影片{#video-segment}

了解 Journey Optimizer 如何使用規則產生對象，以及了解如何使用屬性、事件和現有對象來建立對象。

>[!VIDEO](https://video.tv.adobe.com/v/3425020?quality=12)
