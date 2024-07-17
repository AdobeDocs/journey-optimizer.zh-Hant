---
solution: Journey Optimizer
product: journey optimizer
title: 使用運算式片段
description: 瞭解如何在 [!DNL Journey Optimizer] 個人化編輯器中使用運算式片段。
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

使用&#x200B;**個人化編輯器**&#x200B;時，您可以利用所有已建立或已儲存至目前沙箱的運算式片段。

片段是可重複使用的元件，可跨[!DNL Journey Optimizer]個行銷活動和歷程參照。 此功能允許預先建置多個自訂內容區塊，可供行銷使用者在改良的設計流程中快速組合內容。 [瞭解如何建立和管理片段](../content-management/fragments.md)。

➡️[在此影片中瞭解如何管理、編寫和使用片段](../content-management/fragments.md#video-fragments)

## 使用運算式片段 {#use-expression-fragment}

若要將運算式片段新增至您的內容，請遵循下列步驟。

>[!NOTE]
>
>您最多可以在給定傳送中新增30個片段。 片段最多只能巢狀1個層級。

1. 開啟[個人化編輯器](personalization-build-expressions.md)並在左窗格上選取&#x200B;**[!UICONTROL 片段]**&#x200B;按鈕。

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
   >您可以將任何&#x200B;**草稿**&#x200B;或&#x200B;**即時**&#x200B;片段新增至您的內容。 但是，如果正在使用狀態為草稿的片段，您將無法啟用您的歷程或行銷活動。 在歷程或行銷活動發佈中，草稿片段將顯示錯誤，您需要核准它們才能發佈。

1. 在新增片段ID後，如果您開啟對應的運算式片段並從介面[編輯它](../content-management/fragments.md#edit-fragments)，變更便會同步。 它們會自動傳播到包含該片段ID的所有草稿或即時歷程/行銷活動。

1. 按一下片段旁的&#x200B;**[!UICONTROL 更多動作]**&#x200B;按鈕。 從開啟的關聯功能表中，選取&#x200B;**[!UICONTROL 檢視片段]**&#x200B;以取得有關該片段的詳細資訊。 也會顯示&#x200B;**[!UICONTROL 片段ID]**，可從此處複製。

   ![](assets/expression-fragment-view.png)

1. 您可以在另一個視窗中開啟運算式片段，以編輯其內容和屬性 — 使用內容功能表中的&#x200B;**[!UICONTROL 開啟片段]**&#x200B;選項或從&#x200B;**[!UICONTROL 片段資訊]**&#x200B;窗格。 [瞭解如何編輯片段](../content-management/fragments.md#edit-fragments)

   ![](assets/expression-fragment-open.png)

1. 然後您就可以照常使用[個人化編輯器](personalization-build-expressions.md)的所有個人化和編寫功能，自訂及驗證您的內容。

>[!NOTE]
>
>如果您建立包含多個分行符號的運算式片段，並將其用於[簡訊](../sms/create-sms.md#sms-content)或[推播](../push/design-push.md)內容，則會保留分行符號。 因此，在傳送您的[簡訊](../sms/send-sms.md)或[推播](../push/send-push.md)訊息之前，請務必先測試該訊息。

## 自訂可編輯欄位 {#customize-fields}

如果運算式片段的某些部分已使用變數設為可編輯，您可以使用特定語法覆寫其預設值。 [瞭解如何使您的片段可自訂](../content-management/customizable-fragments.md)

若要自訂欄位，請執行下列步驟：

1. 從&#x200B;**片段**&#x200B;功能表將片段插入您的程式碼中。

1. 在語法結尾使用`<fieldId>="<value>"`程式碼以覆寫變數的預設值。

   在以下範例中，我們以「yoga」值覆寫ID為「sports」之變數的值。 只要引用「sport」變數，片段內容中就會顯示「瑜伽」。

   ![](../content-management/assets/fragment-expression-use.png)

[本節](../content-management/customizable-fragments.md#example)提供範例，說明如何在建立電子郵件時，將可編輯欄位新增至運算式片段並覆寫其值。

## 中斷繼承 {#break-inheritance}

將片段ID新增至個人化編輯器時，會同步對原始運算式片段所做的變更。

不過，您也可以將運算式片段的內容貼到編輯器中。 從內容功能表中，選取&#x200B;**[!UICONTROL 貼上片段]**&#x200B;以插入該內容。

![](assets/expression-fragment-paste.png)

在這種情況下，來自原始片段的繼承會中斷。 片段內容會複製到編輯器中，且變更不再同步。

它會變成不再連結至原始片段的獨立元素；您可以像在程式碼中的任何其他元素一樣加以編輯。

