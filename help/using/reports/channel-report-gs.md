---
solution: Journey Optimizer
product: journey optimizer
title: 管道報表
description: 開始使用管道報告
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: e812621c0b365e07432f6b517a012cf59c37f01f
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 1%

---

# 開始使用管道報告 {#channel-report-gs}

管道報表是一個功能強大的工具，可針對每個管道將流量和參與量度的全面概觀納入統一報表中，包括所有行銷活動和歷程的所有動作。 它分為不同的Widget，每個都提供行銷活動或歷程績效的特定檢視。

管道報表是完全可自訂的，因此您可以調整大小或移除Widget，以建立符合您特定需求的儀表板。 您也可以將報表資料匯出至PDF或CSV檔案，以供進一步分析。

瞭解更多適用於此管道報表的不同量度和Widget [頁面](channel-report.md).

## 開始之前 {#manage-reports-prereq}

開始之前，請檢查您是否有許可權存取 **[!UICONTROL 報表]** 功能表。

如果您看不到 **[!UICONTROL 報表]** 功能表，您的存取權必須擴充，以包含 **[!UICONTROL 檢視管道報表]** 許可權。 如果您有Adobe Experience Platform的存取權，可以擴充您自己的許可權 [許可權](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant){target="_blank"} 為您的組織所用。 如果沒有，請連絡您的Adobe Journey Optimizer管理員。

+++瞭解如何指派報表許可權

請注意，此許可權包含在下列內建中 **[!UICONTROL 角色]**：促銷活動管理員、促銷活動核准者、促銷活動檢視者和促銷活動管理員。

若要將對應許可權指派給您的 **[!UICONTROL 角色]**：

1. 從 [!DNL Permissions] 產品，導覽至 **[!UICONTROL 角色]** 功能表，並選取您要使用新設定的角色 **[!UICONTROL 檢視管道報表]** 許可權。

1. 從您的 **[!UICONTROL 角色]** 儀表板，按一下 **[!UICONTROL 編輯]**.

   ![](assets/channel_permission_1.png)

1. 拖放 **[!UICONTROL 報告]** 指派許可權的資源。

   從 **[!UICONTROL 報告]** resource下拉式清單，選取 **[!UICONTROL 檢視管道報表]** 許可權。

   ![](assets/channel_permission_2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

指派給此的使用者 **[!UICONTROL 角色]** 現在可以存取 **[!UICONTROL 報表]** 功能表。

+++

## 管理您的報告儀表板 {#manage-reports}

若要存取及管理您的管道報表，請遵循下列步驟：

1. 導覽至 **[!UICONTROL 報表]** 功能表中的 **[!UICONTROL 歷程管理]** 區段。

   ![](assets/channel_report_1.png)

1. 從您的控制面板中，選擇 **開始** 和 **[!UICONTROL 結束時間]** 以鎖定特定資料。

1. 從 **[!UICONTROL 動作來源]** 下拉式清單，選取您要鎖定促銷活動、歷程或兩者。

   ![](assets/channel_report_2.png)

1. 按一下 **[!UICONTROL 修改]** 調整或移除Widget以建立符合您特定需求的儀表板。

   ![](assets/channel_report_3.png)

1. 在您滿意顯示順序和Widget的大小後，請按一下 **[!UICONTROL 儲存]**.

1. 視Widget而定，您可以選擇從表格、長條圖或環形圖切換。

1. 按一下百分比圖示，將您的資料顯示為費率。

   ![](assets/channel_report_4.png)

## 匯出您的報告 {#export-reports}

您可以輕鬆地將不同的報表匯出為PDF或CSV格式，讓您能夠共用、操縱或列印它們。 匯出管道報表的詳細步驟可在下列標籤中取得：

>[!BEGINTABS]

>[!TAB 將報表匯出為PDF檔案]

1. 在報表中，按一下 **[!UICONTROL 匯出]** 並選取 **[!UICONTROL PDF檔案]**.

1. 在「列印」視窗中，視需要設定檔案。 請注意，選項可能會依您的瀏覽器而有所不同。

1. 選擇列印或儲存報表為PDF。

1. 找到您要儲存檔案的資料夾，視需要重新命名，然後按一下「儲存」。

您的報告現在可以在pdf檔案中檢視或共用。

>[!TAB 將報表匯出為CSV檔案]

1. 在報表中，按一下 **[!UICONTROL 匯出]** 並選取 **[!UICONTROL CSV檔案]** 在整體報表層級產生CSV檔案。

1. 您也可以選擇從特定Widget匯出資料。 按一下 **[!UICONTROL 將Widget資料匯出至CSV]** 位於選取的Widget旁。

1. 您的檔案會自動下載，並位於您的本機檔案中。

   如果在報表層級產生檔案，檔案會包含每個Widget的詳細資訊，包括其標題和資料。

   如果您在Widget層級產生檔案，它會特別提供所選Widget的資料。

>[!ENDTABS]
