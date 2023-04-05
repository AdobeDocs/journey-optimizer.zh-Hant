---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個合成工作流程
description: 了解如何建立構圖工作流程，以結合和排列現有對象。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informity"
source-git-commit: 242fd8dbb04d62b9ec838655985add4ea0d7b377
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 7%

---

# 建立您的第一個合成工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

本檔案提供下列內容：

* [開始使用對象組合](get-started-audience-orchestration.md)
* **[建立您的第一個合成工作流程](create-compositions.md)**
* [使用組合畫布](composition-canvas.md)
* [存取及管理對象](access-audiences.md)

>[!ENDSHADEBOX]

## 建立合成工作流程 {#create}

要建立合成工作流，請執行以下步驟：

1. 存取 **[!UICONTROL 區段]** 選取 **[!UICONTROL 建立對象]**.

1. 選擇 **[!UICONTROL 撰寫對象]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >此 **[!UICONTROL 建置規則]** 建立方法可讓您使用 [區段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html).

1. 合成畫布會顯示兩個預設活動：

   * **[!UICONTROL 對象]**:構圖的起點。 此活動可讓您選取一或多個對象，作為工作流程的基礎，

   * **[!UICONTROL 儲存]**:作品的最後一步。 此活動可讓您將工作流程的結果儲存至新對象。
   有關如何在合成工作流程畫布中配置活動的詳細資訊，請參閱 [使用合成畫布](composition-canvas.md).

1. 開啟合成屬性以指定標題和說明。

   如果屬性中未定義標題，則合成的標籤將設定為「合成」，隨後將設定其建立日期和時間。

   ![](assets/audiences-properties.png)

1. 視需要在 **[!UICONTROL 對象]** 和 **[!UICONTROL 儲存]** 活動。 [了解如何使用構圖畫布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 當您的構圖準備就緒後，按一下 **[!UICONTROL 發佈]** 按鈕來發佈構圖，並將產生的對象儲存至Adobe Experience Platform。

   如果發佈期間發生任何錯誤，則會顯示警報，其中包含如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 作文已發佈。 產生的對象會儲存至Adobe Experience Platform中，且已準備好在Journey Optimizer行銷活動中定位。 [了解如何使用行銷活動](../campaigns/get-started-with-campaigns.md)

## 存取組合物 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="發佈您的對象"
>abstract="發佈您的組合以將產生的對象儲存到 Adobe Experience Platform 中。"

所有建立的組合皆可從 **[!UICONTROL 組合物]** 標籤。 它們可以有多種狀態：

* **[!UICONTROL 草稿]**:該構成正在進行中，尚未公佈。
* **[!UICONTROL 已發佈]**:合成內容已發佈，因此已儲存對象並可供使用。
* **[!UICONTROL 已封存]**:已封存了構成。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以隨時使用清單中的刪節號按鈕複製或刪除現有的合成內容。
