---
solution: Journey Optimizer
product: journey optimizer
title: 排程API觸發的行銷活動
description: 瞭解如何排程API觸發的行銷活動。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 行銷活動， API觸發， REST，最佳化工具，訊息
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# 排程API觸發的行銷活動 {#api-schedule}

使用&#x200B;**[!UICONTROL 排程]**&#x200B;索引標籤來定義行銷活動排程。

## 設定開始和結束日期

根據預設，API觸發的行銷活動會在觸發後開始，並在訊息傳送後立即結束。 如果您不想在行銷活動觸發後立即執行，可以使用&#x200B;**[!UICONTROL 行銷活動開始]**&#x200B;選項指定傳送訊息的日期和時間。

**[!UICONTROL 行銷活動end]**&#x200B;選項可讓您指定行銷活動何時應停止執行。 在指定日期以外，將不會執行行銷活動。

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>在[!DNL Adobe Journey Optimizer]中排程行銷活動時，請確定您的開始日期/時間與所要的首次傳遞一致。

## 設定速率控制

[!DNL Journey Optimizer]可讓您啟用傳出動作（電子郵件、簡訊、推播通知）的速率控制。

此功能對於防止下游系統（例如登陸頁面或客戶服務平台）上的超載特別有用。 例如，您可以將速率限制設為每秒165則訊息，以確保穩定傳送，而不會對下游系統造成衝擊。

若要設定速率控制，請在&#x200B;**[!UICONTROL 傳遞設定]**&#x200B;區段中啟用&#x200B;**[!UICONTROL 節流傳遞]**&#x200B;選項，並指定所要的&#x200B;**[!UICONTROL 傳遞速率]**。

![](assets/throttling-rate-control.png)

## 後續步驟 {#next}

行銷活動設定和內容準備就緒後，您就可以檢閱並啟用它。 [了解更多](review-activate-campaign.md)
