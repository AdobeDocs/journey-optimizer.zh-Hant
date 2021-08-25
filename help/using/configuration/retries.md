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
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# 重試次數 {#retries}

當電子郵件訊息因暫時&#x200B;**軟退信**&#x200B;或&#x200B;**Ignored**&#x200B;錯誤而失敗時，會執行多次重試。 每個錯誤都會增加一個錯誤計數器。 當此計數器達到限制閾值時，該地址將添加到隱藏清單中。

>[!NOTE]
>
>進一步了解[傳送失敗類型](../suppression-list.md#delivery-failures)區段中的錯誤類型。

在預設設定中，臨界值設定為三個錯誤：

* 對於相同傳送，在第三次遇到錯誤時，會抑制該位址。

* 如果有不同的傳送，且至少24小時之外發生兩個錯誤，則錯誤計數器會在每個錯誤時增加，而地址也會在第三次嘗試時被抑制。

如果重試後傳送成功，則地址的錯誤計數器會重新初始化。

您可以使用&#x200B;**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**&#x200B;功能表中的&#x200B;**[!UICONTROL Edit]**&#x200B;按鈕修改限制閾值。

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## 重試時間段 {#retry-duration}

**重試時段**&#x200B;是傳送中遇到暫時錯誤或軟退信的任何電子郵件將重試的時間範圍。

依預設，從將訊息新增至電子郵件佇列時起，將對&#x200B;**3.5天**（或&#x200B;**84小時**）執行重試。

不過，為確保不再需要重試嘗試時，您可以在建立或編輯套用至電子郵件通道的[訊息預設集](message-presets.md)時，根據您的需求變更此設定。

例如，對於與密碼重設相關的交易式電子郵件，並且包含僅有一天有效的連結，您可以將重試期間設為24小時。 同樣地，對於午夜銷售，您可能想要定義6小時的重試期間。

>[!NOTE]
>
>重試期不能超過84小時。 行銷電子郵件的最低重試時間為6小時，交易式電子郵件的最低重試時間為10分鐘。

了解在[此區段](message-presets.md#create-message-preset)中建立訊息預設集時，如何調整電子郵件重試參數。

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->