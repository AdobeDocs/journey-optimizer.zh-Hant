---
solution: Journey Optimizer
product: journey optimizer
title: 將內容屬性新增到已發佈的片段
description: 瞭解如何新增內容屬性至已發佈的片段（可用性限制）
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
exl-id: a274656e-2570-4a9c-b72b-4e8e920b7462
TQID: https://experienceleague.adobe.com/yweu8QtcWU42ZI2z93vIf5-LUGP7pQ16bJUQnmDKNGY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: c6e980f5-2d4f-494f-beef-186b9ecf1513id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 363
ht-degree: 8%

---

# 將內容屬性新增到已發佈的片段 {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>此功能僅適用於特定客戶，且涉及重大風險。 請向您的Adobe代表確認此功能已為您的組織啟用。

依預設，不支援將新的[個人化屬性](../personalization/personalization-build-expressions.md)新增至已發佈的片段。 片段發佈後，所有行銷活動和歷程的設定檔或內容屬性集都會鎖定。

但是，對於特定客戶，只能將&#x200B;**關聯式屬性**&#x200B;新增至已發佈的片段。

>[!WARNING]
>
>將個人化屬性新增到已發佈的片段時，驗證程式較不嚴格，並且可能無法偵測錯誤。 這可能會造成在使用該片段大規模進行的歷程和行銷活動間發生意外中斷。

## 護欄與限制 {#limitations}

* 請確定目前使用片段的所有歷程和行銷活動都可以處理新的內容屬性。
* 無法將設定檔屬性新增到發佈的片段。 僅支援內容屬性。
* 內容屬性必須手動輸入至程式碼編輯器，且無法從個人化編輯器UI中選取。
* 將個人化屬性新增到即時片段時，驗證會寬鬆，這表示可能無法偵測錯誤，並可能導致大規模意外中斷。
* 發佈後，任何錯誤都將立即影響使用該片段的所有通訊。

## 新增內容屬性 {#add-contextual-attributes}

若要將內容屬性新增至已發佈的片段，請遵循下列步驟。

>[!IMPORTANT]
>
>只有在您完全[瞭解對參照片段的歷程和行銷活動的影響](#limitations)時，才能繼續。

1. 瀏覽至&#x200B;**[!UICONTROL 內容管理]** > **[!UICONTROL 片段]**。

1. 選取已發佈的片段，然後按一下&#x200B;**[!UICONTROL 修改]**&#x200B;以建立草稿版本。

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. 按一下「**[!UICONTROL 編輯]**」以開啟片段內容編輯器。

1. 切換至個人化編輯器中的&#x200B;**[!UICONTROL 程式碼編輯器]**&#x200B;或&#x200B;**[!UICONTROL 進階模式]**。

1. 使用`{{context.attribute_name}}`語法手動輸入或複製貼上內容屬性：

   `promotionCode`屬性的範例：

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >仔細檢查屬性路徑是否準確。 可能無法偵測到錯誤，並且可能會大規模中斷歷程或行銷活動通訊。

1. 儲存您的變更。

1. 確認後，按一下&#x200B;**[!UICONTROL 發佈]**，讓您的變更上線。

>[!NOTE]
>為避免歷程和行銷活動之間發生意外中斷，您可在非生產環境中測試內容屬性路徑。

## 相關主題 {#related-topics}

* [管理片段](manage-fragments.md)
* [編輯片段](manage-fragments.md#edit-fragments)
* [API 觸發的行銷活動](../campaigns/api-triggered-campaigns.md)
* [個人化語法](../personalization/personalization-syntax.md)
