---
title: 建立訊息預設集
description: 了解如何設定和監視訊息預設集
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 9038528f-3da0-4e0e-9b82-b72c67b42391
source-git-commit: 2e91fc884ea6e83a2590c5beca7840a6fc4c9b78
workflow-type: tm+mt
source-wordcount: '1688'
ht-degree: 1%

---

# 建立訊息預設集

使用 [!DNL Journey Optimizer]，您可以設定訊息預設集，以定義電子郵件和推播通知訊息所需的所有技術參數：電子郵件類型、寄件者電子郵件和名稱、行動應用程式等。

>[!CAUTION]
>
> * 訊息預設集設定僅限於歷程管理員。 [了解更多](../administration/ootb-product-profiles.md#journey-administrator)
>
> * 您必須執行電子郵件設定， [推送設定](../push-configuration.md) 建立訊息預設集之前的步驟。


設定訊息預設集後，您就可以在從 **[!UICONTROL Presets]** 清單。

➡️ [了解如何在此影片中建立和使用電子郵件預設集](#video-presets)

## 建立訊息預設集 {#create-message-preset}

若要建立訊息預設集，請依照下列步驟操作：

1. 存取 **[!UICONTROL Channels]** > **[!UICONTROL Branding]** > **[!UICONTROL Message presets]** ，然後按一下 **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. 輸入預設集的名稱和說明（選用），然後選取要設定的通道。

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

1. 設定 **電子郵件** 設定。

   ![](../assets/preset-email.png)

   * 選取將與預設集一併傳送的訊息類型： **交易** 或 **行銷**

      >[!CAUTION]
      >
      > **交易** 可將訊息傳送給從行銷通訊取消訂閱的設定檔。 這些訊息只能在特定內容中傳送，例如密碼重設、順序狀態、傳送通知。

   * 選取用來傳送電子郵件的子網域。 [了解更多](about-subdomain-delegation.md)
   * 選擇要與預設集關聯的IP池。 [了解更多](ip-pools.md)
   * 輸入使用該預設集傳送之電子郵件的標題參數。

      >[!CAUTION]
      >
      >電子郵件地址必須使用目前選取的 [委派子網域](about-subdomain-delegation.md).

      <!--CAUTION: Except for the **Reply to (forward email)** field-->

      * **[!UICONTROL Sender name]**:寄件者的名稱，例如您的品牌名稱。

      * **[!UICONTROL Sender email]**:您要用於通訊的電子郵件地址。 例如，如果委派的子網域為 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com*.

      * **[!UICONTROL Reply to (name)]**:收件者點按 **回覆** 按鈕。

      * **[!UICONTROL Reply to (email)]**:收件者點按 **回覆** 按鈕。 <!--The emails sent to this address will be forwarded to the **[!UICONTROL Reply to (forward email)]** address provided below. -->您必須使用在委派子網域上定義的位址(例如 *reply@marketing.luma.com*)，否則會捨棄電子郵件。

      * **[!UICONTROL Error email]**:在傳送數天郵件（非同步退信）後，ISP產生的所有錯誤都會在此位址上接收。

      <!--**[!UICONTROL Reply to (forward email)]**: All emails received by [!DNL Journey Optimizer] for the delegated subdomain will be forwarded to this email address. You can specify any address, except an email address defined on the delegated subdomain. For example, if the delegated subdomain is *marketing.luma.com*, any address like *abc@marketing.luma.com* is prohibited.-->

      >[!NOTE]
      >
      >自2021年10月發行版本起，您無法再從 [!DNL Journey Optimizer] 使用者介面。 如果您想要收到 [!DNL Journey Optimizer] 若要將委派的子網域轉送至特定電子郵件地址，請聯絡 [Adobe客戶服務支援團隊](https://helpx.adobe.com/tw/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}。 <!--move to Deprecated features section when created?-->

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線 `_`，點`.` 連字型大小 `-` 字元。

   * 設定 **電子郵件重試參數**. 依預設， [重試時間段](retries.md#retry-duration) 設為84小時，但您可以調整此設定以更符合您的需求。

      ![](../assets/preset-retry-paramaters.png)

      您必須在以下範圍內輸入整數值（以小時或分鐘為單位）:
      * 對於行銷電子郵件類型，最低重試期間為6小時。
      * 對於交易式電子郵件類型，最低重試期間為10分鐘。
      * 對於這兩種電子郵件類型，最大重試時間為84小時（或5040分鐘）。


1. 設定 **推播通知** 設定。

   ![](../assets/preset-push.png)

   * 至少選擇一個平台： **iOS** 和/或 **Android**

   * 選取用於每個平台的行動應用程式。

      如需如何設定您的環境以傳送推播通知的詳細資訊，請參閱 [本節](../push-gs.md).

1. 完成所有參數設定後，按一下 **[!UICONTROL Submit]** 確認。 您也可以將訊息預設集儲存為草稿，稍後繼續其設定。

   ![](../assets/preset-submit.png)

1. 建立訊息預設集後，訊息預設集會顯示在清單中，並搭配 **[!UICONTROL Processing]** 狀態。

   在此步驟中，將執行數項檢查，以確認其已正確設定。 處理時間已到 **48h-72h**，並可以 **7-10個工作天**.

   這些檢查包括由Adobe傳遞團隊執行的傳遞能力測試：

   * SPF驗證
   * DKIM驗證
   * MX記錄驗證
   * 檢查IP密碼清單
   * 主機檢查
   * IP池驗證
   * A/PTR記錄、t/m/res子域驗證

   >[!NOTE]
   >
   >如果檢查未成功，請進一步了解中可能的失敗原因。 [本節](#monitor-message-presets).

1. 檢查成功後，訊息預設集會取得 **[!UICONTROL Active]** 狀態。 它已準備好用於傳送訊息。

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 監視消息預設集 {#monitor-message-presets}

所有訊息預設集都會顯示在 **[!UICONTROL Channels]** > **[!UICONTROL Message presets]** 功能表。 篩選器可協助您瀏覽清單（通道類型、使用者、狀態）。

![](../assets/preset-filters.png)

訊息預設集可以有下列狀態：

* **[!UICONTROL Draft]**:訊息預設集已儲存為草稿，但尚未提交。 開啟它以繼續設定。
* **[!UICONTROL Processing]**:訊息預設集已提交，且正在執行數個驗證步驟。
* **[!UICONTROL Active]**:消息預設集已驗證，可以選擇建立消息。
* **[!UICONTROL Failed]**:在消息預設集驗證期間，一個或多個檢查失敗。
* **[!UICONTROL Deactivated]**:訊息預設集已停用。 它無法用於建立新郵件。

如果訊息預設集建立失敗，以下說明每個可能失敗原因的詳細資訊。

如果發生其中一個錯誤，請與 [Adobe客戶服務支援團隊](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;}以取得協助。

* **SPF驗證失敗**:SPF（發件人策略框架）是一種電子郵件驗證協定，它允許指定可從給定子域發送電子郵件的授權IP。 SPF驗證失敗意味著SPF記錄中的IP地址與用於向郵箱提供程式發送電子郵件的IP地址不匹配。

* **DKIM驗證失敗**:DKIM(DomainKeys Indified Mail)允許接收伺服器驗證接收的郵件是由關聯域的正版發件人發送的，並且原始郵件的內容在其過程中沒有更改。 DKIM驗證失敗意味著接收郵件伺服器無法驗證郵件內容的真實性及其與發送域的關聯。

* **MX記錄驗證失敗**:MX(Mail eXchange)記錄驗證失敗表示代表指定子網域接受入站電子郵件的郵件伺服器未正確設定。

* **傳遞能力配置失敗**:傳遞能力配置可能會因下列原因而失敗：
   * 已分配IP的封鎖清單
   * 無效 `helo` 名稱
   * 從IP（不是相應預設集的IP池中指定的IP）發送的電子郵件
   * 無法傳送電子郵件至Gmail和Yahoo等主要ISP的收件匣

## 編輯訊息預設集 {#edit-message-preset}

若要編輯訊息預設集，請遵循下列步驟。

>[!NOTE]
>
>您無法編輯 **[!UICONTROL Push notification settings]**. 如果訊息預設集僅針對推播通知通道設定，則無法編輯。

1. 從清單中，按一下訊息預設集名稱以開啟它。

   ![](../assets/preset-name.png)

1. 視需要編輯其屬性。

   >[!NOTE]
   >
   >如果訊息預設集具有 **[!UICONTROL Active]** 狀態、 **[!UICONTROL Name]**, **[!UICONTROL Select channel]** 和 **[!UICONTROL Subdomain]** 欄位會呈現灰色且無法編輯。

1. 按一下 **[!UICONTROL Submit]** 確認變更。

   ![](../assets/preset-confirm-update.png)

   >[!NOTE]
   >
   >您也可以將訊息預設集儲存為草稿，稍後繼續更新。

提交變更後，訊息預設集將會經過類似下列情形的驗證週期： [建立預設集](#create-message-preset).

對於具有 **[!UICONTROL Active]** 狀態，您可以檢查更新的詳細資訊。 若要這麼做：

* 按一下 **[!UICONTROL Recent update]** 圖示顯示在使用中預設集名稱旁。

   ![](../assets/preset-recent-update-icon.png)

* 您也可以在進行更新時，從使用中的訊息預設集存取更新詳細資訊。

   ![](../assets/preset-view-update-details.png)

在 **[!UICONTROL Recent update]** 螢幕上，您可以看到更新狀態、<!--the approximate remaining time before completion (if validation is in progress)--> 和請求的更改清單。

![](../assets/preset-recent-update-screen.png)

### 更新狀態 {#update-statuses}

訊息預設集更新可能具有下列狀態：

* **[!UICONTROL Processing]**:訊息預設集更新已提交，正在執行數個驗證步驟。
* **[!UICONTROL Success]**:更新的消息預設集已驗證，可以選擇建立消息。
* **[!UICONTROL Failed]**:在消息預設集更新驗證期間，一個或多個檢查失敗。

**正在處理**

將執行數個傳遞能力檢查，以確認預設集已正確更新。 處理時間已到 **48h-72h**，並可以 **7-10個工作天**. 進一步了解在驗證週期期間執行的檢查，位於 [本節](#create-message-preset).

>[!NOTE]
>
>更新正在進行時，無法修改消息預設集。 您仍可以按一下其名稱，但所有欄位都會呈現灰色。 更新成功前，不會反映變更。

如果您編輯已啟用的預設集：

* 其地位仍然 **[!UICONTROL Active]** 當驗證程式進行中時。

* 此 **[!UICONTROL Recent update]** 圖示會顯示在訊息預設集清單中預設集的名稱旁。

* 在驗證程式期間，使用此預設集設定的訊息仍使用舊版預設集。

**成功**

驗證程式一旦成功，使用此預設集的所有訊息中都會自動使用新版本的預設集。 不過，您可能必須等待：
* 在被統一消息使用前幾分鐘，
* 直到預設集的下一個批次在批次訊息中生效為止。

<!--Changes made to a message preset with the **[!UICONTROL Active]** status will automatically be applied to all messages currently using this preset.-->

**已失敗**

如果驗證程式失敗，系統仍會使用舊版的預設集。

可能的更新錯誤類型如下：
* **授權錯誤**:承載令牌無效或未授權。
* **非法修改**:對一個或多個不允許的欄位執行了編輯。
* **先決條件失敗**:某些欄位只能有特定值，因此未執行。

<!--Learn more on the possible failure reasons in [this section](#monitor-message-presets).-->

更新失敗時，預設集會重新變成可編輯。 您可以按一下名稱，並更新需要修正的設定。

## 停用訊息預設集 {#deactivate-preset}

若要將 **[!UICONTROL Active]** 無法建立新消息的消息預設集，您可以將其停用。 不過，使用此預設集的已發佈訊息將不會受影響，且會繼續運作。

>[!NOTE]
>
>您無法在處理更新時停用訊息預設集。 必須等待更新成功或失敗。 深入了解 [編輯訊息預設集](#edit-message-preset) 和 [更新狀態](#update-statuses).

1. 訪問消息預設集清單。

1. 針對您選取的使用中預設集，按一下 **[!UICONTROL More actions]** 按鈕。

1. 選擇「**[!UICONTROL Deactivate]**」。

   ![](../assets/preset-deactivate.png)

>[!NOTE]
>
>無法刪除停用中的訊息預設集，以避免使用這些預設集傳送訊息的歷程中出現任何問題。

您無法直接編輯停用中的訊息預設集。 不過，您可以複製郵件並編輯復本，以建立將用來建立新訊息的新版本。 您也可以再次啟動，然後等到更新成功編輯為止。

![](../assets/preset-activate.png)

<!--1. Access the message presets list.

1. Deactivate the message preset that you want to edit.

1. Duplicate the deactivated message preset. A copy with the **[!UICONTROL Draft]** status is automatically added to the list.

    ![](../assets/preset-duplicated.png)

1. Open the duplicated message preset, modify it according to your needs, then submit your changes. The message preset will go through the same validation cycle as during the [creation step](#create-message-preset).

1. Once validated, it gets the **[!UICONTROL Active]** status and is ready to be used to create new messages.-->

## 作法影片{#video-presets}

了解如何建立訊息預設集、如何使用這些預設集，以及如何委派子網域和建立IP池。

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
