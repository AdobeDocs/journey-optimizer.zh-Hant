---
solution: Journey Optimizer
product: journey optimizer
title: 與 Adobe Campaign Standard 整合
description: 了解如何整合Journey Optimizer與Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin,Developer
level: Intermediate
keywords: campaign, standard，整合， capping，限定，action
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 與 Adobe Campaign Standard 整合 {#using_adobe_campaign_standard}

您可以使用Adobe Campaign Standard的「交易訊息」功能來傳送電子郵件、推播通知和簡訊。

如果您有Adobe Campaign Standard，則可使用內建動作來允許連線至Adobe Campaign Standard。

必須發佈Campaign Standard交易式訊息及其相關事件，才能在Journey Optimizer中使用。 如果已發佈事件但未顯示訊息，則訊息將不會顯示在Journey Optimizer介面中。 如果訊息已發佈，但其相關事件未發佈，則會顯示在Journey Optimizer介面中，但無法使用。

## 重要備註 {#important-notes}

* 系統會自動為Adobe Campaign Standard動作定義每5分鐘4000次呼叫的上限規則。 這對應於Adobe Campaign Standard交易訊息的官方規模。 閱讀更多有關交易式訊息SLA的資訊，請參閱 [Adobe Campaign Standard產品說明](https://helpx.adobe.com/legal/product-descriptions/campaign-standard.html).

* Adobe Campaign Standard整合是透過動作清單中的專用內建動作來設定。 這必須針對每個沙箱進行設定。

* 您無法搭配「區段」資格或「讀取」區段活動使用Campaign Standard動作。

* 歷程無法同時使用訊息和Campaign Standard動作。

## 設定動作 {#configure-action}

以下是設定此變數的步驟：

1. 選擇 **[!UICONTROL 配置]** （在「管理」菜單部分）。 在  **[!UICONTROL 動作]** ，按一下 **[!UICONTROL 管理]**. 畫面隨即顯示動作清單。

1. 選取內建 **[!UICONTROL AdobeCampaignStandard]** 動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/actioncampaign.png)

1. 複製您的Adobe Campaign Standard執行個體URL並貼到 **[!UICONTROL URL]** 欄位。

1. 按一下 **[!UICONTROL 測試執行個體URL]** 來測試例項的有效性。

   >[!NOTE]
   >
   >此測試驗證：
   >
   >主機為「.campaign.adobe.com」、「.campaign-sandbox.adobe.com」、「.campaign-demo.adobe.com」、「.ats.adobe.com」或「.adls.adobe.com」。
   >
   >URL的開頭為https,
   >
   >與此Adobe Campaign Standard例項相關聯的ORG與Journey Optimizer的ORG相同。

設計歷程時， **[!UICONTROL 動作]** 類別： **[!UICONTROL 電子郵件]**, **[!UICONTROL 推播]**, **[!UICONTROL 簡訊]** (請參閱 [使用Adobe Campaign動作](../building-journeys/using-adobe-campaign-standard.md))。

![](assets/journey58.png)

您可以使用 **反應** 事件，以回應在相同歷程中傳送之Campaign Standard訊息的相關追蹤資料。 若是推播通知，您可以對點按、傳送或失敗的訊息做出反應。 對於SMS訊息，您可以對已傳送或失敗的訊息做出反應。 若是電子郵件，您可以對點按、傳送、開啟或失敗的訊息做出反應。 請參閱 [反應事件](../building-journeys/reaction-events.md).

如果您使用協力廠商系統來傳送訊息，則需要新增及設定自訂動作。 請參閱 [關於自訂動作設定](../action/about-custom-action-configuration.md).
