---
title: 批次決策
description: 瞭解如何向給定的Adobe Experience Platform部門中的所有配置檔案提供服務決策。
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# 批次決策 {#deliver}

## 開始批量決策 {#start}

Journey Optimizer允許您向給定Adobe Experience Platform段中的所有配置檔案提供優惠決定。

為此，您需要在Journey Optimizer建立一個作業請求，該請求將包含有關要目標的段和要使用的聘用決定的資訊。 然後，將段中每個配置檔案的提供內容放在Adobe Experience Platform資料集中，在該資料集中可用於自定義批處理工作流。

也可以使用API執行批傳送。 有關詳細資訊，請參閱 [批決策API文檔](api-reference/offer-delivery-api/batch-decisioning-api.md)。

## 先決條件 {#prerequisites}

在配置作業請求之前，請確保已建立：

* **資料集** 在Adobe Experience Platform。 此資料集將用於使用「ODE DecisionEvents」架構儲存決策結果。 在 [資料集文檔](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant)。

* **段** 在Adobe Experience Platform。 應評估該段，然後進行更新。 瞭解如何更新中的段成員資格評估 [分段服務文檔](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >批處理作業將運行每天發生一次的配置檔案快照。 批決策會限制頻率並始終從最近的快照載入配置檔案。 在嘗試批處理決策API之前，請在建立段後等待最多24小時。

* **決定** 在Adobe Journey Optimizer。 [瞭解如何建立決策](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 建立作業請求

要建立新作業請求，請執行以下步驟。

1. 在 **[!UICONTROL 優惠]** 菜單開啟它 **[!UICONTROL 批量決策]** 按鈕 **[!UICONTROL 建立請求]**。

   ![](assets/batch-create.png)

1. 將作業請求命名，然後選擇應將作業資料發送到的資料集。

1. 選擇要瞄準的Adobe Experience Platform段。

1. 選擇一個或多個要用於將優惠交付給該段的優惠決策範圍：
   1. 從清單中選取一個放置。
   1. 顯示可用於選定放置的決定。 選擇您選擇的決定，然後按一下 **[!UICONTROL 添加]**。
   1. 重複該操作，以根據需要添加任意多個決策範圍。

   ![](assets/batch-decision.png)

1. 預設情況下，每個配置檔案都返回一個決策範圍。 您可以使用 **[!UICONTROL 按配置檔案請求聘用]** 的雙曲餘切值。 例如，如果選擇2，則最佳的2個優惠將顯示為所選決策範圍。

   >[!NOTE]
   >
   >每個決策範圍最多可請求30個優惠。

1. 如果要在資料集中包括優惠內容，請切換 **[!UICONTROL 包括內容]** 的上界。 預設情況下禁用此選項。

1. 按一下 **[!UICONTROL 建立]** 執行作業請求。

## 監視批處理作業

所有請求的批處理作業都可從 **[!UICONTROL 批量決策]** 頁籤。 此外，搜索和篩選工具還可幫助您細化清單。

![](assets/batch-list.png)

### 作業請求狀態

建立作業請求後，批作業將經歷多個狀態：

>[!NOTE]
>
>為確保您獲得有關作業請求狀態的最新資訊，請使用作業旁邊的省略號按鈕來刷新它。

1. **[!UICONTROL 已排隊]**:已建立作業請求並已進入處理隊列。 每個資料集一次最多可運行5個批處理作業。 具有相同輸出資料集的任何其他批處理請求都會添加到隊列。 已排隊的作業在前一作業完成運行後被拾取處理。
1. **[!UICONTROL 處理]**:正在處理作業請求
1. **[!UICONTROL 英格斯廷]**:作業請求已執行，結果資料正在所選資料集中被攝取，
1. **[!UICONTROL 已完成]**:已執行作業請求，結果資料現在被儲存到所選資料集中。

   >[!NOTE]
   >
   >通過按一下作業清單中的作業名稱，可以訪問儲存作業結果的資料集。

如果在執行作業請求時出錯，它將 **[!UICONTROL 錯誤]** 狀態。 嘗試複製批處理作業以建立新請求。 [瞭解如何複製批處理作業](#duplicate)

### 批處理作業處理時間

每個批處理作業的端到端時間是從建立工作負載到輸出資料集中提供決策結果的持續時間。

段大小是影響端到端批決策時間的主要因素。 如果合格的優惠啟用了全局頻率上限，則完成批量確定需要額外時間。 下面是針對其各自段大小的端到端處理時間的一些近似值，其中包括對合格報價進行頻率封頂和不進行頻率封頂：

啟用頻率上限後，可提供以下服務：

| 段大小 | 端到端處理時間 |
|--------------|----------------------------|
| 一萬個配置檔案或更少 | 7 分鐘 |
| 100萬個配置檔案或更少 | 30 分鐘 |
| 1500萬個配置檔案或更少 | 50 分鐘 |

沒有合格報價的頻率上限：

| 段大小 | 端到端處理時間 |
|--------------|----------------------------|
| 一萬個配置檔案或更少 | 6 分鐘 |
| 100萬個配置檔案或更少 | 8 分鐘 |
| 1500萬個配置檔案或更少 | 16 分鐘 |

## 復製作業請求 {#duplicate}

您可以重用現有作業的資訊來建立新請求。

為此，請按一下複製表徵圖，在必要時編輯作業資訊，然後按一下 **[!UICONTROL 建立]** 來修改標籤元素的屬性。

![](assets/batch-duplicate.png)
