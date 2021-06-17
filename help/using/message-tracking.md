---
title: 追蹤您的訊息
description: 了解如何追蹤已傳送的訊息
feature: 監控
topic: 內容管理
role: User
level: Intermediate
source-git-commit: e27472cc6186cf7cb25fdb93d15720fc837c58bb
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---

# 訊息追蹤 {#tracking}

使用[!DNL Journey Optimizer]追蹤已傳送的訊息和收件者的行為。

## 啟用追蹤{#enable-tracking}

當[建立您的訊息](create-message.md)時，您可以檢查&#x200B;**[!UICONTROL Open Tracking for email]**&#x200B;和/或&#x200B;**[!UICONTROL Click Tracking for email]**&#x200B;選項，以啟用訊息層級的追蹤。

![](assets/message-tracking.png)

>[!NOTE]
>
>預設會啟用這兩個選項。

這可讓您透過以下方式追蹤收件者的行為：
* **[!UICONTROL Open Tracking for email]**:已開啟的訊息。
* **[!UICONTROL Click Tracking for email]**:點按電子郵件中的連結。

## 插入連結{#insert-links}

設計訊息時，您可以新增連結至內容。

>[!NOTE]
>
>當[追蹤啟用](#enable-tracking)時，會追蹤包含在訊息內容中的所有連結。

若要將連結插入電子郵件內容，請遵循下列步驟：

1. 選取元素，然後從內容工具列按一下&#x200B;**[!UICONTROL Insert link]**。

   ![](assets/message-tracking-insert-link.png)

1. 選擇要建立的連結類型：

   * **[!UICONTROL External link]**:插入外部URL的連結。

   * **[!UICONTROL Unsubscription link]**:插入連結以取消訂閱以免接收來自您品牌的通訊。進一步了解[本區段](consent.md#opt-out-management)中的選擇退出管理。

   * **[!UICONTROL Mirror page]**:插入連結以在網頁瀏覽器中顯示電子郵件內容。

   ![](assets/message-tracking-links.png)

1. 您只能使用簡單的運算式來個人化您的連結。 在[此區段](personalization/personalization-syntax.md)中深入了解個人化。

1. 儲存您的變更。

1. 建立連結後，您仍可從右側的&#x200B;**[!UICONTROL Component settings]**&#x200B;窗格修改該連結。

   * 按一下鉛筆圖示即可編輯連結。
   * 您可以核取對應的選項，選擇是否將連結加底線。

   ![](assets/message-tracking-link-settings.png)

## 管理追蹤{#manage-tracking}

[電子郵件設計工具](create-email-content.md)可讓您管理追蹤的URL，例如編輯每個連結的追蹤類型。

1. 按一下左窗格中的&#x200B;**[!UICONTROL Links]**&#x200B;圖示，以顯示要追蹤之內容的所有URL清單。

   此清單可讓您集中檢視，並找出電子郵件內容中的每個URL。

1. 若要編輯連結，請按一下對應的鉛筆圖示。

   ![](assets/message-tracking-edit-links.png)

1. 您可以視需要修改&#x200B;**[!UICONTROL Tracking Type]**:


   ![](assets/message-tracking-edit-a-link.png)

   對於每個追蹤的URL，您可以將追蹤模式設為下列其中一個值：

   * **[!UICONTROL Tracked]**:在此URL上啟用追蹤。
   * **[!UICONTROL Opt out]**:將此URL視為選擇退出或取消訂閱URL。
   * **[!UICONTROL Mirror page]**:將此URL視為鏡像頁面URL。
   * **[!UICONTROL Never]**:切勿啟用此URL的追蹤。  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

[Executions頁簽](message-monitoring.md)中列出已開啟的消息數和已點擊的連結數。

[電子郵件即時報表](reports/email-live-report.md)和[電子郵件全域報表](reports/email-global-report.md)中提供關於開啟和點按次數的報表。


