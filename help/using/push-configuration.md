---
title: 推播通知設定
description: 瞭解如何設定您的環境以傳送推播通知給Journey Optimizer
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 0%

---

# 推播通知設定{#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## 開始使用推播設定{#gs-push}

開始使用[!DNL Journey Optimizer]傳送推播通知之前，您必須先在[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中定義設定。

## Adobe Experience Platform設定{#platform-settings}

若要在[!DNL Adobe Experience Platform Launch]中設定您的行動應用程式，請依照下列步驟進行：

1. [分配財產和公司權利](#push-rights)
1. [在Platform launch中新增行動應用程式的推播憑證](#push-credentials-launch)。
1. [建立Edge](#edge-configuration) 設定，以便延伸功能 **[!UICONTROL Edge]** 用來將自訂資料從行動裝置傳送至 [!DNL Adobe Experience Platform]。
1. [設定Platform launch屬性](#launch-property)。
1. [發佈屬性](#publish-property)。
1. [設定ProfileDataSource](#configure-profiledatasource)。

### 步驟1:分配屬性和公司權利{#push-rights}

在建立行動應用程式之前，您必須先確定您擁有或指派正確的使用者權限。

有關[!DNL Adobe Experience Platform Launch]的用戶管理的詳細資訊，請參閱[Platform launch文檔](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions)。

要分配屬性和公司權利，請執行以下操作：

1. 訪問[!DNL Admin Console]。

1. 從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

   ![](assets/push_product_1.png)

1. 選擇現有的&#x200B;**[!UICONTROL Product Profile]**&#x200B;或使用&#x200B;**[!UICONTROL New profile]**&#x200B;按鈕建立新。 有關如何建立新&#x200B;**[!UICONTROL New profile]**&#x200B;的詳細資訊，請參閱[管理控制台文檔](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui)。

1. 從&#x200B;**[!UICONTROL Permissions]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 按一下「**[!UICONTROL Add all]**」。這會將下列權限新增至您的產品設定檔：
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   ![](assets/push_product_3.png)

1. 然後，在左側菜單中選擇&#x200B;**[!UICONTROL Company rights]**。

   ![](assets/push_product_4.png)

1. 新增下列權限：

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   ![](assets/push_product_5.png)

1. 按一下「**[!UICONTROL Save]**」。

要將此&#x200B;**[!UICONTROL Product profile]**&#x200B;分配給用戶：

1. 在[!DNL Admin Console]的&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

1. 選擇您先前配置的&#x200B;**[!UICONTROL Product profile]**。

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add user]**。

   ![](assets/push_product_6.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。 然後，按一下&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果先前未在管理控制台中建立使用者，請參閱[新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](assets/push_product_7.png)


您現在擁有在[!DNL Adobe Experience Platform Launch]中建立和設定行動應用程式的正確使用者權限。

### 步驟2:在{#push-credentials-launch}Platform launch中新增行動應用程式推播憑證

>[!NOTE]
>
> 若要在[!DNL Adobe Experience Platform Launch]中添加推播憑證，行動應用程式的擁有者應從APNs/FCM擷取憑證。

1. 在[!DNL Adobe Experience Platform Launch]中，確保在下拉菜單中選擇了&#x200B;**[!UICONTROL Client Side]**。

1. 在左側面板中選擇&#x200B;**[!UICONTROL App Configurations]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL App Configuration]**&#x200B;以建立新配置。

1. 為配置輸入&#x200B;**[!UICONTROL Name]**。

1. 從&#x200B;**[!UICONTROL Messaging Service Type]**&#x200B;下拉菜單中，選擇要用於這些憑據的&#x200B;**[!UICONTROL Messaging service type]**。 在此，我們選擇&#x200B;**[!UICONTROL Apple Push Notification Service]**，因為我們使用iOS。

1. 如果您使用Apple推播通知服務，請在&#x200B;**[!UICONTROL App ID (iOS Bundle ID)]**&#x200B;欄位中輸入行動應用程式&#x200B;**[!UICONTROL Bundle Id]**；如果您使用Firebase Cloud訊息，請在&#x200B;**[!UICONTROL App ID (Android package name)]**&#x200B;欄位中輸入。

   ![](assets/push_launch_app_configuration.png)

1. 將。p8金鑰檔案或。json私密金鑰檔案拖放至&#x200B;**[!UICONTROL Push Credentials]**&#x200B;欄位。

1. 如果您使用Apple推播通知服務，請輸入&#x200B;**[!UICONTROL Key Id]**&#x200B;和&#x200B;**[!UICONTROL Team Id]**。

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以建立您的應用程式設定。

### 步驟3:建立邊緣配置{#edge-configuration}

**[!UICONTROL Edge configuration]** 延伸功能會 **[!UICONTROL Edge]** 用來將自訂資料從行動裝置傳送至 [!DNL Adobe Experience Platform]。要配置[!DNL Adobe Experience Platform]，必須提供&#x200B;**[!UICONTROL Sandbox]**&#x200B;名稱和&#x200B;**[!UICONTROL Event Dataset]**。

1. 在[!DNL Adobe Experience Platform Launch]中，選擇&#x200B;**[!UICONTROL Edge Configurations]**&#x200B;頁籤，然後按一下&#x200B;**[!UICONTROL Edge Configurations]**。

1. 選擇&#x200B;**[!UICONTROL New Edge Configuration]**&#x200B;以添加新&#x200B;**[!UICONTROL Edge Configuration]**。
1. 輸入&#x200B;**[!UICONTROL Name]**&#x200B;並按一下&#x200B;**[!UICONTROL Save]**

1. 按一下&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;切換以啟用它。

1. 填寫&#x200B;**[!UICONTROL Sandbox]**、**[!UICONTROL Event dataset]**&#x200B;和&#x200B;**[!UICONTROL Profile Dataset]**&#x200B;欄位。 然後，按一下&#x200B;**[!UICONTROL Save]**。

   ![](assets/push-config-4.png)

### 步驟4:設定Platform launch屬性{#launch-property}

設定[!DNL Adobe Experience Platform Launch]屬性可讓行動應用程式開發人員或行銷人員設定行動SDK屬性，例如作業逾時、要定位的[!DNL Adobe Experience Platform]沙盒，以及要用於傳送資料至行動SDK的&#x200B;**[!UICONTROL Adobe Experience Platform Datasets]**。

1. 在[!DNL Adobe Experience Platform Launch]中，確保在下拉菜單中選擇了&#x200B;**[!UICONTROL Client Side]**。

1. 選擇&#x200B;**[!UICONTROL Properties]**&#x200B;頁籤，然後按一下&#x200B;**[!UICONTROL New Property]**。

   ![](assets/push-config-6.png)

1. 為新屬性輸入&#x200B;**[!UICONTROL Name]**。

1. 選擇&#x200B;**[!UICONTROL Mobile]**&#x200B;作為&#x200B;**[!UICONTROL Platform]**。

   ![](assets/push-config-7.png)

1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以建立新屬性。

若要取得推播通知所需的SDK，您需要下列Android和iOS的SDK擴充功能：

* **[!UICONTROL Mobile Core]** （自動安裝）
* **[!UICONTROL Profile]** （自動安裝）
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**，可選，但建議對行動實作進行除錯。

若要進一步瞭解[!DNL Adobe Experience Platform Launch]擴充功能，請參閱[Platform launch檔案](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html)。

若要設定&#x200B;**[!UICONTROL Adobe Experience Platform Edge Extension]**&#x200B;將自訂資料從行動裝置傳送至[!DNL Adobe Experience Platform]。

1. 選擇您先前建立的屬性，然後選擇&#x200B;**[!UICONTROL Extensions]**&#x200B;頁籤以查看此屬性的副檔名。

   ![](assets/push-config-8.png)

1. 按一下&#x200B;**[!UICONTROL Adobe Experience Platform Edge]**&#x200B;網路副檔名下的&#x200B;**[!UICONTROL Configure]**。

1. 從&#x200B;**[!UICONTROL Edge Configuration]**&#x200B;下拉式清單中，選取在前述步驟中建立的&#x200B;**[!UICONTROL Edge Configuration]**。 有關&#x200B;**[!UICONTROL Edge Configuration]**&#x200B;的詳細資訊，請參閱[部分](#edge-configuration)。

1. 按一下「**[!UICONTROL Save]**」。

若要設定&#x200B;**[!UICONTROL Adobe Experience Platform Messaging]**&#x200B;擴充功能，將推播設定檔和推播互動傳送至正確的資料集，請遵循上述相同步驟。 使用在[Adobe Experience Platform設定](#edge-configuration)中建立的&#x200B;**[!UICONTROL Sandbox]**、**[!UICONTROL Event dataset]**&#x200B;和&#x200B;**[!UICONTROL  Profile Dataset]**。

### 步驟5:發佈屬性{#publish-property}

您現在需要發佈屬性，以整合您的設定，並在行動應用程式中使用。
若要發佈您的屬性，請參閱[Adobe Experience Platform行動SDK檔案](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)中詳細說明的步驟

### 步驟6:配置ProfileDataSource {#configure-profiledatasource}

若要設定`ProfileDataSource`，請使用[!DNL Adobe Experience Platform]設定中的`ProfileDCInletURL`，並在行動應用程式中新增下列項目：

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->
