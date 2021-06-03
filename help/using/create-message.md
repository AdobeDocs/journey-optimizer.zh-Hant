---
title: 建立訊息
description: 了解如何建立訊息
source-git-commit: d2928efec66cd42f86868449d0289a23c78dd7c1
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 2%

---

# 建立訊息{#create-message}

![](assets/do-not-localize/badge.png)

可從左側導覽的&#x200B;**[!UICONTROL Messages]**&#x200B;快捷鍵取得訊息。 會列出所有訊息，依發佈日期（針對已發佈訊息）或建立日期（針對草稿訊息）排序。

>[!NOTE]
>
>每位使用者都可以存取、建立、編輯和發佈訊息。 了解更多有關[的用戶權限，請參閱本節](../using/administration/permissions.md)。

![](assets/messages-list.png)

使用&#x200B;**[!UICONTROL Show recents]**&#x200B;切換，將直接連結新增至您過去5天記憶體取的訊息。

![](assets/show-recent-messages.png)

使用篩選表徵圖只顯示草稿、已發佈或正在發佈的消息。 您也可以搜尋訊息標籤，如下所示：

![](assets/filter-messages.png)

## 建立新訊息

若要建立新訊息，請遵循下列步驟：

1. 訪問消息清單，然後按一下&#x200B;**[!UICONTROL Create Message]**。

1. 定義訊息屬性。

   ![](assets/create-message-properties.png)

   * 輸入&#x200B;**[!UICONTROL Title]**（必填）和&#x200B;**[!UICONTROL Description]**。

   * 選取要用於訊息的&#x200B;**[!UICONTROL Preset]**。

      預設集包含根據您的品牌傳送電子郵件和/或推播通知所需的所有參數。 [進一步了解預設集](../using/configuration/message-presets.md)。

   * 選取您要用於該訊息的通道：電子郵件和/或推播通知。 您必須選取至少一個管道才能建立訊息。
   請注意，您隨時都可以使用訊息介面中的&#x200B;**[!UICONTROL Properties]**&#x200B;按鈕來存取及修改訊息的標題、說明和預設集。

   ![](assets/message-properties.png)


1. 按一下&#x200B;**[!UICONTROL Create]**&#x200B;以確認建立訊息。 您的訊息會新增至訊息清單中，且處於&#x200B;**[!UICONTROL Draft]**&#x200B;狀態。

   每個選取的通道都有一個索引標籤。 使用這些標籤來設定每個頻道的內容。 您可以選取索引標籤，然後按一下右側的&#x200B;**[!UICONTROL Delete channel]**&#x200B;按鈕，以移除該索引標籤。

   ![](assets/create-messages-content.png)

   您現在可以建立訊息的內容並調整設定。 以下章節提供電子郵件和推播通知設定的詳細資訊：

   * [建立電子郵件](create-email.md)
   * [建立推播通知](create-push.md)

   >[!NOTE]
   >   
   >您可以使用運算式編輯器，使用設定檔資料個人化您的訊息。 如需個人化的詳細資訊，請參閱[此區段](personalization/personalize.md)。


1. 使用左側的預覽區段，控制訊息的轉譯，並使用測試設定檔檢查個人化設定。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/messages-simple-preview.png)

1. 檢查編輯器上方區段的警報。  其中有些是簡單的警告，但有些警告可能會阻止您發佈訊息。 進一步了解[本節](alerts.md)。

1. 您現在可以按一下&#x200B;**[!UICONTROL Publish]**&#x200B;按鈕以發佈訊息，或保留訊息為草稿，稍後再發佈。 有關如何發佈消息的詳細資訊，請參閱[此部分](publish-manage-message.md)。

## 複製訊息

要從現有消息建立消息，請使用消息介面中的&#x200B;**[!UICONTROL Duplicate]**&#x200B;按鈕。 所有設定和配置都將複製到新消息

![](assets/message-duplicate.png)

您可以在確認複製前重新命名訊息。

![](assets/message-duplicate-confirm.png)

建立新訊息後，確認訊息會顯示在視窗底部。

您也可以使用專用圖示，從訊息清單複製訊息。

![](assets/message-duplicate-from-list.png)

同樣的確認程式適用。
