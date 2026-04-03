---
solution: Journey Optimizer
product: journey optimizer
title: AEM內容片段
description: 瞭解如何存取及管理AEM內容片段
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

---

# 開始使用Adobe Experience Manager內容片段 {#aem-fragments}

>[!AVAILABILITY]
>
>對於醫療保健客戶，只有在授權Journey Optimizer Healthcare Shield和Adobe Experience Manager增強式安全性附加方案後，才會啟用整合。

透過將 Adobe Experience Manager as a Cloud Service 與 Adobe Journey Optimizer 整合在一處，您可以立即將 AEM 內容片段順利整合到 Journey Optimizer 內容當中。已簡化的連線可以簡化存取，並運用 AEM 內容的程式，讓您建立個人化的動態行銷活動和歷程。

若要深入瞭解AEM內容片段，請參閱Experience Manager檔案中的[使用內容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}。

## 內容片段生命週期

![](assets/do-not-localize/AEM_CF.png)

內容片段會根據其存在的Adobe Experience Manager層級遵循不同的生命週期階段。 [在Adobe Experience Manager檔案中進一步瞭解](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

內容是在&#x200B;**製作層級**&#x200B;上建立和管理的，其中片段可以具有狀態，例如，新增、草稿、已發佈、已修改或已取消發佈。 這些狀態僅適用於&#x200B;**作者階層**，並支援內容建立和檢閱。

發佈內容片段時，會在&#x200B;**發佈階層**&#x200B;上建立復本，並透過公開、未驗證的端點公開。 Journey Optimizer只與此&#x200B;**發佈階層**&#x200B;整合。

因此，Journey Optimizer只會顯示已發佈或已修改的內容片段，並一律使用最新發佈的版本。 發佈後所做的任何變更，在重新發佈內容片段之前都不會反映在Journey Optimizer中。
