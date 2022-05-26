---
title: 與 Adobe Campaign Standard 整合
description: 瞭解如何與Adobe Campaign Standard整合
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: d1902ac35d78ba73051b41b4fc82dc284382d1a4
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 5%

---

# 與 Adobe Campaign Standard 整合 {#using_adobe_campaign_standard}

您可以使用Adobe Campaign Standard的事務性消息傳遞功能發送電子郵件、推送通知和SMS。

如果您有Adobe Campaign Standard，可使用內置操作來連接到Adobe Campaign Standard。

必須發佈Campaign Standard事務性消息及其關聯事件，以便在Journey Optimizer使用。 如果事件已發佈但消息未發佈，則在Journey Optimizer介面中將不可見。 如果發佈消息，但其關聯事件未發佈，則該消息在Journey Optimizer介面中可見，但不可用。

## 重要備註 {#important-notes}

* 自動為Adobe Campaign Standard操作定義每5分鐘4000次呼叫的上限規則。 這與Adobe Campaign Standard事務性資訊的正式規模相符。 閱讀有關中事務性消息傳遞SLA的詳細資訊 [Adobe Campaign Standard產品說明](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html)。

* Adobe Campaign Standard一體化是通過行動清單中的專門內置行動建立的。 需要為每個沙箱配置此項。

* 您不能將Campaign Standard活動與段資格或讀取段活動一起使用。

* 行程不能同時使用消息和Campaign Standard操作。

## 配置操作 {#configure-action}

以下是配置它的步驟：

1. 選擇 **[!UICONTROL Configurations]** 的子菜單。 在  **[!UICONTROL Actions]** ，按一下 **[!UICONTROL Manage]**。 畫面隨即顯示動作清單。

1. 選擇內置 **[!UICONTROL AdobeCampaignStandard]** 操作。 操作配置窗格在螢幕右側開啟。

   ![](assets/actioncampaign.png)

1. 複製您的Adobe Campaign Standard實例URL並將其貼上到 **[!UICONTROL URL]** 的子菜單。

1. 按一下 **[!UICONTROL Test the instance URL]** test案件的效力。

   >[!NOTE]
   >
   >此test驗證：
   >
   >主機為&quot;。campaign.adobe.com&quot;、&quot;。campaign-sandbox.adobe.com&quot;、&quot;。campaign-demo.adobe.com&quot;、&quot;。ats.adobe.com&quot;或&quot;。adls.adobe.com&quot;。
   >
   >URL以https開頭，
   >
   >與此Adobe Campaign Standard實例關聯的ORG與Journey Optimizer的ORG相同。

在設計行程時，在 **[!UICONTROL Action]** 類別： **[!UICONTROL Email]**。 **[!UICONTROL Push]**。 **[!UICONTROL SMS]** （請參見） [使用Adobe Campaign操作](../building-journeys/using-adobe-campaign-standard.md))。

![](assets/journey58.png)

您可以使用 **反應** 事件，以對與同一行程內發送的Campaign Standard消息相關的跟蹤資料做出響應。 對於推送通知，您可以對按一下的、發送的或失敗的消息做出響應。 對於SMS消息，您可以對已發送或失敗的消息做出響應。 對於電子郵件，您可以對按一下的、發送的、開啟的或失敗的郵件做出反應。 請參閱 [反應事件](../building-journeys/reaction-events.md)。

如果您使用第三方系統發送消息，則需要添加和配置自定義操作。 請參閱 [關於自定義操作配置](../action/about-custom-action-configuration.md)。
