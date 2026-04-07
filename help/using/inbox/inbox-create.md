---
title: 建立收件匣
description: 瞭解如何在Adobe Journey Optimizer中建立及設定收件匣，以傳送永續性、非侵入式訊息給您的使用者。
feature: Content Cards
topic: Content Management
role: User
level: Beginner
source-git-commit: d84cc0f4d9226876e55e37409a685550fe0c9050
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 3%

---

# 建立收件匣 {#inbox-create}

在建立收件匣之前，請先完成[收件匣組態](inbox-configuration.md)中的步驟。 此管道設定可識別目標應用程式或網站、頁面或規則，以及收件匣轉譯的位置。

若要透過行銷活動建立訊息收件匣，請執行下列步驟：

1. 建立行銷活動。 [了解更多](../campaigns/create-campaign.md)

1. 選取您要執行的行銷活動型別：

   * **[!UICONTROL 已排程 — 行銷]**：立即或在指定日期執行行銷活動。 已排程的行銷活動旨在傳送&#x200B;**行銷**&#x200B;訊息。 可從使用者介面設定及執行。

   * **[!UICONTROL API觸發 — 行銷/異動]**：使用API呼叫執行行銷活動。 API觸發的行銷活動旨在傳送&#x200B;**行銷**&#x200B;或&#x200B;**異動**&#x200B;訊息，即在個人執行動作後傳送的訊息：密碼重設、購物車購買等。 [瞭解如何使用API觸發行銷活動](../campaigns/api-triggered-campaigns.md)

1. 在&#x200B;**[!UICONTROL 屬性]**&#x200B;索引標籤中，指定行銷活動的名稱和說明。

1. 從&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取&#x200B;**[!UICONTROL 收件匣]**&#x200B;動作。

   ![](assets/inbox-create-1.png)

1. 選取或建立新的[收件匣組態](inbox-configuration.md)。

   ![](assets/inbox-create-2.png)

1. 存取「內容」標籤，使用內容設計工具來設計訊息。 [了解更多](inbox-design.md)

1. 在「**[!UICONTROL 對象]**」標籤中，按一下「**[!UICONTROL 選取對象]**」按鈕以顯示可用Adobe Experience Platform對象清單。 [了解更多關於客群](../audience/about-audiences.md)

1. 在&#x200B;**[!UICONTROL 身分識別名稱空間]**&#x200B;欄位中，選擇要使用的名稱空間，以識別所選區段中的個人。 [進一步瞭解名稱空間](../event/about-creating.md#select-the-namespace)

1. 您可以將行銷活動排程至特定日期，或設定為定期重複進行。 [了解更多](../campaigns/create-campaign.md#schedule)

1. 檢閱並啟用您的行銷活動，以傳送訊息至收件匣。

您現在可以在建立[內容卡行銷活動](../content-card/create-content-card.md)時選擇此收件匣。
