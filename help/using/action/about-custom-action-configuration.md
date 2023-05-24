---
solution: Journey Optimizer
product: journey optimizer
title: 配置自定義操作
description: 瞭解如何配置自定義操作
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: action，第三方，custom, journeys，旅程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 15%

---

# 配置自定義操作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自訂動作"
>abstract="如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您的歷程的連線。 例如，您可使用自訂動作連線至下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等等。"

如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您的歷程的連線。 例如，可以使用自定義操作連接到以下系統：ε,Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 配置後，它們會出現在您旅程的左側調色板中， **[!UICONTROL 操作]** 的子菜單。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

## 限制{#custom-actions-limitations}

自定義操作附帶了中列出的一些限制 [此頁](../start/guardrails.md)。

在自定義操作參數中，可以傳遞簡單集合以及對象集合。 瞭解有關中的收集限制的詳細資訊 [此頁](../building-journeys/collections.md#limitations)。

另請注意，自定義操作參數具有預期格式(例如：字串、小數等)。 您必須小心遵守這些預期格式。 瞭解更多資訊 [用例](../building-journeys/collections.md)。

## 同意和資料治理 {#privacy}

在Journey Optimizer，您可以將資料治理和同意策略應用到您的自定義操作，以防止特定欄位導出到第三方系統或排除未同意接收電子郵件、推送或SMS通信的客戶。 有關詳細資訊，請參閱以下頁：

* [資料治理](../action/action.md)。
* [同意](../action/action.md).


## 設定步驟 {#configuration-steps}

以下是配置自定義操作所需的主要步驟：

1. 在「管理」(ADMINISTRATION)菜單部分，選擇 **[!UICONTROL 配置]**。 在  **[!UICONTROL 操作]** ，按一下 **[!UICONTROL 管理]**。 按一下 **[!UICONTROL 建立操作]** 的子菜單。 操作配置窗格在螢幕右側開啟。

   ![](assets/custom2.png)

1. 輸入操作的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 向操作添加說明。 此步驟為選填。
1. 使用此操作的行程數顯示在 **[!UICONTROL 用於]** 的子菜單。 您可以按一下 **[!UICONTROL 查看行程]** 按鈕來顯示使用此操作的行程清單。
1. 定義不同 **[!UICONTROL URL配置]** 參數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置 **[!UICONTROL 驗證]** 的子菜單。 此配置與資料源相同。  請參閱[本節](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義 **[!UICONTROL 操作參數]**。 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   現在已配置自定義操作，並準備在您的旅途中使用。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在行程中使用自定義操作時，大多數參數都是只讀的。 您只能修改 **[!UICONTROL 名稱]**。 **[!UICONTROL 說明]**。 **[!UICONTROL URL]** 和 **[!UICONTROL 驗證]** 的子菜單。

## URL 組態 {#url-configuration}

配置自定義操作時，需要定義以下 **[!UICONTROL URL配置]** 參數：

![](assets/journeyurlconfiguration.png)

1. 在 **[!UICONTROL URL]** 欄位，指定外部服務的URL:

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，則只輸入該URL的靜態部分，即方案、主機、埠以及（可選）路徑的靜態部分。

      範例：`https://xxx.yyy.com/somethingstatic/`

      將自定義操作添加到行程時，將指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >出於安全原因，強烈建議您將HTTPS方案用於URL。 我們不允許使用非公有的Adobe地址和IP地址。
   >
   >定義自定義操作時僅允許預設埠：80表示http,443表示https。

1. 選擇呼叫 **[!UICONTROL 方法]**:它可以 **[!UICONTROL POST]** 或 **[!UICONTROL PUT]**。

   >[!NOTE]
   >
   > 的 **DELETE** 方法不受支援。 如果需要更新現有資源，請選擇 **PUT** 的雙曲餘切值。

1. 定義標題和查詢參數：

   * 在 **[!UICONTROL 標題]** ，按一下 **[!UICONTROL 添加標題欄位]** 定義要發送到外部服務的請求消息的HTTP標頭。 的 **[!UICONTROL 內容類型]** 和 **[!UICONTROL 沙爾塞]** 預設情況下設定標題欄位。 不能修改或刪除這些欄位。

   * 在 **[!UICONTROL 查詢參數]** ，按一下 **[!UICONTROL 添加查詢參數欄位]** 定義要在URL中添加的參數。

   ![](assets/journeyurlconfiguration2bis.png)

1. 輸入欄位的標籤或名稱。

1. 選擇類型： **[!UICONTROL 常數]** 或 **[!UICONTROL 變數]**。 如果已選擇 **[!UICONTROL 常數]**，然後在 **[!UICONTROL 值]** 的子菜單。 如果已選擇 **[!UICONTROL 變數]**，則在將自定義操作添加到行程時將指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >在將自定義操作添加到行程後，如果行程處於草稿狀態，則仍可向其添加題頭或查詢參數欄位。 如果不希望行程受配置更改的影響，請複製自定義操作並將欄位添加到新的自定義操作。
   >
   >根據欄位分析規則驗證標頭。 瞭解詳情 [本文檔](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}。

## 定義操作參數 {#define-the-message-parameters}

在 **[!UICONTROL 操作參數]** 部分，貼上要發送到外部服務的JSON負載示例。

![](assets/messageparameterssection.png)

>[!NOTE]
>
>負載示例不能包含空值。 負載中的欄位名稱不能包含「。」 字元. 它們不能以「$」字元開頭。

您將能夠定義參數類型(例如：字串、整數等)。

還可以選擇指定參數是常數還是變數：

* **常數** 表示參數的值在操作配置窗格中由技術角色定義。 不同旅程的價值始終相同。 它不會變化，營銷人員在旅途中使用自定義操作時不會看到它。 例如，可能是第三方系統需要的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* **變數** 表示參數的值將發生變化。 在行程中使用此自定義操作的營銷人員可以免費傳遞他們想要的值，或指定在何處檢索此參數的值(例如從事件、從Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是標籤商在命名此參數的旅程中將看到的標籤。

![](assets/customactionpayloadmessage2.png)
