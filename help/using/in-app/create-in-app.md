---
title: 在Journey Optimizer中建立應用程式內通知
description: 瞭解如何在Journey Optimizer中建立應用程式內訊息
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 應用程式內、訊息、建立、開始
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '1961'
ht-degree: 13%

---

# 建立應用程式內訊息 {#create-in-app}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_triggers"
>title="管理應用程式內觸發器"
>abstract="透過選取將會啟動訊息的特定活動與條件，有效率地管理觸發器。透過規則產生器，使用者可以定義精確的條件與值。符合這些條件時，就會觸發一系列的動作，包括傳遞應用程式內的訊息。"

您可以在行銷活動或歷程中新增應用程式內訊息。 請依照下列詳細步驟，在兩個內容中建立應用程式內訊息。

請注意，使用者在作業系統上選擇加入或選擇退出推播通知，並不會影響應用程式內訊息。

>[!BEGINTABS]

>[!TAB 將應用程式內訊息新增至歷程]

若要在歷程中新增應用程式內訊息，請遵循下列步驟：

1. 開啟您的歷程，然後拖放 **[!UICONTROL 應用程式內]** 活動來自 **[!UICONTROL 動作]** 區段。

   當設定檔到達其歷程結尾時，顯示給設定檔的任何應用程式內訊息都會自動過期。 因此，會在應用程式內活動後自動新增等待活動，以確保適當的時機。

   ![](assets/in_app_journey_1.png)

1. 輸入 **[!UICONTROL 標籤]** 和 **[!UICONTROL 說明]** 您的訊息。

1. 選擇 [應用程式內表面](inapp-configuration.md) 以使用。

   ![](assets/in_app_journey_2.png)

1. 您現在可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。 [了解更多](design-in-app.md)

1. 按一下 **[!UICONTROL 編輯觸發程式]** 以選擇將觸發訊息的事件和條件。 規則產生器可讓使用者指定條件和值，在符合條件時會觸發一組動作，例如傳送應用程式內訊息。

   ![](assets/in_app_journey_4.png)

   1. 視需要按一下事件下拉式清單，以變更您的觸發器。

      +++請參閱可用的觸發器。

      | 套件 | 觸發 | 定義 |
      |---|---|---|
      | 傳送資料至Platform | 已將資料傳送至Platform | 在行動應用程式發出邊緣體驗事件以將資料傳送至Adobe Experience Platform時觸發。 通常是API呼叫 [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) 從AEP Edge擴充功能。 |
      | 核心追蹤 | 追蹤動作 | 當行動程式碼API中提供的舊版功能時觸發 [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) 稱為。 |
      | 核心追蹤 | 追蹤狀態 | 當行動程式碼API中提供的舊版功能時觸發 [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) 稱為。 |
      | 核心追蹤 | 收集PII | 當行動程式碼API中提供的舊版功能時觸發 [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) 稱為。 |
      | 應用程式生命週期 | 應用程式啟動 | 在每次執行時觸發，包括當機和安裝。在超過生命週期工作階段逾時的情況下，也會在從背景恢復時觸發。 |
      | 應用程式生命週期 | 應用程式安裝 | 在安裝或重新安裝後首次執行時觸發。 |
      | 應用程式生命週期 | 應用程式更新 | 在升級或版本編號變更後首次執行時觸發。 |
      | 應用程式生命週期 | 應用程式關閉 | 應用程式關閉時觸發。 |
      | 應用程式生命週期 | 應用程式當機 | 於關閉前，應用程式不在背景執行時觸發。事件會在當機後啟動應用程式時傳送。 Adobe Mobile 當機報告不會實施未攔截之例外狀況的全域處理常式。 |
      | 地點 | 輸入POI | 當您的客戶進入您設定的興趣點(POI)時，由Places SDK觸發。 |
      | 地點 | 退出POI | 在您的客戶離開您設定的興趣點(POI)時，由Places SDK觸發。 |

+++

   1. 按一下 **[!UICONTROL 新增條件]** 是否希望觸發器考量多個事件或條件。

   1. 選擇 **[!UICONTROL 或]** 條件（若您想要新增更多） **[!UICONTROL 觸發器]** 以進一步展開規則。

      ![](assets/in_app_create_3.png)

   1. 選擇 **[!UICONTROL 與]** 條件（如果想要新增） **[!UICONTROL 特徵]** 更進一步微調規則。

      +++檢視可用的特徵。

      | 套件 | 特徵 | 定義 |
      |---|---|---|
      | 裝置資訊 | 電信業者名稱 | 當符合清單中的其中一個電信業者名稱時觸發。 |
      | 裝置資訊 | 裝置名稱 | 符合其中一個裝置名稱時觸發。 |
      | 裝置資訊 | 地區設定 | 當符合清單中的語言之一時觸發。 |
      | 裝置資訊 | 作業系統版本 | 當符合其中一個指定的作業系統版本時觸發。 |
      | 裝置資訊 | 舊版作業系統 | 符合其中一個指定的先前作業系統版本時觸發。 |
      | 裝置資訊 | 執行模式 | 如果「執行」模式為應用程式或擴充功能，則會觸發。 |
      | 應用程式生命週期 | 應用程式 ID | 符合指定的應用程式ID時觸發。 |
      | 應用程式生命週期 | 星期幾 | 當符合指定的星期幾時觸發。 |
      | 應用程式生命週期 | 首次使用後間隔天數 | 當符合自首次使用以來的指定天數時觸發。 |
      | 應用程式生命週期 | 上次使用後間隔天數 | 當符合自上次使用以來的指定天數時觸發。 |
      | 應用程式生命週期 | 升級後間隔天數 | 當符合自上次升級以來的指定天數時觸發。 |
      | 應用程式生命週期 | 安裝日期 | 當符合指定的安裝日期時觸發。 |
      | 應用程式生命週期 | 啟動 | 當符合指定的啟動次數時觸發。 |
      | 應用程式生命週期 | 時間 | 符合指定的當日時間時觸發。 |
      | 地點 | 目前POI | 當您的客戶進入指定的興趣點(POI)時，由Places SDK觸發。 |
      | 地點 | 上次輸入的POI | 根據您上次進入興趣點(POI)的客戶，由Places SDK觸發。 |
      | 地點 | 上次退出的POI | 根據您的客戶上次退出興趣點(POI)，由Places SDK觸發。 |

+++

      ![](assets/in_app_create_8.png)

   1. 按一下 **[!UICONTROL 建立群組]** 將觸發程式群組在一起。

      ![](assets/in_app_journey_3.png)

   1. 選擇應用程式內訊息生效時的觸發頻率：

      * **[!UICONTROL 每次都顯示]**：永遠顯示中選取的事件時的訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
      * **[!UICONTROL 顯示一次]**：僅在中選取的事件第一次顯示這則訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
      * **[!UICONTROL 顯示直到點進為止]**：當在選取的事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單會一直出現，直到SDK以「已點按」的動作傳送互動事件為止。

1. 如有必要，請拖放其他動作或事件以完成您的歷程流程。 [了解更多](../building-journeys/about-journey-activities.md)

1. 應用程式內訊息準備就緒後，請完成設定並發佈您的歷程以將其啟用。

有關如何設定歷程的詳細資訊，請參閱 [此頁面](../building-journeys/journey-gs.md).

>[!TAB 新增應用程式內訊息至行銷活動]

若要在促銷活動中新增應用程式內訊息，請遵循下列步驟：

1. 存取 **[!UICONTROL 行銷活動]** 功能表，然後按一下 **[!UICONTROL 建立行銷活動]**.

1. 在 **[!UICONTROL 屬性]** 區段，選取行銷活動執行型別的時機：排程或API觸發。 進一步瞭解中的行銷活動型別 [此頁面](../campaigns/create-campaign.md#campaigntype).

1. 在 **[!UICONTROL 動作]** 區段，選擇 **[!UICONTROL 應用程式內訊息]** 和 **[!UICONTROL 應用程式表面]** 先前為您的應用程式內訊息所設定。 然後，按一下 **[!UICONTROL 建立]**.

   進一步瞭解中的應用程式內設定，請參閱 [此頁面](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. 從 **[!UICONTROL 屬性]** 區段，輸入 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]** 說明。

1. 若要將自訂或核心資料使用標籤指派給應用程式內訊息，請選取 **[!UICONTROL 管理存取權]**. [了解更多](../administration/object-based-access.md)。

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform對象清單定義要定位的對象。 [了解更多](../audience/about-audiences.md)。

   ![](assets/in_app_create_2.png)

1. 在 **[!UICONTROL 身分名稱空間]** 欄位，選擇要使用的名稱空間，以識別所選對象中的個人。 [了解更多](../event/about-creating.md#select-the-namespace)。

1. 按一下 **[!UICONTROL 建立實驗]** 開始設定內容實驗並建立處理方式，以測量其效能並識別目標對象的最佳選項。 [了解更多](../content-management/content-experiment.md)

1. 按一下 **[!UICONTROL 編輯觸發程式]** 以選擇將觸發訊息的事件和條件。 規則產生器可讓使用者指定條件和值，在符合條件時會觸發一組動作，例如傳送應用程式內訊息。

   1. 視需要按一下事件下拉式清單，以變更您的觸發器。

      +++請參閱可用的觸發器。

      | 套件 | 觸發 | 定義 |
      |---|---|---|
      | 傳送資料至Platform | 已將資料傳送至Platform | 在行動應用程式發出邊緣體驗事件以將資料傳送至Adobe Experience Platform時觸發。 通常是API呼叫 [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent) 從AEP Edge擴充功能。 |
      | 核心追蹤 | 追蹤動作 | 當行動程式碼API中提供的舊版功能時觸發 [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction) 稱為。 |
      | 核心追蹤 | 追蹤狀態 | 當行動程式碼API中提供的舊版功能時觸發 [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate) 稱為。 |
      | 核心追蹤 | 收集PII | 當行動程式碼API中提供的舊版功能時觸發 [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii) 稱為。 |
      | 應用程式生命週期 | 應用程式啟動 | 在每次執行時觸發，包括當機和安裝。在超過生命週期工作階段逾時的情況下，也會在從背景恢復時觸發。 |
      | 應用程式生命週期 | 應用程式安裝 | 在安裝或重新安裝後首次執行時觸發。 |
      | 應用程式生命週期 | 應用程式更新 | 在升級或版本編號變更後首次執行時觸發。 |
      | 應用程式生命週期 | 應用程式關閉 | 應用程式關閉時觸發。 |
      | 應用程式生命週期 | 應用程式當機 | 於關閉前，應用程式不在背景執行時觸發。事件會在當機後啟動應用程式時傳送。 Adobe Mobile 當機報告不會實施未攔截之例外狀況的全域處理常式。 |
      | 地點 | 輸入POI | 當您的客戶進入您設定的興趣點(POI)時，由Places SDK觸發。 |
      | 地點 | 退出POI | 在您的客戶離開您設定的興趣點(POI)時，由Places SDK觸發。 |

+++

   1. 按一下 **[!UICONTROL 新增條件]** 是否希望觸發器考量多個事件或條件。

   1. 選擇 **[!UICONTROL 或]** 條件（若您想要新增更多） **[!UICONTROL 觸發器]** 以進一步展開規則。

      ![](assets/in_app_create_3.png)

   1. 選擇 **[!UICONTROL 與]** 條件（如果想要新增） **[!UICONTROL 特徵]** 更進一步微調規則。

      +++檢視可用的特徵。

      | 套件 | 特徵 | 定義 |
      |---|---|---|
      | 裝置資訊 | 電信業者名稱 | 當符合清單中的其中一個電信業者名稱時觸發。 |
      | 裝置資訊 | 裝置名稱 | 符合其中一個裝置名稱時觸發。 |
      | 裝置資訊 | 地區設定 | 當符合清單中的語言之一時觸發。 |
      | 裝置資訊 | 作業系統版本 | 當符合其中一個指定的作業系統版本時觸發。 |
      | 裝置資訊 | 舊版作業系統 | 符合其中一個指定的先前作業系統版本時觸發。 |
      | 裝置資訊 | 執行模式 | 如果「執行」模式為應用程式或擴充功能，則會觸發。 |
      | 應用程式生命週期 | 應用程式 ID | 符合指定的應用程式ID時觸發。 |
      | 應用程式生命週期 | 星期幾 | 當符合指定的星期幾時觸發。 |
      | 應用程式生命週期 | 首次使用後間隔天數 | 當符合自首次使用以來的指定天數時觸發。 |
      | 應用程式生命週期 | 上次使用後間隔天數 | 當符合自上次使用以來的指定天數時觸發。 |
      | 應用程式生命週期 | 升級後間隔天數 | 當符合自上次升級以來的指定天數時觸發。 |
      | 應用程式生命週期 | 安裝日期 | 當符合指定的安裝日期時觸發。 |
      | 應用程式生命週期 | 啟動 | 當符合指定的啟動次數時觸發。 |
      | 應用程式生命週期 | 時間 | 符合指定的當日時間時觸發。 |
      | 地點 | 目前POI | 當您的客戶進入指定的興趣點(POI)時，由Places SDK觸發。 |
      | 地點 | 上次輸入的POI | 根據您上次進入興趣點(POI)的客戶，由Places SDK觸發。 |
      | 地點 | 上次退出的POI | 根據您的客戶上次退出興趣點(POI)，由Places SDK觸發。 |

+++

      ![](assets/in_app_create_8.png)

   1. 按一下 **[!UICONTROL 建立群組]** 將觸發程式群組在一起。

1. 選擇應用程式內訊息生效時的觸發頻率。 提供下列選項：

   * **[!UICONTROL 每次]**：永遠顯示中選取的事件時的訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
   * **[!UICONTROL 一次]**：僅在中選取的事件第一次顯示這則訊息 **[!UICONTROL 行動應用程式觸發器]** 會出現下拉式清單。
   * **[!UICONTROL 直到點進為止]**：當在選取的事件時顯示此訊息 **[!UICONTROL 行動應用程式觸發器]** 下拉式清單會一直出現，直到SDK以「已點按」的動作傳送互動事件為止。
   * **[!UICONTROL X次數]**：此訊息顯示X次。

1. 如有需要，請選擇要 **[!UICONTROL 星期]** 或 **[!UICONTROL 時間]** 將會顯示應用程式內訊息。

1. 行銷活動旨在特定日期或循環頻率執行。 瞭解如何設定 **[!UICONTROL 排程]** 中的行銷活動 [本節](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. 您現在可以開始使用設計內容 **[!UICONTROL 編輯內容]** 按鈕。 [了解更多](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 作法影片{#video}

* 以下影片說明如何在行銷活動中建立、設定和發佈應用程式內訊息。

  +++請觀看影片

  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

+++

* 以下影片說明如何設定和分析A/B測試應用程式內訊息的內容實驗。

  +++請觀看影片

  >[!VIDEO](https://video.tv.adobe.com/v/3419898)

+++

* 以下影片說明如何在歷程中建立應用程式內訊息，以及如何測試和發佈您的歷程。

  +++請觀看影片

  >[!VIDEO](https://video.tv.adobe.com/v/3423077)

+++

**相關主題：**

* [設計應用程式內訊息](design-in-app.md)
* [測試並傳送您的應用程式內訊息](send-in-app.md)
* [應用程式內報告](../reports/campaign-global-report.md#inapp-report)
* [應用程式內設定](inapp-configuration.md)