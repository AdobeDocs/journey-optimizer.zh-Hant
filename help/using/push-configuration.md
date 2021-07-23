---
title: 推播通知設定
description: 了解如何設定您的環境，以使用Journey Optimizer傳送推播通知
feature: 應用程式設定
topic: 推播
role: Admin
level: Intermediate
source-git-commit: ac6ba317909c962a81c7043bfa2a56e94bc5c9ad
workflow-type: tm+mt
source-wordcount: '1450'
ht-degree: 4%

---

# 設定推播通知頻道 {#push-notification-configuration}

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。開始使用[!DNL Journey Optimizer]傳送推播通知前，您必須確定已在行動應用程式、[!DNL Adobe Experience Platform]和[!DNL Adobe Experience Platform Launch]中部署設定和整合。 若要了解[!DNL Adobe Journey Optimizer]中的推播通知資料流程，請參閱[本頁面](push-gs.md)。

## 開始之前

<!--
### Check provisioning

Your Adobe Experience Platform account must be provisioned to contain following schemas and datasets for push notification data flow to function correctly:

| Schema <br>Dataset                                                                       | Group of fields                                                                                                                                                                         | Operation                                                |
| -------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| CJM Push Profile Schema <br>CJM Push Profile Dataset                                     | Push Notification Details<br>Adobe CJM ExperienceEvent - Message Profile Details<br>Adobe CJM ExperienceEvent - Message Execution Details<br>Application Details<br>Environment Details | Register Push Token                                      |
| CJM Push Tracking Experience Event Schema<br>CJM Push Tracking Experience Event Dataset | Push Notification Tracking                                                                                                                                                              | Track interactions and provide data for the reporting UI |
-->

### 設定權限

建立行動應用程式之前，您必須先確定在&#x200B;**Adobe Experience Platform Launch**&#x200B;中擁有或指派正確的使用者權限。 進一步了解[Adobe Experience Platform Launch檔案](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html){target=&quot;_blank&quot;}。

>[!CAUTION]
>
>推播設定必須由專家使用者執行。 根據您的實作模式和此實作中涉及的角色，您可能需要將完整的權限集指派給單一產品設定檔，或在應用程式開發人員與&#x200B;**Adobe Journey Optimizer**&#x200B;管理員之間共用權限。 深入了解[本檔案](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#platform-launch-permissions){target=&quot;_blank&quot;}中的&#x200B;**Adobe Experience Platform Launch**&#x200B;權限。

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

若要指派&#x200B;**Property**&#x200B;和&#x200B;**Company**&#x200B;權限，請遵循下列步驟：

1. 訪問&#x200B;**[!DNL Admin Console]**。

1. 從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

   ![](assets/push_product_1.png)

1. 選擇現有的&#x200B;**[!UICONTROL Product Profile]**&#x200B;或使用&#x200B;**[!UICONTROL New profile]**&#x200B;按鈕建立新的。 了解如何在[管理控制台檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target=&quot;_blank&quot;}中建立新的&#x200B;**[!UICONTROL New profile]**。

1. 在&#x200B;**[!UICONTROL Permissions]**&#x200B;索引標籤中，選取&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 按一下「**[!UICONTROL Add all]**」。這會將下列內容新增至您的產品設定檔：
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   安裝和發佈Adobe Journey Optimizer擴充功能以及在Adobe Experience Platform Mobile SDK中發佈應用程式屬性時，需要具備這些權限。

1. 然後，在左側菜單中選擇&#x200B;**[!UICONTROL Company rights]**。

   ![](assets/push_product_4.png)

1. 新增下列權限：

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   行動應用程式開發人員必須具備這些權限，才能在&#x200B;**Adobe Experience Launch**&#x200B;中設定推播憑證，並在&#x200B;**Adobe Journey Optimizer**&#x200B;中定義推播通知預設集。

   ![](assets/push_product_5.png)

1. 按一下「**[!UICONTROL Save]**」。

若要將此&#x200B;**[!UICONTROL Product profile]**&#x200B;指派給使用者，請遵循下列步驟：

1. 訪問&#x200B;**[!DNL Admin Console]**。

1. 從&#x200B;**[!UICONTROL Products]**&#x200B;標籤中，選擇&#x200B;**[!UICONTROL Adobe Experience Platform Launch]**&#x200B;卡。

1. 選取您先前設定的&#x200B;**[!UICONTROL Product profile]**。

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add user]**。

   ![](assets/push_product_6.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。 然後，按一下&#x200B;**[!UICONTROL Save]**。

   >[!NOTE]
   >
   >如果先前未在Admin Console中建立該使用者，請參閱[新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users)。

   ![](assets/push_product_7.png)

### 設定您的應用程式

技術設定涉及應用程式開發人員與業務管理員之間的緊密協作。 開始使用[!DNL Journey Optimizer]傳送推播通知前，您必須先在Adobe Experience Platform Launch中定義設定，並將您的行動應用程式與Adobe Experience Platform Mobile SDK整合。

請遵循以下連結中詳述的實作步驟：

* 對於&#x200B;**Apple iOS**:了解如何在[Apple檔案](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target=&quot;_blank&quot;}中使用APN註冊您的應用程式
* 對於&#x200B;**Google Android**:在[Google檔案](https://firebase.google.com/docs/cloud-messaging/android/client){target=&quot;_blank&quot;}中，了解如何在Android上設定Firebase雲端訊息用戶端應用程式

### 將您的行動應用程式與Adobe Experience Platform SDK整合

Adobe Experience Platform Mobile SDK透過Android和iOS相容的SDK，為您的行動裝置提供用戶端整合API。 請依照[Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/getting-started/overview){target=&quot;_blank&quot;}，在您的應用程式中使用Adobe Experience Platform Mobile SDK進行設定。

到此結尾，您也應該已在Adobe Experience Platform Launch中建立並設定行動屬性。 您通常會為要管理的每個行動應用程式建立行動屬性。 了解如何在[Adobe Experience Platform Launch檔案](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property){target=&quot;_blank&quot;}中建立和設定行動屬性。


## 步驟1:在Adobe Experience Platform Launch中新增您的應用程式推送憑證 {#push-credentials-launch}

授予正確的使用者權限後，您現在需要在[!DNL Adobe Experience Platform Launch]中新增行動應用程式推送憑證。

必須註冊行動應用程式推播憑證，才能授權Adobe代表您傳送推播通知。 請參閱以下詳細步驟：

1. 在[!DNL Adobe Experience Platform Launch]中，確認已在下拉式功能表中選取&#x200B;**[!UICONTROL Client Side]**。

1. 在左側面板中選擇&#x200B;**[!UICONTROL App Configurations]**&#x200B;頁簽，然後按一下&#x200B;**[!UICONTROL App Configuration]**&#x200B;以建立新配置。

1. 輸入配置的&#x200B;**[!UICONTROL Name]**。

1. 從&#x200B;**[!UICONTROL Messaging Service Type]**&#x200B;下拉式選單中，選擇要用於這些憑據的&#x200B;**[!UICONTROL Messaging service type]**。

   * **適用於Android**

      ![](assets/add-app-config-android.png)

      1. 提供&#x200B;**[!UICONTROL App ID (Android package name)]**:套件名稱通常是`build.gradle`檔案中的應用程式id。

      1. 拖放FCM推播憑證。 如需如何取得推送憑證的詳細資訊，請參閱[Google檔案](https://firebase.google.com/docs/admin/setup#initialize-sdk){target=&quot;_blank&quot;}。
   * **適用於iOS**

      ![](assets/add-app-config-ios.png)

      1. 在&#x200B;**[!UICONTROL App ID (iOS Bundle ID)]**&#x200B;欄位中輸入行動應用程式&#x200B;**套件組合Id**。 您可在&#x200B;**XCode**&#x200B;主要目標的&#x200B;**一般**&#x200B;標籤中找到應用程式套件ID。

      1. 拖放您Apple開發人員帳戶的&#x200B;**Apple推播通知驗證金鑰**。 可從&#x200B;**Certificates**、**Identifiers**&#x200B;和&#x200B;**Profiles**&#x200B;頁獲取此密鑰。

      1. 提供&#x200B;**密鑰ID**。 這是在建立p8驗證金鑰期間指派的10個字元字串。 您可以在&#x200B;**Certificates**、**Identifiers**&#x200B;和&#x200B;**Profiles**&#x200B;頁面的&#x200B;**Keys**&#x200B;標籤下找到。

      1. 提供&#x200B;**團隊ID**。 這是字串值，可在「成員資格」頁簽下找到。


1. 按一下&#x200B;**[!UICONTROL Save]**&#x200B;以建立您的應用程式配置。

<!--
## Step 2: Set up a mobile property in Adobe Experience Platform Launch {#launch-property}

Setting up a mobile property allows the mobile app developer or marketer to configure the mobile SDKs attributes such as Session Timeouts, the [!DNL Adobe Experience Platform] sandbox to be targeted and the **[!UICONTROL Adobe Experience Platform Datasets]** to be used for mobile SDK to send data to.

For further details and procedures on how to set up a **[!UICONTROL Platform Launch property]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).


To get the SDKs needed for push notification to work you will need the following SDK extensions, for both Android and iOS:

* **[!UICONTROL Mobile Core]** (installed automatically)
* **[!UICONTROL Profile]** (installed automatically)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, optional but recommended to debug the mobile implementation.

Learn more about [!DNL Adobe Experience Platform Launch] extensions in [Adobe Experience Platform Launch documentation](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).
-->

## 步驟2:在您的行動屬性中設定Adobe Journey Optimizer擴充功能

適用於Adobe Experience Platform Mobile SDK的&#x200B;**Adobe Journey Optimizer擴充功能**&#x200B;可支援行動應用程式的推播通知，並協助您收集使用者推播代號，以及管理與Adobe Experience Platform服務的互動測量。

了解如何在[Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target=&quot;_blank&quot;}中設定Journey Optimizer擴充功能。


<!-- 
**[!UICONTROL Edge configuration]** is used by **[!UICONTROL Edge]** extension to send custom data from mobile device to [!DNL Adobe Experience Platform]. 
To configure [!DNL Adobe Experience Platform], you must provide the **[!UICONTROL Sandbox]** name and **[!UICONTROL Event Dataset]**.

For further details and procedures on how to create **[!UICONTROL Edge configuration]**, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)



1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

<!--
## Step 4: Publish the Property {#publish-property}

You now need to publish the property to integrate your configuration and to use it in the mobile app. 

To publish your property, refer to the steps detailed in [Adobe Experience Platform Mobile SDK documentation](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

## Step 5: Configure the ProfileDataSource {#configure-profiledatasource}

To configure the `ProfileDataSource`, use the `ProfileDCInletURL` from [!DNL Adobe Experience Platform] setup and add the following in the mobile app:

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

-->

## 步驟3:使用事件測試您的行動應用程式 {#mobile-app-test}

在Adobe Experience Platform和AdobeLaunch中設定您的行動應用程式後，您現在可以先測試應用程式，再將推播通知傳送至您的設定檔。 在此使用案例中，我們將建立歷程來定位行動應用程式，並設定會觸發推播通知的事件。

<!--
You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).
-->

若要讓此歷程正常運作，您需要建立XDM結構。 如需詳細資訊，請參閱[XDM檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target=&quot;_blank&quot;}。

1. 在左側功能表中，瀏覽至&#x200B;**[!UICONTROL Schemas]**。

1. 按一下&#x200B;**[!UICONTROL Create schema]**，然後選擇&#x200B;**[!UICONTROL XDM ExperienceEvent]**。

   ![](assets/test_push_2.png)

1. 選擇「**[!UICONTROL Create a new field group]**」。

1. 輸入&#x200B;**[!UICONTROL Display Name]**&#x200B;和&#x200B;**[!UICONTROL Description]**。 完成時，按一下 **[!UICONTROL Add field groups]**。有關如何建立欄位組的詳細資訊，請參閱[XDM系統文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant){target=&quot;_blank&quot;}。


   ![](assets/test_push_4.png)

1. 在左側，選取架構。 在右窗格中，輸入架構名稱和說明。 為&#x200B;**[!UICONTROL Profile]**&#x200B;啟用此架構。

   ![](assets/test_push_4b.png)


1. 在左側，選取欄位群組，然後按一下+圖示以建立新欄位。 在&#x200B;**[!UICONTROL Field groups properties]**&#x200B;的右側，鍵入&#x200B;**[!UICONTROL Field name]**、**[!UICONTROL Display name]**，並選擇&#x200B;**[!UICONTROL String]**&#x200B;作為&#x200B;**[!UICONTROL Type]**。

   ![](assets/test_push_5.png)

1. 檢查&#x200B;**[!UICONTROL Required]**，然後按一下&#x200B;**[!UICONTROL Apply]**。

1. 按一下「**[!UICONTROL Save]**」。您的架構現在已建立，且可用於事件。

然後您需要設定事件。

1. 從首頁的左菜單的「管理」下，選擇&#x200B;**[!UICONTROL Configurations]**。 按一下&#x200B;**[!UICONTROL Events]**&#x200B;區段中的&#x200B;**[!UICONTROL Manage]**&#x200B;以建立新事件。

1. 按一下&#x200B;**[!UICONTROL Create Event]**，事件配置窗格就會在螢幕右側開啟。

   ![](assets/test_push_6.png)

1. 輸入事件名稱。 您也可以新增說明。

1. 在 **[!UICONTROL Event ID type]** 欄位中，選取 **[!UICONTROL Rule Based]**。

1. 在&#x200B;**[!UICONTROL Parameters]**&#x200B;中，選取您先前建立的架構。

   ![](assets/test_push_7.png)

1. 在欄位清單中，檢查是否已選取架構欄位群組中建立的欄位。

   ![](assets/test_push_7b.png)

1. 在&#x200B;**[!UICONTROL Event ID condition]**&#x200B;欄位中按一下&#x200B;**[!UICONTROL Edit]**。 拖放您先前新增的欄位，以定義系統將使用的條件，以識別將觸發您歷程的事件。

   ![](assets/test_push_8.png)

1. 在此範例中，輸入在測試應用程式中觸發推播通知所需的語法，**order confirmation**。

   ![](assets/test_push_9.png)

1. 選擇&#x200B;**[!UICONTROL ECID]**&#x200B;作為&#x200B;**[!UICONTROL Namespace]**。

1. 按一下 **[!UICONTROL Ok]**，之後 **[!UICONTROL Save]**。

您的事件現在已建立，現在可用於歷程中。

1. 在左側功能表中，按一下&#x200B;**[!UICONTROL Journeys]**。

1. 按一下&#x200B;**[!UICONTROL Create Journey]**&#x200B;以建立新歷程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。了解更多[小節](building-journeys/journey-gs.md#change-properties)。

1. 首先，從&#x200B;**[!UICONTROL Events]**&#x200B;下拉式清單中拖放先前步驟中建立的事件。

   ![](assets/test_push_11.png)

1. 從&#x200B;**[!UICONTROL Actions]**&#x200B;下拉式清單中，將&#x200B;**[!UICONTROL Message]**&#x200B;活動拖放至您的歷程。

1. 選取先前建立的訊息。 如需如何建立推播通知的詳細資訊，請參閱此[page](create-message.md)。

1. 將&#x200B;**[!UICONTROL End]**&#x200B;活動拖放至歷程。

1. 按一下&#x200B;**[!UICONTROL Test]**&#x200B;切換開始測試推播通知，然後按一下&#x200B;**[!UICONTROL Trigger an event]**。

   ![](assets/test_push_12.png)

1. 在&#x200B;**[!UICONTROL Key]**&#x200B;欄位中輸入ECID，然後在第二個欄位中輸入&#x200B;**訂單確認**。

   ![](assets/test_push_13.png)

1. 按一下「**[!UICONTROL Send]**」。

您的事件將會觸發，而您會收到您的行動應用程式推播通知。

## 步驟4:建立推送訊息預設集{#message-preset}

在[!DNL Adobe Experience Platform Launch]中設定您的行動應用程式後，您需要建立訊息預設集，才能從&#x200B;**[!DNL Journey Optimizer]**&#x200B;傳送推播通知。

了解如何在[此區段](configuration/message-presets.md)中建立和設定訊息預設集。

您現在可以使用Journey Optimizer傳送推播通知。

* 了解如何在[此頁面](create-push.md)中建立推送訊息。
* 了解如何在[此區段](building-journeys/journeys-message.md)的歷程中傳送新增訊息。
