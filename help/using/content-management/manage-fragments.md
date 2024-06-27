---
solution: Journey Optimizer
product: journey optimizer
title: 管理片段
description: 瞭解如何管理您的內容片段
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: c42fc1069e11b8e34b7477fc26ed8a6b4ef95ac7
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 18%

---

# 管理片段 {#manage-fragments}

若要管理您的片段，請從以下位置存取片段清單： **[!UICONTROL 內容管理]** > **[!UICONTROL 片段]** 左側功能表。

在目前沙箱建立的所有片段 —  [從 **[!UICONTROL 片段]** 功能表](#create-fragments)，使用 [另存為片段](#save-as-fragment) 選項 — 會顯示。

![](assets/fragment-list-filters.png)

您可以在其上篩選片段：

* 狀態（草稿或即時）
* 型別（視覺效果或運算式）
* 建立或修改日期
* 狀態（是否封存）
* 標記

您也可以選擇顯示所有片段，或僅顯示目前使用者建立或修改的專案。

從 **[!UICONTROL 更多動作]** 按鈕時，您可以：

* 復製片段。
* 使用 **[!UICONTROL 探索引用]** 檢視歷程、行銷活動或使用範本的選項。 [了解更多](#explore-references)
* 封存片段。 [了解更多](#archive-fragments)
* 編輯片段的標籤 [瞭解如何使用統一標籤](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## 片段的狀態

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="新的片段狀態"
>abstract="由於 Journey Optimizer 6 月版本引入了&#x200B;**草稿**&#x200B;和&#x200B;**即時**&#x200B;狀態，因此在此版本之前建立的所有片段都具有「草稿」狀態，即使這些片段用於旅程或活動中也是如此。如果您對這些片段進行任何變更，則需要發佈它們以使其進入「即時」狀態，並將變更內容傳遞到關聯的行銷活動和旅程。您還需要建立一個新的旅程/行銷活動版本，然後進行發佈。<br/>發佈需要 <a href="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Publish片段</a> 使用者許可權。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="進一步瞭解內容片段許可權"

片段可以有多個狀態：

* **[!UICONTROL 草稿]**：片段正在編輯且尚未核准。

* **[!UICONTROL 即時]**：片段已核准並上線。 [瞭解如何發佈片段](../content-management/create-fragments.md#publish)

  編輯即時片段時，其狀態旁邊會顯示特定圖示。 按一下此圖示以開啟片段的草稿版本。

* **[!UICONTROL 發佈]**：片段已核准且正在發佈。
* **[!UICONTROL 已封存]**：片段已封存。 [瞭解如何封存片段](#archive-fragments)

>[!CAUTION]
>
>由於 Journey Optimizer 6 月版本引入了&#x200B;**草稿**&#x200B;和&#x200B;**即時**&#x200B;狀態，因此在此版本之前建立的所有片段都具有「草稿」狀態，即使這些片段用於旅程或活動中也是如此。如果您對這些片段進行任何變更，則需要發佈它們以使其進入「即時」狀態，並將變更內容傳遞到關聯的行銷活動和旅程。您還需要建立一個新的旅程/行銷活動版本，然後進行發佈。發佈需要 [Publish片段](../administration/ootb-product-profiles.md#content-library-manager) 使用者許可權。

## 編輯片段 {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="行銷活動中的片段更新"
>abstract="如果您發佈對片段的變更，將不會更新此行銷活動。 它需要發佈新版本，以便可以支援片段更新功能。"

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="歷程中的片段更新"
>abstract="如果您發佈對片段的變更，將不會更新此歷程。 它需要發佈新版本，以便可以支援片段更新功能。"

若要編輯片段，請遵循以下步驟。

1. 從以下位置按一下所需的片段： **[!UICONTROL 片段]** 清單。

1. 片段屬性隨即開啟，並預覽其內容。

1. 如果正在編輯的片段具有 **即時** 狀態，按一下 **修改** 按鈕以建立片段的草稿版本。 片段的目前版本將繼續上線，直到您發佈草稿版本為止。

1. 對片段進行所需的變更。 若要編輯其內容，請按一下 **編輯** 按鈕然後編輯您的內容，就像從頭開始建立片段時所做的那樣。 [瞭解如何建立片段](#create-from-scratch)

   >[!NOTE]
   >
   >編輯運算式片段時，您可以移除任何個人化欄位，但無法將新欄位新增至片段內容。 如果您想要新增個人化欄位，請復製片段以建立新片段。

   您還可以透過選擇 **瀏覽器參考** 選項。 [了解更多](#explore-references)

   ![](assets/fragment-edit.png)

1. 準備好變更後，按一下 **Publish** 按鈕讓您的修改上線。

當您編輯片段時，變更會自動傳播至使用該片段的所有內容，包括即時歷程和行銷活動，但您中斷原始片段繼承的內容除外。 瞭解如何在中中斷繼承 [將視覺化片段新增至您的電子郵件](../email/use-visual-fragments.md#break-inheritance) 和 [利用運算式片段](../personalization/use-expression-fragments.md#break-inheritance) 區段。

## 探索參考 {#explore-references}

您可以顯示目前使用片段的歷程、行銷活動和內容範本清單。 若要這麼做，請選取 **[!UICONTROL 探索引用]** 來自 **[!UICONTROL 更多動作]** 「片段」清單或「片段屬性」畫面中的「 」功能表。

![](assets/fragment-explore-references.png)

選取索引標籤以在歷程、行銷活動、範本和片段之間切換。 您可以檢視其狀態，然後按一下名稱，重新導向至已引用片段的對應專案。

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>如果片段用於歷程、行銷活動或範本中，且標籤阻止您存取該片段，您會在選取的標籤上方看到警告訊息。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

## 封存片段 {#archive-fragments}

您可以從不再與您的品牌相關的專案清除片段清單。

若要這麼做，請按一下 **[!UICONTROL 更多動作]** 按鈕並選取 **[!UICONTROL 封存]**. 它會從片段清單中消失，從而防止使用者在未來的電子郵件或範本中使用它。

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>如果您封存內容中使用的片段， <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->該內容將不會受到影響。

若要取消封存片段，請在 **[!UICONTROL 已封存]** 專案並選取 **[!UICONTROL 取消封存]** 從 **[!UICONTROL 更多動作]** 功能表。 現在仍可從片段清單存取，並可用於任何電子郵件或範本。

![](assets/fragment-list-unarchive.png)
