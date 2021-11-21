---
title: 推播通知設定
description: 了解如何設定您的環境，以使用Journey Optimizer傳送推播通知
role: Admin
level: Intermediate
exl-id: 7099d44e-5d5d-4eef-9477-f68f4eaa1983
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1447'
ht-degree: 4%

---

# 設定推播通知頻道 {#push-notification-configuration}

[!DNL Journey Optimizer] 可讓您建立歷程並傳送訊息給目標對象。 開始傳送推播通知之前，請使用 [!DNL Journey Optimizer]，您必須確保行動應用程式上已部署設定和整合，以及 [!DNL Adobe Experience Platform] 和 [!DNL Adobe Experience Platform Launch]. 若要了解推播通知資料在 [!DNL Adobe Journey Optimizer] 請參閱 [本頁](push-gs.md).

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

建立行動應用程式之前，您必須先確定您擁有或指派正確的使用者權限，位於 **Adobe Experience Platform Launch**. 深入了解 [Adobe Experience Platform Launch檔案](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html){target=&quot;_blank&quot;}。

>[!CAUTION]
>
>推播設定必須由專家使用者執行。 根據您的實作模式和此實作中涉及的角色，您可能需要將完整的權限集指派給單一產品設定檔，或在應用程式開發人員與 **Adobe Journey Optimizer** 管理員。 深入了解 **Adobe Experience Platform Launch** 權限 [本檔案](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html#platform-launch-permissions){target=&quot;_blank&quot;}。

<!--ou need to your have access to perform following roles :

* Manage Datastreams
* Manage Client-side Properties
* Manage App Configurations
-->

要分配 **屬性** 和 **公司** 權限，請遵循下列步驟：

1. 存取 **[!DNL Admin Console]**.

1. 從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Adobe Experience Platform Launch]** 卡片。

   ![](assets/push_product_1.png)

1. 選取現有 **[!UICONTROL Product Profile]** 或使用 **[!UICONTROL New profile]** 按鈕。 了解如何建立新 **[!UICONTROL New profile]** 在 [Admin Console檔案](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui){target=&quot;_blank&quot;}。

1. 在&#x200B;**[!UICONTROL Permissions]**&#x200B;索引標籤中，選取&#x200B;**[!UICONTROL Property rights]**。

   ![](assets/push_product_2.png)

1. 按一下「**[!UICONTROL Add all]**」。這會將下列內容新增至您的產品設定檔：
   * **[!UICONTROL Approve]**
   * **[!UICONTROL Develop]**
   * **[!UICONTROL Manage Environments]**
   * **[!UICONTROL Manage Extensions]**
   * **[!UICONTROL Publish]**

   安裝和發佈Adobe Journey Optimizer擴充功能以及在Adobe Experience Platform Mobile SDK中發佈應用程式屬性時，需要具備這些權限。

1. 然後，選取 **[!UICONTROL Company rights]** 的下一頁。

   ![](assets/push_product_4.png)

1. 新增下列權限：

   * **[!UICONTROL Manage App Configurations]**
   * **[!UICONTROL Manage Properties]**

   行動應用程式開發人員若要在 **Adobe Experience Launch** 和定義中的推播通知預設集 **Adobe Journey Optimizer**.

   ![](assets/push_product_5.png)

1. 按一下「**[!UICONTROL Save]**」。

若要指派此 **[!UICONTROL Product profile]** 若為使用者，請遵循下列步驟：

1. 存取 **[!DNL Admin Console]**.

1. 從 **[!UICONTROL Products]** 頁簽，選擇 **[!UICONTROL Adobe Experience Platform Launch]** 卡片。

1. 選取您先前設定的&#x200B;**[!UICONTROL Product profile]**。

1. 在 **[!UICONTROL Users]** 索引標籤中，按一下 **[!UICONTROL Add user]**。

   ![](assets/push_product_6.png)

1. 輸入您的使用者名稱或電子郵件地址，然後選取使用者。 然後，按一下 **[!UICONTROL Save]**.

   >[!NOTE]
   >
   >如果使用者先前未在Admin Console中建立，請參閱 [新增使用者檔案](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)

### 設定您的應用程式

技術設定涉及應用程式開發人員與業務管理員之間的緊密協作。 開始傳送推播通知之前，請使用 [!DNL Journey Optimizer]，您需要定義Adobe Experience Platform Launch中的設定，並整合您的行動應用程式與Adobe Experience Platform Mobile SDK。

請遵循以下連結中詳述的實作步驟：

* 針對 **AppleiOS**:了解如何使用APN註冊您的應用 [Apple檔案](https://developer.apple.com/documentation/usernotifications/registering_your_app_with_apns){target=&quot;_blank&quot;}
* 針對 **Google Android**:了解如何在Android上設定Firebase雲端訊息用戶端應用程式，位於 [Google檔案](https://firebase.google.com/docs/cloud-messaging/android/client){target=&quot;_blank&quot;}

### 將您的行動應用程式與Adobe Experience Platform SDK整合

Adobe Experience Platform Mobile SDK透過Android和iOS相容的SDK，為您的行動裝置提供用戶端整合API。 追隨 [Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/getting-started/overview){target=&quot;_blank&quot;}以在您的應用程式中使用Adobe Experience Platform Mobile SDK進行設定。

到此結尾，您也應該已在Adobe Experience Platform Launch中建立並設定行動屬性。 您通常會為要管理的每個行動應用程式建立行動屬性。 了解如何在 [Adobe Experience Platform Launch檔案](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property){target=&quot;_blank&quot;}。


## 步驟1:在Adobe Experience Platform Launch中新增您的應用程式推送憑證 {#push-credentials-launch}

授予正確的使用者權限後，您現在需要在 [!DNL Adobe Experience Platform Launch].

必須註冊行動應用程式推播憑證，才能授權Adobe代表您傳送推播通知。 請參閱以下詳細步驟：

1. 從 [!DNL Adobe Experience Platform Launch]，請確定 **[!UICONTROL Client Side]** 中選取的值。

1. 選取 **[!UICONTROL App Configurations]** 標籤，然後按一下 **[!UICONTROL App Configuration]** 來建立新配置。

1. 輸入 **[!UICONTROL Name]** ，以取得設定。

1. 從 **[!UICONTROL Messaging Service Type]** 下拉式功能表，選取 **[!UICONTROL Messaging service type]** 以用於這些憑證。

   * **適用於Android**

      ![](assets/add-app-config-android.png)

      1. 提供 **[!UICONTROL App ID (Android package name)]**:通常封裝名稱為 `build.gradle` 檔案。

      1. 拖放FCM推播憑證。 如需如何取得推送憑證的詳細資訊，請參閱 [Google檔案](https://firebase.google.com/docs/admin/setup#initialize-sdk){target=&quot;_blank&quot;}。
   * **針對iOS**

      ![](assets/add-app-config-ios.png)

      1. 輸入行動應用程式 **套件Id** 在 **[!UICONTROL App ID (iOS Bundle ID)]** 欄位。 可在 **一般** 中的主要目標標籤 **XCode**.

      1. 拖放 **Apple推播通知驗證金鑰** Apple開發人員帳戶。 此金鑰可從 **憑證**, **識別碼** 和 **設定檔** 頁面。

      1. 提供 **索引鍵ID**. 這是在建立p8驗證金鑰期間指派的10個字元字串。 可在下方找到 **金鑰** 標籤 **憑證**, **識別碼** 和 **設定檔** 頁面。

      1. 提供 **團隊ID**. 這是字串值，可在「成員資格」頁簽下找到。


1. 按一下 **[!UICONTROL Save]** 來建立應用程式設定。

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

此 **Adobe Journey Optimizer擴充功能**  針對Adobe Experience Platform Mobile SDK可支援行動應用程式的推播通知，並協助您收集使用者推播代號，以及管理與Adobe Experience Platform服務的互動測量。

了解如何在中設定Journey Optimizer擴充功能 [Adobe Experience Platform Mobile SDK檔案](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-journey-optimizer){target=&quot;_blank&quot;}。


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

若要讓此歷程正常運作，您需要建立XDM結構。 如需詳細資訊，請參閱 [XDM檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html#schemas-and-data-ingestion){target=&quot;_blank&quot;}。

1. 在左側功能表中，瀏覽至 **[!UICONTROL Schemas]**.

1. 按一下 **[!UICONTROL Create schema]** 然後選取 **[!UICONTROL XDM ExperienceEvent]**.

   ![](assets/test_push_2.png)

1. 選擇「**[!UICONTROL Create a new field group]**」。

1. 輸入 **[!UICONTROL Display Name]** 和 **[!UICONTROL Description]**. 完成時，按一下 **[!UICONTROL Add field groups]**。有關如何建立欄位組的詳細資訊，請參閱 [XDM系統檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh-Hant){target=&quot;_blank&quot;}。


   ![](assets/test_push_4.png)

1. 在左側，選取架構。 在右窗格中，輸入架構名稱和說明。 為啟用此架構 **[!UICONTROL Profile]**.

   ![](assets/test_push_4b.png)


1. 在左側，選取欄位群組，然後按一下+圖示以建立新欄位。 在 **[!UICONTROL Field groups properties]**，在右側輸入 **[!UICONTROL Field name]**, **[!UICONTROL Display name]** 選取 **[!UICONTROL String]** as **[!UICONTROL Type]**.

   ![](assets/test_push_5.png)

1. 檢查 **[!UICONTROL Required]** 按一下 **[!UICONTROL Apply]**.

1. 按一下「**[!UICONTROL Save]**」。您的架構現在已建立，且可用於事件。

然後您需要設定事件。

1. 從首頁的左菜單的「管理」下，選擇 **[!UICONTROL Configurations]**. 點按 **[!UICONTROL Manage]** 在 **[!UICONTROL Events]** 區段來建立新事件。

1. 按一下 **[!UICONTROL Create Event]**，則會在畫面右側開啟事件設定窗格。

   ![](assets/test_push_6.png)

1. 輸入事件名稱。 您也可以新增說明。

1. 在 **[!UICONTROL Event ID type]** 欄位中，選取 **[!UICONTROL Rule Based]**。

1. 在 **[!UICONTROL Parameters]**，請選取您先前建立的結構。

   ![](assets/test_push_7.png)

1. 在欄位清單中，檢查是否已選取架構欄位群組中建立的欄位。

   ![](assets/test_push_7b.png)

1. 按一下 **[!UICONTROL Edit]** 在 **[!UICONTROL Event ID condition]** 欄位。 拖放您先前新增的欄位，以定義系統將使用的條件，以識別將觸發您歷程的事件。

   ![](assets/test_push_8.png)

1. 在此範例中，輸入在測試應用程式中觸發推播通知所需的語法 **訂購確認**.

   ![](assets/test_push_9.png)

1. 選擇 **[!UICONTROL ECID]** 作為 **[!UICONTROL Namespace]**.

1. 按一下 **[!UICONTROL Ok]**，之後 **[!UICONTROL Save]**。

您的事件現在已建立，現在可用於歷程中。

1. 在左側功能表中，按一下 **[!UICONTROL Journeys]**.

1. 按一下 **[!UICONTROL Create Journey]** 來建立新歷程。

1. 在右側顯示的設定窗格中，編輯歷程的屬性。了解更多資訊 [節](building-journeys/journey-gs.md#change-properties).

1. 首先，從 **[!UICONTROL Events]** 下拉式清單。

   ![](assets/test_push_11.png)

1. 從 **[!UICONTROL Actions]** 拖放 **[!UICONTROL Message]** 活動至您的歷程。

1. 選取先前建立的訊息。 如需如何建立推播通知的詳細資訊，請參閱 [頁面](create-message.md).

1. 拖放 **[!UICONTROL End]** 活動至您的歷程。

1. 按一下 **[!UICONTROL Test]** 切換為開始測試推播通知，然後按一下 **[!UICONTROL Trigger an event]**.

   ![](assets/test_push_12.png)

1. 在 **[!UICONTROL Key]** 欄位，然後輸入 **訂購確認** 在第二個欄位。

   ![](assets/test_push_13.png)

1. 按一下「**[!UICONTROL Send]**」。

您的事件將會觸發，而您會收到您的行動應用程式推播通知。

## 步驟4:建立推送訊息預設集{#message-preset}

在 [!DNL Adobe Experience Platform Launch]，您需要建立訊息預設集，才能傳送推播通知 **[!DNL Journey Optimizer]**.

了解如何建立和設定訊息預設集，位於 [本節](configuration/message-presets.md).

您現在可以使用Journey Optimizer傳送推播通知。

* 了解如何在 [本頁](create-push.md).
* 了解如何在 [本節](building-journeys/journeys-message.md).
