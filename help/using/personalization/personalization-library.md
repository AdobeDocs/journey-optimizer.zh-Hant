---
title: 使用儲存的運算式
description: 瞭解如何使用保存的表達式 [!DNL Journey Optimizer] 的下界。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 49c09fbcf3be595e2a636f395fa89915e9e9c802
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 8%

---

# 使用儲存的運算式 {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="關於Expression庫"
>abstract="[!DNL Journey Optimizer] 提供了一個庫，您可以在其中訪問已保存的由管理員用戶配置的個性化表達式。 "

[!DNL Journey Optimizer] 提供了一個庫，您可以在其中訪問以前保存的由管理員用戶添加的個性化表達式。

➡️ [瞭解如何使用此視頻中保存的表達式](#video-preview)

要訪問保存的表達式，請按一下 **[!UICONTROL Library]** 按鈕。 該清單顯示管理員用戶保存的所有表達式(請參見 [將表達式保存到庫](#save-expressions))。

>[!NOTE]
>
>可以使用「資訊」按鈕獲取有關已保存表達式內容的詳細資訊。 如果您具有管理庫項目的適當權限，資訊按鈕將顯示在橢圓菜單中。

![](assets/library-list.png)

按一下+將表達式插入編輯器。 然後，您可以像往常一樣自定義和驗證個性化內容。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/library-add.png)

## 將表達式保存到庫 {#save-expressions}

[!DNL Journey Optimizer] 允許管理員用戶將個性化表達式保存到庫。 然後，所有用戶都可以使用這些表達式來生成個性化內容。

要將表達式保存到庫，請執行以下步驟：

1. 在編輯器介面中，生成表達式，然後按一下 **[!UICONTROL Add to library]**。

   >[!NOTE]
   >
   >如果按鈕不可見，請簽入您具有所需權限的Admin Console(請參閱 [權限級別](../administration/high-low-permissions.md))。

   ![](assets/library-save.png)

1. 在右窗格中，輸入表達式的標題和說明以幫助用戶更輕鬆地找到它，然後按一下 **[!UICONTROL Add]**。

   ![](assets/add-expression.png)

1. 表達式將添加到庫中。 用戶現在將能夠使用它來構建其個性化內容。


>[!NOTE]
>
>* 表達式不能超過200KB。
>
>* 保存的表達式按建立日期排序：最近添加的表達式將首先顯示在清單中。



要編輯現有表達式，請將其添加到編輯器中，然後根據需要修改它。 按一下 **[!UICONTROL Add to library]** 驗證語法並保存表達式。

要刪除表達式，請按一下橢圓按鈕，然後按一下 **[!UICONTROL Delete]**。

## How-to視頻{#video}

瞭解如何在訊息中使用已儲存的個人化資料庫項目，以及如何建立和管理個人化資料庫項目。

>[!VIDEO](https://video.tv.adobe.com/v/340941?quality=12)

