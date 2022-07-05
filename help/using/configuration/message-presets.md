---
title: 設定訊息預設集
description: 瞭解如何配置和監視消息預設
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: ac3c49c16a2496b3d5bc9b803589644b69c6565c
workflow-type: tm+mt
source-wordcount: '1498'
ht-degree: 2%

---

# 設定訊息預設集 {#message-presets-creation}

與 [!DNL Journey Optimizer]，您可以設定消息預設，這些預設定義電子郵件和推送通知消息所需的所有技術參數：電子郵件類型、發件人電子郵件和姓名、移動應用等。

>[!CAUTION]
>
> * 要建立、編輯和刪除消息預設，必須具有 [管理郵件預設](../administration/high-low-permissions.md#manage-message-presets)。
>
> * 必須執行 [電子郵件配置](#configure-email-settings) 和 [推送配置](../configuration/push-configuration.md) 建立消息預設之前的步驟。


一旦配置了消息預設，您將能夠在從 **[!UICONTROL Presets]** 清單框。

➡️ [瞭解如何在此視頻中建立和使用電子郵件預設](#video-presets)

## 建立消息預設 {#create-message-preset}

>[!CONTEXTUALHELP]
>id="ajo_admin_message_presets"
>title="消息預設詳細資訊和設定"
>abstract="通過設定消息預設，您可以選擇它所應用的頻道，並定義您的消息所需的所有技術參數，如電子郵件類型、要使用的子域、發件人姓名、移動應用等。"

要建立消息預設，請執行以下步驟：

1. 訪問 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 菜單，然後按一下 **[!UICONTROL Create Message preset]**。

   ![](assets/preset-create.png)

1. 輸入預設的名稱和說明（可選），然後選擇要配置的通道。

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 配置 **電子郵件** 的子菜單。 [了解更多](#configure-email-settings)

1. 配置 **推送通知** 的子菜單。 [了解更多](#configure-push-settings)

1. 配置 **簡訊** 的子菜單。 [了解更多](sms-configuration.md)

1. 配置完所有參數後，按一下 **[!UICONTROL Submit]** 確認。 您也可以將消息預設保存為草稿，並稍後恢復其配置。

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >當所選IP池位於以下位置時，無法繼續建立預設 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL Processing]** 狀態)，且從未與所選子域關聯。 [了解更多](#subdomains-and-ip-pools)
   >
   >將預設另存為草稿，並等待IP池 **[!UICONTROL Success]** 狀態以繼續建立預設。

1. 建立消息預設後，它將顯示在清單中 **[!UICONTROL Processing]** 狀態。

   在此步驟中，將執行多項檢查，以驗證是否已正確配置了該步驟。 處理時間在 **48小時–72小時**，並且 **7-10個工作日**。

   這些檢查包括由Adobe團隊執行的配置和技術test:

   * SPF驗證
   * DKIM驗證
   * MX記錄驗證
   * 檢查IP密碼清單
   * Helo主機檢查
   * IP池驗證
   * A/PTR記錄， t/m/res子域驗證

   >[!NOTE]
   >
   >如果檢查不成功，請詳細瞭解中可能的失敗原因 [此部分](#monitor-message-presets)。

1. 檢查成功後，消息預設將獲取 **[!UICONTROL Active]** 狀態。 它已準備好用於傳遞消息。

   ![](assets/preset-active.png)

## 設定電子郵件設定 {#configure-email-settings}

電子郵件設定在消息預設配置的專用部分中定義。

![](assets/preset-email.png)

按中所述配置設定 [此部分](email-settings.md)。

## 配置推送設定 {#configure-push-settings}

推送設定在消息預設配置的專用部分中定義。

要定義與消息預設關聯的推送設定，請執行以下步驟：

1. 至少選擇一個平台： **iOS** 和/或 **安卓**。

1. 選擇要用於每個平台的移動應用程式。

![](assets/preset-push.png)

有關如何配置環境以發送推送通知的詳細資訊，請參閱 [此部分](../configuration/push-gs.md)。

<!--
## Configure SMS settings {#configure-sms-settings}

1. Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**.

    ![](assets/preset-sms.png)
    
1. Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
    For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

1. Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

## 監視消息預設 {#monitor-message-presets}

所有郵件預設都顯示在 **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** 的子菜單。 篩選器可幫助您瀏覽清單（通道類型、用戶、狀態）。

![](assets/preset-filters.png)

建立消息預設後，可以具有以下狀態：

* **[!UICONTROL Draft]**:消息預設已保存為草稿，但尚未提交。 開啟它以恢復配置。
* **[!UICONTROL Processing]**:消息預設已提交，正在執行幾個驗證步驟。
* **[!UICONTROL Active]**:已驗證消息預設，可以選擇該預設以建立消息。
* **[!UICONTROL Failed]**:在消息預設驗證期間，一個或多個檢查失敗。
* **[!UICONTROL Deactivated]**:消息預設被停用。 不能用於建立新郵件。

如果消息預設建立失敗，則下面將介紹每種可能失敗原因的詳細資訊。

如果出現其中一個錯誤，請與 [Adobe客戶關懷](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以獲取幫助。

* **SPF驗證失敗**:SPF（發件人策略框架）是一種電子郵件身份驗證協定，它允許指定可從給定子域發送電子郵件的授權IP。 SPF驗證失敗意味著SPF記錄中的IP地址與用於向郵箱提供程式發送電子郵件的IP地址不匹配。

* **DKIM驗證失敗**:DKIM(DomainKeys Indifed Mail)允許收件人伺服器驗證所接收的郵件是否由關聯域的正版發件人發送，並且原始郵件的內容在發送過程中未被更改。 DKIM驗證失敗意味著接收郵件伺服器無法驗證郵件內容的真實性及其與發送域的關聯：

* **MX記錄驗證失敗**:MX(Mail eXchange)記錄驗證失敗意味著負責代表給定子域接受入站電子郵件的郵件伺服器配置不正確。

* **可交付性配置失敗**:可交付性配置可能會因以下原因而失敗：
   * 已分配IP的阻止清單
   * 無效 `helo` 名稱
   * 從IP發送的電子郵件，而不是在相應預設的IP池中指定的電子郵件
   * 無法將電子郵件發送到Gmail和Yahoo等主要ISP的收件箱

## 編輯消息預設 {#edit-message-preset}

要編輯消息預設，請執行以下步驟。

>[!NOTE]
>
>無法編輯 **[!UICONTROL Push notification settings]**。 如果僅為推送通知通道配置了消息預設，則不可編輯。

1. 從清單中，按一下消息預設名稱以將其開啟。

   ![](assets/preset-name.png)

1. 根據需要編輯其屬性。

   >[!NOTE]
   >
   >如果消息預設具有 **[!UICONTROL Active]** 狀態， **[!UICONTROL Name]**。 **[!UICONTROL Select channel]** 和 **[!UICONTROL Subdomain]** 欄位呈灰色，無法編輯。

1. 按一下 **[!UICONTROL Submit]** 確認更改。

   ![](assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >您還可以將消息預設保存為草稿，稍後繼續更新。

提交更改後，消息預設將經過與當時的驗證週期類似的驗證週期 [建立預設](#create-message-preset)。 編輯處理時間可能 **3小時**。

>[!NOTE]
>
>如果僅編輯 **[!UICONTROL Description]**。 **[!UICONTROL Email type]** 和/或 **[!UICONTROL Email retry parameters]** 欄位，更新是即時的。

對於具有 **[!UICONTROL Active]** 狀態，您可以檢查更新的詳細資訊。 若要這麼做：

* 按一下 **[!UICONTROL Recent update]** 表徵圖。

   ![](assets/preset-recent-update-icon.png)

* 您還可以在進行更新時從活動消息預設訪問更新詳細資訊。

   ![](assets/preset-view-update-details.png)

在 **[!UICONTROL Recent update]** 螢幕中，您可以查看更新狀態和請求的更改清單等資訊。

![](assets/preset-recent-update-screen.png)

### 更新狀態 {#update-statuses}

消息預設更新可具有以下狀態：

* **[!UICONTROL Processing]**:消息預設更新已提交，正在執行幾個驗證步驟。
* **[!UICONTROL Success]**:已驗證更新的消息預設，並且可以選擇該預設來建立消息。
* **[!UICONTROL Failed]**:在消息預設更新驗證期間，一個或多個檢查失敗。

每種狀態詳見下文。

### 正在處理

將執行多次可傳送性檢查，以驗證預設是否已正確更新。

>[!NOTE]
>
>如果僅編輯 **[!UICONTROL Description]**。 **[!UICONTROL Email type]** 和/或 **[!UICONTROL Email retry parameters]** 欄位，更新是即時的。

處理時間可能需要 **3小時**。 瞭解有關在驗證週期中執行的檢查的詳細資訊，請參閱 [此部分](#create-message-preset)。

如果編輯已處於活動狀態的預設：

* 其地位仍然 **[!UICONTROL Active]** 正在驗證進程。

* 的 **[!UICONTROL Recent update]** 表徵圖顯示在消息預設清單中預設的名稱旁邊。

* 在驗證過程中，使用此預設配置的消息仍在使用該預設的舊版本。

>[!NOTE]
>
>更新正在進行時，無法修改消息預設。 您仍然可以按一下其名稱，但所有欄位都呈灰色顯示。 在更新成功之前，不會反映更改。

### 成功 {#success}

驗證過程成功後，使用此預設的所有消息中將自動使用新版本的預設。 但是，您可能必須等待：
* 在被統一消息消耗前幾分鐘，
* 直到預設在批消息中生效的下一個批。

### 已失敗 {#failed}

如果驗證過程失敗，則仍將使用預設的舊版本。

瞭解有關中可能的失敗原因的詳細資訊 [此部分](#monitor-message-presets)。

更新失敗時，預設將再次變為可編輯。 您可以按一下其名稱並更新需要修復的設定。

## 停用消息預設 {#deactivate-preset}

要生成 **[!UICONTROL Active]** 消息預設不可用於建立新消息，您可以停用它。 但是，使用此預設的已發佈消息將不受影響，並將繼續工作。

>[!NOTE]
>
>無法在更新正在處理時停用消息預設。 必須等待更新成功或失敗。 瞭解更多 [編輯郵件預設](#edit-message-preset) 在 [更新狀態](#update-statuses)。

1. 訪問消息預設清單。

1. 對於所選的活動預設，按一下 **[!UICONTROL More actions]** 按鈕

1. 選擇「**[!UICONTROL Deactivate]**」。

   ![](assets/preset-deactivate.png)

>[!NOTE]
>
>無法刪除停用的郵件預設以避免使用這些預設來發送郵件的行程中的任何問題。

不能直接編輯已停用的消息預設。 但是，您可以複製該副本並編輯該副本，以建立將用於建立新郵件的新版本。 您也可以再次激活它，並等待更新成功編輯它。

![](assets/preset-activate.png)

## How-to視頻{#video-presets}

瞭解如何建立消息預設、如何使用這些預設以及如何委託子域和建立IP池。

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
