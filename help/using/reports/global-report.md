---
solution: Journey Optimizer
product: journey optimizer
title: 全域報告
description: 瞭解如何使用全域報告中的資料
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 82b8c9032d6c377cb76acce4d5cc45afb0ddd6ba
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 1%

---

# 開始使用全域報告 {#global-report}

>[!NOTE]
>
> 如果使用查詢服務時若透過API進行自訂查詢，您的報告可能會有延遲。

使用 **[!UICONTROL 全域報告]** 測量選定時段內您的歷程與傳送的影響。

* 如果您想在歷程內容中定位歷程或傳遞，請從 **[!UICONTROL 歷程]** 選單，存取您的歷程，然後按一下 **[!UICONTROL 檢視報告]** 按鈕。 然後您可以找到歷程、電子郵件、簡訊和推播全域報告。

  ![](assets/report_journey.png)

* 如果您想要鎖定促銷活動，請從 **[!UICONTROL 行銷活動]** 選單，存取您的行銷活動，然後按一下 **[!UICONTROL 報表]** 按鈕。

  ![](assets/report_campaign.png)

* 如果您要從 **[!UICONTROL 即時報告]** 至 **[!UICONTROL 全域報告]** 針對您的傳遞，按一下 **[!UICONTROL 所有時間]** 從標籤切換器。

  ![](assets/report_5.png)

如需Adobe Journey Optimizer中可用每個量度的詳細清單，請參閱 [此頁面](#list-of-components-global)

## 自訂儀表板 {#modify-dashboard}

每個報告儀表板都可透過變更時段、調整大小或移除Widget來修改。 變更Widget只會影響目前使用者的儀表板。 其他使用者將看到自己的儀表板或預設設定的儀表板。

1. 在全域報表中，選取以特定資料為目標的「開始」和「結束」時間。

   ![](assets/report_modify_1.png)

1. 對於包含多個已設定的歷程報告 **[!UICONTROL 動作]**，選擇特定的 **[!UICONTROL 動作]** （從下拉式功能表）。

1. 如果您只想鎖定一或多個週期性訊息，請從 **[!UICONTROL 執行時間]** 下拉式清單。

   ![](assets/report_modify_12.png)

1. 選擇是否要使用切換列從報表中排除測試事件。 有關測試事件的詳細資訊，請參閱 [此頁面](../building-journeys/testing-the-journey.md).

   請注意 **[!UICONTROL 排除測試事件]** 選項僅適用於歷程報告。

   ![](assets/report_modify_2.png)

1. 按一下 **[!UICONTROL 修改]** 以開始自訂您的儀表板。

   ![](assets/report_modify_3.png)

1. 拖曳小工具的右下角，調整其大小。

   ![](assets/report_modify_4.png)

1. 按一下 **[!UICONTROL 移除]** 以移除您不需要的任何Widget。

   ![](assets/report_modify_5.png)

1. 在您滿意顯示順序和Widget的大小後，請按一下 **[!UICONTROL 儲存]**.

1. 若要自訂資料的顯示方式，您可以切換不同的視覺化選項，例如圖形、表格和環圈圖。

   ![](assets/report_modify_10.png)

您的儀表板現在已儲存。 您的不同變更將會重新套用，以供稍後使用您的即時報告。 如有需要，請使用 **[!UICONTROL 重設]** 還原預設Widget和Widget順序的選項。

## 匯出您的報告 {#export-reports}

您可以輕鬆地將不同的報表匯出為PDF或CSV格式，以便共用或列印它們。 匯出報告的步驟會在以下標籤中詳細說明。

➡️ [在影片中探索此功能](#video-csv)


>[!BEGINTABS]

>[!TAB 將報表匯出為CSV檔案]

1. 在報表中，按一下 **[!UICONTROL 匯出]** 並選取 **[!UICONTROL CSV檔案]** 在整體報表層級產生CSV檔案。

   ![](assets/export_1.png)

1. 您也可以選擇從特定Widget匯出資料。 按一下 **[!UICONTROL 將Widget資料匯出至CSV]** 位於選取的Widget旁。

   ![](assets/export_3.png)

1. 您的檔案會自動下載，並位於您的本機檔案中。

   如果在報表層級產生檔案，檔案會包含每個Widget的詳細資訊，包括其標題和資料。

   如果您在Widget層級產生檔案，它會特別提供所選Widget的資料。

>[!TAB 將報表匯出為PDF檔案]

1. 在報表中，按一下 **[!UICONTROL 匯出]** 並選取 **[!UICONTROL PDF檔案]**.

   ![](assets/export_2.png)

1. 在「列印」視窗中，視需要設定檔案。 請注意，選項可能會依您的瀏覽器而有所不同。

1. 選擇列印或儲存報表為PDF。

1. 找到您要儲存檔案的資料夾，視需要重新命名，然後按一下「儲存」。

您的報告現在可以在pdf檔案中檢視或共用。



>[!ENDTABS]


### 匯出報表（影片） {#video-csv}

透過下列作法影片，瞭解如何下載適用於報表和單一Widget的CSV報表。

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)

