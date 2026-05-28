---
solution: Journey Optimizer
product: journey optimizer
title: 定義「動作」行銷活動對象
description: 瞭解如何定義「動作」行銷活動對象。
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: 建立，最佳化工具，行銷活動，表面，訊息
exl-id: 5635ef04-c69d-4397-9762-7a6f1265d453
TQID: https://experienceleague.adobe.com/3lWwW0Lru2D5D83QqHl48Gsxv7JVKjX8ZBmZAiMFiB0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 6%

---

# 定義「動作」行銷活動對象 {#action-campaign-audience}

使用&#x200B;**[!UICONTROL 對象]**&#x200B;標籤來定義行銷活動對象。

![](assets/campaign-audience.png)

1. **選取客群**

   針對行銷活動，按一下&#x200B;**[!UICONTROL 選取對象]**&#x200B;按鈕以顯示可用Adobe Experience Platform對象清單。 [進一步瞭解對象](../audience/about-audiences.md)。

   >[!IMPORTANT]
   >
   >[對象構成](../audience/get-started-audience-orchestration.md)的對象和屬性目前無法用於Healthcare Shield或Privacy and Security Shield。

1. **選取身分型別**

   在&#x200B;**[!UICONTROL 身分型別]**&#x200B;欄位中，選擇用來識別所選對象中個人的金鑰型別。 您可以使用現有的身分型別，或使用Adobe Experience Platform Identity Service建立新的身分型別。 標準身分名稱空間列於[此頁面](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}。

   每個行銷活動只允許一個身分型別。 如果屬於區段的個人在不同身分中沒有選取的身分型別，則無法將該行銷活動設為目標。 在[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=zh-Hant){target="_blank"}中進一步瞭解身分型別和名稱空間。

## 後續步驟 {#next}

一旦您的動作行銷活動的對象準備就緒後，您就可以排程行銷活動。 [了解更多](campaign-schedule.md)
