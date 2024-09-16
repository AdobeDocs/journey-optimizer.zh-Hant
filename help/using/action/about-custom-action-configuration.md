---
solution: Journey Optimizer
product: journey optimizer
title: 設定自訂動作
description: 瞭解如何設定自訂動作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 動作，協力廠商，自訂，歷程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 3d79eca67dbfe5011a4bbc4955bbbfb5d6c17b38
workflow-type: tm+mt
source-wordcount: '1553'
ht-degree: 21%

---

# 設定自訂動作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自訂動作"
>abstract="如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。例如，您可使用自訂動作連線至下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等等。"

如果您使用協力廠商系統來傳送訊息，或想要歷程傳送 API 呼叫至協力廠商系統，請使用自訂動作來設定系統至您歷程的連線。例如，您可以使用自訂動作連線到下列系統：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等。

自訂動作是技術使用者定義的其他動作，可供行銷人員使用。 設定之後，它們會顯示在您歷程的左側浮動視窗，位於&#x200B;**[!UICONTROL 動作]**&#x200B;類別中。 在[本頁](../building-journeys/about-journey-activities.md#action-activities)中瞭解更多。

## 限制{#custom-actions-limitations}

自訂動作在[此頁面](../start/guardrails.md)中列出一些限制。

在自訂動作引數中，您可以傳遞簡單集合以及物件集合。 在[此頁面](../building-journeys/collections.md#limitations)中進一步瞭解集合限制。

另請注意，自訂動作引數採用預期格式（例如：字串、小數等）。 您必須注意遵守這些預期的格式。 在此[使用案例](../building-journeys/collections.md)中瞭解更多。

自訂動作只有在使用[要求](../action/about-custom-action-configuration.md#define-the-message-parameters)或[回應承載](../action/action-response.md)時才支援JSON格式。

## 最佳作法{#custom-action-enhancements-best-practices}

使用自訂動作選擇要作為目標的端點時，請確定：

* 此端點可使用來自[節流 API](../configuration/throttling.md) 或[設定 API 上限](../configuration/capping.md)的設定來支援歷程的輸送量，藉此加以限制。 請留意，節流設定不可低於 200 TPS。任何目標端點至少需要支援 200 TPS。
* 此端點的回應時間必須儘可能縮短。 根據預期輸送量，高回應時間可能會影響實際輸送量。

所有自訂動作皆已定義1分鐘上300,000次呼叫的上限。 此外，預設上限會針對每個主機和每個沙箱執行。 例如，在沙箱上，如果您有主機相同的兩個端點 (例如：`https://www.adobe.com/endpoint1` 和 `https://www.adobe.com/endpoint2`)，此上限會套用至 adobe.com 主機下的所有端點。 「endpoint1」和「endpoint2」會共用相同的上限設定，而且讓一個端點達到限制會影響到另一個端點。

此限制是根據客戶使用情況來設定，可保護自訂動作鎖定為目標的外部端點。您需要定義適當的讀取率 (使用自訂動作時為每秒 5000 個輪廓)，以在客群歷程中將其列入考量。 如有需要，您可以透過上限/節流 API 定義較高的上限或節流限制來覆寫此設定。 請參閱[此頁面](../configuration/external-systems.md)。

基於以下各種原因，您不應使用自訂動作來鎖定公用端點：

* 如果沒有適當的上限或節流，可能會傳送過多呼叫至可能不支援此磁碟區的公用端點。
* 設定檔資料可透過自訂動作傳送，因此定位公用端點可能會導致無意間在外部共用個人資訊。
* 您無法控制公用端點傳回的資料。 如果端點變更其API或開始傳送不正確的資訊，這些資訊將可在傳送的通訊中使用，並可能產生負面影響。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md)。
* [同意](../action/action-privacy.md)。


## 設定步驟 {#configuration-steps}

以下是設定自訂動作所需的主要步驟：

1. 在「管理」功能表區段中，選取&#x200B;**[!UICONTROL 組態]**。 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 管理]**。 按一下&#x200B;**[!UICONTROL 建立動作]**&#x200B;以建立新動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/custom2.png)

1. 輸入動作的名稱。

   >[!NOTE]
   >
   >只允許使用英數字元和底線。 長度上限為30個字元。

1. 新增說明至您的動作。 此步驟為選填。
1. 使用此動作的歷程次數會顯示在&#x200B;**[!UICONTROL 用於]**&#x200B;欄位中。 您可以按一下&#x200B;**[!UICONTROL 檢視歷程]**&#x200B;按鈕，以顯示使用此動作的歷程清單。
1. 定義不同的&#x200B;**[!UICONTROL URL組態]**&#x200B;引數。 請參閱[此頁面](../action/about-custom-action-configuration.md#url-configuration)。
1. 設定&#x200B;**[!UICONTROL 驗證]**&#x200B;區段。 此設定與資料來源的設定相同。  請參閱[本節](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定義&#x200B;**[!UICONTROL 動作引數]**。 請參閱[此頁面](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   自訂動作現已設定完畢，且可供您在歷程中使用。 請參閱[此頁面](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >當歷程中使用自訂動作時，大部分引數均為唯讀。 您只能修改&#x200B;**[!UICONTROL 名稱]**、**[!UICONTROL 描述]**、**[!UICONTROL URL]**&#x200B;欄位和&#x200B;**[!UICONTROL 驗證]**&#x200B;區段。

## 端點設定 {#url-configuration}

設定自訂動作時，您必須定義下列&#x200B;**[!UICONTROL 端點設定]**&#x200B;引數：

![](assets/action-response1bis.png){width="70%" align="left"}

1. 在&#x200B;**[!UICONTROL URL]**&#x200B;欄位中，指定外部服務的URL：

   * 如果URL是靜態的，請在此欄位中輸入URL。

   * 如果URL包含動態路徑，請只輸入URL的靜態部分，也就是配置、主機、連線埠，以及（選擇性）路徑的靜態部分。

     範例：`https://xxx.yyy.com/somethingstatic/`

     將自訂動作新增至歷程時，您將指定URL的動態路徑。 [了解更多](../building-journeys/using-custom-actions.md)。

   >[!NOTE]
   >
   >基於安全考量，我們強烈建議您針對URL使用HTTPS配置。 我們不允許使用非公開的Adobe位址和IP位址。
   >
   >定義自訂動作時只允許預設連線埠：80用於http，443用於https。

1. 選取呼叫&#x200B;**[!UICONTROL 方法]**：它可以是&#x200B;**[!UICONTROL POST]**、**[!UICONTROL GET]**&#x200B;或&#x200B;**[!UICONTROL PUT]**。

   >[!NOTE]
   >
   > 不支援&#x200B;**DELETE**&#x200B;方法。 如果您需要更新現有的資源，請選取&#x200B;**PUT**&#x200B;方法。

1. 定義標頭和查詢引數：

   * 在&#x200B;**[!UICONTROL 標頭]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 新增標頭欄位]**&#x200B;以定義要傳送給外部服務的要求訊息的HTTP標頭。 預設會設定&#x200B;**[!UICONTROL Content-Type]**&#x200B;和&#x200B;**[!UICONTROL Charset]**&#x200B;標頭欄位。 您無法刪除這些欄位。 只有&#x200B;**[!UICONTROL Content-Type]**&#x200B;標頭可以修改。 其值應符合JSON格式。 以下是預設值：

   ![](assets/content-type-header.png)

   * 在&#x200B;**[!UICONTROL 查詢引數]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 新增查詢引數欄位]**&#x200B;以定義您要新增到URL中的引數。

   ![](assets/journeyurlconfiguration2bis.png)

1. 輸入欄位的標籤或名稱。

1. 選取型別： **[!UICONTROL 常數]**&#x200B;或&#x200B;**[!UICONTROL 變數]**。 如果您已選取&#x200B;**[!UICONTROL 常數]**，請在&#x200B;**[!UICONTROL 值]**&#x200B;欄位中輸入常數值。 如果您已選取&#x200B;**[!UICONTROL 變數]**，則您將在新增自訂動作至歷程時指定此變數。 [了解更多](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >將自訂動作新增至歷程後，如果歷程處於草稿狀態，您仍可新增標題或查詢引數欄位至歷程。 如果您不希望歷程受設定變更影響，請複製自訂動作，並將欄位新增到新的自訂動作。
   >
   >標頭會根據欄位剖析規則進行驗證。 深入瞭解[此檔案](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}。

## mTLS通訊協定支援 {#mtls-protocol-support}

您現在可以使用相互傳輸層安全性(mTLS)，確保對Adobe Journey Optimizer自訂動作的輸出連線具有增強的安全性。 mTLS是一種用於相互驗證的端對端安全性方法，可確保共用資訊的雙方在共用資料之前，都是聲稱的身分。 mTLS包括相較於TLS的額外步驟，其中伺服器也會要求使用者端的憑證並在其末端驗證它。

自訂動作支援雙向TLS (mTLS)驗證。 自訂動作或歷程中不需要額外設定即可啟用 mTLS；當偵測到啟用 mTLS 的端點時，它會自動發生。 [了解更多](https://experienceleague.adobe.com/en/docs/experience-platform/landing/governance-privacy-security/encryption#mtls-protocol-support)。

## 定義裝載引數 {#define-the-message-parameters}

1. 在&#x200B;**[!UICONTROL Request]**&#x200B;區段中，貼上要傳送至外部服務的JSON裝載範例。 此欄位是選用欄位，僅適用於POST和PUT呼叫方法。

1. 在&#x200B;**[!UICONTROL 回應]**&#x200B;區段中，貼上呼叫傳回之裝載的範例。 此欄位是選用欄位，可用於所有呼叫方法。 如需如何在自訂動作中運用API呼叫回應的詳細資訊，請參閱[此頁面](../action/action-response.md)。

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>裝載範例不可包含Null值。 承載中的欄位名稱不得包含「。」 字元。 開頭不能為「$」字元。

您將能夠定義引數型別（例如：字串、整數等）。

您也可以選擇指定引數是常數還是變數：

* **常數**&#x200B;表示引數值是由技術角色在動作設定窗格中定義。 值在歷程中一律相同。 這不會改變，且行銷人員在歷程中使用自訂動作時不會看到。 例如，它可能是協力廠商系統期望的ID。 在這種情況下，切換常數/變數右側的欄位是傳遞的值。
* **變數**&#x200B;表示引數的值會有所不同。 在歷程中使用此自訂動作的行銷人員可自由傳遞所需值，或指定從何處擷取此引數的值(例如從事件、Adobe Experience Platform等)。 在這種情況下，切換常數/變數右側的欄位是行銷人員將在歷程中看到的標籤，以命名此引數。

![](assets/customactionpayloadmessage2.png)
