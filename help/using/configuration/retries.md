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
feature: 應用程式設定
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# 重試次數 {#retries}

當訊息因暫時&#x200B;**軟退信**&#x200B;或&#x200B;**Ignored**&#x200B;錯誤而失敗時，會執行多次重試。 每個錯誤都會增加一個錯誤計數器。 當此計數器達到限制閾值時，該地址將添加到隱藏清單中。

在預設配置<!--so can you edit this setting or not?? contradictory information was given-->中，閾值設定為三個錯誤：

* 對於相同傳送，在第三次遇到錯誤時，會抑制該位址。

* 如果有不同的傳送，且至少24小時之外發生兩個錯誤，則錯誤計數器會在每個錯誤時增加，而地址也會在第三次嘗試時被抑制。

如果重試後傳送成功，則地址的錯誤計數器會重新初始化。

您可以使用&#x200B;**[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**&#x200B;菜單中的&#x200B;**[!UICONTROL Edit]**&#x200B;按鈕修改限制閾值。<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## 消息重試持續時間 {#retry-duration}

從將郵件新增至電子郵件佇列時，將對&#x200B;**3.5天**&#x200B;執行重試。

根據IP在歷史和當前指定域的執行狀況，要執行的重試之間的最小延遲和最大重試次數為<!--managed by the Enhanced MTA,-->。

3.5天後，重試佇列中的任何郵件都會從佇列中移除，並以退信的形式傳回。<!--???-->