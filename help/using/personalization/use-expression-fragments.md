---
solution: Journey Optimizer
product: journey optimizer
title: 使用運算式片段
description: 瞭解如何在中使用運算式片段 [!DNL Journey Optimizer] 個人化編輯器。
feature: Personalization, Fragments
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，資料庫，個人化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: e6924928e03d494817a2368b33997029ca2eca1c
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# 利用運算式片段 {#use-expression-fragments}

使用時 **個人化編輯器**，您可以利用已建立或儲存至目前沙箱的所有運算式片段。

片段是可重複使用的元件，可在以下位置參照： [!DNL Journey Optimizer] 行銷活動和歷程。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合內容。 [瞭解如何建立和管理片段](../content-management/fragments.md).

➡️ [在本影片中瞭解如何管理、編寫和使用片段](../content-management/fragments.md#video-fragments)

## 使用運算式片段 {#use-expression-fragment}

若要將運算式片段新增至您的內容，請遵循下列步驟。

>[!NOTE]
>
>您最多可以在給定傳送中新增30個片段。 片段最多只能巢狀1個層級。

1. 開啟 [個人化編輯器](personalization-build-expressions.md) 並選取 **[!UICONTROL 片段]** 按鈕。

   清單會顯示目前沙箱上已建立或儲存為片段的所有運算式片段。 它們會依建立日期排序：最近新增的運算式片段會先顯示在清單中。 [了解更多](../content-management/fragments.md#create-expression-fragment)

   ![](assets/expression-fragments-pane.png)

   您也可以重新整理此清單。

   >[!NOTE]
   >
   >如果您在編輯內容時修改或新增了某些片段，清單會以最新變更更新。

1. 按一下運算式片段旁的+圖示，將對應的片段ID插入編輯器中。

   ![](assets/expression-fragment-add.png)

   >[!CAUTION]
   >
   >您可以新增任何 **草稿** 或 **即時** 片段至您的內容。 但是，如果正在使用狀態為草稿的片段，您將無法啟用您的歷程或行銷活動。 在歷程或行銷活動發佈中，草稿片段將顯示錯誤，您需要核准它們才能發佈。

1. 在新增片段ID後，如果您開啟對應的運算式片段並 [編輯它](../content-management/fragments.md#edit-fragments) 從介面中，變更會同步化。 它們會自動傳播到包含該片段ID的所有草稿或即時歷程/行銷活動。

1. 按一下 **[!UICONTROL 更多動作]** 按鈕尋找片段。 從開啟的關聯功能表中，選取 **[!UICONTROL 檢視片段]** 以取得該片段的詳細資訊。 此 **[!UICONTROL 片段ID]** 也會顯示，而且可以從此處複製。

   ![](assets/expression-fragment-view.png)

1. 您可以在另一個視窗中開啟運算式片段，以編輯其內容和屬性 — 使用 **[!UICONTROL 開啟片段]** 選項(位於內容功能表或 **[!UICONTROL 片段資訊]** 窗格。 [瞭解如何編輯片段](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 接著，您就可以照常使用，使用的所有個人化和撰寫功能，自訂及驗證內容 [個人化編輯器](personalization-build-expressions.md).

>[!NOTE]
>
>如果您建立包含多個分行符號的運算式片段，並在中使用它 [簡訊](../sms/create-sms.md#sms-content) 或 [推播](../push/design-push.md) 內容，則會保留分行符號。 因此，請務必測試您的 [簡訊](../sms/send-sms.md) 或 [推播](../push/send-push.md) 訊息傳送之前。

## 自訂可編輯欄位 {#customize-fields}

如果運算式片段的某些部分已使用變數設為可編輯，您可以使用特定語法覆寫其預設值。 [瞭解如何使您的片段可自訂](../content-management/customizable-fragments.md)

若要自訂欄位，請執行下列步驟：

1. 從將片段插入您的程式碼中 **片段** 功能表。

1. 使用 `<fieldId>="<value>"` 語法末尾的程式碼，用來覆寫變數的預設值。

   在以下範例中，我們以「yoga」值覆寫ID為「sports」之變數的值。 只要引用「sport」變數，片段內容中就會顯示「瑜伽」。

   ![](../content-management/assets/fragment-expression-use.png)

以下範例提供建立電子郵件時，如何將可編輯欄位新增至運算式片段並覆寫其值的說明： [本節](../content-management/customizable-fragments.md#example).

## 中斷繼承 {#break-inheritance}

將片段ID新增至個人化編輯器時，會同步對原始運算式片段所做的變更。

不過，您也可以將運算式片段的內容貼到編輯器中。 從內容功能表中，選取 **[!UICONTROL 貼上片段]** 以插入該內容。

![](assets/expression-fragment-paste.png)

在這種情況下，來自原始片段的繼承會中斷。 片段內容會複製到編輯器中，且變更不再同步。

它會變成不再連結至原始片段的獨立元素；您可以像在程式碼中的任何其他元素一樣加以編輯。

