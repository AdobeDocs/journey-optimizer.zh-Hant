---
title: 建立訊息預設集
description: 了解如何建立電子郵件和推播通知訊息預設集
source-git-commit: 4353b8f01bb4e47f6f2384e464341c0ee80ecaf2
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# 建立訊息預設集

透過[!DNL Journey Optimizer]，您可以設定訊息預設集，以定義電子郵件和推播通知訊息（電子郵件類型、寄件者電子郵件和名稱、行動應用程式等）所需的所有技術參數。

您可以視需要溝通的不同品牌，視需要設定任意數量的訊息預設集。

在配置消息預設集後，從&#x200B;**[!UICONTROL Presets]**&#x200B;清單建立消息時，可以選擇它們。

## 建立訊息預設集{#create-message-preset}

若要建立訊息預設集，請依照下列步驟操作：

1. 訪問&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Message presets]**&#x200B;菜單，然後按一下&#x200B;**[!UICONTROL Create Message preset]**。

   ![](../assets/preset-create.png)

1. 提供預設集的名稱和說明（選用），然後指定您要設定的通道。

   ![](../assets/preset-general.png)

1. 配置電子郵件和推播通知設定：

   對於電子郵件通道，請指定：

   * 隨預設集（交易式或行銷訊息）傳送的通訊類型，
   * 用於傳送電子郵件的[子網域](about-subdomain-delegation.md)
   * 要與預設集關聯的[IP池](ip-pools.md),
   * 使用預設集傳送之電子郵件的標題參數。

   ![](../assets/preset-email.png)

   針對推播通知通道，指定要用於訊息的IOS和/或Android行動應用程式。 如需如何設定您的環境以傳送推播通知的詳細資訊，請參閱[此區段](../push-configuration.md)。

   ![](../assets/preset-push.png)

1. 配置所有參數後，按一下&#x200B;**[!UICONTROL Submit]**&#x200B;進行確認。 您也可以將訊息預設集儲存為草稿，稍後繼續其設定。

   ![](../assets/preset-submit.png)

1. 建立訊息預設集後，該預設集會顯示在狀態為&#x200B;**[!UICONTROL Processing]**&#x200B;的清單中。

   在此步驟中，將執行數項檢查，以確認其已正確設定。 處理時間在48-72h之間，最長可能需要7-10天。

   這些檢查包括由Adobe傳遞團隊執行的傳遞能力測試：

   * SPF驗證，
   * DKIM驗證，
   * MX記錄驗證，
   * 檢查IP黑名單，
   * 主機檢查，
   * IP池驗證，
   * A/PTR記錄，t/m/res子域驗證。

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
   >無法刪除已停用的訊息預設集，以避免在使用這些預設集來傳送訊息的歷程中發生任何問題。