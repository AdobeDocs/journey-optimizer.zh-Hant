---
solution: Journey Optimizer
product: journey optimizer
title: 動態媒體
description: 搭配Journey Optimizer使用Dynamic Media
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: 3e777cc5-a935-4e68-9de7-60b241e78f63
source-git-commit: 3a10f8440515bd569f9def6d15ac74d57427c1cf
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 2%

---

# 使用 Dynamic Media 工作 {#aem-dynamic}

>[!AVAILABILITY]
>
>這項整合僅適用於使用Dynamic Media Manager as a Cloud Service的客戶。

「資產」選擇器現在支援Dynamic Media，讓您在Journey Optimizer中順暢地選取並使用核准的Dynamic Media轉譯。 對Adobe Experience Manager中的資產所做的變更會立即反映在您的Journey Optimizer內容中，以確保最新版本始終在使用中，而不需要手動更新。

若要深入瞭解Adobe Experience Manager as a Cloud Service中的Dynamic Media，請參閱[Experience Manager檔案](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/dynamicmedia/dynamic-media)。

## 新增及管理Dynamic Media

直接從Adobe Experience Manager as a Cloud Service將動態媒體插入您的Journey Optimizer內容，以針對任何熒幕或瀏覽器增強及最佳化您的內容。  然後您可以視需要調整大小、裁切、增強及進行其他調整。

1. 將&#x200B;**[!UICONTROL HTML元件]**&#x200B;拖放到您的內容中。

1. 選取&#x200B;**[!UICONTROL 顯示原始程式碼]**。

   ![](assets/dynamic-media-1.png)

1. 在&#x200B;**[!UICONTROL 編輯HTML]**&#x200B;功能表中，導覽至&#x200B;**[!UICONTROL Assets]**，然後按一下&#x200B;**[!UICONTROL 開啟資產選擇器]**。

   或者，您也可以複製並貼上資產的URL。

   ![](assets/dynamic-media-2.png)

1. 瀏覽您的AEM資產，並選取您要新增至內容的資產。

1. 視需要調整影像引數（例如高度、寬度、旋轉、翻轉、亮度、色相等），以符合您的資產需求。

   如需可新增至URL的影像引數完整清單，請參閱[Experience Manager檔案](https://experienceleague.adobe.com/en/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/c-command-reference)。

   ![](assets/dynamic-media-3.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

您的內容現在包含動態媒體。 您在Experience Manager中所做的任何更新都會自動顯示在Journey Optimizer中。

## 個人化您的文字覆蓋

使用您選擇的新文字取代現有的文字覆蓋圖，輕鬆自訂任何動態媒體，實現順暢的更新及個人化。

例如，使用實驗功能，您可以更新現有的文字覆蓋，方法為使用不同文字取代每個處理，以確保在開啟訊息時為每個設定檔自訂它。

![](assets/dynamic-media-layout-1.png)

1. 將&#x200B;**[!UICONTROL HTML元件]**&#x200B;拖放到您的內容中。

1. 選取&#x200B;**[!UICONTROL 顯示原始程式碼]**。

1. 從&#x200B;**[!UICONTROL 編輯HTML]**&#x200B;功能表，存取&#x200B;**[!UICONTROL Assets]**，然後&#x200B;**[!UICONTROL 開啟資產選擇器]**。

   您也可以直接複製並貼上資產URL。

1. 瀏覽您的AEM資產，並選取您要新增至內容的資產。

1. 將覆蓋圖取代為所需文字。

   ![](assets/do-not-localize/dynamic_media_layout.gif)

1. 更新影像引數：

   * **Layer**：輸入放置文字的基元素。
   * **大小**：更新文字區塊的大小。
   * **TextAttr**：調整文字字型的大小。
   * **Pos**：設定文字在影像中的位置。

   >[!WARNING]
   >
   >更新動態媒體需要Layer引數。

   ![](assets/dynamic-media-layout-2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

您的內容現在包含更新的文字覆蓋。

![](assets/dynamic-media-layout-3.png)

<!--
## Personalization with Text Overlay

Easily customize any dynamic media by replacing the existing text overlay with new text of your choice, allowing for seamless updates and personalization.

In this example, our goal is to update the existing text overlay by replacing it with a new validity date and adding a personalization block, ensuring it is customized for each profile when they open their messages.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Replace the overlay with the desired text.

    Here we change the validity date from 31st December 2024 to the 1st July 2025.

1. Add the required personalization fields to your image.

1. Click **[!UICONTROL Save]**.

Your content now includes your updated text overlay and personalization.

## Add Dynamic media conditional content

Enable conditional content in your dynamic media to better target your audience and deliver a more personalized experience.

1. Drag and drop an **[!UICONTROL HTML component]** into your content.

1. Select **[!UICONTROL Show the source code]**.

1. From the **[!UICONTROL Edit HTML]** menu, access **[!UICONTROL Assets]** then **[!UICONTROL Open asset selector]**.

    You can also simply copy and paste your assets URL.

1. Browse through your AEM assets and select the one you want to add to your content.

1. Once your dynamic media is inserted to your content, select **[!UICONTROL Enable conditional]** content from your HTML component toolbar to create your different user experiences. 

1. From the Variant - 1, click **[!UICONTROL Select condition]** to fine tune your audience.

1. Choose your condition or create a new one if needed and click **[!UICONTROL Select]**.

    [Learn more on conditions](../personalization/create-conditions.md)

1. Select your **[!UICONTROL Component]** and access the **[!UICONTROL Settings]** menu.

1. In the **[!UICONTROL Custom Attributes]** menu, populate the Dynamic Media text and personalization fields to customize the content for your audience.

-->
