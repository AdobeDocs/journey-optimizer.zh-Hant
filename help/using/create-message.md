---
title: 建立訊息
description: 了解如何建立訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 186a43cd-c5eb-4de1-8713-95399d802d36
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 3%

---

# 建立訊息 {#create-message}

訊息可從 **[!UICONTROL Messages]** 左側導覽的捷徑。 會列出所有訊息，依發佈日期（針對已發佈訊息）或建立日期（針對草稿訊息）排序。

>[!NOTE]
>
>使用者可依其產品設定檔存取、建立、編輯和/或發佈訊息。 深入了解使用者權限 [在本節](../using/administration/permissions.md).

![](assets/messages-list.png)

使用 **[!UICONTROL Show recents]** 切換，將直接連結新增至您最近5天存取的訊息。

![](assets/show-recent-messages.png)

使用篩選表徵圖只顯示草稿、已發佈或正在發佈的消息。 您也可以搜尋訊息標籤，如下所示：

![](assets/filter-messages.png)

## 建立新訊息

若要建立新訊息，請遵循下列步驟：

1. 存取訊息清單，然後按一下 **[!UICONTROL Create Message]**.

1. 定義訊息屬性。

   ![](assets/create-message-properties.png)

   * 輸入 **[!UICONTROL Title]** （必填）和 **[!UICONTROL Description]**.

   * 選取 **[!UICONTROL Preset]** 以用於訊息。

      預設集包含根據您的品牌傳送電子郵件和/或推播通知所需的所有參數。 [深入了解預設集](../using/configuration/message-presets.md).

   * 選取您要用於該訊息的通道：電子郵件和/或推播通知。 您必須選取至少一個管道才能建立訊息。
   請注意，您隨時都可以使用 **[!UICONTROL Properties]** 按鈕。

   ![](assets/message-properties.png)


1. 按一下 **[!UICONTROL Create]** 確認訊息建立。 您的訊息會新增至訊息清單中，位於 **[!UICONTROL Draft]** 狀態。

   每個選取的通道都有一個索引標籤。 使用這些標籤來設定每個頻道的內容。 您可以選取索引標籤，然後按一下 **[!UICONTROL Delete channel]** 按鈕。

   ![](assets/create-messages-content.png)

   您現在可以建立訊息的內容並調整設定。 以下章節提供電子郵件和推播通知設定的詳細資訊：

   * [建立電子郵件](create-email.md)
   * [建立推播通知](create-push.md)

   >[!NOTE]
   >   
   >您可以使用運算式編輯器，使用設定檔資料個人化您的訊息。 如需個人化的詳細資訊，請參閱 [本節](personalization/personalize.md).


1. 使用左側的預覽區段，控制訊息的轉譯，並使用測試設定檔檢查個人化設定。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/messages-simple-preview.png)

1. 檢查編輯器上方區段的警報。  其中有些是簡單的警告，但有些警告可能會阻止您發佈訊息。 深入了解 [本節](alerts.md).

1. 您現在可以按一下 **[!UICONTROL Publish]** 按鈕，或保留為草稿，稍後再發佈。 如需如何發佈訊息的詳細資訊，請參閱 [本節](publish-manage-message.md).

## 複製訊息

若要從現有訊息建立訊息，請使用 **[!UICONTROL Duplicate]** 按鈕。 所有設定和配置都將複製到新消息

![](assets/message-duplicate.png)

您可以在確認複製前重新命名訊息。

![](assets/message-duplicate-confirm.png)

建立新訊息後，確認訊息會顯示在視窗底部。

您也可以使用專用圖示，從訊息清單複製訊息。

![](assets/message-duplicate-from-list.png)

同樣的確認程式適用。
