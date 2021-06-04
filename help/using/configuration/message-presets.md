---
title: 建立訊息預設集
description: 了解如何設定和監視訊息預設集
source-git-commit: 5490a12f7babc7d615f22f919e58b8eff51cf79c
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# 建立訊息預設集

透過[!DNL Journey Optimizer]，您可以設定訊息預設集，以定義電子郵件和推播通知訊息所需的所有技術參數：電子郵件類型、寄件者電子郵件和名稱、行動應用程式等。

>[!CAUTION]
>
> 訊息預設集設定僅限於歷程管理員。 [了解更多](../administration/ootb-product-profiles.md#journey-administrator)



在配置消息預設集後，從&#x200B;**[!UICONTROL Presets]**&#x200B;清單建立消息時，可以選擇它們。

## 建立訊息預設集{#create-message-preset}

若要建立訊息預設集，請依照下列步驟操作：

1. 訪問&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Message presets]**&#x200B;菜單，然後按一下&#x200B;**[!UICONTROL Create Message preset]**。

   ![](../assets/preset-create.png)


1. 輸入預設集的名稱和說明（選用），然後選取要設定的通道。

   ![](../assets/preset-general.png)


   >[!NOTE]
   >
   > 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。

1. 配置&#x200B;**email**&#x200B;設定。

   ![](../assets/preset-email.png)

   * 選取將與預設集一併傳送的訊息類型：**交易式**&#x200B;或&#x200B;**行銷**

      >[!CAUTION]
      >
      > **** 交易式訊息可傳送給從行銷通訊取消訂閱的設定檔。這些訊息只能在特定內容中傳送，例如密碼重設、順序狀態、傳送通知。

   * 選取用來傳送電子郵件的子網域。 [了解更多](about-subdomain-delegation.md)
   * 選擇要與預設集關聯的IP池。 [了解更多](ip-pools.md)
   * 輸入使用預設集傳送之電子郵件的標題參數。

      >[!NOTE]
      >
      > * 名稱必須以字母(A-Z)開頭。 它只能包含英數字元。 您也可以使用底線`_`、點`.`和連字型大小`-`字元。
         > 
         > 
      * 除了&#x200B;**回覆（轉寄電子郵件）**&#x200B;之外，電子郵件地址網域必須使用目前選取的子網域。



1. 配置&#x200B;**推播通知**&#x200B;設定。

   ![](../assets/preset-push.png)

   * 至少選擇一個平台：**iOS**&#x200B;及/或&#x200B;**Android**

   * 選取用於每個平台的行動應用程式。

      如需如何設定您的環境以傳送推播通知的詳細資訊，請參閱[此區段](../push-configuration.md)。

1. 配置所有參數後，按一下&#x200B;**[!UICONTROL Submit]**&#x200B;進行確認。 您也可以將訊息預設集儲存為草稿，稍後繼續其設定。

   ![](../assets/preset-submit.png)

1. 建立訊息預設集後，該預設集會顯示在狀態為&#x200B;**[!UICONTROL Processing]**&#x200B;的清單中。

   在此步驟中，將執行數項檢查，以確認其已正確設定。 處理時間在&#x200B;**48h-72h**&#x200B;左右，最長可以是&#x200B;**7-10天**。

   這些檢查包括由Adobe傳遞團隊執行的傳遞能力測試：


   * SPF驗證
   * DKIM驗證
   * MX記錄驗證
   * 檢查IP密碼清單
   * 主機檢查
   * IP池驗證
   * A/PTR記錄、t/m/res子域驗證


1. 檢查成功後，訊息預設集會取得&#x200B;**[!UICONTROL Active]**&#x200B;狀態。 它已準備好用於傳送訊息。

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## 監視消息預設集

所有訊息預設集都會顯示在&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Message presets]**&#x200B;功能表中。 篩選器可協助您瀏覽清單（通道類型、使用者、狀態）。

![](../assets/preset-filters.png)

訊息預設集可以有下列狀態：

* **[!UICONTROL Draft]**:訊息預設集已儲存為草稿，但尚未提交。開啟它以繼續設定。
* **[!UICONTROL Processing]**:訊息預設集已提交，且正在執行數個驗證步驟。
* **[!UICONTROL Active]**:消息預設集已驗證，可以選擇建立消息。
* **[!UICONTROL Failed]**:在消息預設集驗證期間，一個或多個檢查失敗。
* **[!UICONTROL De-activated]**:消息預設集已取消激活。它無法用於建立新郵件。

## 編輯訊息預設集

若要編輯訊息預設集，您必須先將其停用，使其無法用於建立新訊息（使用此預設集發佈的訊息將不受影響，且會繼續運作）。 然後，您需要複製訊息預設集，以建立將用來建立新訊息的新版本：

1. 存取訊息預設集清單，然後停用您要編輯的訊息預設集。

   ![](../assets/preset-deactivate.png)

1. 複製已停用的訊息預設集。 狀態為&#x200B;**[!UICONTROL Draft]**&#x200B;的副本會自動添加到清單中。

   ![](../assets/preset-duplicated.png)

1. 開啟複製的訊息預設集，根據您的需求加以修改，然後提交您的變更。 訊息預設集將會執行與[建立步驟](#create-message-preset)期間相同的驗證週期。

1. 驗證後，它會取得&#x200B;**[!UICONTROL Active]**&#x200B;狀態，並準備好用於建立新訊息。

   >[!NOTE]
   >
   >無法刪除停用中的訊息預設集，以避免使用這些預設集傳送訊息的歷程中出現任何問題。

