---
title: 登錄頁使用案例
description: 在Journey Optimizer登錄頁中發現最常見的使用案例
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 17%

---

# 登錄頁使用案例 {#lp-use-cases}

下面是一些示例，說明如何使用 [!DNL Journey Optimizer] 登錄頁，讓您的客戶選擇接收部分或全部通信。

## 訂閱服務 {#subscription-to-a-service}

最常見的使用情形之一是邀請客戶 [訂閱服務](subscription-list.md) （例如新聞簡報或活動）。 主要步驟如下圖所示：

![](assets/lp_subscription-uc.png)

例如，假設您下個月組織一個活動，並且要啟動一個活動註冊活動<!--to keep your customers that are interested updated on that event-->。 為此，您將發送一封電子郵件，其中包括指向登錄頁的連結，該登錄頁將允許您的收件人註冊此事件。 註冊的用戶將被添加到為此目的建立的訂閱清單中。

### 設定登錄頁 {#set-up-lp}

1. 建立事件註冊的訂閱清單，該清單將儲存已註冊的用戶。 瞭解如何建立訂閱清單 [這裡](subscription-list.md#define-subscription-list)。

   ![](assets/lp_subscription-uc-list.png)

1. [建立登錄頁](create-lp.md) 允許收件人註冊您的活動。

   ![](assets/lp_create-lp-details.png)

1. 配置註冊 [主登錄頁](create-lp.md#configure-primary-page)。

1. 設計 [登錄頁內容](design-lp.md)，選擇您建立的訂閱清單，以使用選中註冊複選框的配置檔案更新它。

   ![](assets/lp_subscription-uc-lp-list.png)

1. 建立一個「感謝」頁面，在收件人提交註冊表後，該頁面將顯示給他們。 瞭解如何配置登錄子頁 [這裡](create-lp.md#configure-subpages)。

   ![](assets/lp_subscription-uc-thanks.png)

1. [發佈](create-lp.md#publish) 登錄頁。

1. [建立電子郵件](../messages/get-started-content.md) 以宣佈註冊現已開啟，您可以參加活動。

1. [插入連結](../design/message-tracking.md#insert-links) 內容。 選擇 **[!UICONTROL Landing page]** 的 **[!UICONTROL Link type]** 選擇 [登錄頁](create-lp.md#configure-primary-page) 為註冊而建立的。

   ![](assets/lp_subscription-uc-link.png)

   >[!NOTE]
   >
   >若要發佈消息，請確保您選擇的登錄頁尚未過期。 瞭解如何更新到期日期 [此部分](create-lp.md#configure-primary-page)。

1. 儲存您的內容並[發佈您的訊息](../messages/publish-manage-message.md)。

1. 通過 [旅程](../building-journeys/journey.md) 將流量驅動到註冊登錄頁。

   ![](assets/lp_subscription-uc-journey.png)

   收到電子郵件後，如果您的收件人按一下登錄頁的連結，他們將被定向到「感謝您」頁，並將被添加到訂閱清單。

### 發送確認電子郵件 {#send-confirmation-email}

此外，您還可以向註冊參加活動的收件人發送確認電子郵件。 為此，請執行以下步驟。

1. 建立其他 [旅程](../building-journeys/journey.md)。 通過按一下 **[!UICONTROL Create journey]** 按鈕 瞭解更多資訊 [這裡](create-lp.md#configure-primary-page)

   ![](assets/lp_subscription-uc-create-journey.png)

1. 展開 **[!UICONTROL Events]** 類別並刪除 **[!UICONTROL Segment Qualification]** 活動到畫布中。 瞭解更多資訊 [這裡](../building-journeys/segment-qualification-events.md)

1. 按一下 **[!UICONTROL Segment]** ，然後選擇您建立的訂閱清單。

   ![](assets/lp_subscription-uc-confirm-journey.png)

1. 選擇您選擇的確認電子郵件，並在旅程中發送。

   ![](assets/lp_subscription-uc-confirm-email.png)

所有為您的活動註冊的用戶都將收到確認電子郵件。

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 選擇退出 {#opt-out}

若要使您的收件人取消訂閱您的通信，您可以將指向「退出」登錄頁的連結添加到您的電子郵件中。

瞭解有關管理收件人同意的詳細資訊，以及為什麼在 [此部分](../messages/consent.md)。

### 選擇退出管理 {#opt-out-management}

法律規定必須讓收件者提供能夠取消訂閱來自品牌的通訊。 進一步了解 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hant){target=&quot;_blank&quot;} 中的適用法規。

因此，您必須在每封傳送給收件者的電子郵件中一律包含&#x200B;**取消訂閱連結**：

* 按一下此連結後，收件者會被導向至包含確認選擇退出按鈕的登陸頁面。
* 按一下「選擇退出」按鈕後，將使用此資訊更新配置檔案資料。

### 配置選擇退出 {#configure-opt-out}

要使電子郵件的收件人能夠通過登錄頁取消訂閱您的通信，請執行以下步驟。

1. 建立登錄頁。 [了解更多](create-lp.md)

1. 定義首頁。 [了解更多](create-lp.md#configure-primary-page)

1. [設計](design-lp.md) 主要頁面內容：使用登錄頁特定 **[!UICONTROL Form]** 元件，定義 **[!UICONTROL Opt-out]** 複選框，然後選擇更新 **[!UICONTROL Channel (email)]**:在登錄頁上選中「選擇退出」框的配置檔案將被從您的所有通信中選擇。

   ![](assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice.-->

1. 添加確認 [子頁](create-lp.md#configure-subpages) 顯示給提交表單的用戶。

   ![](assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >確保引用首頁中的子頁 **[!UICONTROL Call to action]** 的下界 **[!UICONTROL Form]** 元件。 [了解更多](design-lp.md)

1. 配置和定義頁面內容後， [發佈](create-lp.md#publish) 登錄頁。

   ![](assets/lp_opt-out-publish.png)

1. [建立電子郵件](../messages/get-started-content.md) 在 [!DNL Journey Optimizer]。

1. 選擇內容中的文字，並使用內容相關工具列[插入連結](../design/message-tracking.md#insert-links)。您還可以使用按鈕上的連結。

   ![](assets/lp_opt-out-insert-link.png)

1. 選擇 **[!UICONTROL Landing page]** 從 **[!UICONTROL Link type]** 下拉清單，然後選擇 [登錄頁](create-lp.md#configure-primary-page) 你為退出而創造的。

   ![](assets/lp_opt-out-landing-page.png)

   >[!NOTE]
   >
   >若要發佈消息，請確保您選擇的登錄頁尚未過期。 瞭解如何更新到期日期 [此部分](create-lp.md#configure-primary-page)。

1. 儲存您的內容並[發佈您的訊息](../messages/publish-manage-message.md)。

1. 在旅途中發送您的資訊。 [了解更多](../building-journeys/journey.md)。

1. 一旦收到消息，如果收件人按一下電子郵件中的取消訂閱連結，則會顯示登錄頁。

   ![](assets/lp_opt-out-submit-form.png)

   如果收件人選中該框並提交表單：

   * 已選擇的收件人將重定向到確認消息螢幕。

   * 配置檔案資料將更新，除非再次訂閱，否則將不會從您的品牌接收通信。

若要檢查對應的設定檔選擇是否已更新，請前往 Experience Platform，並透過選取識別名稱空間和對應的識別值來存取設定檔。 在 [Experience Platform 文件](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hant){target=&quot;_blank&quot;}中進一步瞭解。

![](assets/lp_opt-out-profile-choice.png)

在 **[!UICONTROL Attributes]** 頁籤，您可以看到 **[!UICONTROL choice]** 已更改為 **[!UICONTROL no]**。

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../messages/consent.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../messages/consent.md#unsubscribe-header)
-->
