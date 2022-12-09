---
title: 建立應用程式內通知
description: 了解如何在Journey Optimizer中建立應用程式內訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# 建立應用程式內訊息 {#create-in-app}

## 建立促銷活動和應用程式內訊息{#create-in-app-in-a-campaign}

若要建立應用程式內訊息，請遵循下列步驟：

1. 存取 **[!UICONTROL Campaigns]** ，然後按一下 **[!UICONTROL Create campaign]**.

1. 在 **[!UICONTROL Properties]** 區段，指定您要執行促銷活動的時間。

1. 在 **[!UICONTROL Actions]** 區段，選擇 **[!UICONTROL In-app message]** 和 **[!UICONTROL App surface]** 先前已針對您的應用程式內訊息設定。 然後，按一下 **[!UICONTROL Create]**.

   [深入了解應用程式內設定](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 從 **[!UICONTROL Properties]** 區段，編輯您的促銷活動 **[!UICONTROL Title]** 和 **[!UICONTROL Description]**.

1. 若要將自訂或核心資料使用量標籤指派至登陸頁面，請選取 **[!UICONTROL Manage access]**. [深入了解](../administration/object-based-access.md).

1. 按一下 **[!UICONTROL Select audience]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。 [深入了解](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL Identity namespace]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [深入了解](../event/about-creating.md#select-the-namespace).

1. 選擇應用程式內訊息作用中時觸發的頻率：

   * **[!UICONTROL Show every time]**:在 **[!UICONTROL Mobile app trigger]** 下拉式清單中。
   * **[!UICONTROL Show once]**:只會在第一次選取事件時顯示此訊息， **[!UICONTROL Mobile app trigger]** 下拉式清單中。
   * **[!UICONTROL Show until click through]**:當 **[!UICONTROL Mobile app trigger]** 下拉式清單，直到SDK以「已點按」動作傳送interact事件為止。

1. 從 **[!UICONTROL Mobile app trigger]** 下拉式清單，選擇將觸發訊息的事件和條件：

   1. 從左側下拉式清單中，選取觸發訊息所需的事件。
   1. 從右下拉式清單中，選取所選事件所需的驗證。
   1. 按一下 **[!UICONTROL Add]** 按鈕。 然後，重複上述步驟。
   1. 選取事件的連結方式，例如選擇 **[!UICONTROL And]** 如果您想要 **both** 觸發為true，以便顯示或選擇訊息 **[!UICONTROL Or]** 如果您想要顯示訊息，如果 **heer** 觸發器是真的。

   ![](assets/in_app_create_3.png)

1. 從 **[!UICONTROL Mobile app trigger]**
下拉式清單。

   選擇觸發器後，您就會選擇要顯示應用程式內訊息的使用者動作。

   ![](assets/in_app_create_3.png)

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL Schedule]** 在 [本節](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您現在可以開始使用 **[!UICONTROL Edit content]** 按鈕。

   ![](assets/in_app_create_4.png)

## 傳送您的應用程式內訊息{#in-app-send}

### 在裝置上預覽 {#preview-device}

您可以在特定裝置中預覽應用程式內通知。

1. 按一下 **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. 從 **[!UICONTROL Connect to device]** 按一下 **[!UICONTROL Start]**.

1. 在 **[!UICONTROL Base URL]** 按一下 **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. 使用您的裝置掃描QR碼，然後輸入顯示的PIN碼。

您的應用程式內訊息現在可以直接在裝置上觸發，讓您在實際裝置上預覽和檢閱訊息。

### 檢閱並啟動您的應用程式內通知{#in-app-review}

建立應用程式內訊息，並定義及個人化其內容後，您就可以檢閱及啟用訊息。

若要執行此作業，請遵循下列步驟：

1. 使用 **[!UICONTROL Review to activate]** 按鈕以顯示訊息摘要。

   摘要可讓您視需要修改促銷活動，並檢查是否有任何參數不正確或遺失。

   ![](assets/in_app_create_5.png)

1. 檢查促銷活動是否已正確設定，然後按一下 **[!UICONTROL Activate]**.

您的促銷活動現在已啟用。 行銷活動中設定的應用程式內通知會立即傳送，或在指定日期傳送。

傳送後，您就可以在Campaign報表中測量應用程式內訊息的影響。 如需報告的詳細資訊，請參閱 [本節](inapp-report.md).

**相關主題：**

* [設計應用程式內訊息](design-in-app.md)
* [應用程式內報表](inapp-report.md)
* [應用程式內設定](inapp-configuration.md)
