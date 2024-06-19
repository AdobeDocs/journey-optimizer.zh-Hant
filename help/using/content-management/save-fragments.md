---
solution: Journey Optimizer
product: journey optimizer
title: 將內容另存為片段
description: 瞭解如何將內容儲存為片段，以便在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 70e88ea0-f2b0-4c13-8693-619741762429
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# 將內容另存為片段 {#save-as-fragment}

在中編輯內容時 [!DNL Journey Optimizer]，您可以將全部或部分內容儲存為片段，以供日後重複使用。 您可以將內容另存為片段 [從電子郵件設計工具](#save-as-visual-fragment)，或 [從運算式編輯器](#save-as-expression-fragment).

## 另存為視覺片段 {#save-as-visual-fragment}

若要將電子郵件設計工具的內容儲存為片段，請執行下列步驟：

1. 在 [電子郵件設計工具](../email/get-started-email-design.md)，按一下畫面右上方的省略符號。

1. 選取 **[!UICONTROL 另存為片段]** （從下拉式功能表）。

   ![](assets/fragment-save-as.png)

1. 此 **[!UICONTROL 另存為片段]** 熒幕顯示。 在該處選取您要納入片段中的元素，包括個人化欄位和動態內容。 請注意，片段中不支援內容屬性。

   ![](assets/fragment-save-as-screen.png)

   >[!CAUTION]
   >
   >您只能選取彼此相鄰的截面。 您無法選取空的結構或其他片段。

1. 按一下 **[!UICONTROL 建立]** 並填入片段名稱和說明（如有需要）。

1. 若要指派自訂或核心資料使用標籤給片段，請按一下 **[!UICONTROL 管理存取權]** 按鈕來切換畫面。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md).

1. 選擇或建立Adobe Experience Platform標籤，從 **標籤** 將範本分類以改善搜尋的欄位。 [了解更多](../start/search-filter-categorize.md#tags)

1. 按一下 **[!UICONTROL 建立]**。片段會新增至 [片段清單](#access-manage-fragments) 使用 **草稿** 狀態。 它會變成獨立的片段，可當作該清單中的任何其他視覺片段使用。

   >[!NOTE]
   >
   >對該新片段所做的任何變更都不會傳播到該新片段來自的電子郵件或範本。 同樣地，在該電子郵件或範本中編輯原始內容時，不會修改新片段。

1. 為了能夠在您的歷程和行銷活動中使用片段，您需要讓它上線。 [瞭解如何預覽和發佈片段](../content-management/create-fragments.md#publish)

>[!NOTE]
>
>在Journey Optimizer 6月發行後的數天內，片段發佈功能將逐步推出。 雖然有些使用者可以立即存取，但有些使用者在其環境中使用前可能會遇到延遲問題。 如果您的環境尚未提供此增強功能，請注意，在您的歷程和行銷活動中使用片段不需要發佈片段。

## 另存為運算式片段 {#save-as-expression-fragment}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="另存為運算式片段"
>abstract="[!DNL Journey Optimizer] 個人化編輯器可讓您將內容另存為運算式片段。然後這些運算式可用於建置個人化內容。"

[!DNL Journey Optimizer] 個人化編輯器可讓您將內容另存為運算式片段。然後這些運算式可用於建置個人化內容。

若要將內容另存為運算式片段，請遵循下列步驟。

1. 在 [個人化編輯器](../personalization/personalization-build-expressions.md) 介面，建立運算式，然後按一下 **[!UICONTROL 另存為片段]**.

   >[!NOTE]
   >
   >運算式不能超過200KB。

1. 在右窗格中，輸入運算式的名稱和說明，以協助使用者更輕鬆地找到它。

   ![](assets/expression-fragment-save-as.png)

1. 按一下 **[!UICONTROL 儲存片段]**.

   <!--An expression fragment cannot be nested inside another fragment.-->

1. 片段會新增至 [片段清單](#access-manage-fragments) 使用 **草稿** 狀態。 它會變成獨立的片段，可當作該清單中的任何其他運算式片段使用。

1. 為了能夠在您的歷程和行銷活動中使用片段，您需要讓它上線。 [瞭解如何預覽和發佈片段](../content-management/create-fragments.md#publish)

>[!NOTE]
>
>在Journey Optimizer 6月發行後的數天內，片段發佈功能將逐步推出。 雖然有些使用者可以立即存取，但有些使用者在其環境中使用前可能會遇到延遲問題。 如果您的環境尚未提供此增強功能，請注意，在您的歷程和行銷活動中使用片段不需要發佈片段。
