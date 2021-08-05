---
title: 允許清單
description: 了解如何使用允許的清單。
feature: 傳遞能力
topic: 內容管理
role: User
level: Intermediate
source-git-commit: 288c27d4fc64a6d0a6f07b634ed044a6e858d0c1
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 1%

---

# 允許的清單 {#allow-list}

您現在可以在[sandbox](administration/sandboxes.md)層級定義特定的傳送安全清單，以便擁有用於測試的安全環境。 在可能發生錯誤的非生產執行個體上，允許的清單可確保您沒有將不需要的訊息傳送給客戶的風險。

>[!CAUTION]
>
>生產沙箱無法使用此功能。

允許的清單可讓您指定個別電子郵件地址或網域，這些地址或網域將是唯一獲授權接收您從特定沙箱傳送之電子郵件的收件者或網域。 這可防止您在測試環境中意外傳送電子郵件至真實的客戶地址。

>[!NOTE]
>
>此功能僅適用於電子郵件通道。

## 啟用允許的清單 {#enable-allow-list}

若要在非生產沙箱上啟用允許的清單，您必須進行AdobeAPI呼叫。

* 使用此API，您也可以隨時停用功能。

* 您可以在啟用功能之前或之後更新允許的清單。

* 允許的清單邏輯會在功能啟用且允許的清單不為空時套用。 進一步了解[本節](#logic)。

>[!NOTE]
>
>啟用後，執行歷程時，以及使用[校樣](preview.md#send-proofs)測試訊息，以及使用[測試模式](building-journeys/testing-the-journey.md)測試歷程時，都會採用允許的清單功能。

## 將實體新增至允許的清單 {#add-entities}

>[!CAUTION]
>
>此功能&#x200B;**不**&#x200B;適用於生產沙箱。 它僅適用於電子郵件通道。

若要將新電子郵件地址或網域新增至特定沙箱的允許清單，您必須使用`listType`屬性的`ALLOWED`值呼叫抑制API。 例如：

![](assets/allow-list-api.png)

您可以執行&#x200B;**Add**、**Delete**&#x200B;和&#x200B;**Get**&#x200B;操作。

>[!NOTE]
>
>允許的清單最多可包含1,000個項目。

在[Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-guide.html?lang=en)中，深入了解進行AdobeAPI呼叫。

## 允許的清單邏輯 {#logic}

<!-- When the allowed list is \[enabled\]\(\add link here\) at the sandbox level using the API call above, the following applies.-->

1. 當允許的清單為&#x200B;**empty**&#x200B;時，不會應用允許的清單邏輯。 這表示您可以傳送電子郵件給任何設定檔，但前提是它們不在[隱藏清單](suppression-list.md)中。

1. 當允許的清單為&#x200B;**非空**&#x200B;時，將應用允許的清單邏輯：

   * 如果允許的清單&#x200B;**上沒有實體，且隱藏清單上沒有實體，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Not allowed]**。**

   * 如果允許的清單&#x200B;**上的實體為**，而非隱藏清單上的實體，則可以將電子郵件發送到相應的收件人。 但是，如果實體也在[隱藏清單](suppression-list.md)中，則相應的收件人將不會收到電子郵件，原因為&#x200B;**[!UICONTROL Suppressed]**。




