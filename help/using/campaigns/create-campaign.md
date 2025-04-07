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
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '1277'
ht-degree: 21%

---

# 建立行銷活動 {#create-campaign}

若要建立新的行銷活動，請瀏覽至左側邊欄上的&#x200B;**[!UICONTROL 行銷活動]**&#x200B;功能表，然後按一下&#x200B;**[!UICONTROL 建立行銷活動]**。 您也可以複製現有的即時行銷活動，以建立新的行銷活動。 [瞭解如何進行](modify-stop-campaign.md#duplicate)。

開始之前，請先閱讀[此頁面](get-started-with-campaigns.md#before-starting-campaign-prerequisites)上的行銷活動先決條件。

## 選取行銷活動類型 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="**排程的行銷活動**&#x200B;會立即執行或在指定的日期執行，其目的在傳送行銷類型訊息。**API 觸發的**&#x200B;行銷活動是使用 API 呼叫執行的。這些目的是傳送行銷訊息 (需要使用者同意的促銷訊息) 或交易型訊息 (非商業訊息，也可以在特定情況下傳送到未訂閱的設定檔)。"

建立新行銷活動時，必須先選取行銷活動的型別。 可用的行銷活動型別有三種：

1. **[!UICONTROL 已排程 — 行銷]** — 這些行銷活動會立即執行或在指定日期執行。 已排程的行銷活動旨在傳送&#x200B;**行銷**&#x200B;訊息，或建立傳入動作。 可從使用者介面設定及執行。

1. **[!UICONTROL API觸發 — 行銷]** — 這些行銷活動會使用API呼叫執行。 選取此型別的行銷活動，將個人化行銷通訊傳送至目標對象。  [瞭解如何使用API觸發行銷活動](api-triggered-campaigns.md)

1. **[!UICONTROL API觸發 — 異動]** — 與API觸發的行銷活動相同，這些行銷活動是使用API呼叫執行。 API觸發的交易式行銷活動旨在傳送&#x200B;**交易式**&#x200B;訊息，也就是在個人執行動作後傳送的訊息：密碼重設要求、購物車購買等。  [瞭解如何使用API觸發行銷活動](api-triggered-campaigns.md)

   ![](assets/create-campaign-modal.png)

## 定義行銷活動屬性 {#create}

行銷活動建立後，您必須定義其屬性。 請遵循以下步驟：

1. 在&#x200B;**[!UICONTROL 屬性]**&#x200B;區段中，輸入行銷活動的名稱和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../content-management/content-experiment.md).-->

1. （選用）使用&#x200B;**標籤**&#x200B;欄位將Adobe Experience Platform統一標籤指派給您的行銷活動。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [瞭解如何使用標籤](../start/search-filter-categorize.md#tags)。

1. （選用）您可以根據存取標籤來限制此行銷活動的存取權。 若要新增存取限制，請瀏覽至此頁面最上方的「**[!UICONTROL 管理存取]**」按鈕。請確定只選取您具有許可權的標籤。 [進一步瞭解物件層級存取控制](../administration/object-based-access.md)。

## 定義行銷活動對象 {#audience}

現在您可以選取行銷活動的閱聽眾。 受眾是指一組具有類似行為和/或特徵的人。

>[!IMPORTANT]
>
>* [對象構成](../audience/get-started-audience-orchestration.md)的對象和屬性目前無法用於Healthcare Shield或Privacy and Security Shield。
>
>* 針對API觸發的行銷活動，必須透過API呼叫設定對象。

若要定義排程行銷活動定位的母體，請遵循下列步驟：

1. 在&#x200B;**對象**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 選取對象]**&#x200B;按鈕以顯示可用Adobe Experience Platform對象清單。 在[本節](../audience/about-audiences.md)中進一步瞭解對象。

1. 在&#x200B;**[!UICONTROL 身分型別]**&#x200B;欄位中，選擇用來識別所選對象中個人的金鑰型別。 您可以使用現有的身分型別，或使用Adobe Experience Platform Identity Service建立新的身分型別。 標準身分名稱空間列於[此頁面](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}。

   每個行銷活動只允許一個身分型別。 如果屬於區段的個人在不同身分中沒有選取的身分型別，則無法將該行銷活動設為目標。

   ![](assets/create-campaign-namespace.png)

   在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解身分型別和名稱空間。

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->


## 選取頻道 {#channel}

您現在可以選取通道及其設定。 請遵循以下步驟：

1. 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，選取通訊通道。

   可用管道的清單取決於您的授權模式及附加元件。 針對API觸發的行銷活動，只有電子郵件、簡訊和推播通知通道可用。

1. 選取通道設定。

   設定是由[系統管理員](../start/path/administrator.md)所定義。 它包含所有用於傳送訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   下拉式清單中只會列出與行銷活動型別相容的管道設定。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果您正在建立推播通知行銷活動，可以啟用&#x200B;**[!UICONTROL 快速傳送模式]**，這是Journey Optimizer的附加元件，允許以大量快速推播訊息傳送。 [了解更多](../push/create-push.md#rapid-delivery)

## 編輯內容 {#content}

您現在可以從&#x200B;**[!UICONTROL 編輯內容]**&#x200B;按鈕定義訊息的內容。 內容建立程式取決於您選取的管道。

在以下頁面瞭解建立訊息內容的詳細步驟：


<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="電子郵件" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>電子郵件</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="簡訊" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>簡訊</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="推播" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>推播通知</strong></a></div></td>
<td><a href="../direct-mail/create-direct-mail.md"><img alt="直接郵件" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
<div align="center"><a href="../direct-mail/create-direct-mail.md"><strong>直接郵件</strong></a></div></td>
</tr></table>

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../in-app/create-in-app.md"><img alt="應用程式內" src="../channels/assets/do-not-localize/inapp.jpg"></a>
<div align="center"><a href="../in-app/create-in-app.md"><strong>應用程式內</strong></a></div></td>
<td><a href="../web/create-web.md"><img alt="網頁" src="../channels/assets/do-not-localize/web.jpg"></a>
<div align="center"><a href="../web/create-web.md"><strong>網頁</strong></a></div></td>
<td><a href="../code-based/create-code-based.md"><img alt="程式碼型體驗" src="../channels/assets/do-not-localize/code.png"></a>
<div align="center"><a href="../code-based/create-code-based.md"><strong>程式碼型體驗</strong></a></div></td>
<td><a href="../content-card/create-content-card.md"><img alt="內容卡片" src="../channels/assets/do-not-localize/cards.png"></a>
<div align="center"><a href="../content-card/create-content-card.md"><strong>內容卡</strong></a></div></td>
</tr></table>

定義內容後，請使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;按鈕，以測試設定檔或從CSV / JSON檔案上傳的範例輸入資料來預覽和測試您的內容，或手動新增。 [進一步瞭解](../content-management/preview-test.md)。若要瀏覽回到行銷活動建立畫面，請按一下向左箭頭。

![](assets/create-campaign-design.png)

除了訊息內容本身之外，您還可以進行下列設定：

1. （選擇性）在&#x200B;**[!UICONTROL 內容實驗]**&#x200B;區段中，您可以使用&#x200B;**[!UICONTROL 建立實驗]**&#x200B;按鈕來測試哪些內容效果更好。 在[本節](../content-management/content-experiment.md)中詳細說明內容實驗功能。

1. 在&#x200B;**[!UICONTROL 動作追蹤]**&#x200B;區段中，指定是否要追蹤收件者對傳遞的反應：您可以追蹤點按和/或開啟。

   執行行銷活動後，即可從行銷活動報表存取追蹤結果。 [進一步瞭解行銷活動報告](../reports/campaign-global-report-cja.md)

## 排程行銷活動 {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="行銷活動排程"
>abstract="預設情況下，行銷活動經由手動啟用後開始執行，並在訊息傳送一次後立即結束。您可以彈性設定發送訊息的具體日期和時間。此外，你可以對定期執行或 API 觸發的行銷活動指定結束日期。在操作觸發條件中，你亦可根據自己的偏好設定訊息傳送頻率。"

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

根據預設，排程的行銷活動在手動啟動後開始，並在傳送一次訊息後立即結束。

如果您不想在行銷活動啟動後立即執行，可以使用&#x200B;**[!UICONTROL 行銷活動開始]**&#x200B;選項指定傳送訊息的日期和時間。 **[!UICONTROL 行銷活動end]**&#x200B;選項可讓您指定行銷活動何時應停止執行。

![](assets/create-campaign-schedule.png)

對於電子郵件、簡訊和推播通知行銷活動，您可以定義行銷活動訊息的傳送頻率。 若要這麼做，請使用行銷活動建立畫面中的&#x200B;**[!UICONTROL 動作觸發器]**&#x200B;選項，指定行銷活動應該每日、每週或每月執行。

>[!NOTE]
>
>在[!DNL Adobe Journey Optimizer]中排程行銷活動時，請確定您的開始日期/時間與所要的首次傳遞一致。 對於循環行銷活動，如果初始排程時間已過，行銷活動將根據其循環規則滾動至下一個可用時段。

## 其他設定 {#settings}

某些設定專用於為行銷活動選取的通訊頻道，或用於特定使用案例。 其詳情如下。

* 對於電子郵件，您可以建立特定的IP熱身計畫啟用行銷活動。 請參閱[此章節](../configuration/ip-warmup-campaign.md)深入瞭解。
* 對於網頁、應用程式內和程式碼型頻道，您可以為行銷活動指派優先順序分數。 請參閱[此章節](../conflict-prioritization/priority-scores.md)深入瞭解。
* 對於內容卡行銷活動，您可以啟用其他傳送規則，以選擇觸發訊息的事件和條件。 請參閱[此章節](../content-card/create-content-card.md)深入瞭解。
* 針對應用程式內訊息，您可以使用&#x200B;**[!UICONTROL 編輯觸發器]**&#x200B;按鈕，選擇觸發訊息的事件和條件。 請參閱[此章節](../in-app/create-in-app.md)深入瞭解。

## 後續步驟 {#next}

行銷活動設定和內容準備就緒後，您就可以檢閱並啟用它。 [了解更多](review-activate-campaign.md)
