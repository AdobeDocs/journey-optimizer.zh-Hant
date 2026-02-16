---
solution: Journey Optimizer
product: journey optimizer
title: 疑難排解自訂動作
description: 瞭解如何疑難排解自訂動作
feature: Journeys, Actions, Custom Actions, Monitoring
topic: Administration
role: Developer, Admin
level: Experienced
keywords: 動作，協力廠商，自訂，歷程， API
exl-id: c0bb473a-82dc-4604-bd8a-020447ac0c93
source-git-commit: bae446ea38a0cb97487201f7dcf4df751578ad0a
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 1%

---

# 疑難排解自訂動作 {#troubleshoot-a-custom-action}

您可以從Journey Optimizer使用者介面的管理區段傳送API呼叫，以測試自訂動作。 此功能可協助您在歷程中使用自訂動作之前或之後，進行疑難排解。

作為管理員，使用&#x200B;**[!UICONTROL 傳送測試要求]**&#x200B;功能，直接從Adobe Journey Optimizer發出真正的API呼叫，以驗證您的自訂動作設定。 此功能可確保請求結構、標頭、驗證和裝載的格式正確，然後才會用於歷程中。

![](assets/send-test-request.png){width="70%" align="left"}

此功能可簡化測試和驗證程式，確保自訂動作在即時歷程中正常運作。

>[!NOTE]
>
>如果您的組織已啟用IP （輸出） Proxy，**[!UICONTROL 傳送測試要求]**&#x200B;呼叫會略過該要求。 若要確認Proxy路由，請執行測試或即時歷程。 深入瞭解[與外部系統整合](../configuration/external-systems.md#faq)中的IP （輸出） Proxy和啟用。


## 先決條件 {#troubleshoot-custom-action-prereq}

若要使用&#x200B;**[!UICONTROL 傳送測試要求]**&#x200B;功能，**自訂動作**&#x200B;必須預先設定URL、標頭和驗證設定。

管理員若要使用此功能，需要下列許可權：

* 使用者必須有&#x200B;**[!DNL Manage journeys events, data sources and actions]**&#x200B;許可權。
* 此許可權包含在&#x200B;*歷程管理員*&#x200B;角色中。
* 僅使用&#x200B;**[!DNL View journeys events]**&#x200B;許可權是不夠的。

在[本節](../administration/high-low-permissions.md#journey-capability)中進一步瞭解歷程許可權。

## 如何使用傳送測試請求功能 {#troubleshoot-custom-action-use}

若要測試自訂動作，請遵循下列步驟：

1. 導覽至&#x200B;**動作**&#x200B;設定畫面，然後選取自訂動作。
1. 按一下動作設定畫面底部的&#x200B;**[!UICONTROL 傳送測試要求]**按鈕。
   ![在動作設定面板中傳送測試要求按鈕](assets/test-request.png){width="70%" align="left"}
1. 在快顯視窗中，允許您指定請求引數：

   * 如果&#x200B;**自訂動作方法是GET**，則不需要裝載。
   * 如果&#x200B;**自訂動作方法是POST**，您必須提供JSON裝載。

     >[!NOTE]
     >
     >如果此JSON的結構不正確，Adobe Journey Optimizer會引發錯誤；但如果資料型別不相符，則不會引發。 例如，若將整數引數用於字串，則不會發生錯誤。

   * 如果已定義驗證，系統將提示您輸入驗證詳細資訊。

1. 按一下&#x200B;**傳送**&#x200B;以執行要求。
1. 來自API的回應（包括標題和狀態代碼）將顯示在介面中。

## 驗證處理 {#troubleshoot-custom-action-auth}

當自訂動作包含驗證時，Adobe Journey Optimizer會要求使用者為每個測試請求輸入驗證詳細資訊：

* **基本驗證：**&#x200B;使用者必須提供&#x200B;*密碼*。
* **API金鑰驗證：**&#x200B;使用者必須輸入API金鑰&#x200B;*值*。
* **自訂驗證：**&#x200B;使用者必須在要求&#x200B;*bodyParam*&#x200B;中提供驗證引數。 在此案例中新增了兩個區段： **驗證要求**&#x200B;和&#x200B;**驗證回應**。

## 主要優點 {#troubleshoot-custom-action-benefits}

身為Journey Optimizer管理員，您也可以使用外部工具(例如Postman)來測試自訂動作。 以下列出產品內故障診斷功能與外部測試相比的主要優點：

* 測試要求是由&#x200B;**AJO歷程**&#x200B;執行，表示：

   * 系統會使用確切的請求結構(包括Adobe Journey Optimizer專屬標頭)。
   * 來源IP和標題與即時歷程中使用的相符。

* **[!UICONTROL 傳送測試要求]**&#x200B;功能可用於疑難排解&#x200B;**即時歷程**，因為已部署自訂動作。

* 此產品內測試功能消除了在工具之間手動複製設定詳細資訊的需求，降低錯誤風險。

## 疑難排解 {#troubleshoot-custom-action-check}

如果請求失敗，您可以檢查：

* 在測試中輸入的驗證認證。
* 要求方法(GET與POST的比較)和對應的裝載。
* 自訂動作中定義的API端點和標題。
* 使用回應資料來識別可能的設定錯誤。

## 處理捨棄事件和閒置逾時 {#handling-discard-events-and-idle-timeouts}

當一個歷程中的自訂動作觸發旨在開始&#x200B;**第二個歷程**&#x200B;的事件時，請確保第二個歷程處於有效狀態並且可識別該事件。 如果事件不符合第二個歷程的進入條件，則事件可以是&#x200B;**捨棄**，並出現在包含`notSuitableInitialEvent`等程式碼的記錄中。 如果第二個歷程尚未就緒，可能會發生閒置逾時，導致記錄中捨棄事件。

**常見原因：**

* **不符合事件資格** — 第二個歷程使用具有資格條件的規則型事件（例如，必要欄位必須是非空白的，例如特定欄位上的`isNotEmpty`）。 如果事件裝載未滿足該條件（例如，欄位空白或遺失），則事件為&#x200B;**已接收但已捨棄**，且未觸發第二個歷程。 這是預期行為；檔案和記錄會確認，如果不符合資格條件，則會捨棄事件，且不會為該設定檔觸發歷程。 確認自訂動作傳送的裝載包含第二個歷程的事件設定所需的所有欄位和值。 瞭解如何在歷程執行中[設定規則型事件](../event/about-creating.md)和[疑難排解事件接收](../building-journeys/troubleshooting-execution.md#checking-if-people-enter-the-journey)。

* **第二個歷程未就緒** — 如果第二個歷程尚未作用中（例如，未處於測試模式或未上線），或是自訂動作觸發與第二個歷程準備好接收之間有時間間隔，則可能會發生閒置逾時。 在觸發自訂動作之前，請確定目標歷程已發佈或處於測試模式。

* **正在診斷捨棄事件** — 如果您在記錄檔中看到捨棄事件，請檢查歷程記錄檔和Splunk追蹤以確認是否已收到該事件，但因資格（承載不符合規則）或時間限制而捨棄該事件。 確保第二個歷程的開始日期和設定正確，且歷程處於其有效日期範圍內。

若要在通過自訂動作鏈結歷程時避免捨棄事件，請根據第二個歷程的事件規則驗證事件裝載，並確認目標歷程為上線或處於測試中且在其有效日期範圍內。

## 其他資源

瀏覽以下章節，進一步瞭解設定及使用自訂動作：

* [開始使用自訂動作](../action/action.md) — 瞭解什麼是自訂動作，以及它們如何協助您連線至您的協力廠商系統
* [設定您的自訂動作](../action/about-custom-action-configuration.md) — 瞭解如何建立和設定自訂動作
* [使用自訂動作](../building-journeys/using-custom-actions.md) — 瞭解如何在歷程中使用自訂動作
* [將集合傳遞至自訂動作引數](../building-journeys/collections.md) — 瞭解如何在執行階段動態填入的自訂動作引數中傳遞集合

