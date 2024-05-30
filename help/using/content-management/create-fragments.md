---
solution: Journey Optimizer
product: journey optimizer
title: 建立片段
description: 瞭解如何建立片段以在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 1%

---


# 從頭開始建立片段 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="選取視覺效果型別"
>abstract="建立獨立的視覺片段，讓您的內容可重複用於歷程或行銷活動內的電子郵件中，或內容範本中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="將視覺化片段新增至您的電子郵件"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="選取運算式型別"
>abstract="建立獨立的運算式片段，讓您的內容可跨多個歷程和行銷活動重複使用。 使用個人化編輯器時，您可以善用已在目前沙箱上建立的所有運算式片段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="利用運算式片段"

片段是從以下專案建立： **[!UICONTROL 片段]** 左側功能表。 此外，您也可以在設計內容時，將現有內容的一部分儲存為片段。 [了解作法](#save-as-fragment)

儲存後，您的片段即可用於歷程、行銷活動或範本。 您現在可以在中建置任何內容時使用此片段 [!DNL Journey Optimizer]. 另請參閱 [新增視覺片段](../email/use-visual-fragments.md) 和 [利用運算式片段](../personalization/use-expression-fragments.md)

若要從頭開始建立片段，請遵循下列步驟。

1. [存取片段清單](#access-manage-fragments) 透過 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左側功能表。

1. 選取 **[!UICONTROL 建立片段]**.

1. 填寫片段詳細資訊，即名稱和說明（如果需要）。

   ![](assets/fragment-details.png)

1. 選擇或建立Adobe Experience Platform標籤，從 **[!UICONTROL 標籤]** 將片段分類的欄位有助改善搜尋。 [了解更多](../start/search-filter-categorize.md#tags)

1. 選擇片段型別： [視覺片段](#create-visual-fragment) 或 [運算式片段](#create-expression-fragment).

   >[!NOTE]
   >
   >目前僅針對視覺化片段 **電子郵件** 支援管道。

1. 如果您正在建立運算式片段，請選取您要使用的程式碼型別： **[!UICONTROL HTML]**， **[!UICONTROL JSON]** 或 **[!UICONTROL 文字]**.

   ![](assets/fragment-expression-type.png)

1. 若要指派自訂或核心資料使用標籤給片段，請選取「 」 **[!UICONTROL 管理存取權]**. [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 此 [電子郵件設計工具](../email/get-started-email-design.md) 或者會開啟個人化編輯器，具體取決於您建立的片段型別。

   * 針對視覺片段，視需要編輯您的內容，就像處理歷程或行銷活動中的任何電子郵件一樣。

     >[!NOTE]
     >
     >您可以新增個人化欄位和動態內容，但片段中不支援內容屬性。

     ![](assets/fragment-designer.png)

   * 針對運算式片段，請使用 [!DNL Journey Optimizer] 個人化編輯器及其所有個人化和編寫功能，可建置您的片段內容。 [了解更多](../personalization/personalization-build-expressions.md)

     ![](assets/fragment-expression-editor.png)

1. 片段準備就緒後，請按一下 **[!UICONTROL 儲存]**.

片段會新增至 [片段清單](#access-manage-fragments). 現在已準備好在中建置任何內容時使用 [!DNL Journey Optimizer] 電子郵件設計工具或個人化編輯器。

* [瞭解如何使用視覺化片段](../email/use-visual-fragments.md)
* [瞭解如何使用運算式片段](../personalization/use-expression-fragments.md)
