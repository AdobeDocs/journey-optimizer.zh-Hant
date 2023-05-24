---
solution: Journey Optimizer
product: journey optimizer
title: 建立您的第一個組合工作流程
description: 瞭解如何建立合成工作流以組合和安排現有受眾。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
badge: label="Beta" type="Informative"
source-git-commit: 818c3ff2d159ec3a668c55224996b4736f950e5d
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 14%

---

# 建立您的第一個組合工作流程 {#create-compositions}

>[!BEGINSHADEBOX]

本文件提供下列內容：

* [開始使用對象組合](get-started-audience-orchestration.md)
* **[建立您的第一個組合工作流程](create-compositions.md)**
* [使用組合畫布](composition-canvas.md)
* [存取及管理對象](access-audiences.md)

>[!ENDSHADEBOX]

## 建立合成工作流 {#create}

要建立合成工作流，請執行以下步驟：

1. 訪問 **[!UICONTROL 段]** 的 **[!UICONTROL 建立受眾]**。

1. 選擇 **[!UICONTROL 撰寫受眾]**。

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >的 **[!UICONTROL 生成規則]** 建立方法允許您使用 [分段服務](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html)。

1. 合成畫布顯示有兩個預設活動：

   * **[!UICONTROL 觀眾]**:你作文的起點。 此活動允許您選擇一個或多個受眾作為工作流的基礎，

   * **[!UICONTROL 保存]**:最後一步。 此活動允許您將工作流的結果保存到新的受眾中。
   有關如何在合成工作流畫布中配置活動的詳細資訊，請參閱 [使用合成畫布](composition-canvas.md)。

1. 開啟合成屬性以指定標題和說明。

   如果屬性中未定義標題，則合成的標籤將設定為「合成」，然後是其建立日期和時間。

   ![](assets/audiences-properties.png)

1. 通過根據需要在 **[!UICONTROL 觀眾]** 和 **[!UICONTROL 保存]** 活動。 [瞭解如何使用合成畫布](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. 在您的作品準備好後，按一下 **[!UICONTROL 發佈]** 按鈕，可以發佈作文並將生成的觀眾保存到Adobe Experience Platform。

   >[!IMPORTANT]
   >
   >在給定沙盒中，最多可發佈75種作品。 如果已達到此閾值，則需要刪除合成以釋放空間並發佈新合成。

   如果發佈期間發生任何錯誤，則將顯示警報，其中包含有關如何解決問題的資訊。

   ![](assets/audiences-alerts.png)

1. 該作文已發佈。 由此產生的受眾被保存到Adobe Experience Platform，並準備成為Journey Optimizer運動的目標。 [了解如何使行銷活動](../campaigns/get-started-with-campaigns.md)

## 存取組合物 {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="發佈您的對象"
>abstract="發佈您的組合以將產生的對象儲存到 Adobe Experience Platform 中。"

可從 **[!UICONTROL 組合物]** 頁籤。 它們可以具有多個狀態：

* **[!UICONTROL 草稿]**:該組合正在進行中，尚未發佈。
* **[!UICONTROL 已發佈]**:已發佈作文，因此已保存並可供使用。
* **[!UICONTROL 存檔]**:作品已存檔。

![](assets/audiences-compositions.png)

>[!NOTE]
>
>您可以隨時使用清單中的省略號按鈕複製或刪除現有合成。
