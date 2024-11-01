---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個組合工作流程
description: 瞭解如何建立組合工作流程，以組合和排列現有對象。
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 01c14590fe55d8f11c1ff2b18141933b0b3dd5ca
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 16%

---

# 建立您的第一個組合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

此文件提供如何在 Adobe Journey Optimizer 中使用客群構成的詳細資訊。 如果您沒有使用Adobe Journey Optimizer，[請按一下這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hant){target="_blank"}。

>[!ENDSHADEBOX]

## 建立構成工作流程 {#create}

若要建立構成工作流程，請遵循下列步驟：

1. 存取&#x200B;**[!UICONTROL 對象]**&#x200B;功能表並選取&#x200B;**[!UICONTROL 建立對象]**。

1. 選取&#x200B;**[!UICONTROL 撰寫對象]**。

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >**[!UICONTROL 建置規則]**&#x200B;建立方法可讓您使用[分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant)來建立新的區段定義。

1. 構成畫布會顯示兩個預設活動：

   * **[!UICONTROL 對象]**：構成起點。 此活動可讓您選取一或多個對象作為工作流程的基礎。

   * **[!UICONTROL 儲存]**：構成的最後一個步驟。 此活動可讓您將工作流程的結果儲存至新受眾。

   如需如何在構成工作流程畫布中設定活動的詳細資訊，請參閱[使用構成畫布](composition-canvas.md)。

1. 開啟構成屬性以指定標題和說明。

   如果屬性中未定義標題，構成標籤會設為「構成」，接著是建立日期和時間。

   ![](assets/audiences-properties.png)

1. 在&#x200B;**[!UICONTROL 對象]**&#x200B;和&#x200B;**[!UICONTROL 儲存]**&#x200B;活動之間新增所需數量的活動，以設定您的組合。 [瞭解如何使用構成畫布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 一旦您的構成準備就緒，請按一下&#x200B;**[!UICONTROL Publish]**&#x200B;按鈕以發佈構成，並將產生的對象儲存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您可以在指定的沙箱中發佈最多10個組合。 如果您達到此臨界值，則需要刪除組合以釋放空間，才能發佈新的組合。

   如果在發佈期間發生任何錯誤，將顯示警報，其中包含如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 組合已發佈。 產生的對象會儲存至Adobe Experience Platform，並準備好在Journey Optimizer中鎖定目標。 [瞭解如何在Journey Optimizer中鎖定對象](../audience/about-audiences.md#segments-in-journey-optimizer)

## 存取組合 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="發佈您的客群"
>abstract="發佈您的組合以將產生的客群儲存到 Adobe Experience Platform 中。"

所有建立的構成都可以從&#x200B;**[!UICONTROL 構成]**&#x200B;索引標籤存取。 您可以使用清單中的省略符號按鈕，隨時複製或刪除現有的構成。

構成可以有多種狀態：

* **[!UICONTROL 草稿]**：構成正在進行中，尚未發佈。
* **[!UICONTROL 已發佈]**：構成已發佈，產生的對象已儲存並可使用。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>對象構成目前未與沙箱重設功能整合。 在起始沙箱重設之前，您需要手動刪除您的構圖，以確保適當的清理關聯的對象資料。 Adobe Experience Platform [沙箱檔案](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html#delete-audience-compositions)中有提供詳細資訊
