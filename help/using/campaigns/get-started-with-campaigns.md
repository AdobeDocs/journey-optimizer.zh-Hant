---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用行銷活動
description: 深入了解 Journey Optimizer 的行銷活動
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 行銷活動、如何進行、開始、最佳化程式
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 71%

---

# 開始使用行銷活動 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="行銷活動排程"
>abstract="預設情況下，行銷活動經由手動啟用後開始執行，並在訊息傳送一次後立即結束。您可以彈性設定發送訊息的具體日期和時間。此外，您可以對定期執行的動作行銷活動指定結束日期。在操作觸發條件中，你亦可根據自己的偏好設定訊息傳送頻率。"

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

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="節流率控制"
>abstract="節流率控制"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="建立行銷活動"
>abstract="使用 **Adobe Journey Optimizer**，透過各種管道將一次性內容傳遞至特定對象。當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。"

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="行銷活動"
>abstract="建立行銷活動以跨不同管道向特定客群提供一次性內容。建立行銷活動之前，請確保您準備好可供使用的管道設定與 Adobe Experience Platform 客群。"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="行銷活動類型"
>abstract="**排程的行銷活動**&#x200B;會立即執行或在指定的日期執行，其目的在傳送行銷類型訊息。**API 觸發的**&#x200B;行銷活動是使用 API 呼叫執行的。這些目的是傳送行銷訊息 (需要使用者同意的促銷訊息) 或交易型訊息 (非商業訊息，也可以在特定情況下傳送到取消訂閱的輪廓)。"

使用 Journey Optimizer 行銷活動，透過各種頻道將一次性內容傳遞至特定客群。 當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。

![](assets/gs-campaigns.png)

您可以在Journey Optimizer中建立不同型別的行銷活動：

* **動作行銷活動**

  行動行銷活動（或排程行銷活動）允許對行銷使用案例進行簡單的臨時批次通訊，例如促銷優惠、參與行銷活動、公告、法律通知或原則更新。

* **API觸發的行銷活動**

  API觸發的行銷活動可讓行銷通訊在適當的時間聯絡對象，或讓交易/營運訊息聯絡個人（例如密碼重設），其需求可能涉及個人化，不僅使用設定檔屬性，還會在觸發程式（即REST API裝載）中使用即時內容資料。

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, Orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## 開始之前 {#campaign-prerequisites}

在[!DNL Journey Optimizer]中開始建立第一個行銷活動之前，請先檢查下列必要條件：

1. **您需要適當的權限**。行銷活動僅適用於具有行銷活動相關&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;存取權的使用者，例如行銷活動管理員、行銷活動核准者、行銷活動管理員及/或行銷活動檢視者。 如果您無法存取行銷活動，則必須擴充您的許可權。

   +++了解如何指派行銷活動相關角色

   1. 若要將角色指派給 [!DNL Permissions] 產品中的使用者，請導覽至&#x200B;**[!UICONTROL 角色]**&#x200B;標籤，然後選擇與行銷活動相關的內建角色之一&#x200B;**[!UICONTROL 角色]**：Campaign 管理員、Campaign 核准者、Campaign 經理或行銷活動檢視者。

   1. 在&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤中，按一下&#x200B;**[!UICONTROL 新增使用者]**。

   1. 輸入您的使用者名稱或電子郵件地址，或從清單中選擇使用者，然後按一下&#x200B;**[!UICONTROL 儲存]**。

      如果之前未建立使用者，請參閱[新增使用者文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/ui/users)。

   接著，使用者應會收到一封電子郵件，並重新導向至您的執行個體。

   +++

1. **您需要客群**。建立行銷活動之前必須有可用的客群。 [開始使用對象](../audience/about-audiences.md)。

1. **需要管道設定**。若要選取管道，您必須建立相對應的管道設定 (即預設)，使其可供使用。[了解如何設定頻道設定](../configuration/channel-surfaces.md)。

## 讓我們深入探討

現在您已瞭解[!DNL Journey Optimizer]中的行銷活動，是時候深入探討這些檔案區段，以開始建立您的第一個行銷活動了。

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="動作行銷活動" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">動作行銷活動</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="簡訊" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">API 觸發的行銷活動</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
