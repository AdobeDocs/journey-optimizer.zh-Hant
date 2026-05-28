---
solution: Journey Optimizer
product: journey optimizer
title: 檢閱並啟用API觸發的行銷活動
description: 瞭解如何檢閱及啟用API觸發的行銷活動。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 行銷活動， API觸發， REST，最佳化工具，訊息
exl-id: 561f1215-d13d-4ffc-b6f1-396ae67774c8
TQID: https://experienceleague.adobe.com/nP10Q8F2mo1JIcRiFOPRXqlrhRCDKKdtmgFJhRDOTAU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: c998adc41e5696cc24bb7c640ec330ccfefa139a
workflow-type: tm+mt
source-wordcount: 314
ht-degree: 5%

---

# 檢閱並啟用API觸發的行銷活動 {#api-review}

設定API觸發的行銷活動後，您必須先檢閱其引數和內容，才能加以啟用。 要執行此操作，請依照下列步驟執行：

>[!IMPORTANT]
>
> 如果您的行銷活動受核准政策的約束，您將需要請求核准才能傳送您的行銷活動。 [了解更多](../test-approve/gs-approval.md)

1. 在行銷活動設定畫面中，按一下&#x200B;**[!UICONTROL 檢閱以啟動]**&#x200B;以顯示行銷活動的摘要。

   ![](assets/campaign-review.png)

1. 行銷活動設定摘要隨即顯示，供您檢查是否有任何引數不正確或遺失，並視需要修改行銷活動。

   如果發生錯誤，便無法啟用行銷活動。 請先解決錯誤，然後再繼續。

   ![](assets/create-campaign-alerts.png)

1. 當行銷活動在其內容中使用[決定原則](../experience-decisioning/create-decision.md)時，您可以檢閱每個原則的結構，並直接從行銷活動摘要複製技術詳細資訊。 [了解做法](../experience-decisioning/use-decision-policy.md#decision-policy-summary)

1. 檢查您的行銷活動是否已正確設定，然後按一下[啟動]。****

1. 行銷活動已啟動。 其狀態為&#x200B;**[!UICONTROL 即時]**，或者&#x200B;**[!UICONTROL 已排程]** （如果您已輸入開始日期）。

   **[!UICONTROL 已完成]**&#x200B;狀態會在行銷活動啟動3天後自動指派給行銷活動，如果行銷活動有週期性執行，則會在行銷活動的結束日期自動指派。 [進一步瞭解行銷活動狀態](manage-campaigns.md#statuses)。

   如果未指定結束日期，則行銷活動會保留&#x200B;**[!UICONTROL 即時]**&#x200B;狀態。 若要變更，您必須手動停止行銷活動。 [瞭解如何停止行銷活動](manage-campaigns.md)

1. 行銷活動啟動後，您可以隨時透過開啟行銷活動來檢查其資訊。 摘要可讓您取得目標設定檔與傳送和失敗動作數的統計資料。

   您也可以按一下&#x200B;**[!UICONTROL 報表]**&#x200B;按鈕，在專用報表中取得其他統計資料。 [了解更多](../reports/campaign-global-report-cja.md)

   ![](assets/create-campaign-summary.png)

## 後續步驟 {#next}

一旦API觸發的行銷活動準備就緒後，您就可以使用API觸發其執行。 [了解更多](trigger-campaigns.md)