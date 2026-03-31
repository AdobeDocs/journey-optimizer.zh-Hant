---
solution: Journey Optimizer
product: journey optimizer
title: 使用訊號觸發協調的行銷活動
description: 瞭解如何使用 [!DNL Adobe Journey Optimizer]中的訊號觸發協調的行銷活動。
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
source-git-commit: ec52b62c2d0626b9047eebb54e0a44fee096ec05
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 0%

---

# 使用訊號觸發協調的行銷活動 {#trigger-signal}

您可以傳送訊號來觸發協調的行銷活動，而非依排程執行。 訊號會透過來自外部系統或應用程式的API呼叫傳送。 使用訊號時，您可以傳遞引數。 接著，這些變數便可在協調的行銷活動中作為執行內容中的事件變數使用，以用於目標定位、條件或運算式。

使用訊號觸發協調行銷活動的端對端程式：

1. [排程要由訊號觸發的行銷活動](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [新增訊號承載的引數](#add-parameters-for-the-signal-payload-optional-parameters) （選擇性）
1. [建置及測試行銷活動](#build-and-test-the-campaign-build-and-test)
1. [發佈並觸發行銷活動](#publish-and-trigger-the-campaign-publish)

>[!NOTE]
>
>若要使用訊號觸發協調的行銷活動，您需要&#x200B;**[!DNL Publish orchestrated campaigns]**&#x200B;許可權(`orchestrated-campaign.publish`)。 請參閱[內建許可權](../administration/ootb-permissions.md)。

## 排程要由訊號觸發的行銷活動 {#configure-signal}

若要將協調的行銷活動設為從訊號而非排程開始，請遵循下列步驟：

1. 使用訊號開啟您要觸發的「協調流程」行銷活動。

1. 開啟排程設定。 [瞭解如何排程協調的行銷活動](create-orchestrated-campaign.md#schedule)。

1. 選取&#x200B;**[!UICONTROL 由訊號觸發]**，讓行銷活動等待訊號而不是依排程執行。

   ![排程功能表，已選取由訊號選項觸發](assets/triggered-oc-scheduler.png){zoomable="yes"}

## 新增訊號承載的引數（選擇性） {#parameters}

您可以在觸發訊號中傳遞引數，並在執行內容中的行銷活動中使用這些引數，例如，在鎖定目標、條件或運算式中。 先定義排程設定中的每個引數，然後在您呼叫觸發程式API時傳遞其值。

1. 開啟行銷活動排程器，並選取&#x200B;**[!UICONTROL 新增引數]**。

1. 定義要在訊號裝載中傳送的每個引數名稱和資料型別。 您也可以提供&#x200B;**測試值**，當您在測試模式中觸發行銷活動時，將會使用這些值。 [瞭解如何測試觸發的行銷活動](#build-and-test)。

   ![新增引數以定義訊號的裝載引數](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>如果您在API呼叫中傳遞未在排程器中定義的引數，API呼叫仍會成功，且引數會傳播，而您可以在運算式中使用它。 不過，協調的行銷活動介面將無法協助您使用它，例如，「測試」活動不會列出或顯示排程器中未定義的引數。

## 建置及測試行銷活動 {#build-and-test}

在畫布上建立您的行銷活動，然後在您發佈之前，選擇透過API觸發訊號，在草稿中測試。

1. 在畫布上新增並連結活動（對象、目標定位、傳送）。 [了解如何協調行銷活動](orchestrate-activities.md)

1. 如果您已在訊號中定義引數，則可以將它們匯入畫布邏輯（例如，在條件或目標定位中）。 在此範例中，&quot;channel&quot;引數是當作&#x200B;**[!UICONTROL 測試]**&#x200B;活動中的條件。

   ![在測試活動中作為條件使用的管道引數](assets/triggered-oc-use-parameters.png)

   若要在運算式編輯器中使用訊號引數（例如，在&#x200B;**[!UICONTROL 建立對象]**&#x200B;活動中建立查詢），請在運算式欄位中輸入`$(vars/@<parameterName>)`。 以排程器中定義的引數名稱取代`<parameterName>`，例如`$(vars/@channel)`。 [瞭解如何使用運算式編輯器](edit-expressions.md)。

1. 開啟行銷活動排程器，選取「**[!UICONTROL 複製API請求]**」並選擇格式（cURL或HTTP請求）。

   複製的資訊包括協調的行銷活動ID、沙箱名稱、組織ID以及引數的測試值（如果您已新增某些值）。

   ![在排程組態中複製API要求選項](assets/triggered-oc-copy.png)

   +++包含引數和測試值的範例cURL請求

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. 按一下&#x200B;**[!UICONTROL 開始]**&#x200B;以開始行銷活動。

1. 使用您從排程器複製的範例要求傳送觸發API呼叫。<!--For the complete API reference, refer to the [Journey Optimizer API documentation](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.-->

對測試結果感到滿意時，[發佈行銷活動](#publish)。

## 發佈並觸發行銷活動 {#publish}

在您[建置並測試行銷活動](#build-and-test)之後，請發佈行銷活動，以便從您的應用程式觸發。

1. 在行銷活動畫布中按一下&#x200B;**[!UICONTROL 發佈]**。 必須先發佈行銷活動，才能從外部系統觸發。 [進一步瞭解如何啟動及監視行銷活動](start-monitor-campaigns.md#publish)。

1. 開啟行銷活動排程器，選取「**[!UICONTROL 複製API請求]**」並選擇格式（cURL或HTTP請求）。

   複製的資訊包括協調的行銷活動ID、沙箱名稱、組織ID以及引數（如果您已新增一些的話）。

   ![在排程設定中複製API請求](assets/triggered-oc-copy.png)

1. 從您的系統呼叫觸發程式API。

   >[!IMPORTANT]
   >
   >對於即時協調的行銷活動，節流護欄會強制兩個API觸發執行之間的最小間隔為&#x200B;**一小時**。 如果您在該間隔經過之前再次呼叫API，API會傳回&#x200B;**HTTP 429**&#x200B;錯誤（請求過多）。 當您觸發草稿版本以進行測試時，不會套用此護欄。

   如果您將引數新增至訊號裝載，則行銷活動執行時，您在API呼叫中傳遞的值會顯示為行銷活動事件變數。 若要進行檢查，請從行銷活動畫布工具列開啟行銷活動記錄。 在&#x200B;**[!UICONTROL 工作]**&#x200B;標籤中，識別與訊號對應的工作，然後按一下鉛筆圖示以存取相關的事件變數。 [瞭解如何存取記錄檔和工作](start-monitor-campaigns.md#logs-tasks)。

   ![有可用的行銷活動事件變數的記錄檔與工作畫面](assets/trigger-events-variables.png){zoomable="yes"}
