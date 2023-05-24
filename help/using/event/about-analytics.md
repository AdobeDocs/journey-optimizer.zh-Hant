---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Analytics 整合
description: 瞭解如何在Journey Optimizer利用Adobe Analytics資料
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 分析，整合， web sdk，平台
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# 使用Adobe Analytics資料 {#analytics-data}

您可以利用您已通過Adobe Analytics或Web SDK捕獲並流入Adobe Experience Platform的所有Web行為事件資料，以觸發旅程並為客戶自動化體驗。

為了與Adobe Analytics合作，您必須：

1. 激活要使用的報表套件。 [了解更多](#leverage-analytics-data)
1. 使Journey Optimizer能夠使用您的Adobe Analytics資料源。 [了解更多](#activate-analytics-data)
1. 在旅途中添加特定事件。 [了解更多](#event-analytic)

>[!NOTE]
>
>本節僅適用於需要使用Adobe Analytics或Web SDK資料的基於規則的事件和客戶。
> 
>如果您使用Adobe Customer Journey Analytics，請參閱 [此頁](../reports/cja-ajo.md)。

## 配置Adobe Analytics或Web SDK資料 {#leverage-analytics-data}

來自Adobe Analytics或Adobe Experience PlatformWeb SDK的資料需要在您的旅途中使用。

請依照下列步驟執行此操作：

1. 瀏覽到 **[!UICONTROL 源]** 的子菜單。

1. 在「Adobe Analytics」部分，選擇 **[!UICONTROL 添加資料]**

   ![](assets/ajo-aa_1.png)

1. 從可用的Adobe Analytics報告套件清單中，選擇 **[!UICONTROL 報表套件]** 的子菜單。 然後，按一下 **[!UICONTROL 下一個]**。

   ![](assets/ajo-aa_2.png)

1. 選擇是要使用預設方案還是自定義方案。

1. 從 **[!UICONTROL 資料流詳細資訊]** 螢幕，選擇 **[!UICONTROL 資料流名稱]**。

1. 配置完成後，按一下 **[!UICONTROL 完成]**。

   ![](assets/ajo-aa_3.png)

這將啟用該報告套件的分析源連接器。 每當資料進入時，它就會轉換為「體驗」活動併發送到Adobe Experience Platform。

![](assets/ajo-aa_4.png)

瞭解有關中的Adobe Analytics源連接器的詳細資訊  [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hant){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=zh-Hant){target="_blank"}。

## 激活此配置 {#activate-analytics-data}

完成此配置後，請與Adobe聯繫，使Journey Optimizer環境能夠使用此資料源。 此步驟僅對Adobe Analytics資料源是必需的。 要執行此操作，請執行以下操作：

1. 獲取資料源ID。 此資訊在用戶介面中可用：瀏覽到從 **資料流** 頁籤 **源** 的子菜單。 找到它的最簡單方法是過濾Adobe Analytics源。
1. 聯繫Adobe客戶關懷，具體包括以下詳細資訊：

   * 主題：啟用Adobe Analytics事件進行旅程

   * 內容：請啟用我的環境以使用AA事件。

      * 組織ID:&quot;XXX@AdobeOrg&quot;

      * 資料源ID:&quot;ID:xxxx&quot;

1. 一旦確認您的環境已準備好，您就可以在您的旅途中使用Adobe Analytics資料。

## 使用Adobe Analytics或Web SDK資料建立活動行程 {#event-analytics}

現在，您可以基於Adobe Analytics或Adobe Experience PlatformWeb SDK資料建立一個活動，以用於旅程。

在下面的示例中，瞭解如何將產品添加到購物車中的用戶作為目標：

* 如果訂單完成，用戶將在兩天後收到一封后續電子郵件，要求提供反饋。
* 如果訂單未完成，用戶將收到一封電子郵件，提醒他們完成訂單。

1. 從Adobe Journey Optimizer，進入 **[!UICONTROL 配置]** 的子菜單。

1. 然後，選擇 **[!UICONTROL 管理]** 從 **[!UICONTROL 事件]** 卡。

   ![](assets/ajo-aa_5.png)

1. 按一下 **[!UICONTROL 建立事件]**。 事件設定窗格會在畫面右側開啟。

1. 填寫 **[!UICONTROL 事件]** 參數：

   * **[!UICONTROL 名稱]**:個性化您的名稱 **[!UICONTROL 事件]**。
   * **[!UICONTROL 類型]**:選擇 **[!UICONTROL 酉]** 鍵入。 [了解更多](../event/about-events.md)
   * **[!UICONTROL 事件ID類型]**:選擇 **[!UICONTROL 基於規則]** 事件ID類型。 [了解更多](../event/about-events.md#event-id-type)
   * **[!UICONTROL 架構]**:選擇分析或WebSDK架構 [建立之前](#leverage-analytics-data)。
   * **[!UICONTROL 欄位]**:選擇「負載」欄位。 [了解更多](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL 事件ID條件]**:定義條件以標識將觸發行程的事件。

      在此處，當客戶將項目添加到其購物車時，將觸發事件。
   * **[!UICONTROL 配置檔案標識符]**:從有效負載欄位中選擇一個欄位，或定義一個公式，以標識與事件關聯的人員。

   ![](assets/ajo-aa_6.png)

1. 配置後，選擇 **[!UICONTROL 保存]**。

現在該事件已準備就緒，請建立一個使用它的旅程。

1. 從 **[!UICONTROL 旅程]** 的子菜單。 如需詳細資訊，請參閱[本章節](../building-journeys/journey-gs.md)。

1. 將您以前配置的分析事件添加到您的旅途中。

   ![](assets/ajo-aa_8.png)

1. 添加在訂單完成時將觸發的事件。

1. 從 **[!UICONTROL 事件菜單]**，選擇 **[!UICONTROL 定義事件超時]** 和 **[!UICONTROL 設定超時路徑]** 頁籤

   ![](assets/ajo-aa_9.png)

1. 從超時路徑中，添加 **[!UICONTROL 電子郵件]** 操作。 此路徑將用於向未完成訂單的客戶發送電子郵件，以提醒他們他們的購物車仍然可用。

1. 添加 **[!UICONTROL 等待]** 在主路徑後進行活動，並將其設定為所需的持續時間。

   ![](assets/ajo-aa_10.png)

1. 然後，添加 **[!UICONTROL 電子郵件操作]**。 在此電子郵件中，將提示客戶提供有關已下訂單的反饋。

你現在可以test和發佈你的旅程。 [了解更多](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
