---
title: 建立模擬
description: 瞭解如何建立模擬
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

---

# 建立模擬

## 關於模擬

要驗證您的決策邏輯，您可以模擬將哪些優惠交付給給定位置的test配置檔案。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

這使您能夠test和改進您提供的各種版本，而不會影響目標收件人。

>[!NOTE]
>
>此功能將單個請求模擬到 [!DNL Decisions] API。 瞭解更多 [使用決策API提供服務](../api-reference/decisions-api/deliver-offers.md)。

要訪問此功能，請選擇 **[!UICONTROL Simulation]** 的 **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** 的子菜單。

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## 選擇test配置檔案

首先，您需要選擇要用於模擬的test配置檔案。

1. 按一下「**[!UICONTROL Manage profile]**」。

   ![](../../assets/offers_simulation-manage-profile.png)

1. 選擇要用於標識test配置檔案的標識命名空間。 在此示例中，我們將使用 **電子郵件** 命名空間。

   >[!NOTE]
   >
   >標識命名空間定義標識符的上下文，如電子郵件地址或CRM ID。 瞭解有關Adobe Experience Platform標識命名空間的詳細資訊 [此部分](../../get-started-identity.md){target=&quot;_blank&quot;}。

1. 輸入標識值，然後按一下 **[!UICONTROL View]** 清單可用的配置檔案。

   ![](../../assets/offers_simulation-add-profile.png)

1. 如果要test不同的配置檔案資料，則添加其他配置檔案，並保存您的選擇。

   ![](../../assets/offers_simulation-save-profiles.png)

1. 添加後，所有配置檔案都將列在下面的下拉清單中 **[!UICONTROL Test profile]**。 可以在保存的test配置檔案之間切換以顯示每個選定配置檔案的結果。

   ![](../../assets/offers_simulation-saved-profiles.png)

1. 您可以按一下 **[!UICONTROL Profile details]** 連結以顯示所選配置檔案資料。

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## 添加決策作用域

現在，選擇要在您的test配置檔案上模擬的優惠決定。

1. 選擇「**[!UICONTROL Add decision scope]**」。

   ![](../../assets/offers_simulation-add-decision.png)

1. 從清單中選取一個放置。

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. 將顯示可用決策。

   * 您可以使用搜索欄位來細化選擇。
   * 您可以按一下 **[!UICONTROL Open offer decisions]** 連結以開啟您建立的所有決策的清單。 瞭解更多 [決策](create-offer-activities.md)。

   選擇您選擇的決定，然後按一下 **[!UICONTROL Add]**。

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. 您剛定義的決策範圍將顯示在主工作區中。

   您可以調整要請求的優惠數量。 例如，如果選擇2，則此決策範圍將顯示最佳的2個優惠。

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以要求30個優惠。

1. 重複上述步驟，以根據需要添加任意多個決策。

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使定義了多個決策範圍，也只模擬一個API請求。
   >
   >預設情況下，所有重複資料消除標誌都啟用模擬，這意味著決策引擎允許重複項，因此可以在多個決策/放置中做出相同的主張。 瞭解 [!DNL Decisions] API請求屬性 [此部分](../api-reference/decisions-api/deliver-offers.md)。<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## 查看模擬結果 {#simulation-results}

添加決策範圍並選擇test配置檔案後，可以查看結果。

1. 按一下「**[!UICONTROL View results]**」。

   ![](../../assets/offers_simulation-view-results.png)

1. 根據每個決策的所選簡檔顯示最佳可用報價。

   選擇要顯示其詳細資訊的優惠。

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. 從清單中選擇另一個配置檔案，以顯示不同test配置檔案的聘用決定結果。

1. 您可以根據需要添加、刪除或更新決策範圍多次。

>[!NOTE]
>
>每次更改配置檔案或更新決策範圍時，都需要使用 **[!UICONTROL View results]** 按鈕

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

