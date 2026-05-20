---
solution: Journey Optimizer
product: journey optimizer
title: 設定 Sinch 提供者
description: 瞭解如何使用Sinch設定您的環境以使用Journey Optimizer傳送行動訊息
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
exl-id: 85412a85-edf0-4069-8bc7-b80371375f1f
TQID: https://experienceleague.adobe.com/24n9GhVTfQ9y4hlvY6g67dyL0FHqNOJW0aP-WIpzRqs
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: fdac7813-bd56-47ae-9f6d-fa94ad1c5dee
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: a4c92daab69394e6a736517f2e23a941135f7eb4
workflow-type: tm+mt
source-wordcount: 1007
ht-degree: 1%

---

# 設定 Sinch 提供者 {#sms-configuration-sinch}

搭配Journey Optimizer使用Sinch提供者時，您可以找到三個不同的選項：

* **SMS設定**：設定您的Sinch API認證，以順暢地傳送SMS訊息。

* **MMS設定**：對於多媒體訊息(MMS)，請設定您的Sinch MMS API認證。 請注意，追蹤和回應傳入訊息由SMS設定處理。 MMS設定僅適用於MMS訊息的傳出傳遞。

* **RCS設定**：設定您的Sinch API認證，以順暢地傳送RCS訊息。

若要設定Sinch提供者，請遵循下列步驟：

1. [建立API認證](#create-api)
1. [建立 Webhook](mobile-webhook.md)
1. [建立頻道設定](mobile-configuration-surface.md)
1. [透過簡訊頻道動作建立歷程或行銷活動](create-mobile-message.md)

## 設定簡訊的API認證{#create-api}

若要設定您的Sinch提供者使用Journey Optimizer傳送SMS訊息和MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的SMS API認證，如下所述：

   +++ 設定的SMS認證清單

   | 設定欄位 | 說明 |
   |---|---|
   | 簡訊供應商 | Sinch |
   | 名稱 | 選擇您的API認證名稱。 |
   | 服務ID和API權杖 | 存取API頁面，您可以在SMS標籤下找到您的認證。 在[Sinch檔案](https://developers.sinch.com/docs/sms/getting-started/){target="_blank"}中進一步瞭解。 |
   | 傳入號碼 | 新增您的唯一傳入號碼或短代碼。 這可讓您在不同的沙箱中使用相同的API認證，每個沙箱都有自己的傳入號碼或短程式碼。 |
   | 覆寫URL | 輸入您的自訂URL以取代SMS傳送報告、意見資料、傳入訊息或事件通知的預設端點。 Sinch會將所有相關更新傳送至此URL，而非預先定義的更新。 |

   +++

<!--
1. Choose how user consent should be tracked for messaging:

    * **[!UICONTROL Sender short code]**: Inbound keyword consent is keyed to your **sender short code** only. Use when one inbound number is enough to represent consent.

    * **[!UICONTROL Sender short code + profile number]**: Consent is keyed to the **sender short code** and the profile **mobile number**. Use when profiles can have several numbers, or when opt-in/out must apply per sender and recipient pair.
-->

1. 選取&#x200B;**[!UICONTROL 使用傳入的自訂資料集]**，將此認證的傳入SMS路由至您從下拉式清單中選擇的預先建立資料集。 [進一步瞭解如何使用傳入關鍵字的自訂資料集](../mobile/custom-dataset-inbound-keywords.md)

   >[!NOTE]
   >
   >資料集結構描述必須是&#x200B;**[!UICONTROL XDM ExperienceEvent]**，而且至少包含下列欄位群組：
   >* Adobe CJM ExperienceEvent — 訊息互動細節
   >* Adobe CJM ExperienceEvent — 訊息執行詳細資料
   >* Adobe CJM ExperienceEvent — 訊息設定檔詳細資料
   >
   >必須為設定檔啟用結構描述和資料集。


1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

1. 從您現有的API認證按一下&#x200B;**[!UICONTROL 驗證SMS連線]**，透過傳送範例訊息至指定裝置來測試及驗證SMS API認證。

1. 填寫&#x200B;**數字**&#x200B;和&#x200B;**訊息**&#x200B;欄位，然後按一下&#x200B;**[!UICONTROL 驗證連線]**。

   >[!IMPORTANT]
   >
   >訊息的結構必須符合提供者的裝載格式。

   ![](assets/verify-connection.png)

在建立及設定您的API認證後，您現在需要建立[您的Webhook](mobile-webhook.md)以及RCS訊息的通道設定。 [了解更多](mobile-configuration-surface.md)

## 設定MMS的API認證{#sinch-mms}

>[!IMPORTANT]
>
> 除了MMS設定，您還需要建立Sinch API認證，專門用於追蹤傳入訊息及管理同意請求。

若要設定Sinch MMS以使用Journey Optimizer傳送MMS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的MMS API認證，如下所述：

   * **[!UICONTROL SMS廠商]**： Sinch MMS。

   * **[!UICONTROL 名稱]**：輸入您的API認證名稱。

   * **[!UICONTROL 專案識別碼]**、**[!UICONTROL 應用程式識別碼]**&#x200B;和&#x200B;**[!UICONTROL API權杖]**：請依照下列步驟收集您的MMS API認證。

      * 針對&#x200B;**[!UICONTROL 專案識別碼]**&#x200B;和&#x200B;**[!UICONTROL 應用程式識別碼]**：存取您Sinch儀表板上Sinch專案的[交談API總覽](https://dashboard.sinch.com/convapi/overview)頁面。
      * 針對&#x200B;**[!UICONTROL API Token]**：取得您Sinch專案的[存取金鑰](https://community.sinch.com/t5/Customer-Dashboard/Sinch-Access-Keys/ta-p/12638)，並從您的Sinch專案&#x200B;**存取金鑰**&#x200B;中產生&#x200B;**Base64 API Token**。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

在建立及設定您的API認證後，您現在需要建立[您的Webhook](mobile-webhook.md)以及RCS訊息的通道設定。 [了解更多](mobile-configuration-surface.md)

## 設定RCS的API認證

<!--![](assets/do-not-localize/rcs-sms.png)-->

Journey Optimizer透過Sinch支援RCS (Rich Communication Services)傳送訊息，允許使用已驗證的企業設定檔連同商標元素（例如Logos和傳送者名稱）來傳送基本訊息。

原生RCS編寫需要Sinch RCS。 Twilio、Infobip和其他提供者必須使用[自訂提供者整合](mobile-configuration-custom.md)。

請注意，當設定檔的裝置不支援RCS或暫時無法透過RCS連線時，訊息會自動回復到簡訊。

若要使用Journey Optimizer設定Sinch RCS以傳送RCS，請遵循下列步驟：

1. 在左側邊欄中，瀏覽至&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 管道]** `>` **[!UICONTROL SMS設定]**&#x200B;並選取&#x200B;**[!UICONTROL API認證]**&#x200B;功能表。 按一下&#x200B;**[!UICONTROL 建立新的API認證]**&#x200B;按鈕。

1. 設定您的RCS API認證，如下所述：

   * **[!UICONTROL SMS廠商]**： Sinch RCS。

   * **[!UICONTROL 名稱]**：輸入您的API認證名稱。

   * **[!UICONTROL 專案識別碼]**、**[!UICONTROL 應用程式識別碼]**&#x200B;和&#x200B;**[!UICONTROL API權杖]**：從您的Sinch RCS帳戶輸入專案識別碼、應用程式識別碼和API權杖。

   * **[!UICONTROL 服務計畫ID]**：輸入與您的Sinch帳戶相關聯的服務計畫ID。

   * **[!UICONTROL SMS API Token]**：輸入您Sinch帳戶的SMS API Token。

   ![](assets/rcs-config.png)

1. 選擇性地啟用&#x200B;**[!UICONTROL 對傳入]**&#x200B;使用自訂資料集選項，以將傳入RCS訊息儲存在自訂資料集中。 [了解更多](../mobile/custom-dataset-inbound-keywords.md)

1. 設定&#x200B;**[!UICONTROL API速率限制（每秒要求數）]**&#x200B;以限制每秒的API呼叫數上限，使用提供者的建議值以避免節流，或針對無限制的要求將其保留為0。

1. 完成API認證的設定時，請按一下&#x200B;**[!UICONTROL 提交]**。

1. 在&#x200B;**[!UICONTROL API認證]**&#x200B;功能表中，按一下bin圖示以刪除您的API認證。

1. 若要修改現有認證，請找到所需的API認證，然後按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;選項以進行必要的變更。

在建立及設定您的API認證後，您現在需要建立[您的Webhook](mobile-webhook.md)以及RCS訊息的通道設定。 [了解更多](mobile-configuration-surface.md)


<!--
### Basic RCS Messages

>[!AVAILABILITY]
>
> Basic RCS messages is only available upon Adobe RCS add-on offering.

1. **Set up your branded RCS agent**

    Create a branded RCS agent in the Sinch Dashboard. [Learn more on branded RCS agent](https://community.sinch.com/t5/RCS/Getting-Started-with-RCS-using-Conversation-API/ta-p/17844)

1. **Set up your [Custom API credentials](mobile-configuration-custom.md)**
    
    Once your RCS agent is approved, you need to set up your Sinch API credentials, which include your access key, secret, and service plan ID. These credentials will be used by Journey Optimizer to authenticate and send messages through Sinch's platform.

1. **Create a [channel configuration](mobile-configuration-surface.md) for your RCS messages**

    Configure a channel surface in Journey Optimizer by linking your Sinch credentials and defining the messaging parameters. This setup enables you to compose and send RCS messages from Journey Optimizer.

1. **Create and personalize your [SMS message](../mobile/create-mobile-message.md)**

    Your messages automatically falls back to SMS when the profile's device does not support RCS or is temporarily unreachable via RCS.
-->



