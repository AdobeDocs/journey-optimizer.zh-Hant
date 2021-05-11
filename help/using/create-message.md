---
title: 建立訊息
description: 瞭解如何建立訊息
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '470'
ht-degree: 1%

---

# 建立消息{#create-message}

![](assets/do-not-localize/badge.png)

消息可從左側導軌上的&#x200B;**[!UICONTROL Messages]**&#x200B;快捷鍵獲得。 會列出所有訊息，依出版日期（針對發佈訊息）或建立日期（針對草稿訊息）排序。

>[!NOTE]
>
>每位使用者都可以存取、建立、編輯和發佈訊息。 在本節](permissions.md)中進一步瞭解使用者權限[。

![](assets/messages-list.png)

使用&#x200B;**[!UICONTROL Show recents]**&#x200B;切換，將直接連結新增至您最近5天記憶體取的訊息。

![](assets/show-recent-messages.png)

使用篩選圖示，只顯示已草擬、已發佈或正在發佈的訊息。 您也可以在訊息標籤上搜尋，如下所示：

![](assets/filter-messages.png)

## 建立新訊息

要建立新消息，請執行以下步驟：

1. 訪問消息清單，然後按一下&#x200B;**[!UICONTROL Create Message]**。

1. 定義消息屬性。

   ![](assets/create-message-properties.png)

   * 輸入&#x200B;**[!UICONTROL Title]**（必填）和&#x200B;**[!UICONTROL Description]**。

   * 選擇要用於消息的&#x200B;**[!UICONTROL Preset]**。

      預設集包含根據您的品牌傳送電子郵件及／或推播通知所需的所有參數。 [進一步瞭解品牌](administration.md#cjm-branding)。

   * 選取您要用於該訊息的頻道：電子郵件和／或推播通知。 您必須至少選擇一個渠道才能建立消息。
   請注意，您隨時都可以使用訊息介面中的&#x200B;**[!UICONTROL Properties]**&#x200B;按鈕來存取及修改訊息的標題、說明和預設集。

   ![](assets/message-properties.png)


1. 按一下&#x200B;**[!UICONTROL Create]**&#x200B;確認消息建立。 您的消息將添加到消息清單中，處於&#x200B;**[!UICONTROL Draft]**&#x200B;狀態。

   每個選取的頻道都有一個標籤。 使用這些標籤來設定每個頻道的內容。 您可以通過選擇頁籤並按一下右側的&#x200B;**[!UICONTROL Delete channel]**&#x200B;按鈕來刪除該頁籤。

   ![](assets/create-messages-content.png)

   您現在可以建立訊息的內容並調整設定。 以下各節提供有關電子郵件和推播通知設定的詳細資訊：

   * [設定電子郵件](configure-email.md)
   * [設定推播通知](configure-push.md)

   >[!NOTE]
   >   
   >您可以使用運算式編輯器使用描述檔資料個人化您的訊息。 如需個人化的詳細資訊，請參閱[本節](personalization/personalize.md)。


1. 使用左側的預覽區段，控制訊息的轉譯，並使用測試設定檔檢查個人化設定。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/messages-simple-preview.png)

1. 在編輯器的上半部分檢查警報。  其中有些是簡單的警告，但有些則會阻止您發佈訊息。 進一步瞭解[本節](alerts.md)。

1. 您現在可以按一下&#x200B;**[!UICONTROL Publish]**&#x200B;按鈕來發佈訊息，或保留為草稿，稍後再發佈。 有關如何發佈消息的詳細資訊，請參閱[本節](publish-manage-message.md)。

## 複製訊息

要從現有消息建立消息，請使用消息介面中的&#x200B;**[!UICONTROL Duplicate]**&#x200B;按鈕。 所有設定和設定都會複製到新訊息

![](assets/message-duplicate.png)

您可以在確認複製之前重新命名訊息。

![](assets/message-duplicate-confirm.png)

建立新訊息後，視窗底部會顯示確認訊息。

您也可以使用專用表徵圖從消息清單中複製消息。

![](assets/message-duplicate-from-list.png)

同樣的確認程式也適用。
