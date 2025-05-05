---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 整合
description: 瞭解如何在Journey Optimizer 中善用Adobe Analytics數據
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analytics，整合， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 0be35e14dba32523a7f28aaaa28d41ee693d44ba
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 5%

---

# 使用Adobe Analytics數據 {#analytics-data}

您可以善用已通過 Adobe Analytics 或 Web SDK 捕獲的所有 Web 行為事件資料，並流式傳輸到 Adobe Experience Platform，以便觸發旅程並為客戶自動化體驗。

為此，Adobe Analytics，您必須：

1. 激活要使用的報告套裝。 [了解更多](#leverage-analytics-data)
1. 啟用 Journey Optimizer 以使用您的Adobe Analytics資料來源。 [了解更多](#activate-analytics-data)
1. 在歷程中新增特定事件。 [了解更多](#event-analytic)

>[!NOTE]
>
>本節僅適用於規則型事件，以及需要使用Adobe Analytics或Web SDK資料的客戶。
> 
>如果您使用Adobe Customer Journey Analytics，請參閱[此頁面](../reports/cja-ajo.md)。
>

## 設定Adobe Analytics或Web SDK資料 {#leverage-analytics-data}

您必須啟用來自Adobe Analytics或Adobe Experience Platform Web SDK的資料，才能在歷程中使用。

請依照下列步驟執行此操作：

1. 瀏覽至&#x200B;**[!UICONTROL 來源]**&#x200B;功能表。

1. 在Adobe Analytics區段中，選取&#x200B;**[!UICONTROL 新增資料]**

   ![](assets/ajo-aa_1.png)

1. 從可用的Adobe Analytics報表套裝清單中，選取要啟用的&#x200B;**[!UICONTROL 報表套裝]**。 然後，按一下&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/ajo-aa_2.png)

1. 選擇是否要使用「預設」或「自定義」綱要。

1. 從數據流 **[!UICONTROL 詳細信息]** 螢幕中，選擇資料流 **[!UICONTROL 名稱]**。

1. 配置完成後，按兩下 **[!UICONTROL 完成]**。

   ![](assets/ajo-aa_3.png)

如此將可啟用該報表套裝的Analytics來源聯結器。 只要有資料進來，就會轉換為Experience事件並傳送到Adobe Experience Platform。

![](assets/ajo-aa_4.png)

在[Adobe Analytics檔案](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target="_blank"}和[教學課程](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target="_blank"}中進一步瞭解Adobe Experience Platform來源聯結器。

## 啟動此設定 {#activate-analytics-data}

完成此設定后，請連絡 Adobe Systems 讓您的 Journey Optimizer 環境使用此資料來源。 只有Adobe Analytics數據源才需要執行此步驟。 若要執行此動作：

1. 取得 資料來源 ID。 此信息在用戶介面中可用：流覽到從“源&#x200B;**”**&#x200B;功能表的數據流標籤創建的&#x200B;**&#x200B;**&#x200B;資料來源。找到它的最簡單方法是過濾Adobe Analytics來源。
1. 請連絡Adobe Systems客戶服務並提供下列詳細資料：

   * 主旨：為歷程啟用Adobe Analytics事件

   * 內容：請啟用我的環境以使用AA事件。

      * 組織ID： &quot;XXX@AdobeOrg&quot;

      * 資料來源ID： &quot;ID： xxxxx&quot;

1. 一旦您確認環境準備就緒，即可在您的歷程中使用Adobe Analytics資料。

## 使用Adobe Analytics或Web SDK資料建立包含事件的歷程 {#event-analytics}

您現在可以根據Adobe Analytics或Adobe Experience Platform Web SDK資料建立事件，以用於歷程中。

在下列範例中，瞭解如何鎖定在購物車中新增產品的使用者：

* 如果訂單已完成，使用者會在兩天後收到後續電子郵件，要求您提供意見。
* 如果訂單未完成，使用者會收到一封電子郵件，提醒他們完成訂單。

1. 從Adobe Journey Optimizer存取&#x200B;**[!UICONTROL 設定]**&#x200B;功能表。

1. 然後，從“事件&#x200B;**”**&#x200B;卡片中選擇&#x200B;**[!UICONTROL 管理]**。

   ![](assets/ajo-aa_5.png)

1. 按一下&#x200B;**[!UICONTROL 建立事件]**。 事件設定窗格會在畫面右側開啟。

1. 填入&#x200B;**[!UICONTROL 事件]**&#x200B;引數：

   * **[!UICONTROL 名稱]**：個人化&#x200B;**[!UICONTROL 活動]**&#x200B;的名稱。
   * **[!UICONTROL 型別]**：選擇&#x200B;**[!UICONTROL 單一]**&#x200B;型別。 [了解更多](../event/about-events.md)
   * **[!UICONTROL 事件ID型別]**：選擇以&#x200B;**[!UICONTROL 規則為基礎的]**&#x200B;事件ID型別。 [了解更多](../event/about-events.md#event-id-type)
   * **[!UICONTROL 結構描述]**：選取在[&#128279;](#leverage-analytics-data)之前建立的Analytics或WebSDK結構描述。
   * **[!UICONTROL 欄位]**：選取裝載欄位。 [了解更多](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID條件]**：定義條件以識別將觸發您歷程的事件。

     在此，當客戶將專案新增至購物車時會觸發事件。
   * **[!UICONTROL 設定檔識別碼]**：從您的裝載欄位選擇一個欄位，或是定義一個公式，以識別與事件相關聯的人員。

   ![](assets/ajo-aa_6.png)

1. 設定後，選取&#x200B;**[!UICONTROL 儲存]**。

現在事件已準備就緒，請建立歷程以使用它。

1. 從&#x200B;**[!UICONTROL 歷程]**&#x200B;功能表，開啟或建立歷程。 如需詳細資訊，請參閱[本章節](../building-journeys/journey-gs.md)。

1. 將之前配置的Analytics事件添加到您的旅程中。

   ![](assets/ajo-aa_8.png)

1. 添加訂單完成後將觸發的事件。

1. 從“ **[!UICONTROL 事件”功能表中]**，選擇“ **[!UICONTROL 定義事件超時]** ”和 **[!UICONTROL “設置超時路徑]** ”選項。

   ![](assets/ajo-aa_9.png)

1. 從超時路徑中，添加電子郵件&#x200B;**&#x200B;**&#x200B;作。此路徑將用來傳送電子郵件給未完成訂單的客戶，以提醒他們其購物車仍然可用。

1. 在主要路徑後新增&#x200B;**[!UICONTROL 等待]**&#x200B;活動，並將其設定為所需的持續時間。

   ![](assets/ajo-aa_10.png)

1. 然後，添加電子郵件 **[!UICONTROL 作]**。 在此電子郵件中，系統將提示客戶對已下訂單提供反饋。

您現在可以測試和發佈您的旅程。 [了解更多](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
