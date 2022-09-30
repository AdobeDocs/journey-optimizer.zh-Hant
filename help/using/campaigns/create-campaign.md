---
title: 建立行銷活動
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
source-git-commit: 845a8324d96d8891bf1edf64a0962d23976bb29e
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 9%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>建立新促銷活動之前，請確定您有表面通道（即訊息預設集）和Adobe Experience Platform區段可供使用。 了解更多資訊：
>
>* [建立頻道介面](../configuration/channel-surfaces.md)
>* [開始使用區段](../segment/about-segments.md)


## 建立您的第1個行銷活動 {#create}

1. 存取 **[!UICONTROL 行銷活動]** ，然後按一下 **[!UICONTROL 建立行銷活動]**.

   >[!NOTE]
   >
   >您也可以複製現有的即時促銷活動以建立新促銷活動。 [了解更多](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. 在 **[!UICONTROL 屬性]** 區段，指定您要執行促銷活動的時間：

   * **[!UICONTROL 已排程]**:立即執行促銷活動或在指定日期執行。 排程的行銷活動旨在傳送 **行銷** 輸入訊息。
   * **[!UICONTROL API觸發]**:使用API呼叫執行促銷活動。 API觸發的行銷活動旨在傳送 **異動** 訊息，即在個人執行的動作後傳出的訊息：密碼重設、卡放棄等。 [了解如何使用API觸發行銷活動](api-triggered-campaigns.md)

1. 在 **[!UICONTROL 動作]** 區段，選取要用來傳送訊息的通道和通道表面，然後按一下 **[!UICONTROL 建立]**.

   介面是由[系統管理員](../start/path/administrator.md)定義的設定。 它包含所有用於春頌訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉式清單中只列出與行銷促銷活動類型相容的管道表面。

1. 指定促銷活動的標題和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 在 **[!UICONTROL 動作]** 區段，設定要與促銷活動一起傳送的訊息：

   1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，然後配置和設計您的消息內容。 [進一步了解訊息](../messages/get-started-content.md).

      若要瞭解建立訊息內容的詳細步驟，請至以下頁面：

      * [建立電子郵件](../messages/create-email.md)
      * [建立推播通知](../messages/create-push.md)
      * [建立 SMS 訊息](../messages/create-sms.md)
   1. 定義內容後，請使用 **[!UICONTROL 模擬內容]** 按鈕，使用測試設定檔預覽和測試您的內容。 [了解更多](../design/preview.md)。

   1. 按一下箭頭，返回行銷活動建立畫面。

      ![](assets/create-campaign-design.png)

   1. 在 **[!UICONTROL 動作追蹤]** 區段中，指定是否要追蹤收件者對您傳送的反應：您可以追蹤點按和/或開啟次數。

      執行促銷活動後，即可從促銷活動報表存取追蹤結果。 [進一步了解行銷活動報告](../reports/campaign-global-report.md)


1. 定義要鎖定的對象。 若要這麼做，請按一下 **[!UICONTROL 選取對象]** 按鈕以顯示可用的Adobe Experience Platform區段清單。 [深入了解區段](../segment/about-segments.md)

   >[!NOTE]
   >
   >針對API觸發的促銷活動，對象必須透過API呼叫來設定。 [了解更多](api-triggered-campaigns.md)

   在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。 [進一步了解命名空間](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >屬於某個區段的個人若未在其不同身分之間選取身分（命名空間），該促銷活動將不會鎖定該目標。

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

1. 若要在特定日期或循環頻率上執行促銷活動，請設定 **[!UICONTROL 排程]** 區段。 [了解如何排程行銷活動](#schedule)

1. 若要將自訂或核心資料使用量標籤指派給促銷活動，請按一下 **[!UICONTROL 管理存取]** 按鈕。 [進一步了解對象級訪問控制(OLA)](../administration/object-based-access.md)

一旦您的促銷活動準備就緒，您就可以檢閱並發佈。 [了解更多](#review-activate)

## 排程促銷活動 {#schedule}

依預設，促銷活動在手動啟動後就會開始，而在訊息傳送一次後立即結束。

您可以定義應傳送促銷活動訊息的頻率。 若要這麼做，請使用 **[!UICONTROL 動作觸發器]** 選項，以指定促銷活動應按日、每週或每月執行。

如果您不想在促銷活動啟動後立即執行，您可以使用 **[!UICONTROL 促銷活動開始]** 選項。 此  **[!UICONTROL 促銷活動結束]** 選項可讓您指定循環促銷活動何時應停止執行。

![](assets/create-campaign-schedule.png)

## 快速傳遞模式 {#rapid-delivery}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_rapid_delivery"
>title="快速傳遞模式"
>abstract="快速傳送模式是Journey Optimizer附加元件，可讓您在3000萬個設定檔下，為對象執行非個人化訊息的高速支出。"

快速傳送模式（歷程中先前稱為突發模式）是 [!DNL Journey Optimizer] 可透過促銷活動以大量傳送非常快速的推送訊息的附加元件。

當訊息傳送延遲是業務關鍵型時，或您想在行動電話上傳送緊急推播警報（例如，向已安裝您的新聞頻道應用程式的使用者傳送重大新聞），則會使用快速傳送。

如需使用快速傳送模式時效能的詳細資訊，請參閱 [Adobe Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html).

### 先決條件 {#prerequisites}

快速傳遞報文傳送附帶下列要求：

* 可快速傳送 **[!UICONTROL 已排程]** 僅限促銷活動，且不適用於API觸發的促銷活動、
* 推送訊息中不允許任何個人化，
* 目標受眾必須包含少於3000萬個設定檔，
* 您可以使用快速傳送模式同時執行最多5個促銷活動。

### 啟動快速傳遞模式

1. 建立推播通知促銷活動並切換 **[!UICONTROL 快速傳遞]** 選項。

![](assets/create-campaign-burst.png)

1. 設定訊息內容並選取要鎖定的對象。 [了解如何建立行銷活動](#create)

   >[!IMPORTANT]
   >
   >確保訊息內容不包含任何個人化，且對象包含少於3000個設定檔。

1. 照常檢閱並啟動您的行銷活動。 請注意，在測試模式中，訊息不會透過快速傳送模式傳送。 [了解如何檢閱及啟動行銷活動](review-activate-campaign.md)
