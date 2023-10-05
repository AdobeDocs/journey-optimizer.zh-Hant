---
solution: Journey Optimizer
product: journey optimizer
title: 使用儲存的運算式
description: 瞭解如何使用儲存的運算式，從 [!DNL Journey Optimizer] 資料庫。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 運算式，編輯器，資料庫，個人化
exl-id: 74b1be18-4829-4c67-ae45-cf13278cda65
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 14%

---

# 使用儲存的運算式 {#expression-library}

>[!CONTEXTUALHELP]
>id="ajo_perso_library"
>title="關於運算式資料庫"
>abstract="[!DNL Journey Optimizer] 會提供資料庫，您可以在此存取已由管理員使用者設定的已儲存個人化運算式。 "

[!DNL Journey Optimizer] 提供一個資料庫，您可在其中存取管理員使用者新增之先前儲存的個人化運算式。

➡️ [在本影片中瞭解如何使用儲存的運算式](#video-preview)

若要存取儲存的運算式，請按一下 **[!UICONTROL 資料庫]** 按鈕。 此清單會顯示管理員使用者儲存的所有運算式(請參閱 [將運算式儲存至程式庫](#save-expressions))。

>[!NOTE]
>
>您可以從省略符號按鈕取得有關已儲存運算式內容的詳細資訊。 請注意，如果您擁有管理程式庫專案的適當許可權，資訊按鈕將會以省略符號顯示。

按一下+將運算式插入編輯器中。 接著，您就可以照常自訂及驗證個人化內容。 [了解更多](../personalization/personalization-build-expressions.md)

![](assets/library-add.png)

## 將運算式儲存至程式庫 {#save-expressions}

[!DNL Journey Optimizer] 可讓管理員使用者將個人化運算式儲存至程式庫。 所有使用者都可以使用這些運算式來建置個人化內容。

若要將運算式儲存至程式庫，請執行下列步驟：

1. 在編輯器介面中建立運算式，然後按一下 **[!UICONTROL 新增至程式庫]**.

   >[!NOTE]
   >
   >如果按鈕不可見，請簽入您具有必要許可權的Admin Console(請參閱 [許可權層級](../administration/high-low-permissions.md))。

   ![](assets/library-save.png)

1. 在右窗格中，輸入運算式的標題和說明，以協助使用者更容易找到它，然後按一下 **[!UICONTROL 新增]**.

   ![](assets/add-expression.png)

1. 運算式會新增至程式庫。 使用者現在將能夠使用它來建置其個人化內容。


>[!NOTE]
>
>* 運算式不能超過200KB。
>
>* 儲存的運算式會依建立日期排序：最近新增的運算式會顯示在清單中的前面。


若要編輯現有的運算式，請將其新增至編輯器，然後視需要加以修改。 按一下 **[!UICONTROL 新增至程式庫]** 以驗證語法並儲存運算式。

若要刪除運算式，請按一下省略符號按鈕，然後按一下 **[!UICONTROL 刪除]**.

## 操作說明影片{#video}

瞭解如何在訊息中使用已儲存的個人化資料庫項目，以及如何建立和管理個人化資料庫項目。

>[!VIDEO](https://video.tv.adobe.com/v/340941?quality=12)

