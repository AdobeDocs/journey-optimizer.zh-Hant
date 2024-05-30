---
solution: Journey Optimizer
product: journey optimizer
title: 將內容另存為片段
description: 瞭解如何將內容儲存為片段，以便在Journey Optimizer行銷活動和歷程中重複使用內容
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: 83997271d16e15fb0d7ccdd21aa8ac8b8221a0d5
workflow-type: tm+mt
source-wordcount: '412'
ht-degree: 2%

---

# 將內容另存為片段 {#save-as-fragment}

在中編輯內容時 [!DNL Journey Optimizer]，您可以將全部或部分內容儲存為片段，以供日後重複使用。

## 將內容另存為視覺片段 {#save-as-visual-fragment}

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

## 將內容另存為運算式片段 {#save-as-expression-fragment}

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
