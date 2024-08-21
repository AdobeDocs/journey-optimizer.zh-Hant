---
solution: Journey Optimizer
product: journey optimizer
title: 頻道報告
description: 開始使用頻道報告
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 247b966d-4f84-453b-8178-9c9ebcd494ef
source-git-commit: 428e08ca712724cb0b3453681bee1c7e86ce49dc
workflow-type: tm+mt
source-wordcount: '640'
ht-degree: 3%

---

# 開始使用頻道報告 {#channel-report-gs}

>[!AVAILABILITY]
>
>目前的報告體驗將於10月發行後淘汰。 在此日期之後，新的報告體驗將成為標準。 建議您熟悉新功能，以確保順利轉換。 [開始使用Journey Optimizer的新報告介面。](report-gs-cja.md)

管道報表是一個功能強大的工具，可針對每個管道將流量和參與量度的全面概觀納入統一報表中，包括所有行銷活動和歷程的所有動作。 它分為不同的Widget，每個都提供行銷活動或歷程績效的特定檢視。

管道報表是完全可自訂的，因此您可以調整大小或移除Widget，以建立符合您特定需求的儀表板。 您也可以將報表資料匯出至PDF或CSV檔案，以供進一步分析。

在此[頁面](channel-report.md)中瞭解管道報表可用的不同量度和Widget。

## 開始之前 {#manage-reports-prereq}

開始之前，請檢查您是否有許可權存取&#x200B;**[!UICONTROL 報表]**&#x200B;功能表。

如果您看不到&#x200B;**[!UICONTROL 報表]**&#x200B;功能表，必須擴充您的存取許可權以包含&#x200B;**[!UICONTROL 檢視管道報表]**&#x200B;許可權。 如果您擁有貴組織的Adobe Experience Platform [許可權](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=zh-Hant){target="_blank"}存取權，您可以擴充自己的許可權。 如果沒有，請連絡您的Adobe Journey Optimizer管理員。

+++瞭解如何指派報表許可權

請注意，此許可權包含在下列內建&#x200B;**[!UICONTROL 角色]**&#x200B;中：行銷活動管理員、行銷活動核准者、行銷活動檢視者以及行銷活動管理員。

若要指派對應許可權給您的&#x200B;**[!UICONTROL 角色]**：

1. 從[!DNL Permissions]產品，瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;功能表，並選取您要以新&#x200B;**[!UICONTROL 檢視管道報表]**&#x200B;許可權更新的角色。

1. 從您的&#x200B;**[!UICONTROL 角色]**&#x200B;儀表板，按一下&#x200B;**[!UICONTROL 編輯]**。

   ![](assets/channel_permission_1.png)

1. 拖放&#x200B;**[!UICONTROL 報表]**&#x200B;資源以指派許可權。

   從&#x200B;**[!UICONTROL 報表]**&#x200B;資源下拉式清單中，選取&#x200B;**[!UICONTROL 檢視管道報表]**&#x200B;許可權。

   ![](assets/channel_permission_2.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

指派給此&#x200B;**[!UICONTROL 角色]**&#x200B;的使用者現在可以存取&#x200B;**[!UICONTROL 報表]**&#x200B;功能表。

+++

## 管理您的報告儀表板 {#manage-reports}

若要存取及管理您的管道報表，請遵循下列步驟：

1. 導覽至&#x200B;**[!UICONTROL 歷程管理]**&#x200B;區段內的&#x200B;**[!UICONTROL 報表]**&#x200B;功能表。

   ![](assets/channel_report_1.png)

1. 從您的儀表板，選擇&#x200B;**開始**&#x200B;和&#x200B;**[!UICONTROL 結束時間]**&#x200B;以鎖定特定資料。

1. 從&#x200B;]**的**[!UICONTROL &#x200B;動作下拉式清單中，選取您要鎖定促銷活動、歷程或兩者。

   ![](assets/channel_report_2.png)

1. 按一下&#x200B;**[!UICONTROL 修改]**&#x200B;以調整大小或移除Widget，建立符合您特定需求的儀表板。

   ![](assets/channel_report_3.png)

1. 在您滿意顯示順序和Widget的大小後，請按一下&#x200B;**[!UICONTROL 儲存]**。

1. 視Widget而定，您可以選擇從表格、長條圖或環形圖切換。

1. 按一下百分比圖示，將您的資料顯示為費率。

   ![](assets/channel_report_4.png)

## 匯出您的報告 {#export-reports}

您可以輕鬆地將不同的報表匯出為PDF或CSV格式，讓您能夠共用、操縱或列印它們。 匯出管道報表的詳細步驟可在下列標籤中取得：

>[!BEGINTABS]

>[!TAB 將報表匯出為PDF檔案]

1. 在報表中按一下[匯出]，然後選取[PDF檔案]。********

1. 在「列印」視窗中，視需要設定檔案。 請注意，選項可能會依您的瀏覽器而有所不同。

1. 選擇列印或儲存報表為PDF。

1. 找到您要儲存檔案的資料夾，視需要重新命名，然後按一下「儲存」。

您的報告現在可以在pdf檔案中檢視或共用。

>[!TAB 將報表匯出為CSV檔案]

1. 從您的報表按一下[匯出]****，然後選取[CSV檔案]****&#x200B;來產生整體報表層級的CSV檔案。

1. 您也可以選擇從特定Widget匯出資料。 按一下所選Widget旁的&#x200B;**[!UICONTROL 將Widget資料匯出至CSV]**。

1. 您的檔案會自動下載，並位於您的本機檔案中。

   如果在報表層級產生檔案，檔案會包含每個Widget的詳細資訊，包括其標題和資料。

   如果您在Widget層級產生檔案，它會特別提供所選Widget的資料。

>[!ENDTABS]
