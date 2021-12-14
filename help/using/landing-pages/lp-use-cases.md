---
title: 登錄頁面使用案例
description: 探索Journey Optimizer中登錄頁面最常見的使用案例
feature: Landing Pages
topic: Content Management
role: User
level: Intermediate
hidefromtoc: true
hide: true
exl-id: 8c00d783-54a3-45d9-bd8f-4dc58804d922
source-git-commit: 1db755ef3037ca743d86e229ab308e051bae8994
workflow-type: tm+mt
source-wordcount: '847'
ht-degree: 13%

---

# 登錄頁面使用案例

以下是一些可以使用的範例 [!DNL Journey Optimizer] 登錄頁面，讓您的客戶選擇加入/退出，拒絕接收您的部分或全部通訊。

<!--The main use cases are:
* Subscription to a service
* Opt-in
* Opt-out-->

## 訂閱服務 {#subscription-to-a-service}

最常見的使用案例之一是邀請客戶 [訂閱服務](subscription-list.md) （例如電子報或事件）。 主要步驟如下圖所示：

![](../assets/lp_subscription-uc.png)

例如，假設您下月組織一個活動，而您想要啟動事件註冊促銷活動<!--to keep your customers that are interested updated on that event-->. 為此，您將傳送電子郵件，其中包含登錄頁面的連結，可讓您的收件者註冊此事件。 註冊的用戶將添加到您為此目的建立的訂閱清單中。

### 設定登錄頁面

1. 建立事件註冊的訂閱清單，該清單將儲存註冊的用戶。 了解如何建立訂閱清單 [此處](subscription-list.md#define-subscription-list).

   ![](../assets/lp_subscription-uc-list.png)

1. [建立登錄頁面](create-lp.md) 讓收件者註冊您的事件。

1. 配置註冊 [主要登陸頁面](create-lp.md#configure-primary-page).

1. 設計 [登陸頁面內容](design-lp.md)，選取您建立的訂閱清單，以使用選取註冊核取方塊的設定檔來更新。

   ![](../assets/lp_subscription-uc-lp-list.png)

1. 建立「感謝」頁面，收件者提交註冊表單後，就會向收件者顯示該頁面。 了解如何設定登錄子頁面 [此處](create-lp.md#configure-subpages).

   ![](../assets/lp_subscription-uc-thanks.png)

1. [發佈](create-lp.md#publish) 登陸頁面。

1. [建立電子郵件訊息](../create-message.md) 宣佈您的活動現在已開放註冊。

1. [插入連結](../message-tracking.md#insert-links) 填入訊息內容。 選擇 **[!UICONTROL Landing page]** 作為 **[!UICONTROL Link type]** 並選擇 [登陸頁面](create-lp.md#configure-primary-page) 您為註冊而建立的。

   ![](../assets/lp_subscription-uc-link.png)

1. 儲存您的內容並[發佈您的訊息](../publish-manage-message.md)。

1. 透過 [歷程](../building-journeys/journey.md) 來引導流量至註冊登錄頁面。

   ![](../assets/lp_subscription-uc-journey.png)

   收到電子郵件後，如果您的收件者按一下登陸頁面的連結，會將他們導向至「感謝」頁面，並將他們新增至訂閱清單。

### 傳送確認電子郵件 {#send-confirmation-email}

此外，您也可以傳送確認電子郵件給已註冊參加您活動的收件者。 若要這麼做，請遵循下列步驟。

1. 建立其他 [歷程](../building-journeys/journey.md). 您可以按一下 **[!UICONTROL Create journey]** 按鈕。 深入了解 [此處](create-lp.md#configure-primary-page)

   ![](../assets/lp_subscription-uc-create-journey.png)

1. 展開 **[!UICONTROL Events]** 類別和拖放 **[!UICONTROL Segment Qualification]** 活動進入您的畫布。 深入了解 [此處](../building-journeys/segment-qualification-events.md)

1. 按一下 **[!UICONTROL Segment]** 欄位，然後選取您建立的訂閱清單。

   ![](../assets/lp_subscription-uc-confirm-journey.png)

1. 選取您選擇的確認電子郵件，並透過歷程傳送。

   ![](../assets/lp_subscription-uc-confirm-email.png)

所有註冊您事件的使用者都會收到確認電子郵件。

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

若要讓電子郵件的收件者透過登錄頁面取消訂閱您的通訊內容，請遵循下列步驟。

1. 建立您的登錄頁面。 [了解更多](create-lp.md)

1. 定義主要頁面。 [了解更多](create-lp.md#configure-primary-page)

1. [設計](design-lp.md) 主要頁面內容：使用登錄頁面特定 **[!UICONTROL Form]** 元件，定義 **[!UICONTROL Opt-out]** 複選框和選擇更新 **[!UICONTROL Channel (email)]**:會從您的所有通訊中選擇退出，而會在您的登陸頁面上勾選退出方塊的設定檔。

   ![](../assets/lp_opt-out-primary-lp.png)

   <!--You can also build your own landing page and host it on the third-party system of your choice. To keep?-->

1. 新增確認 [子頁面](create-lp.md#configure-subpages) 會顯示給提交表單的使用者。

   ![](../assets/lp_opt-out-subpage.png)

   >[!NOTE]
   >
   >請務必參考 **[!UICONTROL Form]** 元件 **[!UICONTROL Call to action]** 區段。 [了解更多](design-lp.md)

1. 設定並定義頁面內容後， [發佈](create-lp.md#publish) 登陸頁面。

   ![](../assets/lp_opt-out-publish.png)

1. [建立電子郵件訊息](../create-message.md) in [!DNL Journey Optimizer].

1. 選取內容中的文字，並 [插入連結](../message-tracking.md#insert-links) 使用內容工具列。 您也可以在按鈕上使用連結。

   ![](../assets/lp_opt-out-insert-link.png)

1. 選擇 **[!UICONTROL Landing page]** 從 **[!UICONTROL Link type]** 下拉式清單，然後選取 [登陸頁面](create-lp.md#configure-primary-page) 您為選擇退出而建立的。

   ![](../assets/lp_opt-out-landing-page.png)

1. 儲存您的內容並[發佈您的訊息](../publish-manage-message.md)。

1. 透過歷程傳送訊息。 [了解更多](../building-journeys/journey.md)。

1. 收到訊息後，如果收件者按一下電子郵件中的取消訂閱連結，則會顯示您的登錄頁面。

   ![](../assets/lp_opt-out-submit-form.png)

1. 在登錄頁面上，如果收件者核取方塊並提交表單：

   * 退出的收件者會重新導向至確認訊息畫面。

   * 設定檔資料會更新，除非再次訂閱，否則將不會從您的品牌接收通訊。

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
