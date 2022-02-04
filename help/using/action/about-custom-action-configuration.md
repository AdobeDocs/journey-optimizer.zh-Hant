---
solution: Journey Orchestration
title: 關於自訂動作組態
description: 瞭解如何配置自定義操作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 2088b5ba2ec77e56644683e118e734acfe6707fc
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 6%

---

# 設定動作 {#configure-an-action}

如果您使用第三方系統發送消息，或者如果希望行程將API調用發送到第三方系統，則在此處配置其到行程的連接。 然後，技術用戶定義的自定義操作將在您旅程的左側調色板中提供。 **[!UICONTROL Action]** 類別(請參閱 [此頁](../building-journeys/about-journey-activities.md#action-activities)。 以下是一些系統示例，您可以通過自定義操作連接到這些系統：Epsilon、Slack、Adobe.io、Firebase等

限制列在 [此頁](../start/limitations.md)。

您可以使用自定義操作動態傳遞集合。 請參閱此 [用例](../building-journeys/collections.md)。

以下是配置自定義操作所需的主要步驟：

1. 在「管理」(ADMINISTRATION)菜單部分，選擇 **[!UICONTROL Configurations]**。 在  **[!UICONTROL Actions]** ，按一下 **[!UICONTROL Manage]**。 按一下 **[!UICONTROL Create Action]** 的子菜單。 操作配置窗格在螢幕右側開啟。

   ![](../assets/custom2.png)

1. 輸入操作的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 向操作添加說明。 此步驟為選填。
1. 使用此操作的行程數顯示在 **[!UICONTROL Used in]** 的子菜單。 您可以按一下 **[!UICONTROL View journeys]** 按鈕來顯示使用此操作的行程清單。
1. 定義不同 **[!UICONTROL URL Configuration]** 參數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置 **[!UICONTROL Authentication]** 的子菜單。 此配置與資料源相同。  請參閱[本節](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義 **[!UICONTROL Action parameters]**。 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下「**[!UICONTROL Save]**」。

   現在已配置自定義操作，並準備在您的旅途中使用。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在行程中使用自定義操作時，大多數參數都是只讀的。 您只能修改 **[!UICONTROL Name]**。 **[!UICONTROL Description]**。 **[!UICONTROL URL]** 和 **[!UICONTROL Authentication]** 的子菜單。

## URL 組態 {#url-configuration}

配置自定義操作時，需要定義以下 **[!UICONTROL URL Configuration]** 參數：

![](../assets/journeyurlconfiguration.png)

1. 在 **[!UICONTROL URL]** 欄位，指定外部服務的URL:

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，則只輸入該URL的靜態部分，即方案、主機、埠以及（可選）路徑的靜態部分。

      範例: `https://xxx.yyy.com/somethingstatic/`

      將自定義操作添加到行程時，將指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >出於安全原因，強烈建議您將HTTPS方案用於URL。 我們不允許使用非公有的Adobe地址和IP地址。
   >
   >定義自定義操作時僅允許預設埠：80表示http,443表示https。

1. 選擇呼叫 **[!UICONTROL Method]**:它可以 **[!UICONTROL POST]** 或 **[!UICONTROL PUT]**。
1. 在 **[!UICONTROL Headers]** 定義要發送到外部服務的請求消息的HTTP標頭：
   1. 要添加標題欄位，請按一下 **[!UICONTROL Add a header field]**。
   1. 輸入標題欄位的鍵。
   1. 要為鍵值對設定動態值，請選擇 **[!UICONTROL Variable]**。 否則，選擇 **[!UICONTROL Constant]**。

      例如，對於時間戳，可以設定動態值。

   1. 如果已選擇 **[!UICONTROL Constant]**，然後輸入常數值。

      如果已選擇 **[!UICONTROL Variable]**，則在將自定義操作添加到行程時將指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

      ![](../assets/journeyurlconfiguration2.png)

   1. 要刪除標題欄位，請指向標題欄位，然後按一下 **[!UICONTROL Delete]** 表徵圖
   的 **[!UICONTROL Content-Type]** 和 **[!UICONTROL Charset]** 預設情況下設定標題欄位。 不能修改或刪除這些欄位。

   在將自定義操作添加到行程後，如果行程處於草稿狀態，則仍可將題頭欄位添加到行程。 如果不希望行程受配置更改的影響，請複製自定義操作，並將標題欄位添加到新的自定義操作。

   >[!NOTE]
   >
   >根據欄位分析規則驗證標頭。 [了解更多](https://tools.ietf.org/html/rfc7230#section-3.2.4)。

## 定義操作參數 {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

在 **[!UICONTROL Action parameters]** 部分，貼上要發送到外部服務的JSON負載示例。

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>負載中的欄位名稱不能包含「。」 字元. 它們不能以「$」字元開頭。

您將能夠定義參數類型(例如：字串、整數等)。

還可以選擇指定參數是常數還是變數：

* 常數表示參數的值在操作配置窗格中由技術角色定義。 不同旅程的價值始終相同。 它不會變化，營銷人員在旅途中使用自定義操作時不會看到它。 例如，可能是第三方系統需要的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* 變數表示參數的值將發生變化。 在行程中使用此自定義操作的營銷人員可以免費傳遞他們想要的值，或指定在何處檢索此參數的值(例如從事件、從Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是標籤商在命名此參數的旅程中將看到的標籤。

![](../assets/customactionpayloadmessage2.png)

