---
solution: Journey Optimizer
product: journey optimizer
title: 管理品牌
description: 瞭解如何建立和管理您的品牌指引
badge: label="Beta" type="Informative"
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: b1b7abbe-8600-4a8d-b0b5-0dbd49abc275
source-git-commit: 3646c67dd23bb786cf2486c5c43748197ba04f85
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 16%

---

# 建立並管理您的品牌 {#brands}

>[!CONTEXTUALHELP]
>id="ajo_brand_overview"
>title="開始使用品牌"
>abstract="建立並自訂您自己的品牌，以定義您獨特的視覺和口頭身分，同時更輕鬆地產生符合您品牌風格和聲音的內容。"

>[!CONTEXTUALHELP]
>id="ajo_brand_ai_menu"
>title="選取您的品牌"
>abstract="選擇您的品牌，以確保所有AI產生的內容都經過量身打造，符合您品牌的規格和指導方針。"

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="品牌一致性分數"
>abstract="您的品牌一致性分數會測量AI產生的內容遵守您品牌指引的程度，以確保色彩、字型、標誌、影像和寫作風格的一致性。"


>[!AVAILABILITY]
>
>此功能已發佈私人測試版。 未來版本將逐步開放所有客戶使用。

品牌指引是一組詳細的規則和標準，可建立品牌的視覺和口頭識別。 這些可作為參考，以在所有行銷和通訊平台上維持一致的品牌代表性。

在[!DNL Journey Optimizer]中，您現在可以選擇手動輸入及組織您的品牌詳細資料，或上傳品牌指引檔案以進行自動資訊擷取。

## 存取品牌 {#generative-access}

若要存取[!DNL Adobe Journey Optimizer]中的&#x200B;**[!UICONTROL 品牌]**&#x200B;功能表，使用者必須被授與&#x200B;**[!UICONTROL 受管理的品牌套件]**&#x200B;或&#x200B;**[!UICONTROL 啟用AI小幫手]**&#x200B;許可權。 [了解更多](../administration/permissions.md)

+++  瞭解如何指派品牌相關許可權

1. 在&#x200B;**權限**&#x200B;產品中，前往&#x200B;**角色**&#x200B;標籤，然後選取所需的&#x200B;**角色**。

1. 按一下&#x200B;**編輯**&#x200B;以修改權限。

1. 新增&#x200B;**AI小幫手**&#x200B;資源，然後從下拉式功能表中選取&#x200B;**受管理的品牌套件**&#x200B;或&#x200B;**[!UICONTROL 啟用AI小幫手]**。

   請注意，**[!UICONTROL 啟用Ai小幫手]**&#x200B;許可權僅提供&#x200B;**[!UICONTROL 品牌]**&#x200B;功能表的唯讀存取權。

   ![](assets/brands-permission.png){zoomable="yes"}

1. 按一下&#x200B;**儲存**，以套用所做的變更。

   任何已指派給此角色的使用者都會自動更新其權限。

1. 若要將此角色指派給新使用者，請瀏覽至&#x200B;**角色**&#x200B;儀表板中的&#x200B;**使用者**&#x200B;標籤，然後按一下&#x200B;**新增使用者**。

1. 輸入使用者的名稱、電子郵件地址，或從清單當中選擇，然後按一下&#x200B;**儲存**。

1. 如果之前未建立使用者，請參閱[此文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

## 建立您的品牌 {#create-brand-kit}

>[!CONTEXTUALHELP]
>id="ajo_brands_create"
>title="建立您的品牌"
>abstract="輸入您的品牌名稱並上傳您的品牌指南檔案。 此工具會自動擷取關鍵詳細資訊，讓您更輕鬆地維護品牌識別。"

若要建立和管理您的品牌指引，您可以自行輸入詳細資料，或上傳品牌指引檔案以自動擷取資訊：

1. 在&#x200B;**[!UICONTROL 品牌]**&#x200B;功能表中，按一下&#x200B;**[!UICONTROL 建立品牌]**。

   ![](assets/brands-1.png)

1. 輸入您品牌的&#x200B;**[!UICONTROL 名稱]**。

1. 拖放或選取您的檔案，以上傳您的品牌指引，並自動擷取相關的品牌資訊。 按一下&#x200B;**[!UICONTROL 建立品牌]**。

   資訊擷取程式現在開始。 請注意，可能需要幾分鐘才能完成。

   ![](assets/brands-2.png)

1. 系統現在會自動填入您的內容和視覺化建立標準。 瀏覽不同的標籤，視需要調整資訊。

1. 在&#x200B;**[!UICONTROL 撰寫樣式]**&#x200B;索引標籤中，按一下![](assets/do-not-localize/Smock_Add_18_N.svg)以新增指引或排除專案，包括範例。

   ![](assets/brands-3.png)

1. 從&#x200B;**[!UICONTROL 視覺內容]**&#x200B;索引標籤，按一下![](assets/do-not-localize/Smock_Add_18_N.svg)以新增其他准則或排除專案。

1. 若要新增顯示正確使用方式的影像，請選取&#x200B;**[!UICONTROL 範例]**，然後按一下&#x200B;**[!UICONTROL 選取影像]**。 您也可以新增使用方式不正確的影像，作為排除範例。

   ![](assets/brands-4.png)

1. 設定之後，按一下&#x200B;**[!UICONTROL 儲存]**，然後按一下&#x200B;**[!UICONTROL 發佈]**，讓您的品牌指引可在AI助理中取得。

1. 若要修改您發佈的品牌，請按一下[編輯品牌]。****

   >[!NOTE]
   >
   >這會在編輯模式中建立臨時副本，並在發佈後取代即時版本。

   ![](assets/brands-8.png)

1. 從您的&#x200B;**[!UICONTROL 品牌]**&#x200B;儀表板，按一下![](assets/do-not-localize/Smock_More_18_N.svg)圖示以開啟進階功能表：

   * 檢視品牌
   * 編輯
   * 複製
   * 發佈
   * 取消發佈
   * 刪除

   ![](assets/brands-6.png)

您現在可以從AI助理功能表的&#x200B;**[!UICONTROL 品牌]**&#x200B;下拉式清單存取品牌指南，使其產生符合您規格的內容和資產。 [進一步瞭解AI助理](gs-generative.md)

![](assets/brands-7.png)
