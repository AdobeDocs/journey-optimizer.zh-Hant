---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用客群組合
description: 深入了解客群組合
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 435898d7e806e93ee0154c3da22f6a011fc78175
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 28%

---

# 開始使用客群組合 {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="建立構成"
>abstract="建立構成工作流程，以將現有的 Adobe Experience Platform 客群合併到視覺化畫布中，並利用各種活動 (分割、排除…) 建立新的客群。"

>[!BEGINSHADEBOX]

此文件提供如何在 Adobe Journey Optimizer 中使用客群構成的詳細資訊。 如果您是只使用即時客戶輪廓的客戶，且不使用 Adobe Journey Optimizer， 請[按一下這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hant){target="_blank"}。

>[!ENDSHADEBOX]

對象構成可讓您建立&#x200B;**構成工作流程**，您可以在其中將現有Adobe Experience Platform對象結合到視覺畫布中，並利用各種活動（分割、排除……）來建立新對象。

完成後，**產生的對象**會連同現有對象一起儲存到Adobe Experience Platform中，並可在Journey Optimizer行銷活動和歷程中運用於鎖定客戶。 瞭解如何在Journey Optimizer中鎖定對象
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>受眾構成中的受眾和屬性目前無法用於Healthcare Shield或Privacy and Security Shield。
>
>擴充屬性尚未與原則執行服務整合。 因此，您套用至擴充屬性的任何資料使用標籤，都不會在Journey Optimizer行銷活動或歷程中強制執行。

可從 Adobe Journey Optimizer **[!UICONTROL 客群]**&#x200B;選單存取客群構成：

![](assets/audiences-browse.png)

* 此&#x200B;**[!UICONTROL 概觀]**&#x200B;標籤提供與貴組織的客群資料相關的關鍵量度專用儀表板。 若要深入了解，請參閱 [Adobe Experience Platform 儀表板指南](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=zh-Hant)。

* 此&#x200B;**[!UICONTROL 瀏覽]**&#x200B;索引標籤會列出儲存至 Adobe Experience Platform 的所有現有客群。

* 此&#x200B;**[!UICONTROL 組合]**&#x200B;索引標籤可讓您建立組合工作流程，在其中結合並排列客群以建立新客群。

## 建立構成工作流程 {#create}

若要建立構成工作流程，請遵循下列步驟：

1. 存取&#x200B;**[!UICONTROL 對象]**&#x200B;功能表並選取&#x200B;**[!UICONTROL 建立對象]**。

1. 選取&#x200B;**[!UICONTROL 撰寫對象]**。

   ![](assets/audiences-create.png)

1. 構成畫布會顯示兩個預設活動：

   * **[!UICONTROL 對象]**：構成起點。 此活動可讓您選取一或多個對象作為工作流程的基礎。

   * **[!UICONTROL 儲存]**：構成的最後一個步驟。 此活動可讓您將工作流程的結果儲存至新受眾。

1. 開啟構成屬性以指定標題和說明。

   如果屬性中未定義標題，構成標籤會設為「構成」，接著是建立日期和時間。

   ![](assets/audiences-properties.png)

1. 在&#x200B;**[!UICONTROL 對象]**&#x200B;和&#x200B;**[!UICONTROL 儲存]**&#x200B;活動之間新增所需數量的活動，以設定您的組合。 如需如何建立組合的詳細資訊，請參閱[對象組合檔案](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition)。

   ![](assets/audiences-publish.png)

1. 一旦您的構成準備就緒，請按一下&#x200B;**[!UICONTROL Publish]**&#x200B;按鈕以發佈構成，並將產生的對象儲存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您可以在指定的沙箱中發佈最多10個組合。 如果您達到此臨界值，則需要刪除組合以釋放空間，才能發佈新的組合。

   如果在發佈期間發生任何錯誤，將顯示警報，其中包含如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 組合已發佈。 產生的對象會儲存至Adobe Experience Platform，並準備好在Journey Optimizer中鎖定目標。 [瞭解如何在Journey Optimizer中鎖定對象](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>來自&#x200B;**對象構成**&#x200B;的對象會每天執行，因此您可能需要等候最多24小時，才能在Journey Optimizer中使用它們。 對象構成對象中的豐富屬性與上次執行構成一樣新，過去最多可達24小時。

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
