---
solution: Journey Optimizer
product: journey optimizer
title: 建立行銷活動
description: 瞭解如何在Journey Optimizer建立活動
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 建立，優化程式，市場活動，曲面，消息
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 23%

---

# 建立行銷活動 {#create-campaign}

>[!NOTE]
>
>在建立新市場活動之前，請確保您有一個表面通道（即消息預設）和一個Adobe Experience Platform段可供使用。 在以下各節中瞭解更多資訊：
>
>* [建立頻道介面](../configuration/channel-surfaces.md)
>* [開始使用區段](../segment/about-segments.md)


要建立新市場活動，請訪問 **[!UICONTROL 市場活動]** 菜單，然後按一下 **[!UICONTROL 建立市場活動]**。 您還可以複製現有的即時市場活動，以建立新市場活動。 [了解更多](modify-stop-campaign.md#duplicate)

## 選擇市場活動類型和渠道 {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="對於指定傳送日期的行銷訊息，**排程**&#x200B;類型最合適。但是，如果您想傳送密碼重設或購物車未結帳等異動訊息，**API 觸發**&#x200B;類型則是最佳選擇。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="行銷活動類別"
>abstract="類別值會直接關聯到活動類型值。**行銷**&#x200B;類別的排程行銷活動類型和&#x200B;**異動**&#x200B;類別的 API 觸發類型"

1. 在 **[!UICONTROL 屬性]** 部分，指定希望如何執行市場活動。 有兩種類型的活動：

   * **[!UICONTROL 計畫]**:立即或在指定日期執行市場活動。 計畫的市場活動旨在發送 **營銷** 鍵入消息。

   * **[!UICONTROL API觸發]**:使用API調用執行市場活動。 API觸發的市場活動旨在發送 **事務** 消息，即在個人執行的操作後發送的消息：密碼重置、購物車放棄等。 [瞭解如何使用API觸發市場活動](api-triggered-campaigns.md)

1. 在 **[!UICONTROL 操作]** 的子菜單。

   介面是由[系統管理員](../start/path/administrator.md)定義的設定。 它包含所有用於春頌訊息的技術參數，如標頭參數、子網域、行動應用程式等等。[了解更多](../configuration/channel-surfaces.md)。

   下拉清單中只列出與市場營銷活動類型相容的渠道曲面。

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >如果要建立推式通知市場活動，則可以啟用 **[!UICONTROL 快速遞送模式]**，這是一個Journey Optimizer附加模組，它允許在大卷中快速發送推送消息。 [了解更多](../push/create-push.md#rapid-delivery)

1. 按一下 **[!UICONTROL 建立]** 建立市場活動。

## 定義市場活動屬性 {#create}

1. 在 **[!UICONTROL 屬性]** 部分，指定市場活動的名稱和說明。

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. 的 **標籤** 欄位允許您將「Adobe Experience Platform統一標籤」分配給市場活動。 這可讓您輕鬆分類，並改進行銷活動清單的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

1. 要將自定義或核心資料使用標籤分配給市場活動，請按一下 **[!UICONTROL 管理訪問]** 按鈕 [瞭解有關對象級訪問控制(OLA)的詳細資訊](../administration/object-based-access.md)

## 建立消息並配置跟蹤 {#content}

在 **[!UICONTROL 操作]** 的子菜單。

1. 按一下 **[!UICONTROL 編輯內容]** 按鈕，然後建立和設計消息內容。

   瞭解在以下頁面中建立消息內容的詳細步驟：

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
    <a href="../push/create-push.md"><strong>建立推式通知</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="驗證" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>建立SMS消息</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. 定義內容後，使用 **[!UICONTROL 模擬內容]** 按鈕，使用test配置檔案預覽和test內容。 [了解更多](../email/preview.md)。

1. 按一下箭頭返回市場活動建立螢幕。

   ![](assets/create-campaign-design.png)

1. 在 **[!UICONTROL 動作跟蹤]** 部分，指定是否跟蹤收件人對交貨的反應：您可以跟蹤點擊和/或開啟。

   市場活動一旦執行，便可以從市場活動報告訪問跟蹤結果。 [瞭解有關市場活動報告的更多資訊](../reports/campaign-global-report.md)

## 定義對象 {#audience}

按一下 **[!UICONTROL 選擇受眾]** 按鈕來顯示可用的Adobe Experience Platform段清單。 [瞭解有關網段的更多資訊](../segment/about-segments.md)

>[!NOTE]
>
>對於API觸發的市場活動，需要通過API調用來設定受眾。 [了解更多](api-triggered-campaigns.md)

在 **[!UICONTROL 標識命名空間]** 欄位中，選擇要用於標識選定段中的個體的命名空間。 [瞭解有關命名空間的詳細資訊](../event/about-creating.md#select-the-namespace)

![](assets/create-campaign-namespace.png)

    >[！注釋]
    >
    >市場活動不會針對屬於在其不同標識中沒有選定標識（命名空間）的段的個人。

<!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## 計畫市場活動 {#schedule}

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
>title="行銷活動動作觸發器"
>abstract="定義應傳送行銷活動訊息的頻率。"

預設情況下，市場活動在手動激活後開始，並在消息發送一次後立即結束。

您可以定義市場活動消息的發送頻率。 要執行此操作，請使用 **[!UICONTROL 操作觸發器]** 選項，指定是否應每日、每週或每月執行市場活動。

如果您不想在市場活動激活後立即執行市場活動，則可以指定消息應使用的發送日期和時間 **[!UICONTROL 市場活動開始]** 的雙曲餘切值。 的 **[!UICONTROL 市場活動結束]** 選項，您可以指定週期性市場活動停止執行的時間。

![](assets/create-campaign-schedule.png)

一旦您的市場活動準備就緒，您就可以查看並發佈它。 [了解更多](review-activate-campaign.md)
