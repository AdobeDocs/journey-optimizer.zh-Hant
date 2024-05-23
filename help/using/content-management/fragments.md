---
solution: Journey Optimizer
product: journey optimizer
title: 使用片段
description: 瞭解如何建立片段以在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 7131a953-baca-4e7c-a8df-97c0bd6ac567
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1561'
ht-degree: 3%

---

# 使用片段 {#fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="定義您自己的片段"
>abstract="建立並管理獨立片段，讓您的內容可跨多個歷程和行銷活動重複使用。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/reusable-content/fragments.html#create-fragments" text="建立片段"

片段是可重複使用的元件，可在一封或多封電子郵件中加以參照 [!DNL Journey Optimizer] 行銷活動和歷程。

此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合電子郵件內容。

![](../rn/assets/do-not-localize/fragments.gif)

➡️ [瞭解如何在這些影片中管理、編寫和使用片段](#video-fragments)

若要充分利用片段：

* 建立您自己的片段。 您可以建立視覺化片段或運算式片段。 [了解更多](#create-fragments)

* 視需要在您的內容中多次使用。 另請參閱 [新增視覺片段](../email/use-visual-fragments.md) 和 [利用運算式片段](../personalization/use-expression-fragments.md)

>[!NOTE]
>
>**視覺片段** 可用於 [電子郵件設計工具](../email/get-started-email-design.md)，而 **運算式片段** 可透過 [個人化編輯器](../personalization/personalization-build-expressions.md).

此外，您也可以善用Journey Optimizer **內容重設API** 以管理內容片段。 有關詳細資訊，請參閱 [Journey Optimizer API檔案](https://developer.adobe.com/journey-optimizer-apis/references/content/){target="_blank"}.

## 開始之前 {#fragment-prerequisites}

>[!CAUTION]
>
>若要建立、編輯和封存片段，您必須擁有 **[!DNL Manage library items]** 許可權包含在 **[!DNL Content Library Manager]** 產品設定檔。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)

在此版本中，適用下列限制：

* 視覺片段僅適用於電子郵件頻道

* 運算式片段不適用於應用程式內頻道

## 存取及管理片段 {#access-manage-fragments}

若要存取片段清單，請選取「 」 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 從左側功能表。

![](assets/fragment-list.png)

在目前沙箱建立的所有片段 —  [從 **[!UICONTROL 片段]** 功能表](#create-fragments)，使用 [另存為片段](#save-as-fragment) 選項 — 會顯示。

您可以在其上篩選片段：

* 型別： **[!UICONTROL 視覺]** 或 **[!UICONTROL 運算式]**
* 標記
* 建立或修改日期

您可以選擇顯示所有片段，或僅顯示目前使用者建立或修改的專案。

您也可以顯示 **[!UICONTROL 已封存]** 片段。 [了解更多](#archive-fragments)

![](assets/fragment-list-filters.png)

從 **[!UICONTROL 更多動作]** 按鈕時，您可以：

* 復製片段。

* 使用 **[!UICONTROL 探索引用]** 檢視歷程、行銷活動或使用範本的選項。 [了解更多](#explore-references)

* 封存片段。 [了解更多](#archive-fragments)

* 編輯片段的 [標籤](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

### 編輯片段 {#edit-fragments}

若要編輯片段，請遵循以下步驟。

1. 從以下位置按一下所需的專案： **[!UICONTROL 片段]** 清單。
1. 從片段屬性中，您可以 [探索引用](#explore-references)， [管理其存取權](../administration/object-based-access.md)，並更新片段詳細資訊，包括 [標籤](../start/search-filter-categorize.md#tags).

   ![](../email/assets/fragment-edit-content.png)

1. 選取對應的按鈕來編輯內容，就像從頭開始建立片段時一樣。 [了解更多](#create-from-scratch)

>[!NOTE]
>
>當您編輯片段時，變更會自動傳播至使用該片段的所有內容，但中使用的內容除外 **[!UICONTROL 即時]** 歷程或行銷活動。 您也可以中斷原始片段的繼承。 進一步瞭解 [將視覺化片段新增至您的電子郵件](../email/use-visual-fragments.md#break-inheritance) 和 [利用運算式片段](../personalization/use-expression-fragments.md#break-inheritance) 區段。

### 探索參考 {#explore-references}

您可以顯示目前使用片段的歷程、行銷活動和內容範本清單。

若要這麼做，請選取 **[!UICONTROL 探索引用]** 來自 **[!UICONTROL 更多動作]** 「片段」清單或「片段屬性」畫面中的「 」功能表。

![](assets/fragment-explore-references.png)

選取索引標籤以在歷程、行銷活動、範本和片段之間切換。 您可以檢視其狀態，然後按一下名稱，重新導向至已引用片段的對應專案。

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>如果片段用於歷程、行銷活動或範本中，且標籤阻止您存取該片段，您會在選取的標籤上方看到警告訊息。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

### 封存片段 {#archive-fragments}

您可以從不再與您的品牌相關的專案清除片段清單。

若要這麼做，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 封存]**. 它會從片段清單中消失，從而防止使用者在未來的電子郵件或範本中使用它。

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>如果您封存內容中使用的片段， <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->該內容將不會受到影響。

若要取消封存片段，請在 **[!UICONTROL 已封存]** 專案並選取 **[!UICONTROL 取消封存]** 從 **[!UICONTROL 更多動作]** 功能表。 現在仍可從片段清單存取，並可用於任何電子郵件或範本。

![](assets/fragment-list-unarchive.png)

## 建立片段 {#create-fragments}

建立片段的方式有兩種：

* 使用，從頭開始建立片段 **[!UICONTROL 片段]** 專用功能表。 [了解作法](#create-from-scratch)

* 設計內容時，請將部分內容儲存為片段。 [了解作法](#save-as-fragment)

儲存後，您的片段即可用於歷程、行銷活動或範本。 無論是從草稿建立還是從現有內容建立，您現在都可以在中建立任何內容時使用此片段 [!DNL Journey Optimizer]. 另請參閱 [新增視覺片段](../email/use-visual-fragments.md) 和 [利用運算式片段](../personalization/use-expression-fragments.md)

### 從頭開始建立 {#create-from-scratch}

若要從頭開始建立片段，請遵循下列步驟。

1. [存取片段清單](#access-manage-fragments) 透過 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左側功能表。

1. 選取 **[!UICONTROL 建立片段]**.

1. 填寫片段詳細資訊，即名稱和說明（如果需要）。

   ![](assets/fragment-details.png)

1. 選擇片段型別： [視覺片段](#create-visual-fragment) 或 [運算式片段](#create-expression-fragment).

1. 若要指派自訂或核心資料使用標籤給片段，請選取「 」 **[!UICONTROL 管理存取權]**. [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 選擇或建立Adobe Experience Platform標籤，從 **[!UICONTROL 標籤]** 將片段分類的欄位有助改善搜尋。 [了解更多](../start/search-filter-categorize.md#tags)

1. 按一下&#x200B;**[!UICONTROL 建立]**。

### 建立視覺片段 {#create-visual-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="選取視覺效果型別"
>abstract="建立獨立的視覺片段，讓您的內容可重複用於歷程或行銷活動內的電子郵件中，或內容範本中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments.html" text="將視覺化片段新增至您的電子郵件"

1. [建立片段](#create-from-scratch) 從 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左方功能表並選取 **[!UICONTROL 視覺片段]** 型別。

   >[!NOTE]
   >
   >目前僅針對視覺化片段 **電子郵件** 支援管道。

1. 此 [電子郵件設計工具](../email/get-started-email-design.md) 顯示。 視需要編輯您的內容，就像處理歷程或行銷活動中的任何電子郵件一樣。

   >[!NOTE]
   >
   >您可以新增個人化欄位和動態內容，但片段中不支援內容屬性。

   ![](assets/fragment-designer.png)

1. 片段準備就緒後，請按一下 **[!UICONTROL 儲存]**. 它會新增至 [片段清單](#access-manage-fragments).

1. 如有需要，請按一下片段名稱旁的箭頭，以返回 **[!UICONTROL 詳細資料]** 並加以編輯。

   ![](assets/fragment-designer-back.png)

此片段現在已準備好用於建立任何 [電子郵件](../email/get-started-email-design.md) 或 [內容範本](content-templates.md) 範圍 [!DNL Journey Optimizer]. [了解作法](../email/use-visual-fragments.md)

### 建立運算式片段 {#create-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="選取運算式型別"
>abstract="建立獨立的運算式片段，讓您的內容可跨多個歷程和行銷活動重複使用。 使用個人化編輯器時，您可以善用已在目前沙箱上建立的所有運算式片段。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html" text="利用運算式片段"

1. [建立片段](#create-from-scratch) 從 **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左方功能表並選取 **[!UICONTROL 運算式片段]** 型別。

1. 選取您要使用的程式碼型別： **[!UICONTROL HTML]**， **[!UICONTROL JSON]** 或 **[!UICONTROL 文字]**.

   ![](assets/fragment-expression-type.png)

   <!--Expression fragments can be used in any channel.-->

1. 按一下 **[!UICONTROL 建立]**. 個人化編輯器隨即開啟。

1. 您可以善用 [!DNL Journey Optimizer] 具有所有個人化和編寫功能的個人化編輯器。 [了解更多](../personalization/personalization-build-expressions.md)

   ![](assets/fragment-expression-editor.png)

1. 片段準備就緒後，請按一下 **[!UICONTROL 儲存]**. 它會新增至 [片段清單](#access-manage-fragments).

1. 如有需要，請按一下片段名稱旁的箭頭，以返回 **[!UICONTROL 詳細資料]** 並加以編輯。

此片段現在已準備好用於內建置任何內容 [!DNL Journey Optimizer] 個人化編輯器。 [了解作法](../personalization/use-expression-fragments.md)

## 另存為片段 {#save-as-fragment}

在中編輯內容時 [!DNL Journey Optimizer]，您可以將全部或部分內容儲存為片段，以供日後重複使用。

### 另存為視覺片段 {#save-as-visual-fragment}

設計時 [內容範本](content-templates.md) 或 [電子郵件](../email/get-started-email-design.md) 在行銷活動或歷程中，您可以將部分內容儲存為視覺片段。 請依照下列步驟以執行此操作。

1. 在 [電子郵件設計工具](../email/get-started-email-design.md)，按一下畫面右上方的省略符號。

1. 選取 **[!UICONTROL 另存為片段]** （從下拉式功能表）。

   ![](assets/fragment-save-as.png)

1. 此 **[!UICONTROL 另存為片段]** 熒幕顯示。 在該處選取您要納入片段中的元素，包括個人化欄位和動態內容。 請注意，片段中不支援內容屬性。

   >[!CAUTION]
   >
   >您只能選取彼此相鄰的截面。 您無法選取空的結構或其他片段。

   ![](assets/fragment-save-as-screen.png)

1. 按一下 **[!UICONTROL 建立]**. 填寫片段詳細資訊，即名稱和說明（如果需要）。

1. 若要指派自訂或核心資料使用標籤給片段，請選取「 」 **[!UICONTROL 管理存取權]**. [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 選擇或建立Adobe Experience Platform標籤，從 **標籤** 將範本分類以改善搜尋的欄位。 [了解更多](../start/search-filter-categorize.md#tags)

1. 按一下 **[!UICONTROL 建立]** 再來一次。 片段會儲存到中，並新增至 [片段清單](#access-manage-fragments)，可從存取 [!DNL Journey Optimizer] 專用功能表。

   它會變成獨立的片段，可以 [已存取](#access-manage-fragments)， [已編輯](#edit-fragments) 和 [已封存](#archive-fragments) 如同該清單上的任何其他專案。

您現在可以在建置任何 [電子郵件](../email/get-started-email-design.md) 或 [內容範本](content-templates.md) 範圍 [!DNL Journey Optimizer]. [了解作法](../email/use-visual-fragments.md)

>[!NOTE]
>
>對該新片段所做的任何變更都不會傳播到該新片段來自的電子郵件或範本。 同樣地，在該電子郵件或範本中編輯原始內容時，不會修改新片段。

### 另存為運算式片段 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="另存為運算式片段"
>abstract="此 [!DNL Journey Optimizer] 個人化編輯器可讓您將內容儲存為運算式片段。 然後，這些運算式便可用於建置個人化內容。"

此 [!DNL Journey Optimizer] 個人化編輯器可讓您將內容儲存為運算式片段。 然後，這些運算式便可用於建置個人化內容。

若要將內容另存為運算式片段，請遵循下列步驟。

1. 在 [個人化編輯器](../personalization/personalization-build-expressions.md) 介面，建立運算式，然後按一下 **[!UICONTROL 另存為片段]**.

1. 在右窗格中，輸入運算式的名稱和說明，以協助使用者更輕鬆地找到它。

   ![](assets/expression-fragment-save-as.png)

1. 按一下 **[!UICONTROL 儲存片段]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 將運算式片段新增至 [片段清單](#access-manage-fragments). 您現在可以使用它來建置個人化內容。

>[!NOTE]
>
>運算式不能超過200KB。

## 操作說明影片 {#video-fragments}

瞭解如何在中管理、編寫和使用視覺化片段 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3419932/?quality=12)

瞭解如何在中管理、編寫和使用運算式片段 [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3424587/?quality=12)
