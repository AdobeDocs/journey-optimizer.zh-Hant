---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 整合
description: 了解如何在Journey Optimizer中運用Adobe Analytics資料
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics，整合， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# 使用Adobe Analytics資料 {#analytics-data}

您可以運用透過Adobe Analytics或Web SDK擷取並串流至Adobe Experience Platform的所有Web行為事件資料，以觸發歷程並自動化客戶體驗。

若要讓此功能與Adobe Analytics搭配使用，您必須：

1. 啟動您要使用的報表套裝。 [了解更多](#leverage-analytics-data)
1. 啟用Journey Optimizer以使用您的Adobe Analytics資料來源。 [了解更多](#activate-analytics-data)
1. 在您的歷程中新增特定事件。 [了解更多](#event-analytic)

>[!NOTE]
>
>本節僅適用於需要使用Adobe Analytics或Web SDK資料的規則型事件和客戶。
> 
>如果您使用Adobe Customer Journey Analytics，請參閱 [本頁](../reports/cja-ajo.md).

## 設定Adobe Analytics或Web SDK資料 {#leverage-analytics-data}

來自Adobe Analytics或Adobe Experience Platform Web SDK的資料必須啟用，才能用於歷程。

請依照下列步驟執行此操作：

1. 瀏覽至 **[!UICONTROL 來源]** 功能表。

1. 在Adobe Analytics區段中，選取 **[!UICONTROL 新增資料]**

   ![](assets/ajo-aa_1.png)

1. 從可用的Adobe Analytics報表套裝清單中，選取 **[!UICONTROL 報表套裝]** 啟用。 然後，按一下 **[!UICONTROL 下一個]**.

   ![](assets/ajo-aa_2.png)

1. 選擇要使用預設架構還是自定義架構。

1. 從 **[!UICONTROL 資料流詳細資訊]** 螢幕，選擇 **[!UICONTROL 資料流名稱]**.

1. 完成設定後，按一下 **[!UICONTROL 完成]**.

   ![](assets/ajo-aa_3.png)

如此可啟用該報表套裝的Analytics來源連接器。 每當資料傳入時，都會轉換為Experience事件並傳送至Adobe Experience Platform。

![](assets/ajo-aa_4.png)

進一步了解Adobe Analytics來源連接器，位於  [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hant){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=zh-Hant){target="_blank"}.

## 啟動此配置 {#activate-analytics-data}

完成此設定後，請連絡Adobe，讓您的Journey Optimizer環境能使用此資料來源。 只有Adobe Analytics資料來源需要此步驟。 若要執行此動作：

1. 取得資料來源ID。 此資訊可在使用者介面中使用：瀏覽至您從 **資料流** 的 **來源** 功能表。 要找到它，最簡單的方式是篩選Adobe Analytics來源。
1. 請聯絡Adobe客戶服務，並提供下列詳細資訊：

   * 主題：啟用歷程的Adobe Analytics事件

   * 內容：請讓我的環境使用AA事件。

      * 組織ID:&quot;XXX@AdobeOrg&quot;

      * 資料來源ID:&quot;ID:xxxx」

1. 一旦確認您的環境已就緒後，您就可以在歷程中使用Adobe Analytics資料。

## 使用Adobe Analytics或Web SDK資料建立具有事件的歷程 {#event-analytics}

您現在可以根據要用於歷程的Adobe Analytics或Adobe Experience Platform Web SDK資料來建立事件。

在以下範例中，了解如何將新增產品至購物車的使用者鎖定為目標：

* 如果訂單完成，使用者會在兩天後收到後續電子郵件，詢問回饋。
* 如果訂單未完成，使用者會收到電子郵件以提醒他們完成訂單。

1. 從Adobe Journey Optimizer存取 **[!UICONTROL 設定]** 功能表。

1. 然後，選取 **[!UICONTROL 管理]** 從 **[!UICONTROL 事件]** 卡片。

   ![](assets/ajo-aa_5.png)

1. 按一下 **[!UICONTROL 建立事件]**. 事件設定窗格會在畫面右側開啟。

1. 填入 **[!UICONTROL 事件]** 參數：

   * **[!UICONTROL 名稱]**:個人化您的 **[!UICONTROL 事件]**.
   * **[!UICONTROL 類型]**:選擇 **[!UICONTROL 單一]** 類型。 [了解更多](../event/about-events.md)
   * **[!UICONTROL 事件ID類型]**:選擇 **[!UICONTROL 規則型]** 事件ID類型。 [了解更多](../event/about-events.md#event-id-type)
   * **[!UICONTROL 結構]**:選取Analytics或WebSDK結構 [建立於之前](#leverage-analytics-data).
   * **[!UICONTROL 欄位]**:選取「裝載」欄位。 [了解更多](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID條件]**:定義條件以識別將觸發歷程的事件。

      在此，當客戶新增項目至購物車時，就會觸發事件。
   * **[!UICONTROL 設定檔識別碼]**:從您的裝載欄位中選擇欄位，或定義公式，以識別與事件相關聯的人員。

   ![](assets/ajo-aa_6.png)

1. 設定後，請選取 **[!UICONTROL 儲存]**.

事件準備就緒後，請建立歷程以使用它。

1. 從 **[!UICONTROL 歷程]** 功能表、開啟或建立歷程。 如需詳細資訊，請參閱[本章節](../building-journeys/journey-gs.md)。

1. 將先前設定的Analytics事件新增至歷程。

   ![](assets/ajo-aa_8.png)

1. 新增訂單完成時將觸發的事件。

1. 從 **[!UICONTROL 事件功能表]**，請選取 **[!UICONTROL 定義事件逾時]** 和 **[!UICONTROL 設定逾時路徑]** 選項。

   ![](assets/ajo-aa_9.png)

1. 從逾時路徑新增 **[!UICONTROL 電子郵件]** 動作。 此路徑將用來傳送電子郵件給未完成訂單的客戶，提醒他們購物車仍然可用。

1. 新增 **[!UICONTROL 等待]** 活動（在主路徑後），並將其設為所需的持續時間。

   ![](assets/ajo-aa_10.png)

1. 然後，新增 **[!UICONTROL 電子郵件動作]**. 在此電子郵件中，系統會提示客戶提供已下單的回饋。

您現在可以測試並發佈您的歷程。 [了解更多](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
