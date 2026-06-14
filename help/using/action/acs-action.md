---
solution: Journey Optimizer
product: journey optimizer
title: 與 Adobe Campaign Standard 整合
description: 瞭解如何將Journey Optimizer與Adobe Campaign Standard整合
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: 行銷活動，標準，整合，上限，動作
exl-id: 2f0218c9-e1b1-44ba-be51-15824b9fc6d2
TQID: https://experienceleague.adobe.com/1JQFfviWGc3OXYN0YdAh0Koaboro2wJU8HpEf75PoKQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 62bc5f833b5612570ba50c98519a2f9c07d0bd5e
workflow-type: tm+mt
source-wordcount: 475
ht-degree: 5%

---

# 與 Adobe Campaign Standard 整合 {#using_adobe_campaign_standard}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;將Journey Optimizer連線至Adobe Campaign Standard，讓您的歷程可以透過其異動訊息功能傳送電子郵件、推播通知及簡訊。

>[!ENDSHADEBOX]

如果您有Adobe Campaign Standard，則可使用內建動作來允許連線至Adobe Campaign Standard。 您可以使用Adobe Campaign Standard的「交易訊息」功能來傳送電子郵件、推播通知和簡訊。

必須發佈Campaign Standard交易式訊息及其相關事件，才能在Journey Optimizer中使用。 如果事件已發佈，但訊息尚未發佈，將無法在Journey Optimizer介面中看見。 如果訊息已發佈，但其關聯事件尚未發佈，則會顯示在Journey Optimizer介面中，但將無法使用。

## 護欄與限制 {#important-notes}

* 系統會自動為Adobe Campaign Standard動作定義每5分鐘4,000次呼叫的上限規則。 在[Adobe Campaign Standard產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/campaign-standard.html){target="_blank"}中進一步瞭解異動訊息SLA。

* Adobe Campaign Standard整合是透過動作清單中的專屬內建動作來設定。 必須針對每個沙箱進行此設定。

* Campaign Standard動作無法與對象資格或讀取對象活動搭配使用。

* 歷程不能同時使用[內建頻道動作](../building-journeys/journey-action.md)和[Campaign Standard動作](../building-journeys/using-adobe-campaign-standard.md)。

## 設定動作 {#configure-action}

在Journey Optimizer中，您必須為每個異動訊息設定一個動作。

若要設定Campaign Standard動作，請遵循下列步驟：

1. 在[管理]功能表區段中選取&#x200B;**[!UICONTROL 組態]**。

1. 在&#x200B;**[!UICONTROL 動作]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL 管理]**。 畫面隨即顯示動作清單。

1. 選取內建&#x200B;**[!UICONTROL AdobeCampaignStandard]**&#x200B;動作。 動作設定窗格會在畫面右側開啟。

   ![](assets/actioncampaign.png)

1. 複製您的Adobe Campaign Standard執行個體URL，並將其貼到&#x200B;**[!UICONTROL URL]**&#x200B;欄位中。

1. 按一下&#x200B;**[!UICONTROL 測試執行個體URL]**&#x200B;以測試執行個體的有效性。

   >[!NOTE]
   >
   >此測試會驗證：
   >
   >* 主機為「.campaign.adobe.com」、「.campaign-sandbox.adobe.com」、「.campaign-demo.adobe.com」、「.ats.adobe.com」或「.adls.adobe.com」
   >
   >* URL以https開頭
   >
   >* 與此Adobe Campaign Standard例項相關聯的組織與Journey Optimizer組織相同

完成此設定後，在設計歷程時，**[!UICONTROL 動作]**&#x200B;類別中有三個動作可用： **[!UICONTROL 電子郵件]**、**[!UICONTROL 推播]**、**[!UICONTROL 簡訊]**。 [瞭解如何使用它們](../building-journeys/using-adobe-campaign-standard.md)。

![](assets/journey58.png)

使用&#x200B;**回應**&#x200B;事件來回應與相同歷程中傳送之Campaign Standard訊息相關的追蹤資料：

* 對於推播通知，歷程可對點選、傳送或失敗的訊息做出反應。

* 對於SMS訊息，歷程可對已傳送或失敗的訊息做出反應。

* 對於電子郵件，歷程可對點按、傳送、開啟或失敗的訊息做出反應。 [進一步瞭解回應事件](../building-journeys/reaction-events.md)。

使用協力廠商系統傳送訊息時，您必須新增並設定自訂動作。 [進一步瞭解自訂動作組態](../action/about-custom-action-configuration.md)。