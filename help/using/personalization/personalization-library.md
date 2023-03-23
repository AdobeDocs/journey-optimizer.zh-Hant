---
solution: Journey Optimizer
product: journey optimizer
title: 使用儲存的運算式
description: 透過 [!DNL Journey Optimizer] 程式庫。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，程式庫，個人化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 14%

---

# 使用儲存的運算式 {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="關於運算式資料庫"
>abstract="[!DNL Journey Optimizer] 會提供資料庫，您可以在此存取已由管理員使用者設定的已儲存個人化運算式。 "

[!DNL Journey Optimizer] 提供一個程式庫，您可在其中存取管理員使用者新增的先前儲存的個人化運算式。

➡️ [了解如何在此影片中使用儲存的運算式](#video-preview)

若要存取儲存的運算式，請按一下 **[!UICONTROL 程式庫]** 按鈕。 清單會顯示管理員使用者已儲存的所有運算式(請參閱 [將運算式儲存至程式庫](#save-expressions))。

>[!NOTE]
>
>您可以使用資訊按鈕來取得有關已儲存運算式內容的詳細資訊。 如果您有管理程式庫項目的適當權限，資訊按鈕將出現在橢圓菜單中。

![](assets/library-list.png)

按一下+將運算式插入編輯器中。 然後，您可以照常自訂及驗證您的個人化內容。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/library-add.png)

## 將運算式儲存至程式庫 {#save-expressions}

[!DNL Journey Optimizer] 可讓管理員使用者將個人化運算式儲存至程式庫。 然後，所有使用者都可使用這些運算式來建立個人化內容。

若要將運算式儲存至程式庫，請依照下列步驟操作：

1. 在編輯器介面中，建立運算式，然後按一下 **[!UICONTROL 新增至程式庫]**.

   >[!NOTE]
   >
   >如果按鈕未顯示，請簽入您擁有所需權限的Admin Console(請參閱 [權限層級](../administration/high-low-permissions.md))。

   ![](assets/library-save.png)

1. 在右窗格中，輸入表達式的標題和說明，以幫助用戶更輕鬆地查找，然後按一下 **[!UICONTROL 新增]**.

   ![](assets/add-expression.png)

1. 運算式會新增至程式庫。 使用者現在可以用它來建立其個人化內容。


>[!NOTE]
>
>* 運算式不能超過200KB。
>
>* 儲存的運算式會依建立日期排序：最近新增的運算式會先顯示在清單中。



若要編輯現有運算式，請將其新增至編輯器，然後根據您的需求加以修改。 按一下 **[!UICONTROL 新增至程式庫]** 驗證語法並儲存運算式。

若要刪除運算式，請按一下省略號按鈕，然後按一下 **[!UICONTROL 刪除]**.

## 作法影片{#video}

瞭解如何在訊息中使用已儲存的個人化資料庫項目，以及如何建立和管理個人化資料庫項目。

>[!VIDEO](https://video.tv.adobe.com/v/340941?quality=12)

