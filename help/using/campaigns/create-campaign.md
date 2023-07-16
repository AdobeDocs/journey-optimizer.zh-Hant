---
solution: Journey Optimizer
product: journey optimizer
title: 建立行銷活動
description: 瞭解如何在Journey Optimizer中建立行銷活動
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 建立，最佳化工具，行銷活動，表面，訊息
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: ceb37193797c69ee87f136f3abecf54b5927d6a2
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 28%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>建立新行銷活動之前，請確定您有可供使用的表面頻道（即訊息預設集）和Adobe Experience Platform對象。 請前往下列章節深入瞭解：
>
>* [建立頻道介面](../configuration/channel-surfaces.md)
>* [開始使用 Audiences](../audience/about-audiences.md)

若要建立新的行銷活動，請存取 **[!UICONTROL 行銷活動]** 功能表，然後按一下 **[!UICONTROL 建立行銷活動]**. 您也可以複製現有的即時行銷活動，以建立新的行銷活動。 [了解更多](modify-stop-campaign.md#duplicate)

## 選擇行銷活動型別和頻道 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="**排程的行銷活動**&#x200B;會立即執行或在指定的日期執行，其目的在傳送行銷類型訊息。**API 觸發的**&#x200B;行銷活動是使用 API 呼叫執行的。其目的是在傳送行銷訊息或異動訊息，即在個人執行以下動作後傳送的訊息：重設密碼、放棄購物車等。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="行銷活動類別"
>abstract="如果您正在建立排程的行銷活動，系統會自動選取&#x200B;**行銷**&#x200B;類型。如果是 API 觸發的行銷活動，請選擇要傳送&#x200B;**行銷**&#x200B;訊息還是&#x200B;**異動**&#x200B;訊息，即在個人執行以下動作後傳送的訊息：重設密碼、放棄購物車等。"

1. 在 **[!UICONTROL 屬性]** 區段，指定您要如何執行行銷活動。 可用的行銷活動型別有兩種：

   * **[!UICONTROL 已排程]**：立即執行行銷活動或在指定日期執行。 已排程的行銷活動旨在傳送 **行銷** 訊息。 可從使用者介面設定及執行。

   * **[!UICONTROL API觸發]**：使用API呼叫執行行銷活動。 API觸發的行銷活動旨在傳送 **行銷**，或 **異動** 訊息，即在個人執行動作後傳送的訊息：密碼重設、購物車購買等。 [瞭解如何使用API觸發行銷活動](api-triggered-campaigns.md)

1. 如果您正在建立排程的行銷活動，系統會自動選取&#x200B;**行銷**&#x200B;類型。針對API觸發的行銷活動，選擇是否要傳送 **行銷** 或 **異動** 訊息。」

1. 在 **[!UICONTROL 動作]** 區段，選擇頻道和頻道介面來用於傳送您的訊息。

   介面是由[系統管理員](../start/path/administrator.md)定義的設定。 它包含所有用於春頌訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   下拉式清單中只會列出與行銷活動型別相容的管道表面。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果您要建立推播通知行銷活動，可以啟用 **[!UICONTROL 快速傳遞模式]**，這是Journey Optimizer的附加元件，可讓您以非常快的速度大量傳送推送訊息。 [了解更多](../push/create-push.md#rapid-delivery)

1. 按一下 **[!UICONTROL 建立]** 以建立行銷活動。

## 定義行銷活動屬性 {#create}

1. 在 **[!UICONTROL 屬性]** 區段，指定行銷活動的名稱和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 此 **標籤** 欄位可讓您將Adobe Experience Platform統一標籤指派給行銷活動。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

1. 若要將自訂或核心資料使用標籤指派給促銷活動，請按一下 **[!UICONTROL 管理存取權]** 按鈕。 [進一步瞭解物件層級存取控制(OLA)](../administration/object-based-access.md)

## 建立訊息並設定追蹤 {#content}

在 **[!UICONTROL 動作]** 區段，建立要與行銷活動一起傳送的訊息。

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，然後建立並設計訊息內容。

   在以下頁面中瞭解建立訊息內容的詳細步驟：

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

1. 定義內容後，請使用 **[!UICONTROL 模擬內容]** 按鈕以使用測試設定檔預覽和測試您的內容。 [了解更多](../email/preview.md)。

1. 按一下箭頭，返回行銷活動建立畫面。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL 動作追蹤]** 區段，指定是否要追蹤收件者對傳送的反應：您可以追蹤點按和/或開啟。

   執行行銷活動後，即可從行銷活動報表存取追蹤結果。 [進一步瞭解行銷活動報告](../reports/campaign-global-report.md)

## 定義對象 {#audience}

按一下 **[!UICONTROL 選取對象]** 按鈕來顯示可用Adobe Experience Platform區段的清單。 [深入瞭解區段](../audience/about-audiences.md)

>[!NOTE]
>
>針對API觸發的行銷活動，需透過API呼叫設定對象。 [了解更多](api-triggered-campaigns.md)

在 **[!UICONTROL 身分名稱空間]** 欄位中，選擇要使用的名稱空間，以識別所選區段中的個人。 [進一步瞭解名稱空間](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

>[!NOTE]
>
>如果屬於區段的個人在不同身分中沒有選取的身分（名稱空間），則行銷活動不會鎖定該個人。

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 排程行銷活動 {#schedule}

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

依預設，行銷活動在手動啟動後開始，並在訊息傳送後立即結束。

您可以定義行銷活動訊息的傳送頻率。 若要這麼做，請使用 **[!UICONTROL 動作觸發程式]** 行銷活動建立畫面中的選項，用於指定行銷活動應每日、每週或每月執行。

如果您不想在行銷活動啟動後立即執行行銷活動，您可以使用來指定傳送訊息的日期和時間 **[!UICONTROL 行銷活動開始]** 選項。 此 **[!UICONTROL 行銷活動結束]** 選項可讓您指定循環行銷活動何時應停止執行。

![](assets/create-campaign-schedule.png)

行銷活動準備就緒後，您即可進行稽核和發佈。 [了解更多](review-activate-campaign.md)
