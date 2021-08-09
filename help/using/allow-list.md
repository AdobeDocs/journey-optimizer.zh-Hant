---
title: 允許清單
description: 了解如何使用允許的清單。
feature: 傳遞能力
topic: 內容管理
role: User
level: Intermediate
source-git-commit: e2743c8fa624a7a95b12c3adb5dc17a1b632c25d
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 1%

---

# 允許的清單 {#allow-list}

您現在可以在[sandbox](administration/sandboxes.md)層級定義特定的傳送安全清單，以便擁有用於測試的安全環境。 在可能發生錯誤的非生產執行個體上，允許的清單可確保您沒有將不需要的訊息傳送給客戶的風險。

允許的清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 這可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。

>[!CAUTION]
>
>此功能&#x200B;**不**&#x200B;適用於生產沙箱。 它僅適用於電子郵件通道。

## 啟用允許的清單 {#enable-allow-list}

若要在非生產沙箱上啟用此功能，請更新允許的清單，使其不再為空白。 若要停用，請清除允許的清單，使其再次空白。

在[此小節](#logic)中了解更多允許的清單邏輯。

<!--
To enable the allowed list on a non-production sandbox, you need to make an Adobe API call.

* Using this API, you can also disable the feature at any time.

* You can update the allowed list before or after enabling the feature.

* The allowed list logic applies when the feature is enabled and if the allowed list is not empty. Learn more in this section (logic).
-->

>[!NOTE]
>
>啟用後，執行歷程時，以及使用[校樣](preview.md#send-proofs)測試訊息，以及使用[測試模式](building-journeys/testing-the-journey.md)測試歷程時，都會採用允許的清單功能。

## 將實體新增至允許的清單 {#add-entities}

若要將新電子郵件地址或網域新增至特定沙箱的允許清單，您必須使用`listType`屬性的`ALLOWED`值呼叫抑制API。 例如：

![](assets/allow-list-api.png)

您可以執行&#x200B;**Add**、**Delete**&#x200B;和&#x200B;**Get**&#x200B;操作。

>[!NOTE]
>
>允許的清單最多可包含1,000個項目。

<!--Learn more on making Adobe API calls in the [Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en).-->

## 允許的清單邏輯 {#logic}

<!-- When the allowed list is enabled (enable-allow-list) at the sandbox level using the API call above, the following applies.-->

當允許的清單為&#x200B;**empty**&#x200B;時，不會應用允許的清單邏輯。 這表示您可以傳送電子郵件給任何設定檔，但前提是它們不在[隱藏清單](suppression-list.md)中。

當允許的清單為&#x200B;**非空**&#x200B;時，將應用允許的清單邏輯：

* 如果允許的清單&#x200B;**上沒有實體，且隱藏清單上沒有實體，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Not allowed]**。**

* 如果允許的清單&#x200B;**上的實體為**，而非隱藏清單上的實體，則可以將電子郵件發送到相應的收件人。 但是，如果實體也在[隱藏清單](suppression-list.md)中，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Suppressed]**。




