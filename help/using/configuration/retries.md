---
title: 重試次數
description: 了解如何在將地址發送到隱藏清單之前執行重試
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# 重試次數 {#retries}

當電子郵件因暫時性而失敗時 **軟跳出** 錯誤，會執行多次重試。 每個錯誤都會增加一個錯誤計數器。 當此計數器達到限制閾值時，該地址將添加到隱藏清單中。

>[!NOTE]
>
>進一步了解中的錯誤類型 [傳送失敗類型](../suppression-list.md#delivery-failures) 區段。

在預設設定中，臨界值設為5個錯誤。

* 對於相同傳送，在第五個傳送時， [重試時間段](#retry-duration)，則會抑制該地址。

* 如果有不同的傳送，且至少24小時之外發生兩個錯誤，則錯誤計數器會在每個錯誤時增加，而地址也會在第五次嘗試時被抑制。

如果重試後傳送成功，則地址的錯誤計數器會重新初始化。

如果預設值5不符合您的需求，您可以依照下列步驟修改錯誤臨界值。

1. 前往 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Suppression list]**。

1. 選取 **[!UICONTROL Edit suppression rules]** 按鈕。

   ![](../assets/suppression-list-edit-retries.png)

1. 根據您的需求編輯允許的連續軟跳出數。

   ![](../assets/suppression-list-edit-soft-bounces.png)

   您必須輸入介於1和20之間的整數值，這表示最小重試次數為1，最大重試次數為20。

   >[!CAUTION]
   >
   >超過10的值可能會造成傳遞能力信譽問題，以及IP限制或ISP封鎖名單。 [深入了解傳遞能力](../deliverability.md)

<!--![](../assets/retries-edition.png)-->

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## 重試時段 {#retry-duration}

此 **重試時間段** 是傳送中遇到暫時錯誤或軟退信的任何電子郵件訊息會重試的時間範圍。

預設情況下，將對執行重試 **3.5天** (或 **84小時**)，從訊息新增至電子郵件佇列的時間開始。

不過，為確保不再需要時執行重試嘗試，您可以在建立或編輯 [訊息預設集](message-presets.md) 套用至電子郵件通道。

例如，對於與密碼重設相關的交易式電子郵件，並且包含僅有一天有效的連結，您可以將重試期間設為24小時。 同樣地，對於午夜銷售，您可能想要定義6小時的重試期間。

>[!NOTE]
>
>重試期不能超過84小時。 行銷電子郵件的最低重試時間為6小時，交易式電子郵件的最低重試時間為10分鐘。

了解在中建立訊息預設集時，如何調整電子郵件重試參數 [本節](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->

<!--Once a message has been in the retry queue for a maximum of 3.5 days and has failed to deliver, it will time out and its status will be updated to Failed??-->
