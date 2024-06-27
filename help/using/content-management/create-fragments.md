---
solution: Journey Optimizer
product: journey optimizer
title: 建立片段
description: 瞭解如何建立片段以在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 14%

---

# 建立片段 {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="選取視覺內容類型"
>abstract="建立獨立的視覺內容片段，以便在某個歷程或行銷活動的電子郵件中，或是某個內容範本中可以重複使用你的內容。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments" text="在你的電子郵件中新增視覺內容片段"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="選取運算式類型"
>abstract="建立獨立的運算式片段，以便在多個歷程和行銷活動中可重複使用你的內容。使用個人化編輯器時，您可以利用在目前沙箱上建立的所有運算式片段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=zh-Hant" text="利用運算式片段"

片段可從頭開始建立 **[!UICONTROL 片段]** 左側功能表。 此外，您也可以在設計內容時，將現有內容的一部分儲存為片段。 [了解作法](#save-as-fragment)

儲存後，您的片段即可用於歷程、行銷活動或範本。 在歷程和行銷活動中建置任何內容時，可以使用此片段。 另請參閱 [新增視覺片段](../email/use-visual-fragments.md) 和 [利用運算式片段](../personalization/use-expression-fragments.md)

若要建立片段，請遵循以下步驟。

## 定義片段的屬性 {#properties}

1. 透過存取片段清單 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左側功能表。

1. 選取 **[!UICONTROL 建立片段]** 並填入片段名稱和說明（如有需要）。

   ![](assets/fragment-details.png)

1. 選擇或建立Adobe Experience Platform標籤，從 **[!UICONTROL 標籤]** 將片段分類的欄位有助改善搜尋。 [瞭解如何使用統一標籤](../start/search-filter-categorize.md#tags)

1. 選擇片段型別： **視覺片段** 或 **運算式片段**. [進一步瞭解視覺效果和運算式片段](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >目前，視覺片段可用於 **電子郵件** 僅限頻道。

1. 如果您正在建立運算式片段，請選取您要使用的程式碼型別： **[!UICONTROL HTML]**， **[!UICONTROL JSON]** 或 **[!UICONTROL 文字]**.

   ![](assets/fragment-expression-type.png)

1. 若要指派自訂或核心資料使用標籤給片段，請按一下 **[!UICONTROL 管理存取權]** 按鈕來切換畫面。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 按一下 **[!UICONTROL 建立]** 以設計片段的內容。

## 設計片段內容 {#content}

在您設定了片段的屬性後，電子郵件Designer或個人化編輯器會根據您建立的片段型別開啟。

* 針對視覺片段，視需要編輯您的內容，就像處理歷程或行銷活動中的任何電子郵件一樣。 [了解更多](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* 針對運算式片段，請使用 [!DNL Journey Optimizer] 個人化編輯器及其所有個人化和編寫功能，可建置您的片段內容。 [了解更多](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

當您的內容準備就緒時，請按一下 **儲存** 按鈕。 片段會建立，並新增至片段清單，包含 **草稿** 狀態。 您可以預覽並發佈它，使其可在歷程和行銷活動中使用。

## 預覽和發佈片段 {#publish}

>[!NOTE]
>
>若要發佈片段，您必須擁有 [Publish片段](../administration/ootb-product-profiles.md#content-library-manager) 使用者許可權。

如果您的片段已準備好上線，您可以預覽和發佈它以使其可在您的歷程和行銷活動中使用。 若要這麼做，請依照以下步驟進行：

1. 在設計其內容後返回片段建立畫面，或從片段清單中開啟。

1. 片段的預覽可在 **標籤** 欄位，可檢查其轉譯。 如果您需要進行任何變更，請按一下 **編輯** 按鈕來開啟電子郵件Designer或個人化編輯器，具體取決於片段型別。

   ![](assets/fragment-preview.png)

1. 按一下 **Publish** 按鈕以發佈片段。

   如果片段用於即時歷程或行銷活動中，則會開啟訊息以通知您。 按一下 **檢視更多** 用來存取歷程及/或促銷活動清單的連結，其中會參考此連結。 [瞭解如何探索片段的引用](../content-management/manage-fragments.md#explore-references)

   按一下 **確認** 以發佈片段並在使用的即時歷程/行銷活動中更新。

   ![](assets/fragment-publish.png){width="70%" align="center"}

片段現在是 **即時**、和，在內建置任何內容時即可使用 [!DNL Journey Optimizer] 透過電子郵件傳送Designer或個人化編輯器：

* [瞭解如何使用視覺化片段](../email/use-visual-fragments.md)
* [瞭解如何使用運算式片段](../personalization/use-expression-fragments.md)
