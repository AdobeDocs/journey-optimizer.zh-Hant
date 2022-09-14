---
title: 設定頻道介面
description: 了解如何配置和監視通道表面
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 59da1d75885ffc6f4b97e218ea131233c198a7ae
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

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

<!--New contextual help content for September release: A channel surface defines all the technical parameters required for your messages (email type, sender name, mobile apps, SMS configuration, etc.): once configured, you will be able to select it when creating actions from a journey or a campaign. Note that you must have the Manage channel surface permission to create, edit and delete channel surfaces.-->

要建立通道曲面，請執行以下步驟：

1. 存取 **[!UICONTROL 管道]** > **[!UICONTROL 品牌推廣]** > **[!UICONTROL 通道曲面]** ，然後按一下 **[!UICONTROL 建立通道曲面]**.

   ![](assets/preset-create.png)

1. 輸入曲面的名稱和說明（可選），然後選取要配置的通道。

   ![](assets/preset-general.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

1. 如果您選取 **[!UICONTROL 電子郵件]** 管道，如 [本節](email-settings.md).

   ![](assets/preset-email.png)

1. 若 **[!UICONTROL 推播通知]** 通道，選擇至少一個平台 —   **iOS** 和/或 **Android** -，以及用於每個平台的行動應用程式。

   ![](assets/preset-push.png)

   >[!NOTE]
   >
   >如需如何設定您的環境以傳送推播通知的詳細資訊，請參閱 [本節](push-gs.md).

1. 若 **[!UICONTROL 簡訊]** 管道，定義您的設定，詳見 [本節](sms-configuration.md#message-preset-sms).

   ![](assets/preset-sms.png)

   >[!NOTE]
   >
   >如需如何設定環境以傳送SMS訊息的詳細資訊，請參閱 [本節](sms-configuration.md).

1. 完成所有參數設定後，按一下 **[!UICONTROL 提交]** 確認。 也可以將通道曲面另存為草稿，並稍後恢復其配置。

   ![](assets/preset-submit.png)

   >[!NOTE]
   >
   >在所選IP池下時，無法繼續建立曲面 [版本](ip-pools.md#edit-ip-pool) (**[!UICONTROL 處理]** 狀態)，且從未與選取的子網域相關聯。 [了解更多](#subdomains-and-ip-pools)
   >
   >將曲面另存為草稿，然後等待IP池具有 **[!UICONTROL 成功]** 恢復曲面建立的狀態。

1. 建立通道曲面後，該曲面將顯示在清單中，其中 **[!UICONTROL 處理]** 狀態。

   在此步驟中，將執行數項檢查，以確認其已正確設定。 處理時間已到 **48h-72h**，並可以 **7-10個工作天**.

   這些檢查包括由Adobe團隊執行的設定和技術測試：

   * SPF驗證
   * DKIM驗證
   * MX記錄驗證
   * 檢查IP密碼清單
   * 主機檢查
   * IP池驗證
   * A/PTR記錄、t/m/res子域驗證

   >[!NOTE]
   >
   >如果檢查未成功，請進一步了解中可能的失敗原因。 [本節](#monitor-channel-surfaces).

1. 檢查成功後，通道曲面將獲取 **[!UICONTROL 作用中]** 狀態。 它已準備好用於傳送訊息。

   ![](assets/preset-active.png)

## 監視通道表面 {#monitor-channel-surfaces}

所有通道曲面都顯示在 **[!UICONTROL 管道]** > **[!UICONTROL 通道曲面]** 功能表。 篩選器可協助您瀏覽清單（管道、使用者、狀態）。

![](assets/preset-filters.png)

建立通道曲面後，其狀態如下：

* **[!UICONTROL 草稿]**:通道曲面已另存為草稿，但尚未提交。 開啟它以繼續設定。
* **[!UICONTROL 處理]**:通道表面已提交，正在執行數個驗證步驟。
* **[!UICONTROL 作用中]**:通道表面已驗證，可以選中以建立消息。
* **[!UICONTROL 失敗]**:在通道表面驗證期間，一個或多個檢查失敗。
* **[!UICONTROL 已停用]**:通道表面被停用。 它無法用於建立新郵件。

如果通道曲面建立失敗，下面將說明每個可能失敗原因的詳細資訊。

如果發生其中一個錯誤，請與 [Adobe客戶服務](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以取得協助。

* **SPF驗證失敗**:SPF（發件人策略框架）是一種電子郵件驗證協定，它允許指定可從給定子域發送電子郵件的授權IP。 SPF驗證失敗意味著SPF記錄中的IP地址與用於向郵箱提供程式發送電子郵件的IP地址不匹配。

* **DKIM驗證失敗**:DKIM(DomainKeys Indified Mail)允許接收伺服器驗證接收的郵件是由關聯域的正版發件人發送的，並且原始郵件的內容在其過程中沒有更改。 DKIM驗證失敗意味著接收郵件伺服器無法驗證郵件內容的真實性及其與發送域的關聯。

* **MX記錄驗證失敗**:MX(Mail eXchange)記錄驗證失敗表示代表指定子網域接受入站電子郵件的郵件伺服器未正確設定。

* **傳遞能力配置失敗**:傳遞能力配置可能會因下列原因而失敗：
   * 已分配IP的封鎖清單
   * 無效 `helo` 名稱
   * 從IP發送的電子郵件，而不是在相應表面的IP池中指定的IP
   * 無法傳送電子郵件至Gmail和Yahoo等主要ISP的收件匣

## 編輯通道曲面 {#edit-channel-surface}

要編輯通道曲面，請執行以下步驟。

>[!NOTE]
>
>您無法編輯 **[!UICONTROL 推播通知設定]**. 如果管道表面僅針對推播通知管道進行設定，則無法編輯。

1. 從清單中，按一下管道曲面名稱以開啟它。

   ![](assets/preset-name.png)

1. 視需要編輯其屬性。

   >[!NOTE]
   >
   >如果通道曲面具有 **[!UICONTROL 作用中]** 狀態、 **[!UICONTROL 名稱]**, **[!UICONTROL 選取通道]** 和 **[!UICONTROL 子網域]** 欄位會呈現灰色且無法編輯。

1. 按一下 **[!UICONTROL 提交]** 確認變更。

   >[!NOTE]
   >
   >也可以將通道曲面另存為草稿，並稍後繼續更新。

提交變更後，通道曲面會經過與原位置的驗證週期類似的驗證週期，當 [建立通道曲面](#create-channel-surface). 版本處理時間可能 **3小時**.

>[!NOTE]
>
>如果您只編輯 **[!UICONTROL 說明]**, **[!UICONTROL 電子郵件類型]** 和/或 **[!UICONTROL 電子郵件重試參數]** 欄位，更新即時。

### 更新詳細資訊 {#update-details}

對於具有 **[!UICONTROL 作用中]** 狀態，您可以檢查更新的詳細資訊。 若要這麼做：

按一下 **[!UICONTROL 最近更新]** 表徵圖，該表徵圖顯示在活動曲面名稱旁邊。

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
