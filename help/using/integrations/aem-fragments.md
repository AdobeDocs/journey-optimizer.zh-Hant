---
solution: Journey Optimizer
product: journey optimizer
title: AEM內容片段
description: 瞭解如何存取及管理AEM內容片段
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: d9f2dbd5433ec9a89b4ef5a6d1caf6ff81c90a81
workflow-type: tm+mt
source-wordcount: '662'
ht-degree: 0%

---

# 使用Adobe Experience Manager內容片段 {#aem-fragments}

Adobe Experience Manager與Journey Optimizer之間的整合會遵循以下資料流程：

1. **[建立和作者](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**：內容是在Adobe Experience Manager中建立並設定為內容片段。

1. **[標籤](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**：內容片段必須使用Journey Optimizer特定標籤(`ajo-enabled:{OrgId}/{SandboxName}`)標籤。

1. **[發佈](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**：內容片段已發佈至Adobe Experience Manager，可供Journey Optimizer使用。

1. **[存取](#aem-add)**： Journey Optimizer會即時從Adobe Experience Manager發佈執行個體擷取並顯示可用的內容片段。

1. **[整合](#aem-add)**：已選取內容片段並整合至行銷活動或歷程中。

在Adobe Experience Manager中發佈內容片段時，會傳送事件以更新Journey Optimizer端的內容。 如果更新成功，內容片段將在大約5分鐘內可用於單一歷程，以及用於批次使用案例的下一個處理批次。 在Journey Optimizer中提供更新後，最新發佈的內容就會用於所有適用的行銷活動和歷程。

## 在Experience Manager中建立及指派標籤

在Journey Optimizer中使用內容片段之前，您需要建立專門用於Journey Optimizer的標籤：

1. 存取您的&#x200B;**Experience Manager**&#x200B;環境。

1. 從&#x200B;**工具**&#x200B;功能表，選取&#x200B;**標籤**。

   ![](assets/do-not-localize/aem_tag_1.png)

1. 按一下&#x200B;**建立標籤**。

1. 確定ID遵循下列語法： `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`。

1. 按一下&#x200B;**建立**。

1. 定義您的內容片段模式(如[Experience Manager檔案](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"}中所詳述)，並指派您新建立的Journey Optimizer標籤。

此即時連線可確保您的內容永遠保持最新，但也意味著對已發佈片段的任何變更都會立即影響作用中的行銷活動和歷程。

您現在可以開始建立和設定內容片段，以便稍後在Journey Optimizer中使用。 進一步瞭解[Experience Manager檔案](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}。

## 新增Experience Manager內容片段 {#aem-add}

建立並個人化AEM內容片段後，您現在可以將其匯入您的Journey Optimizer行銷活動或歷程。

1. 建立您的[行銷活動](../campaigns/create-campaign.md)或[歷程](../building-journeys/journey-gs.md)。

1. 若要存取您的AEM內容片段，請按一下任何文字欄位中的![Personalization圖示](assets/do-not-localize/Smock_PersonalizationField_18_N.svg)，或透過HTML內容元件開啟原始程式碼。

   ![](assets/aem_campaign_2.png)

1. 從左窗格中的&#x200B;**[!UICONTROL AEM內容片段]**&#x200B;功能表，按一下&#x200B;**[!UICONTROL 開啟AEM CF選取器]**。

   ![](assets/aem_campaign_3.png)

1. 從可用的清單中選取&#x200B;**[!UICONTROL 內容片段]**，以匯入您的Journey Optimizer內容。

1. 按一下「**[!UICONTROL 顯示篩選器]**」以微調您的內容片段清單。

   依預設，內容片段篩選器預設為僅顯示核准的內容。

   ![](assets/aem_campaign_4.png)

1. 選取您的&#x200B;**[!UICONTROL 內容片段]**&#x200B;後，按一下&#x200B;**[!UICONTROL 選取]**&#x200B;以開啟。

   ![](assets/aem_campaign_5.png)

1. 按一下&#x200B;**[!UICONTROL 檢視片段]**&#x200B;以顯示您的片段資訊。 請注意，開啟&#x200B;**[!UICONTROL 片段資訊]**&#x200B;功能表會將編輯器置於唯讀模式。

   從右側選單中選取「**[!UICONTROL 預覽]**」，在Adobe Experience Manager中檢視您的片段。

   ![](assets/aem_campaign_7.png)

1. 按一下![更多動作圖示](assets/do-not-localize/Smock_MoreSmallList_18_N.svg)以存取片段的進階功能表：

   * **[!UICONTROL 交換片段]**
   * **[!UICONTROL 探索參考]**
   * 在AEM中&#x200B;**[!UICONTROL 開啟]**

   ![](assets/aem_campaign_8.png)

1. 從您的&#x200B;**[!UICONTROL 片段]**&#x200B;中選擇所需的欄位以新增至您的內容。
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. 若要啟用即時個人化，**[!UICONTROL 內容片段]**&#x200B;中使用的所有預留位置，必須由使用者明確宣告為片段協助程式標籤中的引數。 您可以使用下列方法，將這些預留位置對應至設定檔屬性、內容屬性、靜態字串或預先定義的變數：

   1. **設定檔或內容屬性對應**：將預留位置指派給設定檔或內容屬性，例如name = profile.person.name.firstName。

   1. **靜態字串對應**：將固定字串值放在雙引號中，例如名稱= &quot;John&quot;，以指派固定字串值。

   1. **變數對應**：參照同一HTML中先前宣告的變數，例如name = &#39;variableName&#39;。
在此情況下，請確保在新增片段ID之前使用以下語法宣告**_variableName_**：

      ```html
      {% let variableName = attribute name %} 
      ```

   在下列範例中，**_name_**&#x200B;預留位置對應至片段中的&#x200B;**_profile.person.name.firstName_**&#x200B;屬性。

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. 按一下&#x200B;**[!UICONTROL 「儲存」]**。您現在可以測試並檢查您的訊息內容，如[本節](../content-management/preview.md)所詳述。
執行測試並驗證內容後，您可以[傳送行銷活動](../campaigns/review-activate-campaign.md)或[發佈您的歷程](../building-journeys/publish-journey.md)給您的對象。

Adobe Experience Manager可讓您識別使用內容片段的Journey Optimizer行銷活動或歷程。 進一步瞭解[Adobe Experience Manager檔案](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references)。

