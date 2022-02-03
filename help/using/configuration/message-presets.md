---
title: 建立訊息預設集
description: 瞭解如何配置和監視消息預設
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: bbc2adabac63ffb813ea2630f29aec552fc3f4df
workflow-type: tm+mt
source-wordcount: '1684'
ht-degree: 1%

---

# 建立訊息預設集 {#message-presets-creation}

與 [!DNL Journey Optimizer]，您可以設定消息預設，這些預設定義電子郵件和推送通知消息所需的所有技術參數：電子郵件類型、發件人電子郵件和姓名、移動應用等。

>[!CAUTION]
>
> * 郵件預設配置僅限於「旅程管理員」。 [進一步了解](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 必須執行電子郵件配置和 [推送配置](../push-configuration.md) 建立消息預設之前的步驟。


一旦配置了消息預設，您就可以在從 **[!UICONTROL Presets]** 清單框。

➡️ [瞭解如何在此視頻中建立和使用電子郵件預設](#video-presets)

## 建立消息預設 {#create-message-preset}

要建立消息預設，請執行以下步驟：

1. 訪問 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** 菜單，然後按一下 **[!UICONTROL Create Message preset]**。

   ![](../assets/preset-create.png)

1. 輸入預設的名稱和說明（可選），然後選擇要配置的通道。

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

1. 配置 **電子郵件** 的子菜單。

   ![](../assets/preset-email.png)

   * 選擇將使用預設發送的消息類型： **事務性** 或 **營銷**

      >[!CAUTION]
      >
      > **事務性** 消息可以發送到從營銷通信中取消訂閱的配置檔案。 這些消息只能在特定的上下文中發送，例如，密碼重置、訂單狀態、傳遞通知。

   * 選擇要用於發送電子郵件的子域。 [進一步了解](about-subdomain-delegation.md)
   * 選擇要與預設關聯的IP池。 [進一步了解](ip-pools.md)
   * 輸入使用該預設發送的電子郵件的標頭參數。

      >[!CAUTION]
      >
      >電子郵件地址必須使用當前選定的 [委託子域](about-subdomain-delegation.md)。

      <!--CAUTION: Except for the **Reply to (forward email)** field-->

      * **[!UICONTROL Sender name]**:發件人的名稱，如您的品牌名稱。

      * **[!UICONTROL Sender email]**:要用於通信的電子郵件地址。 例如，如果委派的子域是 *營銷.luma.com*，您可以使用 *contact@marketing.luma.com*。

      * **[!UICONTROL Reply to (name)]**:收件人按一下 **答復** 按鈕。

      * **[!UICONTROL Reply to (email)]**:收件人按一下 **答復** 按鈕。 <!--The emails sent to this address will be forwarded to the **[!UICONTROL Reply to (forward email)]** address provided below. -->必須使用在委派子域上定義的地址(例如， *reply@marketing.luma.com*)，否則將刪除電子郵件。

      * **[!UICONTROL Error email]**:ISP在發送數天郵件（非同步綁定）後生成的所有錯誤都會在此地址上接收。

      <!--**[!UICONTROL Reply to (forward email)]**: All emails received by [!DNL Journey Optimizer] for the delegated subdomain will be forwarded to this email address. You can specify any address, except an email address defined on the delegated subdomain. For example, if the delegated subdomain is *marketing.luma.com*, any address like *abc@marketing.luma.com* is prohibited.-->

      >[!NOTE]
      >
      >從2021年10月的發行版起，再也不能從 [!DNL Journey Optimizer] 用戶介面。 如果要接收的所有電子郵件 [!DNL Journey Optimizer] 要將委託的子域轉發到特定電子郵件地址，請與 [Adobe客戶服務支援團隊](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。 <!--move to Deprecated features section when created?-->

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >名稱必須以字母(A-Z)開頭。 它只能包含字母數字字元。 您還可以使用下划線 `_`，點`.` 連字元 `-` 字元。

   * 配置 **電子郵件重試參數**。 預設情況下， [重試時間](retries.md#retry-duration) 設定為84小時，但您可以調整此設定以更好地滿足您的需要。

      ![](../assets/preset-retry-paramaters.png)

      必須在以下範圍內輸入整數值（以小時或分鐘為單位）:
      * 對於市場營銷電子郵件類型，最短重試週期為6小時。
      * 對於事務性電子郵件類型，最小重試週期為10分鐘。
      * 對於這兩種電子郵件類型，最大重試時間為84小時（或5040分鐘）。


1. 配置 **推送通知** 的子菜單。

   ![](../assets/preset-push.png)

   * 至少選擇一個平台： **iOS** 和/或 **安卓**

   * 選擇要用於每個平台的移動應用程式。

      有關如何配置環境以發送推送通知的詳細資訊，請參閱 [此部分](../push-gs.md)。

<!--
1. Configure the **SMS** settings.

     ![](../assets/preset-sms.png)

    * Select the **[!UICONTROL SMS Type]** that will be sent with the preset: **[!UICONTROL Transactional]** or **[!UICONTROL Marketing]**
    
    * Select the **[!UICONTROL SMS configuration]** to associate with the preset.
        
      For more on how to configure your environment to send SMS messages, refer to [this section](sms-configuration.md).

    * Enter the **[!UICONTROL Sender number]** ​you want to use for your communications.
-->

1. 配置完所有參數後，按一下 **[!UICONTROL Submit]** 確認。 您也可以將消息預設保存為草稿，並稍後恢復其配置。

   ![](../assets/preset-submit.png)

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

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 監視消息預設 {#monitor-message-presets}

所有郵件預設都顯示在 **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** 的子菜單。 篩選器可幫助您瀏覽清單（通道類型、用戶、狀態）。

![](../assets/preset-filters.png)

消息預設可具有以下狀態：

* **[!UICONTROL Draft]**:消息預設已保存為草稿，但尚未提交。 開啟它以恢復配置。
* **[!UICONTROL Processing]**:消息預設已提交，正在執行幾個驗證步驟。
* **[!UICONTROL Active]**:已驗證消息預設，可以選擇該預設以建立消息。
* **[!UICONTROL Failed]**:在消息預設驗證期間，一個或多個檢查失敗。
* **[!UICONTROL Deactivated]**:消息預設被停用。 不能用於建立新郵件。

如果消息預設建立失敗，則下面將介紹每種可能失敗原因的詳細資訊。

如果出現其中一個錯誤，請與 [Adobe客戶服務支援團隊](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以獲取幫助。

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

   ![](../assets/preset-name.png)

1. 根據需要編輯其屬性。

   >[!NOTE]
   >
   >如果消息預設具有 **[!UICONTROL Active]** 狀態， **[!UICONTROL Name]**。 **[!UICONTROL Select channel]** 和 **[!UICONTROL Subdomain]** 欄位呈灰色，無法編輯。

1. 按一下 **[!UICONTROL Submit]** 確認更改。

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >您還可以將消息預設保存為草稿，稍後繼續更新。

提交更改後，消息預設將經過與當時的驗證週期類似的驗證週期 [建立預設](#create-message-preset)。

>[!NOTE]
>
>如果僅編輯 **[!UICONTROL Description]**。 **[!UICONTROL Email type]** 和/或 **[!UICONTROL Email retry parameters]** 欄位，更新是即時的。

對於具有 **[!UICONTROL Active]** 狀態，您可以檢查更新的詳細資訊。 若要這麼做：

* 按一下 **[!UICONTROL Recent update]** 表徵圖。

   ![](../assets/preset-recent-update-icon.png)

* 您還可以在進行更新時從活動消息預設訪問更新詳細資訊。

   ![](../assets/preset-view-update-details.png)

在 **[!UICONTROL Recent update]** 螢幕上，您可以查看更新狀態、<!--the approximate remaining time before completion (if validation is in progress)--> 和請求的更改清單。

![](../assets/preset-recent-update-screen.png)

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

處理時間在 **48小時–72小時**，並且 **7-10個工作日**。 瞭解有關在驗證週期中執行的檢查的詳細資訊，請參閱 [此部分](#create-message-preset)。

如果編輯已處於活動狀態的預設：

* 其地位仍然 **[!UICONTROL Active]** 正在驗證進程。

* 的 **[!UICONTROL Recent update]** 表徵圖顯示在消息預設清單中預設的名稱旁邊。

* 在驗證過程中，使用此預設配置的消息仍在使用該預設的舊版本。

>[!NOTE]
>
>更新正在進行時，無法修改消息預設。 您仍然可以按一下其名稱，但所有欄位都呈灰色顯示。 在更新成功之前，不會反映更改。

### 成功

驗證過程成功後，使用此預設的所有消息中將自動使用新版本的預設。 但是，您可能必須等待：
* 在被統一消息消耗前幾分鐘，
* 直到預設在批消息中生效的下一個批。

<!--Changes made to a message preset with the **[!UICONTROL Active]** status will automatically be applied to all messages currently using this preset.-->

### 已失敗

如果驗證過程失敗，則仍將使用預設的舊版本。

<!--The possible update error types are as follows:
* **Authorization error**: the bearer token is invalid or not authorized.
* **Illegal modification**: an edit was performed on one or more non-allowed fields.
* **Precondition failed**: some fields can only have specific values and this has not been honored.-->

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

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>無法刪除停用的郵件預設以避免使用這些預設來發送郵件的行程中的任何問題。

不能直接編輯已停用的消息預設。 但是，您可以複製該副本並編輯該副本，以建立將用於建立新郵件的新版本。 您也可以再次激活它，並等待更新成功編輯它。

![](../assets/preset-activate.png)

<!--1. Access the message presets list.

1. Deactivate the message preset that you want to edit.

1. Duplicate the deactivated message preset. A copy with the **[!UICONTROL Draft]** status is automatically added to the list.

    ![](../assets/preset-duplicated.png)

1. Open the duplicated message preset, modify it according to your needs, then submit your changes. The message preset will go through the same validation cycle as during the [creation step](#create-message-preset).

1. Once validated, it gets the **[!UICONTROL Active]** status and is ready to be used to create new messages.-->

## How-to視頻{#video-presets}

瞭解如何建立消息預設、如何使用這些預設以及如何委託子域和建立IP池。

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
