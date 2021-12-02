---
solution: Journey Orchestration
title: 關於自訂動作組態
description: 了解如何設定自訂動作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 9e6e4f30e2f0301157901ea211f984ebcfb99bc4
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 6%

---

# 設定動作 {#configure-an-action}

如果您使用協力廠商系統來傳送訊息，或您想要歷程將API呼叫傳送至協力廠商系統，您可以在此設定其與歷程的連線。 接著，技術使用者定義的自訂動作將可在歷程的左側浮動視窗中使用，位於 **[!UICONTROL Action]** 類別(請參閱 [本頁](../building-journeys/about-journey-activities.md#action-activities). 以下是一些您可透過自訂動作連線至的系統範例：Epsilon、Slack、Adobe、io、Firebase等

限制列於 [本頁](../limitations.md).

您可以使用自訂動作以動態方式傳遞集合。 請參閱 [使用案例](../building-journeys/collections.md).

以下是設定自訂動作所需的主要步驟：

1. 在「管理」(ADMINISTRATION)菜單部分中，選擇 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Actions]** ，按一下 **[!UICONTROL Manage]**. 按一下 **[!UICONTROL Create Action]** 來建立新動作。 動作設定窗格會在畫面右側開啟。

   ![](../assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 為動作新增說明。 此步驟為選填。
1. 使用此動作的歷程次數會顯示在 **[!UICONTROL Used in]** 欄位。 您可以按一下 **[!UICONTROL View journeys]** 按鈕，以顯示使用此動作的歷程清單。
1. 定義不同的 **[!UICONTROL URL Configuration]** 參數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 設定 **[!UICONTROL Authentication]** 區段。 此設定與資料來源的設定相同。  請參閱[本節](../datasource/external-data-sources.md#section_wjp_nl5_nhb)。
1. 定義 **[!UICONTROL Action parameters]**. 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下「**[!UICONTROL Save]**」。

   自訂動作現在已設定完畢，且已準備好用於您的歷程。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在歷程中使用自訂動作時，大部分參數為唯讀。 您只能修改 **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** 欄位和 **[!UICONTROL Authentication]** 區段。

## URL 組態 {#url-configuration}

設定自訂動作時，您需要定義下列項目 **[!UICONTROL URL Configuration]** 參數：

![](../assets/journeyurlconfiguration.png)

1. 在 **[!UICONTROL URL]** 欄位，指定外部服務的URL:

   * 如果URL為靜態，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，則僅輸入URL的靜態部分，即配置、主機、埠，以及路徑的靜態部分（可選）。

      範例: `https://xxx.yyy.com/somethingstatic/`

      將自訂動作新增至歷程時，您會指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >基於安全考量，強烈建議您為URL使用HTTPS配置。 不允許使用非公用的Adobe位址和IP位址。
   >
   >定義自訂動作時，僅允許預設埠：80（適用於http）和443（適用於https）。

1. 選取呼叫 **[!UICONTROL Method]**:它可以是 **[!UICONTROL POST]** 或 **[!UICONTROL PUT]**.
1. 在 **[!UICONTROL Headers]** 一節，定義要傳送至外部服務的要求訊息的HTTP標題：
   1. 若要新增標題欄位，請按一下 **[!UICONTROL Add a header field]**.
   1. 輸入標題欄位的鍵。
   1. 若要設定機碼值組的動態值，請選取 **[!UICONTROL Variable]**. 否則，請選取 **[!UICONTROL Constant]**.

      例如，對於時間戳記，您可以設定動態值。

   1. 如果您已選取 **[!UICONTROL Constant]**，然後輸入常數值。

      如果您已選取 **[!UICONTROL Variable]**，則會在將自訂動作新增至歷程時指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

      ![](../assets/journeyurlconfiguration2.png)

   1. 若要刪除標題欄位，請指向標題欄位，然後按一下 **[!UICONTROL Delete]** 表徵圖。
   此 **[!UICONTROL Content-Type]** 和 **[!UICONTROL Charset]** 預設會設定標題欄位。 您無法修改或刪除這些欄位。

   將自訂動作新增至歷程後，如果歷程處於草稿狀態，您仍可新增標題欄位。 如果您不希望歷程受到設定變更的影響，請複製自訂動作，並將標題欄位新增至新的自訂動作。

   >[!NOTE]
   >
   >標題會根據欄位剖析規則進行驗證。 [了解更多](https://tools.ietf.org/html/rfc7230#section-3.2.4)。

## 定義動作參數 {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

在 **[!UICONTROL Action parameters]** 區段中，貼上要傳送至外部服務的JSON裝載範例。

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>裝載中的欄位名稱不能包含「。」 字元. 開頭不能為「$」字元。

您將能定義參數類型(例如：字串、整數等)。

您也可以選擇指定參數為常數或變數：

* 常數表示參數的值是由技術人員在動作設定窗格中定義。 歷程中的值一律相同。 此值不會有所不同，且行銷人員在歷程中使用自訂動作時不會看到。 例如可能是協力廠商系統預期的ID。 在此情況下，切換常數/變數右側的欄位即為傳遞的值。
* 變數表示參數的值會有所不同。 行銷人員在歷程中使用此自訂動作時，可以免費傳遞所需值，或指定要擷取此參數值的位置(例如從事件、從Adobe Experience Platform等)。 在此情況下，切換常數/變數右側的欄位，就是行銷人員在歷程中看到的為此參數命名的標籤。

![](../assets/customactionpayloadmessage2.png)

