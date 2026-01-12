---
solution: Journey Optimizer
product: journey optimizer
title: 結合目標定位與實驗
description: 瞭解如何在單一歷程或行銷活動中結合目標定位和實驗，以建立複雜的最佳化策略。
role: User
level: Intermediate
keywords: 最佳化，鎖定目標，實驗，組合，進階
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# 結合目標定位與實驗 {#combination}

Journey Optimizer也可讓您在單一歷程或行銷活動中結合目標定位和實驗，以建立更複雜的策略。

事實上，您可以使用鎖定目標建立數個變體，並針對每個變體使用實驗進一步最佳化每個內容。 這可確保實驗特定於每個定位規則，且不會跨越變體。

例如，您可以針對美國客戶測試「促銷活動50%折扣」與「50美元禮品卡」，並針對歐洲客戶執行其他測試，例如「超過50歐元訂單的免運費」與「下次購買折扣20%」。

若要在歷程或行銷活動中同時結合目標定位和實驗，請遵循下列步驟。

1. 建立您定義數個鎖定目標規則的歷程或行銷活動。 [了解作法](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. 為第一個鎖定目標規則建立實驗。

1. 視需要設計和設定您的內容實驗。 [了解作法](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   定義實驗後，該實驗將僅適用於第一個目標規則。

1. 返回&#x200B;**[!UICONTROL 動作]**&#x200B;索引標籤，選取&#x200B;**[!UICONTROL 編輯內容]**。

1. 對於您第一個鎖定目標規則所定義的群組，您可以為實驗的每個變體定義特定的內容。

   如果您將多個入站動作新增至歷程或行銷活動，則定位和實驗會套用至每個動作。 不過，您需要為每個動作的每個變體定義特定內容。

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. 以類似方式處理其他鎖定目標規則，並為每個變體設計對應的內容。

1. 儲存您的變更並[啟用](review-activate-campaign.md)您的歷程或行銷活動。

歷程/行銷活動上線後，每個目標群組的使用者會被隨機指派為其所屬群組定義的不同內容變數。

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

