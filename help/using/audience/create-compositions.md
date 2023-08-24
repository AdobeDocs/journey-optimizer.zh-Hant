---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個組合工作流程
description: 瞭解如何建立組合工作流程，以組合和排列現有對象。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 48a0fb11c141d847fae444909a7e6080e4a4935a
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 17%

---

# 建立您的第一個組合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

此文件提供如何在 Adobe Journey Optimizer 中使用對象構成的詳細資訊。 如果您未使用 Adobe Journey Optimizer， [請按一下這裡](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=zh-Hant){target="_blank"}。

>[!ENDSHADEBOX]

## 建立構成工作流程 {#create}

若要建立構成工作流程，請遵循下列步驟：

1. 存取 **[!UICONTROL 受眾]** 功能表並選取 **[!UICONTROL 建立對象]**.

1. 選取 **[!UICONTROL 撰寫對象]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 建置規則]** 建立方法可讓您使用建立新的區段定義。 [分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant).

1. 構成畫布會顯示兩個預設活動：

   * **[!UICONTROL 對象]**：構成起點。 此活動可讓您選取一或多個對象作為工作流程的基礎。

   * **[!UICONTROL 儲存]**：構成的最後一步。 此活動可讓您將工作流程的結果儲存至新受眾。

   如需有關如何在構成工作流程畫布中設定活動的詳細資訊，請參閱 [使用構成畫布](composition-canvas.md).

1. 開啟構成屬性以指定標題和說明。

   如果屬性中未定義標題，構成標籤會設為「構成」，接著是建立日期和時間。

   ![](assets/audiences-properties.png)

1. 視需要在「 」之間新增任意數量的活動，以設定構成 **[!UICONTROL 對象]** 和 **[!UICONTROL 儲存]** 活動。 [瞭解如何使用構成畫布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 構成準備就緒後，按一下 **[!UICONTROL 發佈]** 按鈕來發佈構成，並將產生的對象儲存到Adobe Experience Platform中。

   >[!IMPORTANT]
   >
   >您可以在指定的沙箱中發佈最多10個組合。 如果您達到此臨界值，則需要刪除構成以釋放空間並發佈新構成。

   如果在發佈期間發生任何錯誤，將顯示警報，其中包含如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 組合已發佈。 產生的受眾會儲存至Adobe Experience Platform中，並準備好在Journey Optimizer行銷活動中成為目標。 [了解如何使行銷活動](../campaigns/get-started-with-campaigns.md)

## 存取組合 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="發佈您的對象"
>abstract="發佈您的組合以將產生的對象儲存到 Adobe Experience Platform 中。"

所有已建立的構成都可從以下位置存取： **[!UICONTROL 組合]** 標籤。 它們可以有多個狀態：

* **[!UICONTROL 草稿]**：構成正在進行中，尚未發佈。
* **[!UICONTROL 已發佈]**：構成已發佈，產生的對象已儲存並可供使用。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以使用清單中的省略符號按鈕，隨時複製或刪除現有的構成。
