---
solution: Journey Orchestration
title: 關於自訂動作組態
description: 瞭解如何設定自訂動作
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 9%

---

# 設定動作 {#configure-an-action}

![](../assets/do-not-localize/badge.png)

如果您使用協力廠商系統來傳送訊息，或如果您想要歷程將API呼叫傳送至協力廠商系統，您可在此設定其與歷程的連線。 然後，技術使用者定義的自訂動作就會出現在您旅程的左側浮動視窗中，位於&#x200B;**[!UICONTROL Action]**&#x200B;類別（請參閱[本頁](../building-journeys/about-journey-activities.md#action-activities)）。 以下是一些您可以使用自訂動作來連接的系統範例：Epsilon、Facebook、Adobe.io、Firebase等。
限制列在[本頁](../building-journeys/limitations.md)中。

以下是設定自訂動作所需的主要步驟：

1. 在&#x200B;**[!UICONTROL Actions]**&#x200B;清單中，按一下&#x200B;**[!UICONTROL Add]**&#x200B;以建立新動作。 動作設定窗格會在畫面的右側開啟。

   ![](../assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 將描述新增至您的動作。 此步驟為選填。
1. 使用此動作的歷程次數會顯示在&#x200B;**[!UICONTROL Used in]**&#x200B;欄位中。 您可以按一下&#x200B;**[!UICONTROL View journeys]**&#x200B;按鈕，以顯示使用此動作的歷程清單。
1. 定義不同的&#x200B;**[!UICONTROL URL Configuration]**&#x200B;參數。 請參閱[本頁](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置&#x200B;**[!UICONTROL Authentication]**&#x200B;部分。 此設定與資料來源的設定相同。  請參閱[本節](../datasource/external-data-sources.md#section_wjp_nl5_nhb)。
1. 定義&#x200B;**[!UICONTROL Message parameters]**。 請參閱[本頁](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下「**[!UICONTROL Save]**」。

   自訂動作現在已設定好，可供您在歷程中使用。 請參閱[本頁](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在歷程中使用自訂動作時，大部分參數都是唯讀的。 您只能修改&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Description]**、**[!UICONTROL URL]**&#x200B;欄位和&#x200B;**[!UICONTROL Authentication]**&#x200B;區段。

## URL 組態 {#url-configuration}

設定自訂動作時，您需要定義下列&#x200B;**[!UICONTROL URL Configuration]**&#x200B;參數：

![](../assets/journeyurlconfiguration.png)

1. 添加外部服務的&#x200B;**[!UICONTROL URL]**。

   >[!NOTE]
   >
   >基於安全考量，我們強烈建議您使用 HTTPS。我們不允許使用非公開的Adobe地址和IP地址。

1. 選擇呼叫&#x200B;**[!UICONTROL Method]**:可以是&#x200B;**[!UICONTROL POST]**&#x200B;或&#x200B;**[!UICONTROL PUT]**。
1. 在&#x200B;**[!UICONTROL Headers]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL Add a header field]**&#x200B;以定義新的鍵／值對。 它們對應於對外部服務所提出請求的HTTP標頭。 要刪除鍵／值對，請將游標置於&#x200B;**[!UICONTROL Headers]**&#x200B;欄位中，然後按一下&#x200B;**[!UICONTROL Delete]**&#x200B;表徵圖。

   **[!UICONTROL Content-Type]** 和 **[!UICONTROL Charset]** 預設設定，不能刪除或覆蓋。

   >[!NOTE]
   >
   >標頭根據以下[解析規則](https://tools.ietf.org/html/rfc7230#section-3.2.4)進行驗證。

## 定義消息參數{#define-the-message-parameters}

![](../assets/messageparameterssection.png)

在&#x200B;**[!UICONTROL Message parameters]**&#x200B;區段中，貼上JSON裝載的範例以傳送至外部服務。

![](../assets/customactionpayloadmessage.png)

您可以定義參數類型(例如：字串、整數等)。

您也可以選擇指定參數是常數還是變數：

* 常數表示參數的值由技術人員在動作配置窗格中定義。 各個旅程的值一律相同。 在歷程中使用自訂動作時，不會有任何變化，行銷人員也不會看到。 例如，可能是協力廠商系統所預期的ID。 在這種情況下，切換常數／變數右側的欄位是傳遞的值。
* 變數表示參數的值會有所不同。 在歷程中使用此自訂動作的行銷人員可自由傳遞他想要的值，或指定擷取此參數值的位置(例如從事件、從Adobe Experience Platform等)。 在這種情況下，切換常數／變數右側的欄位是行銷人員在命名此參數的歷程中所看到的標籤。

![](../assets/customactionpayloadmessage2.png)
