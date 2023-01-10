---
solution: Journey Optimizer
product: journey optimizer
title: 建立行銷活動
description: 了解如何在 [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ef7c1ac61a59407507e9570e1114e6ef0cb8a7ca
workflow-type: tm+mt
source-wordcount: '714'
ht-degree: 8%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>建立新促銷活動之前，請確定您有表面通道（即訊息預設集）和Adobe Experience Platform區段可供使用。 了解更多資訊：
>
>* [建立頻道介面](../configuration/channel-surfaces.md)
>* [開始使用區段](../segment/about-segments.md)


若要建立新促銷活動，請存取 **[!UICONTROL 行銷活動]** ，然後按一下 **[!UICONTROL 建立行銷活動]**. 您也可以複製現有的即時促銷活動以建立新促銷活動。 [了解更多](modify-stop-campaign.md#duplicate)

![](assets/create-campaign.png)

## 選擇促銷活動類型和渠道 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="促銷活動類型"
>abstract="針對行銷訊息，請指定傳送日期， **已排程** 類型最合適。 不過，如果您想要傳送交易式訊息，例如密碼重設或放棄卡片， **API觸發** 類型是最佳選擇。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="促銷活動類別"
>abstract="類別值直接與促銷活動類型值相關聯。 排程 **行銷** 類別和類別的API觸發類型 **交易**"

1. 在 **[!UICONTROL 屬性]** 區段，指定您要如何執行促銷活動。 可用的促銷活動有兩種類型：

   * **[!UICONTROL 已排程]**:立即執行促銷活動或在指定日期執行。 排程的行銷活動旨在傳送 **行銷** 輸入訊息。

   * **[!UICONTROL API觸發]**:使用API呼叫執行促銷活動。 API觸發的行銷活動旨在傳送 **異動** 訊息，即在個人執行的動作後傳出的訊息：密碼重設、卡放棄等。 [了解如何使用API觸發行銷活動](api-triggered-campaigns.md)

1. 在 **[!UICONTROL 動作]** 區段中，選擇要用來傳送訊息的通道和通道表面。

   介面是由[系統管理員](../start/path/administrator.md)定義的設定。 它包含所有用於春頌訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >下拉式清單中只列出與行銷促銷活動類型相容的管道表面。

1. 按一下 **[!UICONTROL 建立]** 來建立促銷活動。

## 定義促銷活動屬性 {#create}

1. 指定促銷活動的標題和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 若要將自訂或核心資料使用量標籤指派給促銷活動，請按一下 **[!UICONTROL 管理存取]** 按鈕。 [進一步了解對象級訪問控制(OLA)](../administration/object-based-access.md)

   ![](assets/create-campaign-properties.png)

## 建立訊息 {#content}

在 **[!UICONTROL 動作]** 區段中，建立要與促銷活動一起傳送的訊息。

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，然後建立和設計您的訊息內容。

   在下列頁面中了解建立訊息內容的詳細步驟：

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="銷售機會" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>建立電子郵件</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="不頻繁" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>建立推播通知</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="驗證" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>建立SMS訊息</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. 定義內容後，請使用 **[!UICONTROL 模擬內容]** 按鈕，使用測試設定檔預覽和測試您的內容。 [了解更多](../email/preview.md)。

1. 按一下箭頭，返回行銷活動建立畫面。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL 動作追蹤]** 區段中，指定是否要追蹤收件者對您傳送的反應：您可以追蹤點按和/或開啟次數。

   執行促銷活動後，即可從促銷活動報表存取追蹤結果。 [進一步了解行銷活動報告](../reports/campaign-global-report.md)

## 定義對象 {#audience}

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

## 排程促銷活動 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="促銷活動開始"
>abstract="指定應傳送訊息的日期和時間。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="促銷活動結束"
>abstract="指定循環促銷活動何時應停止執行。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Campaign動作觸發程式"
>abstract="定義應傳送促銷活動訊息的頻率。"

依預設，促銷活動在手動啟動後就會開始，而在訊息傳送一次後立即結束。

您可以定義應傳送促銷活動訊息的頻率。 若要這麼做，請使用 **[!UICONTROL 動作觸發器]** 選項，以指定促銷活動應按日、每週或每月執行。

如果您不想在促銷活動啟動後立即執行，您可以使用 **[!UICONTROL 促銷活動開始]** 選項。 此 **[!UICONTROL 促銷活動結束]** 選項可讓您指定循環促銷活動何時應停止執行。

![](assets/create-campaign-schedule.png)

一旦您的促銷活動準備就緒，您就可以檢閱並發佈。 [了解更多](review-activate-campaign.md)
