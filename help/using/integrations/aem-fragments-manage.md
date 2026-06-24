---
solution: Journey Optimizer
product: journey optimizer
title: AEM內容片段
description: 瞭解如何管理AEM內容片段
topic: Content Management
role: User
level: Beginner
source-git-commit: ce34eb885d85c6c0f81b477e155cb81547d53e03
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 管理您的Adobe Experience Manager內容片段 {#aem-fragments}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;從內容管理片段清單管理AEM內容片段，以監視狀態和中繼資料，檢視片段在歷程和行銷活動中的使用位置、從Experience Manager同步發佈的更新，以及在不離開Journey Optimizer的情況下開啟片段進行編輯。

>[!ENDSHADEBOX]

將Adobe Experience Manager as a Cloud Service或Managed Services與Adobe Journey Optimizer整合後，您便可在內容中使用AEM內容片段，且無需離開Journey Optimizer即可檢查片段狀態。

當您重新發佈已在歷程或行銷活動中使用的片段時，同步計時器會在片段在Adobe Experience Manager中&#x200B;**已發佈**&#x200B;之後開始。 對於單一歷程與行銷活動，更新內容通常會在約&#x200B;**5分鐘**&#x200B;內在Journey Optimizer中提供；對於批次傳送，變更會顯示在&#x200B;**下一個處理批次**&#x200B;中。 請參閱[使用Adobe Experience Manager內容片段](aem-fragments.md)。 如果發生延遲，您可以從Journey Optimizer手動同步該片段，以提取最新發佈的版本。

## 存取AEM內容片段 {#access-aem-fragments}

1. 從&#x200B;**[!UICONTROL 內容管理]**&#x200B;功能表，選取&#x200B;**[!UICONTROL 片段]**。

1. 開啟&#x200B;**[!UICONTROL AEM片段]**&#x200B;標籤以檢視Adobe Experience Manager中可用的內容片段。

1. 在片段清單中，按一下![進階功能表](assets/do-not-localize/Smock_FolderSearch_18_N.svg)以&#x200B;**[!UICONTROL 探索參考]**。

   ![](assets/fragment-list-1.png)

1. 選取片段以檢閱其狀態和可用動作：

   * **[!UICONTROL 探索引用]**：檢視使用片段的歷程、行銷活動、協調的行銷活動和範本。
   * **[!UICONTROL 在AEM中開啟]**：在Adobe Experience Manager中開啟片段以編輯或重新發佈。
   * **[!UICONTROL 同步]**：將最新發佈的版本從Adobe Experience Manager提取到Journey Optimizer中，例如，當重新發佈的內容未出現在通常的同步視窗之後。 如果控制項已停用，則片段已符合Experience Manager中的發佈版本。

     ![](assets/fragment-list-2.png)

1. **[!UICONTROL 詳細資料]**&#x200B;功能表可讓您檢閱中繼資料並預覽同步處理裝載：

   * **[!UICONTROL 名稱]**：從Adobe Experience Manager匯入的內容片段標題。
   * **[!UICONTROL 描述]**：描述已從Adobe Experience Manager匯入。
   * **[!UICONTROL 變數]**：目前已針對此片段呈現的已發佈變數。
   * **[!UICONTROL 存放庫ID]**： Adobe Experience Manager中片段的存放庫識別碼。
   * **[!UICONTROL AEM片段ID]**： Adobe Experience Manager中的唯一內容片段識別碼。
   * **[!UICONTROL 標籤]**：在Adobe Experience Manager中指派的標籤，包括Journey Optimizer啟用標籤，用於判斷片段是否出現在您組織和沙箱的選取器中。 [瞭解如何建立和指派標籤](aem-fragments.md#create-tag)
   * **[!UICONTROL JSON預覽]**： Journey Optimizer使用的片段內容之唯讀JSON結構。

1. 在&#x200B;**[!UICONTROL 探索參考]**&#x200B;中，使用標籤來檢視參考片段的歷程、行銷活動、協調的行銷活動和範本。

   ![](assets/fragment-list-3.png)

➡️ [進一步瞭解內容片段](aem-fragments.md)


