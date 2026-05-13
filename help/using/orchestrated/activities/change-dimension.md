---
solution: Journey Optimizer
product: journey optimizer
title: 使用變更維度活動
description: 了解如何使用變更維度活動
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/yN2RlYom4xpdiG0G8pt3U4MeY0C1JjDudDqYg-HPv1w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 336
ht-degree: 50%

---

# 變更維度 {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="產生補集"
>abstract="您可以使用剩餘群體 (其已因重複而排除) 產生額外的傳出轉變。 若要這樣做，請開啟「**產生補集**」選項"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="變更維度活動"
>abstract="此活動可讓您在建立對象時變更目標市場選擇維度。 其會根據資料範本和輸入維度來移動軸。 例如，您可以從「合約」維度切換到「用戶端」維度。"

行銷人員可在協調的行銷活動中，從一個資料實體變更為相關的資料實體，藉此增強受眾目標定位。 這可讓您超越使用者輪廓，並專注於特定行為，例如購買、預訂或其他互動。

若要達成此目的，請使用&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動。 它可讓您在協調的行銷活動期間調整目標維度。

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.
-->

## 設定變更維度活動 {#configure}

請按照以下步驟設定&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動：

1. 新增&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動至您的協調行銷活動。

   ![](../assets/orchestrated-change-dimension.png)

1. 定義&#x200B;**[!UICONTROL 新目標維度]**。 「變更」維度步驟使用外部聯結：輸入母體中的所有記錄都會通過，包括新維度中沒有相符條目的記錄。

   >[!IMPORTANT]
   >
   >新目標維度中沒有相符設定檔的記錄會在訊息傳送時間&#x200B;**自動排除**。 此排除目前未反映在排除記錄檔中。 若要及早識別不相符的記錄，請在變更維度步驟之後，在轉變上使用&#x200B;**預覽結果**&#x200B;選項，並在繼續之前驗證記錄計數符合您的預期。


## 範例 {#example}

此使用案例著重於傳送簡訊給在過去一個月內建立願望清單的輪廓。

從&#x200B;**[!UICONTROL 建立客群]**&#x200B;活動開始，使用&#x200B;**[!UICONTROL 願望清單]**&#x200B;目標維度來識別所有相關的願望清單。

然後，新增&#x200B;**[!UICONTROL 變更維度]**&#x200B;活動，以將目標維度從&#x200B;**[!UICONTROL 願望清單]**&#x200B;切換為&#x200B;**[!UICONTROL 收件者]。** 此步驟會確保已協調的行銷活動目標為連結至這些願望清單的正確設定檔，可讓SMS傳送至預期的設定檔。

![](../assets/orchestrated-change-dimension-example.png)
