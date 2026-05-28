---
solution: Journey Optimizer
product: journey optimizer
title: AEM內容片段
description: 瞭解如何存取及管理AEM內容片段
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 18%

---

# 開始使用Adobe Experience Manager內容片段 {#aem-fragments}

>[!AVAILABILITY]
>
>對於醫療保健客戶，只有在授權Journey Optimizer Healthcare Shield和Adobe Experience Manager增強式安全性附加方案後，才會啟用整合。

透過將 Adobe Experience Manager as a Cloud Service 與 Adobe Journey Optimizer 整合在一處，您可以立即將 AEM 內容片段順利整合到 Journey Optimizer 內容當中。 已簡化的連線可以簡化存取，並運用 AEM 內容的程式，讓您建立個人化的動態行銷活動和歷程。

若要深入瞭解AEM內容片段，請參閱Experience Manager檔案中的[使用內容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}。

## 內容片段生命週期

![](assets/do-not-localize/AEM_CF.png)

內容片段會根據其存在的Adobe Experience Manager層級遵循不同的生命週期階段。 [在Adobe Experience Manager檔案中進一步瞭解](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

內容是在&#x200B;**製作層級**&#x200B;上建立和管理的，其中片段可以具有狀態，例如，新增、草稿、已發佈、已修改或已取消發佈。 這些狀態僅適用於&#x200B;**作者階層**，並支援內容建立和檢閱。

發佈內容片段時，會在&#x200B;**發佈階層**&#x200B;上建立復本，並透過公開、未驗證的端點公開。 Journey Optimizer只與此&#x200B;**發佈階層**&#x200B;整合。

因此，Journey Optimizer只會顯示已發佈或已修改的內容片段，並一律使用最新發佈的版本。 發佈後所做的任何變更，在重新發佈內容片段之前都不會反映在Journey Optimizer中。
