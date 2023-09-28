---
solution: Journey Optimizer
product: journey optimizer
title: 設定自訂動作
description: 瞭解如何設定自訂動作
feature: Actions
topic: Administration
role: Admin
level: Experienced
keywords: 動作，協力廠商，自訂，歷程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 2e06ca80a74c6f8a16ff379ee554d57a69ceeffd
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 12%

---

# 設定自訂動作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自訂動作"
>abstract="如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。 例如，您可使用自訂動作連線至下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等等。"

如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。 例如，您可以使用自訂動作連線到下列系統：Epsilon、Slack、 [Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 設定後，其會顯示在您歷程的左側浮動視窗中，位於 **[!UICONTROL 動作]** 類別。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

## 限制{#custom-actions-limitations}

自訂動作隨附下列幾項限制 [此頁面](../start/guardrails.md).

在自訂動作引數中，您可以傳遞簡單集合以及物件集合。 進一步瞭解中的集合限制 [此頁面](../building-journeys/collections.md#limitations).

另請注意，自訂動作引數採用預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。 在本節瞭解更多 [使用案例](../building-journeys/collections.md).

## 最佳做法{#custom-action-enhancements-best-practices}

所有自訂動作的上限為5000次呼叫/秒。 此限制是根據客戶使用狀況所設定，可保護自訂動作鎖定的外部端點。 您需要透過定義適當的讀取率（使用自訂動作時為5000個設定檔/秒），在以對象為基礎的歷程中將其納入考量。 如有需要，您可以透過我們的上限/節流API定義較大的上限或節流限制來覆寫此設定。 請參閱[此頁面](../configuration/external-systems.md)。

基於以下各種原因，您不應使用自訂動作來鎖定公用端點：

* 如果沒有適當的上限或節流，可能會傳送過多呼叫至可能不支援此磁碟區的公用端點。
* 設定檔資料可透過自訂動作傳送，因此定位公用端點可能會導致無意間在外部共用個人資訊。
* 您無法控制公用端點傳回的資料。 如果端點變更其API或開始傳送不正確的資訊，這些資訊將可在傳送的通訊中使用，並可能產生負面影響。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md).
* [同意](../action/action-privacy.md).


## 設定步驟 {#configuration-steps}

以下是設定自訂動作所需的主要步驟：

1. 在「管理」功能表區段中，選取 **[!UICONTROL 設定]**. 在  **[!UICONTROL 動作]** 區段，按一下 **[!UICONTROL 管理]**. 按一下 **[!UICONTROL 建立動作]** 以建立新動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 新增說明至您的動作。 此步驟為選填。
1. 使用此動作的歷程次數會顯示在 **[!UICONTROL 使用位置]** 欄位。 您可以按一下 **[!UICONTROL 檢視歷程]** 按鈕來顯示使用此動作的歷程清單。
1. 定義不同的 **[!UICONTROL URL設定]** 引數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 設定 **[!UICONTROL 驗證]** 區段。 此設定與資料來源的設定相同。  請參閱[本節](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義 **[!UICONTROL 動作引數]**. 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   自訂動作現已設定完畢，且可供您在歷程中使用。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >當歷程中使用自訂動作時，大部分引數均為唯讀。 您只能修改 **[!UICONTROL 名稱]**， **[!UICONTROL 說明]**， **[!UICONTROL URL]** 欄位和 **[!UICONTROL 驗證]** 區段。

## 端點設定 {#url-configuration}

設定自訂動作時，您需要定義下列專案 **[!UICONTROL 端點設定]** 引數：

![](assets/action-response1bis.png){width="70%" align="left"}

1. 在 **[!UICONTROL URL]** 欄位，指定外部服務的URL：

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，請只輸入URL的靜態部分，也就是配置、主機、連線埠，以及（選擇性）路徑的靜態部分。

     範例：`https://xxx.yyy.com/somethingstatic/`

     將自訂動作新增至歷程時，您將指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。

   >[!NOTE]
   >
   >基於安全考量，我們強烈建議您針對URL使用HTTPS配置。 我們不允許使用非公開的Adobe位址和IP位址。
   >
   >定義自訂動作時只允許預設連線埠：80用於http，443用於https。

1. 選取通話 **[!UICONTROL 方法]**：它可以 **[!UICONTROL POST]**， **[!UICONTROL GET]** 或 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 此 **DELETE** 方法不受支援。 如果您需要更新現有資源，請選取 **PUT** 方法。

1. 定義標頭和查詢引數：

   * 在 **[!UICONTROL 標頭]** 區段，按一下 **[!UICONTROL 新增標題欄位]** 定義要傳送給外部服務之要求訊息的HTTP標頭。 此 **[!UICONTROL Content-Type]** 和 **[!UICONTROL 字元集]** 標頭欄位預設為設定。 您無法修改或刪除這些欄位。

   * 在 **[!UICONTROL 查詢引數]** 區段，按一下 **[!UICONTROL 新增查詢引數欄位]** 以定義您要新增至URL的引數。

   ![](assets/journeyurlconfiguration2bis.png)

1. 輸入欄位的標籤或名稱。

1. 選取型別： **[!UICONTROL 常數]** 或 **[!UICONTROL 變數]**. 如果您已選取 **[!UICONTROL 常數]**，然後輸入中的常數值 **[!UICONTROL 值]** 欄位。 如果您已選取 **[!UICONTROL 變數]**，則您會在將自訂動作新增至歷程時指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >將自訂動作新增至歷程後，如果歷程處於草稿狀態，您仍可新增標題或查詢引數欄位至歷程。 如果您不希望歷程受設定變更影響，請複製自訂動作，並將欄位新增到新的自訂動作。
   >
   >標頭會根據欄位剖析規則進行驗證。 進一步瞭解 [本檔案](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## 定義裝載引數 {#define-the-message-parameters}

1. 在 **[!UICONTROL 請求]** 區段，貼上要傳送至外部服務的JSON裝載範例。 此欄位是選用欄位，僅適用於POST和PUT呼叫方法。

1. 在 **[!UICONTROL 回應]** 區段，貼上呼叫傳回之裝載的範例。 此欄位是選用欄位，可用於所有呼叫方法。 如需如何在客戶動作中運用API呼叫回應的詳細資訊，請參閱 [此頁面](../action/action-response.md).

>[!NOTE]
>
>回應功能目前在Beta版中提供。

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>裝載範例不可包含Null值。 承載中的欄位名稱不得包含「。」 字元. 開頭不能為「$」字元。

您將能夠定義引數型別（例如：字串、整數等）。

您也可以選擇指定引數是常數還是變數：

* **常數** 表示引數的值是由技術角色在動作設定窗格中定義。 值在歷程中一律相同。 這不會改變，且行銷人員在歷程中使用自訂動作時不會看到。 例如，它可能是協力廠商系統期望的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* **變數** 表示引數的值會有所不同。 在歷程中使用此自訂動作的行銷人員可自由傳遞所需值，或指定從何處擷取此引數的值(例如從事件、Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是行銷人員將在歷程中看到的標籤，以命名此引數。

![](assets/customactionpayloadmessage2.png)