---
title: 登錄頁面使用案例
description: 探索Journey Optimizer中登錄頁面最常見的使用案例
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
source-git-commit: 4d564ff89a8cb6c6d76161f2e6cedf39d33e70a0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 登錄頁面使用案例

以下是您如何使用的範例 [!DNL Journey Optimizer] 登錄頁面，讓您的客戶選擇加入/退出，拒絕接收您的部分或全部通訊。

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## 訂閱服務 {#subscription-to-a-service}

以下提供讓收件者訂閱服務的主要步驟。

![](../assets/lp_subscription-uc.png)

例如，假設您下月組織一個活動，而且想要啟動事件註冊促銷活動，讓有興趣的客戶隨時更新該事件。

1. 建立事件註冊的訂閱清單。 深入了解 [訂閱清單](subscription-list.md)

1. [建立登錄頁面](create-lp.md)，可讓您的收件者註冊至您的事件。

1. 設定及設計註冊登錄頁面，包括訂閱清單的連結。 深入了解如何建立 [主要登陸頁面](create-lp.md#configure-primary-page)

1. 建立感謝頁面，收件者提交註冊表單後，就會向他們顯示該頁面。 深入了解 [登陸子頁面](create-lp.md#configure-subpages)

1. 建立電子郵件訊息。 深入了解 [建立訊息](../create-message.md)

1. [插入連結](../message-tracking.md#insert-links) 在您的訊息中。 選擇 **[!UICONTROL Landing page]** 作為 **[!UICONTROL Link type]** 並選擇 [登陸頁面](create-lp.md#configure-primary-page) 您為註冊而建立的。

   ![](../assets/lp_subscription-uc-link.png)

1. 儲存您的內容並[發佈您的訊息](../publish-manage-message.md)。

1. 透過 [歷程](../building-journeys/journey.md) 若要宣佈註冊，現在已開啟供您的事件使用，並將流量引至註冊登錄頁面。

   收到電子郵件後，如果您的收件者按一下登陸頁面的連結，就會將他們導向至感謝頁面，並將他們新增至訂閱清單。

1. 您可以傳送確認電子郵件給已註冊參加您活動的收件者。 若要這麼做，請使用 **[!UICONTROL Segment qualification]** 事件，並選取您建立作為區段的訂閱清單。

<!--The event registration's subscription list tracks the profiles who registered and you can send them targeted event updates.-->

## 選擇退出 {#opt-out}

若要讓收件者取消訂閱您的通訊內容，您可以在電子郵件中加入退出登錄頁面的連結。

進一步了解如何管理收件者的同意，以及為何這在 [本節](../consent.md).

### 選擇退出管理 {#opt-out-management}

為接收者提供取消訂閱來自品牌之通訊的能力為法律所規定。 深入了解 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html#regulations){target=&quot;_blank&quot;}。

因此，您必須在每封寄送給收件者的電子郵件中一律包含&#x200B;**取消訂閱連結**：

* 按一下此連結後，收件者會被導向至包含確認選擇退出按鈕的登陸頁面。
* 按一下選擇退出按鈕後，設定檔資料將會隨此資訊更新。

### 設定選擇退出 {#configure-opt-out}

若要讓訊息的收件者透過登錄頁面取消訂閱您的通訊，請遵循下列步驟。

1. 建置 [登陸頁面](create-lp.md). 使用登錄頁面特定 **[!UICONTROL Form]** 元件，定義 **[!UICONTROL Opt-out]** 複選框和選擇更新 **[!UICONTROL Channel (email)]**:會從您的所有通訊中選擇退出，而會在您的登陸頁面上勾選退出方塊的設定檔。 [了解更多](design-lp.md)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. 於[!DNL Journey Optimizer][建立訊息](../create-message.md)。

1. 選取內容中的文字，並 [插入連結](../message-tracking.md#insert-links) 使用內容工具列。 您也可以在按鈕上使用連結。

   ![](../assets/lp_opt-out-insert-link.png)

1. 從&#x200B;**[!UICONTROL Link type]**&#x200B;下拉式清單中選取 **[!UICONTROL Landing page]**。

1. 選取 [登陸頁面](create-lp.md#configure-primary-page) 您為選擇退出而建立的。

   ![](../assets/lp_opt-out-landing-page.png)

1. 按一下「**[!UICONTROL Save]**」。

1. 儲存您的內容並[發佈您的訊息](../publish-manage-message.md)。

1. 透過 [歷程](../building-journeys/journey.md).

1. 收到訊息後，如果收件者按一下取消訂閱連結，就會顯示您的登陸頁面。

   <!--![](../assets/lp_opt-out-lp-example.png)-->

1. 如果收件者按一下登錄頁面中的選擇退出連結，則會更新設定檔資料，除非再次訂閱，否則不會從您的品牌接收通訊。

   <!--The opted-out recipient is then redirected to a confirmation message screen indicating that opting out was successful.-->

   <!--![](../assets/lp_opt-out-confirmation-example.png)-->

若要檢查對應的設定檔選擇是否已更新，請前往 Experience Platform，並透過選取識別名稱空間和對應的識別值來存取設定檔。 了解更多 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}。

![](../assets/lp_opt-out-profile-choice.png)

在 **[!UICONTROL Attributes]** 標籤中，您可以看到 **[!UICONTROL choice]** 的值已變更為 **[!UICONTROL no]**。

<!--

### Other ways to opt out

You can also enable your recipients to unsubscribe whithout using landing pages.

* **One-click opt-out**

    You can add a one-click opt-out link into your email content. This will enable your recipients to quickly unsubscribe from your communications, without being redirected to a landing page where they need to confirm opting out. [Learn more](../message-tracking.md#one-click-opt-out-link)

* **Unsubscribe link in header**

    If the recipients' email client supports displaying an unsubscribe link in the email header, emails sent with [!DNL Journey Optimizer] automatically include this link. [Learn more](../consent.md#unsubscribe-email)
-->