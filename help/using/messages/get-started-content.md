---
title: 開始使用訊息
description: 瞭解如何在 Journey Optimizer 建立訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 15%

---

# 開始使用訊息 {#get-started-contents-messages}

使用 [!DNL Journey Optimizer] 在單一位置運用多種資源 (如資產和內容)，並建立和發佈個人化推播通知和電子郵件訊息。

* 運用[!DNL Journey Optimizer] **電子郵件設計功能**&#x200B;建立或匯入回應式電子郵件。

* 運用 **Adobe Experience Manager Assets Essentials** 建立您自己的資產資料庫，並豐富您的電子郵件。

* 根據客戶的設定檔屬性建立&#x200B;**個人化推播和電子郵件訊息**，以增強客戶體驗。

* 根據這些內容&#x200B;**建立推播和電子郵件訊息** ，然後發佈。

## 訪問消息 {#access-messages}

可從 **[!UICONTROL Messages]** 的下界。 所有消息均按發佈日期（對於已發佈消息）或建立日期（對於草稿消息）列出，排序。

>[!NOTE]
>
>用戶可以根據其產品配置檔案訪問、建立、編輯和/或發佈消息。 瞭解有關用戶權限的詳細資訊 [此部分](../administration/permissions.md)。

![](assets/messages-list.png)

* 使用 **[!UICONTROL Show recents]** 切換以將直接連結添加到您在過去5天內訪問的消息。

   ![](assets/show-recent-messages.png)

* 使用篩選器表徵圖僅顯示已起草、已發佈或正在發佈的消息。 您還可以在郵件標籤上搜索，如下所示：

   ![](assets/filter-messages.png)

* 您可以使用快速操作菜單中的專用表徵圖來存檔未使用的郵件以清除郵件清單。

   ![](assets/archive-message.png)

   使用篩選器表徵圖顯示所有已存檔的郵件，然後按一下 **[!UICONTROL Unarchive]** 表徵圖，從已存檔郵件清單中刪除項目。

   >[!NOTE]
   >
   >無法開啟存檔的郵件。 必須先取消存檔。

## 建立新郵件 {#create-new-message}

要建立新消息，請執行以下步驟：

1. 訪問消息清單，然後按一下 **[!UICONTROL Create Message]**。

1. 定義消息屬性。

   ![](assets/create-message-properties.png)

   * 輸入 **[!UICONTROL Title]** （強制）及 **[!UICONTROL Description]**。

   * 選擇 **[!UICONTROL Message category]**:市場營銷或事務性。

   * 選擇要用於該消息的通道：電子郵件和/或推送通知。 必須至少選擇一個通道才能建立消息。

   * 選擇 **[!UICONTROL Preset]** 的子菜單。

      預設包含根據您的品牌發送電子郵件和/或推送通知所需的所有參數。 [瞭解有關預設的更多資訊](../configuration/message-presets.md)。
   >[!CAUTION]
   >
   >必須為所選類別和頻道選擇有效的消息預設。

   請注意，您可以隨時使用 **[!UICONTROL Properties]** 按鈕。

1. 按一下 **[!UICONTROL Create]** 確認消息建立。 您的消息將添加到消息清單中， **[!UICONTROL Draft]** 狀態。

   每個選定頻道都可使用一個頁籤。 使用這些頁籤為每個頻道配置內容。 通過選擇頁籤並按一下 **[!UICONTROL Delete channel]** 按鈕。

   ![](assets/create-messages-content.png)

   您現在可以建立消息的內容並調整設定。 有關電子郵件和推送通知配置的詳細資訊，請參見以下各節：

   * [建立電子郵件](create-email.md)
   * [建立推送通知](create-push.md)

   >[!NOTE]
   >   
   >可以使用表達式編輯器使用配置檔案的資料個性化您的消息。 有關個性化的詳細資訊，請參閱 [此部分](../personalization/personalize.md)。

1. 使用左側的預覽部分控制消息的呈現，並使用test配置檔案檢查個性化設定。 如需詳細資訊，請參閱[本章節](../design/preview.md)。

   ![](assets/messages-simple-preview.png)

1. 檢查編輯器上半部分的警報。  其中一些是簡單的警告，但其他警告可能會阻止您發佈消息。 瞭解詳情 [此部分](alerts.md)。

1. 您現在可以通過按一下 **[!UICONTROL Publish]** 按鈕，或者將其作為草稿保存並稍後發佈。 有關如何發佈消息的詳細資訊，請參閱 [此部分](publish-manage-message.md)。

## 複製消息 {#duplicate-message}

要從現有消息建立消息，請執行以下步驟。

1. 開啟要複製的郵件。

1. 使用 **[!UICONTROL Duplicate]** 按鈕。

   ![](assets/message-duplicate.png)

   所有設定和配置都將複製到新消息中。

1. 您可以在確認複製之前更名消息。

   ![](assets/message-duplicate-confirm.png)

1. 建立新消息後，窗口底部將顯示一條確認消息。

也可以使用快速操作菜單中的專用表徵圖從消息清單中複製消息。

![](assets/message-duplicate-from-list.png)

同樣的確認過程也適用。

