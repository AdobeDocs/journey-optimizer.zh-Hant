---
solution: Journey Optimizer
product: journey optimizer
title: 建立行銷活動
description: 瞭解如何在Journey Optimizer中建立行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 建立，最佳化工具，行銷活動，表面，訊息
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 2edff0123084fa1736fb8198c3b4e8ff4e40341d
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 33%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>建立新行銷活動之前，請確定您有可供使用的表面頻道（即訊息預設集）和Adobe Experience Platform對象。 請在以下章節瞭解更多資訊：
>
>* [建立管道表面](../configuration/channel-surfaces.md)
>* [開始使用對象](../audience/about-audiences.md)

若要建立新行銷活動，請存取 **[!UICONTROL 行銷活動]** 功能表，然後按一下 **[!UICONTROL 建立行銷活動]**. 您也可以複製現有的即時行銷活動，以建立新的行銷活動。 [了解更多](modify-stop-campaign.md#duplicate)

## 選擇行銷活動類型和管道 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="**排程的行銷活動**&#x200B;會立即執行或在指定的日期執行，其目的在傳送行銷類型訊息。**API 觸發的**&#x200B;行銷活動是使用 API 呼叫執行的。這些目的是傳送行銷訊息 (需要使用者同意的促銷訊息) 或交易型訊息 (非商業訊息，也可以在特定情況下傳送到未訂閱的設定檔)。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="行銷活動類別"
>abstract="如果您正在建立排程的行銷活動，系統會自動選取&#x200B;**行銷**&#x200B;類型。若是 API 觸發的行銷活動，選擇您是否要傳送&#x200B;**行銷**&#x200B;訊息 (需要使用者同意的促銷訊息) 或&#x200B;**交易型**&#x200B;訊息 (非商業訊息，也可以在特定情況下傳送到未訂閱的設定檔)。"

1. 在 **[!UICONTROL 屬性]** 區段，指定您要如何執行行銷活動。 可用的行銷活動型別有兩種：

   * **[!UICONTROL 已排程]**：立即執行促銷活動，或在指定日期執行。 已排程的行銷活動旨在傳送 **行銷** 訊息。 可從使用者介面設定及執行。

   * **[!UICONTROL API觸發]**：使用API呼叫執行行銷活動。 API觸發的行銷活動旨在傳送 **行銷**，或 **異動** 訊息，即在個人執行動作後傳送的訊息：密碼重設、購物車購買等。 [瞭解如何使用API觸發行銷活動](api-triggered-campaigns.md)

1. 如果您正在建立排程的行銷活動，系統會自動選取&#x200B;**行銷**&#x200B;類型。針對API觸發的行銷活動，選取是否要傳送 **行銷** 或 **異動** 訊息。」

1. 在 **[!UICONTROL 動作]** 區段，選擇頻道和用來傳送訊息的頻道介面。

   表面是由[系統管理員](../start/path/administrator.md)定義的設定。它包含所有用於傳送訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   下拉式清單中只會列出與行銷活動型別相容的管道表面。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果您要建立推播通知行銷活動，可以啟用 **[!UICONTROL 快速傳送模式]**，這是Journey Optimizer的附加元件，可讓您以非常快的速度大量傳送推播訊息。 [了解更多](../push/create-push.md#rapid-delivery)

1. 按一下 **[!UICONTROL 建立]** 以建立行銷活動。

## 定義行銷活動屬性 {#create}

1. 在 **[!UICONTROL 屬性]** 區段，指定行銷活動的名稱和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 此 **標籤** 欄位可讓您將Adobe Experience Platform統一標籤指派給您的行銷活動。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

1. 若要指派自訂或核心資料使用標籤給促銷活動，請按一下 **[!UICONTROL 管理存取權]** 按鈕。 [深入瞭解物件層級存取控制(OLA)](../administration/object-based-access.md)

## 建立訊息並設定追蹤 {#content}

在 **[!UICONTROL 動作]** 區段，建立要與行銷活動一起傳送的訊息。

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，然後建立並設計您的訊息內容。

   在以下頁面瞭解建立訊息內容的詳細步驟：

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
    <a href="../sms/create-sms.md"><strong>建立簡訊</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. 定義內容後，請使用 **[!UICONTROL 模擬內容]** 按鈕以使用測試設定檔預覽和測試您的內容。 [了解更多](../content-management/preview-test.md)。

1. 按一下箭頭，返回行銷活動建立畫面。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL 動作追蹤]** 部分，指定是否要追蹤收件者對傳送的反應：您可以追蹤點選和/或開啟。

   一旦執行行銷活動，即可從行銷活動報表存取追蹤結果。 [進一步瞭解行銷活動報告](../reports/campaign-global-report.md)

## 定義對象 {#audience}

按一下 **[!UICONTROL 選取對象]** 按鈕來顯示可用Adobe Experience Platform對象清單。 [進一步了解對象](../audience/about-audiences.md)

>[!IMPORTANT]
>
>使用來自的對象和屬性 [對象構成](../audience/get-started-audience-orchestration.md) 和 [自訂上傳（CSV檔案）對象](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience) 目前不適用於Healthcare Shield或Privacy and Security Shield。
>
>針對API觸發的行銷活動，必須透過API呼叫設定對象。

在 **[!UICONTROL 身分名稱空間]** 欄位，選擇要使用的名稱空間，以識別所選區段中的個人。

如果屬於區段的個人在不同身分中沒有選取的身分（名稱空間），則行銷活動不會鎖定該個人。 [進一步瞭解名稱空間](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 排程行銷活動 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="行銷活動排程"
>abstract="預設情況下，行銷活動經由手動啟動開始執行，並在訊息傳送一次後立即終止。不過，你可以彈性設定發送訊息的具體日期和時間。此外，你可以對定期執行或 API 觸發的行銷活動指定結束日期。在操作觸發條件中，你亦可根據自己的偏好設定訊息傳送頻率。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="行銷活動開始"
>abstract="指定傳送訊息的日期和時間。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="行銷活動結束"
>abstract="指定應停止執行週期性行銷活動的時間。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="行銷活動動作觸發程序"
>abstract="定義應傳送行銷活動訊息的頻率。"

根據預設，行銷活動在手動啟動後開始，並在傳送一次訊息後立即結束。

您可以定義行銷活動訊息的傳送頻率。 若要這麼做，請使用 **[!UICONTROL 動作觸發程式]** 行銷活動建立畫面中的選項，用於指定行銷活動應每日、每週或每月執行。

如果您不想在行銷活動啟動後立即執行，您可以使用來指定傳送訊息的日期和時間 **[!UICONTROL 行銷活動開始]** 選項。 此 **[!UICONTROL 行銷活動結束]** 選項可讓您指定循環行銷活動何時應停止執行。

![](assets/create-campaign-schedule.png)

行銷活動準備就緒後，您即可進行檢閱和發佈。 [了解更多](review-activate-campaign.md)
