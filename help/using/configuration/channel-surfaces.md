---
title: 設定頻道介面
description: 了解如何配置和監視通道表面
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 9e499fd6523e18ecb78e25b306c49f2fc0e4a7c9
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---

# 設定頻道介面 {#set-up-channel-surfaces}

使用 [!DNL Journey Optimizer]，您可以設定可定義訊息所需所有技術參數的通道曲面（即訊息預設集）:電子郵件類型、寄件者電子郵件和名稱、行動應用程式、SMS設定等。

>[!CAUTION]
>
> * 要建立、編輯和刪除通道曲面，必須具有 [管理通道表面](../administration/high-low-permissions.md#manage-channel-surface) 權限。
>
> * 您必須執行 [電子郵件設定](#configure-email-settings), [推送設定](../configuration/push-configuration.md) 和 [SMS設定](../configuration/sms-configuration.md) 建立通道曲面之前的步驟。


設定管道表面後，您就能在從歷程建立訊息時選取它們。

<!--
➡️ [Learn how to create and use email surfaces in this video](#video-presets)
-->

## 建立通道曲面 {#create-channel-surface}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets_header"
>title="通道表面設定"
>abstract="設定通道表面時，請選取其套用的通道，並定義訊息所需的所有技術參數，例如電子郵件類型、子網域、寄件者名稱、行動應用程式、SMS設定等。"

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="通道表面設定"
>abstract="設定通道表面時，請選取其套用的通道，並定義訊息所需的所有技術參數，例如電子郵件類型、寄件者名稱、行動應用程式、SMS設定等。"

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.

To create a channel surface, follow these steps:

1. Access the **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Channel surfaces]** menu, then click **[!UICONTROL Create channel surface]**.

    ![](assets/preset-create.png)

1. Enter a name and a description (optional) for the surface, then select the channel(s) to configure.

    ![](assets/preset-general.png)

    >[!NOTE]
    >
    > Names must begin with a letter (A-Z). It can only contain alpha-numeric characters. You can also use underscore `_`, dot`.` and hyphen `-` characters. 

1. If you selected the **[!UICONTROL Email]** channel, configure your settings as described in [this section](email-settings.md).

    ![](assets/preset-email.png)

1. For the **[!UICONTROL Push Notification]** channel, select at least one platform  -  **iOS** and/or **Android** -, and the mobile applications to use for each platform.

    ![](assets/preset-push.png)
        
    >[!NOTE]
    >
    >For more on how to configure your environment to send push notifications, refer to [this section](push-gs.md).

1. For the **[!UICONTROL SMS]** channel, define your settings as detailed in [this section](sms-configuration.md#message-preset-sms).

    ![](assets/preset-sms.png)

    >[!NOTE]
    >
    >For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Once all the parameters have been configured, click **[!UICONTROL Submit]** to confirm. You can also save the channel surface as draft and resume its configuration later on.

    ![](assets/preset-submit.png)

    >[!NOTE]
    >
    >You cannot proceed with surface creation while the selected IP pool is under [edition](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** status), and has never been associated with the selected subdomain. [Learn more](#subdomains-and-ip-pools)
    >
    >Save the surface as draft and wait until the IP pool has the **[!UICONTROL Success]** status to resume surface creation.
    
1. Once the channel surface has been created, it displays in the list with the **[!UICONTROL Processing]** status.

    During this step, several checks will be performed to verify that it has been configured properly. The processing time is around **48h-72h**, and can take up to **7-10 business days**.

    These checks include configuration and technical tests that are performed by the Adobe team:

    * SPF validation
    * DKIM validation
    * MX record validation
    * Check IPs denylisting
    * Helo host check
    * IP pool verification
    * A/PTR record, t/m/res subdomain verification

    >[!NOTE]
    >
    >If the checks are not successful, learn more on the possible failure reasons in [this section](#monitor-channel-surfaces).  

1. Once the checks are successful, the channel surface gets the **[!UICONTROL Active]** status. It is ready to be used to deliver messages.

    ![](assets/preset-active.png)

## Monitor channel surfaces {#monitor-channel-surfaces}

All your channel surfaces display in the **[!UICONTROL Channels]** > **[!UICONTROL Channel surfaces]** menu. Filters are available to help you browse through the list (channel, user, status).

![](assets/preset-filters.png)

Once created, channel surfaces can have the following statuses:

* **[!UICONTROL Draft]**: The channel surface has been saved as a draft and has not been submitted yet. Open it to resume the configuration.
* **[!UICONTROL Processing]**: The channel surface has been submitted and is going through several verifications steps.
* **[!UICONTROL Active]**: The channel surface has been verified and can be selected to create messages.
* **[!UICONTROL Failed]**: One or several checks have failed during the channel surface verification.
* **[!UICONTROL Deactivated]**: The channel surface is deactivated. It cannot be used to create new messages.

In case a channel surface creation fails, the details on each possible failure reason are described below.

If one of these errors occurs, contact [Adobe Customer Care](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target="_blank"} to get assistance.

* **SPF validation failed**: SPF (Sender Policy Framework) is an email authentication protocol that allows to specify authorized IPs that can send emails from a given subdomain. SPF validation failure means that the IP addresses in the SPF record do not match the IP addresses used for sending emails to the mailbox providers. 

* **DKIM validation failed**: DKIM (DomainKeys Identified Mail) allows the recipient server to verify that the received message was sent by the genuine sender of the associated domain and that the content of the original message was not altered on its way. DKIM validation failure means that the receiving mail servers are unable to verify the authenticity of the message content and its association with the sending domain.:

* **MX record validation failed**: MX (Mail eXchange) record validation failure means that the mail servers responsible for accepting inbound emails on behalf of a given subdomain are not correctly configured.

* **Deliverability configurations failed**: Deliverability configurations failure can happen due to any of the following reasons:
    * Blocklisting of the allocated IPs
    * Invalid `helo` name
    * Emails being sent from IPs other than the ones specified in the IP pool of the corresponding surface
    * Unable to deliver emails to inboxes of major ISPs like Gmail and Yahoo

## Edit a channel surface {#edit-channel-surface}

To edit a channel surface, follow the steps below.

>[!NOTE]
>
>You cannot edit the **[!UICONTROL Push notification settings]**. If a channel surface is only configured for the Push notification channel, it is not editable.

1. From the list, click a channel surface name to open it.

    ![](assets/preset-name.png)

1. Edit its properties as desired.

    >[!NOTE]
    >
    >If a channel surface has the **[!UICONTROL Active]** status, the **[!UICONTROL Name]**, **[!UICONTROL Select channel]** and **[!UICONTROL Subdomain]** fields are greyed out and cannot be edited.

1. Click **[!UICONTROL Submit]** to confirm your changes.

    >[!NOTE]
    >
    >You can also save the channel surface as draft and resume update later on.

Once the changes are submitted, the channel surface will go through a validation cycle similar to the one in place when [creating a channel surface](#create-channel-surface). The edition processing time can take up to **3 hours**.

>[!NOTE]
>
>If you only edit the **[!UICONTROL Description]**, **[!UICONTROL Email type]** and/or **[!UICONTROL Email retry parameters]** fields, the update is instantaneous.

### Update details {#update-details}

For channel surfaces that have the **[!UICONTROL Active]** status, you can check the details of the update. To do so:

Click the **[!UICONTROL Recent update]** icon that is displayed next to the active surface name.

![](assets/preset-recent-update-icon.png)

<!--You can also access the update details from an active channel surface while update is in progress.-->

在 **[!UICONTROL 最近更新]** 螢幕上，您可以看到更新狀態和請求更改清單等資訊。

<!--![](assets/preset-recent-update-screen.png)-->

### 更新狀態 {#update-statuses}

通道曲面更新可具有以下狀態：

* **[!UICONTROL 處理]**:通道表面更新已提交，且正在執行數個驗證步驟。
* **[!UICONTROL 成功]**:已驗證更新的通道表面，可以選擇它以建立消息。
* **[!UICONTROL 失敗]**:在通道表面更新驗證期間，一個或多個檢查失敗。

每個狀態的詳細資訊如下。

#### 正在處理 {#surface-processing}

將執行多項傳遞能力檢查，以驗證表面已正確更新。

>[!NOTE]
>
>如果您只編輯 **[!UICONTROL 說明]**, **[!UICONTROL 電子郵件類型]** 和/或 **[!UICONTROL 電子郵件重試參數]** 欄位，更新即時。

處理時間可能需要 **3小時**. 進一步了解在驗證週期期間執行的檢查，位於 [本節](#create-channel-surface).

如果編輯已處於活動狀態的曲面：

* 其地位仍然 **[!UICONTROL 作用中]** 當驗證程式進行中時。

* 此 **[!UICONTROL 最近更新]** 表徵圖顯示在「通道曲面」(channel surfaces)清單中曲面的名稱旁。

* 在驗證過程中，使用此曲面配置的消息仍使用較舊版本的曲面。

>[!NOTE]
>
>在進行更新時，無法修改通道曲面。 您仍可以按一下其名稱，但所有欄位都會呈現灰色。 更新成功前，不會反映變更。

#### 成功 {#success}

驗證過程成功後，使用此曲面的所有消息中將自動使用新版本的曲面。 不過，您可能必須等待：
* 在被統一消息使用前幾分鐘，
* 直到該曲面在批處理消息中的下一個批處理生效。

#### 已失敗 {#failed}

如果驗證過程失敗，則仍將使用較舊版本的曲面。

進一步了解 [本節](#monitor-channel-surfaces).

更新失敗時，曲面將重新變為可編輯狀態。 您可以按一下名稱，並更新需要修正的設定。

## 停用通道曲面 {#deactivate-a-surface}

若要將 **[!UICONTROL 作用中]** 通道表面無法建立新消息，您可以將其停用。 不過，目前使用此介面的歷程訊息將不會受影響，且會繼續運作。

>[!NOTE]
>
>在處理更新時，不能停用通道曲面。 必須等待更新成功或失敗。 深入了解 [編輯通道曲面](#edit-channel-surface) 和 [更新狀態](#update-statuses).

1. 訪問通道曲面清單。

1. 對於所選的活動曲面，按一下 **[!UICONTROL 更多動作]** 按鈕。

1. 選擇 **[!UICONTROL 停用]**.

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>無法刪除停用的管道介面，以避免使用這些介面來傳送訊息的歷程中出現任何問題。

不能直接編輯停用的通道曲面。 不過，您可以複製郵件並編輯復本，以建立將用來建立新訊息的新版本。 您也可以再次啟動，然後等到更新成功編輯為止。

![](assets/preset-activate.png)

<!--
## How-to video{#video-presets}

Learn how to create channel surfaces, how to use them and how to delegate a subdomain and create an IP pool.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
-->
