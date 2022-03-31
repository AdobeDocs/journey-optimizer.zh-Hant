---
title: 設計Journey Optimizer的電子郵件
description: 瞭解如何從頭開始設計電子郵件內容
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 151594f2-85e4-4c79-9c15-334fbd3768c4
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# 從頭開始 {#create-email-content}

>[!CONTEXTUALHELP]
>id="ac_structure_components"
>title="關於結構元件"
>abstract="結構元件定義電子郵件的佈局。"

>[!CONTEXTUALHELP]
>id="ac_edition_columns"
>title="定義電子郵件列"
>abstract="電子郵件設計器允許您通過定義列結構輕鬆定義電子郵件的佈局。"

電子郵件設計器允許您輕鬆定義電子郵件的結構。 通過使用簡單的拖放操作添加和移動結構元素，您可以在幾秒鐘內設計電子郵件的形狀。

要開始使用電子郵件設計器構建電子郵件內容，請執行以下步驟：

1. 從「電子郵件設計器」首頁中，選擇 **[!UICONTROL Design from scratch]** 的雙曲餘切值。

   ![](assets/email_designer.png)

1. 通過拖放開始設計電子郵件內容 **[!UICONTROL Structure components]** 定義電子郵件的佈局。

   >[!NOTE]
   >
   >請注意，列堆棧與所有電子郵件程式不相容。 不支援時，將不堆疊列。
   >
   >一旦放入電子郵件中，您就不能移動或刪除元件，除非其中已經放有內容元件或片段。

   ![](assets/email_designer_2.png)

1. 添加多個 **[!UICONTROL Structure components]** 按需要。

   選擇 **[!UICONTROL n:n column]** 定義所選列數（介於3和10之間）的元件。 也可以通過移動每列底部的箭頭來定義每列的寬度。

   >[!NOTE]
   >
   >每個列大小不能低於結構元件總寬度的10%。 無法刪除非空的列。

1. 從 **[!UICONTROL Content components]** 下拉框，可以添加 **[!UICONTROL Content components]** 在結構元件中。 [瞭解有關內容元件的詳細資訊](content-components.md)。

   ![](assets/email_designer_3.png)

1. 每個元件可進一步用 **[!UICONTROL Component settings]** 的子菜單。 例如，可以更改元件的文本樣式、填充或邊距。 [瞭解有關對齊和填充的詳細資訊](adjusting-vertical-alignment-and-padding.md)。

   ![](assets/email_designer_4.png)

1. 從 **[!UICONTROL Assets picker]**，您可以直接添加儲存在 **[!UICONTROL Assets library]** 郵件。 [瞭解有關資產管理的更多資訊](assets-essentials.md)。

   按兩下包含您的資產的資料夾，然後拖放要添加到電子郵件中的資產。

   ![](assets/email_designer_5.png)

1. 添加個性化欄位以自定義配置檔案資料中的內容。 [瞭解有關內容個性化的更多資訊](../personalization/personalize.md)。

   ![](assets/email_designer_6.png)

1. 在 **[!UICONTROL Links]** 頁籤，檢查要跟蹤的所有內容URL的清單。 您可以修改 **[!UICONTROL Tracking Type]**。 **[!UICONTROL Label]** 和 **[!UICONTROL Tags]** 如果需要。

   ![](assets/email_designer_7.png)

   >[!NOTE]
   >
   >瞭解有關連結和郵件跟蹤的詳細資訊 [此頁](message-tracking.md)。

1. 如果需要，您可以切換到代碼編輯器，通過按一下 **[!UICONTROL Switch to code editor]** 的子菜單。 有關代碼編輯器的詳細資訊，請參閱 [此頁](code-content.md#)。

   >[!NOTE]
   >
   >切換到代碼編輯器後，您將無法使用此電子郵件的可視設計器。

   ![](assets/email_designer_26.png)

1. 按一下 **[!UICONTROL Show preview]** 檢查您的電子郵件呈現。 您可以選擇案頭或移動視圖。

   有關如何預覽電子郵件的詳細資訊，請參閱 [此頁](preview.md)。

   ![](assets/email_designer_8.png)

1. 當您的電子郵件準備好後，按一下 **[!UICONTROL Save & Close]**。

您的電子郵件內容現在可以用在郵件中。 [瞭解如何發送消息](../messages/publish-manage-message.md)。

## How-to視頻 {#video}

瞭解如何使用消息編輯器建立電子郵件內容。

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)