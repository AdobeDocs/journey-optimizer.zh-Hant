---
title: 建立訊息
description: 瞭解如何建立郵件
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 186a43cd-c5eb-4de1-8713-95399d802d36
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 3%

---

# 建立訊息 {#create-message}

可從 **[!UICONTROL Messages]** 的下界。 所有消息均按發佈日期（對於已發佈消息）或建立日期（對於草稿消息）列出，排序。

>[!NOTE]
>
>用戶可以根據其產品配置檔案訪問、建立、編輯和/或發佈消息。 瞭解有關用戶權限的詳細資訊 [此部分](../administration/permissions.md)。

![](assets/messages-list.png)

使用 **[!UICONTROL Show recents]** 切換以將直接連結添加到您在過去5天內訪問的消息。

![](assets/show-recent-messages.png)

使用篩選器表徵圖僅顯示已起草、已發佈或正在發佈的消息。 您還可以在郵件標籤上搜索，如下所示：

![](assets/filter-messages.png)

## 建立新郵件 {#create-new-message}

要建立新消息，請執行以下步驟：

1. 訪問消息清單，然後按一下 **[!UICONTROL Create Message]**。

1. 定義消息屬性。

   ![](assets/create-message-properties.png)

   * 輸入 **[!UICONTROL Title]** （強制）及 **[!UICONTROL Description]**。

   * 選擇 **[!UICONTROL Message category]**:市場營銷或事務性。

   * 選擇 **[!UICONTROL Preset]** 的子菜單。

      預設包含根據您的品牌發送電子郵件和/或推送通知所需的所有參數。 [瞭解有關預設的更多資訊](../configuration/message-presets.md)。

   * 選擇要用於該消息的通道：電子郵件和/或推送通知。 必須至少選擇一個通道才能建立消息。
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

1. 使用左側的預覽部分控制消息的呈現，並使用test配置檔案檢查個性化設定。 如需詳細資訊，請參閱[本章節](preview.md)。

   ![](assets/messages-simple-preview.png)

1. 檢查編輯器上半部分的警報。  其中一些是簡單的警告，但其他警告可能會阻止您發佈消息。 瞭解詳情 [此部分](alerts.md)。

1. 您現在可以通過按一下 **[!UICONTROL Publish]** 按鈕，或者將其作為草稿保存並稍後發佈。 有關如何發佈消息的詳細資訊，請參閱 [此部分](publish-manage-message.md)。

## 複製消息 {#duplicate-message}

要從現有消息建立消息，請使用 **[!UICONTROL Duplicate]** 按鈕。 所有設定和配置都將複製到新消息

![](assets/message-duplicate.png)

您可以在確認複製之前更名消息。

![](assets/message-duplicate-confirm.png)

建立新消息後，窗口底部將顯示一條確認消息。

您還可以使用專用表徵圖從消息清單中複製消息。

![](assets/message-duplicate-from-list.png)

同樣的確認過程也適用。
