---
title: 批次決策
description: 了解如何將優惠方案決策傳送至指定Adobe Experience Platform區段中的所有設定檔。
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: a56d675e014d55064073eba011fb50e2d363844d
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---

# 批次決策 {#deliver}

## 開始使用批次決策功能 {#start}

Journey Optimizer可讓您將優惠方案決策傳送至指定Adobe Experience Platform區段中的所有設定檔。

若要這麼做，您必須在Journey Optimizer中建立工作請求，其中包含要鎖定的區段及要使用的優惠方案決策的相關資訊。 區段中每個設定檔的選件內容會放入Adobe Experience Platform資料集，供自訂批次工作流程使用。

您也可以使用API執行批次傳送。 有關詳細資訊，請參閱 [Batch Decisioning API檔案](api-reference/offer-delivery-api/batch-decisioning-api.md).

## 先決條件 {#prerequisites}

設定工作請求之前，請確定您已建立：

* **資料集** 在Adobe Experience Platform。 此資料集將用於使用「ODE DecisionEvents」架構儲存決策結果。 了解更多 [資料集檔案](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh-Hant).

* **區段** 在Adobe Experience Platform。 應評估區段，然後更新。 了解如何在 [區段服務檔案](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >批次作業會關閉每天發生一次的設定檔快照。 批次決策會限制頻率，並一律從最新快照載入設定檔。 建立區段後，請等候最多24小時，再嘗試批次決策API。

* **決定** 在Adobe Journey Optimizer。 [了解如何建立決策](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## 建立作業請求

要建立新的作業請求，請執行以下步驟。

1. 在 **[!UICONTROL 選件]** 菜單，開啟 **[!UICONTROL 批次決策]** 按一下 **[!UICONTROL 建立請求]**.

   ![](assets/batch-create.png)

1. 為工作請求命名，然後選取應將工作資料傳送至哪個資料集。

1. 選取要定位的Adobe Experience Platform區段。

1. 選取一或多個優惠方案決策範圍，以用於將優惠方案傳送至區段：
   1. 從清單中選取位置。
   1. 將顯示所選位置可用的決策。 選取您所選的決策，然後按一下 **[!UICONTROL 新增]**.
   1. 重複操作，以根據需要添加任意數量的決策範圍。

   ![](assets/batch-decision.png)

1. 依預設，會為每個設定檔傳回一個決策範圍選件。 您可以使用 **[!UICONTROL 每個設定檔的要求選件]** 選項。 例如，若您選取2，則會針對所選決策範圍顯示最佳2個選件。

   >[!NOTE]
   >
   >每個決策範圍最多可請求30個優惠方案。

1. 如果您想在資料集中包含選件內容，請切換 **[!UICONTROL 包含內容]** 選項。 預設會停用此選項。

1. 按一下 **[!UICONTROL 建立]** 執行作業請求。

## 監視批處理作業

所有請求的批處理作業均可從 **[!UICONTROL 批次決策]** 標籤。 此外，搜尋和篩選工具也可協助您調整清單。

![](assets/batch-list.png)

### 作業請求狀態

建立作業請求後，批處理作業會經歷多個狀態：

>[!NOTE]
>
>要確保獲取有關作業請求狀態的最新資訊，請使用作業旁的橢圓按鈕來刷新它。

1. **[!UICONTROL 已排隊]**:作業請求已建立，並已進入處理佇列。 每個資料集一次最多可執行5個批次作業。 具有相同輸出資料集的任何其他批次請求都會新增至佇列。 系統會擷取已排入佇列的作業，以在上一個作業完成執行後進行處理。
1. **[!UICONTROL 處理]**:正在處理作業請求
1. **[!UICONTROL 擷取]**:作業請求已執行，結果資料正在所選資料集中擷取，
1. **[!UICONTROL 已完成]**:作業請求已執行，結果資料現在會儲存到選取的資料集中。

   >[!NOTE]
   >
   >您可以在作業清單中按一下作業名稱，以存取儲存作業結果的資料集。

如果在執行工作要求時發生錯誤，則會取得 **[!UICONTROL 錯誤]** 狀態。 嘗試複製批處理作業以建立新請求。 [了解如何複製批次工作](#duplicate)

### 批次作業處理時間

每個批處理作業的端到端時間是從建立工作量到輸出資料集中提供決策結果的持續時間。

區段大小是影響端到端批決策時間的主要因素。 如果符合資格的優惠方案已啟用全域頻率上限，則批次決策需要額外的時間才能完成。 以下是其各自區段大小的端對端處理時間的一些近似值，包括合格選件具有頻率限定和不具有頻率限定：

對符合資格的優惠方案啟用頻率上限：

| 區段大小 | 端對端處理時間 |
|--------------|----------------------------|
| 10,000個設定檔或更少 | 7 分鐘 |
| 100萬個用戶檔案 | 30 分鐘 |
| 1,500萬個用戶檔案或更少 | 50 分鐘 |

符合資格優惠方案沒有頻率上限：

| 區段大小 | 端對端處理時間 |
|--------------|----------------------------|
| 10,000個設定檔或更少 | 6 分鐘 |
| 100萬個用戶檔案 | 8 分鐘 |
| 1,500萬個用戶檔案或更少 | 16 分鐘 |

## 復製作業請求 {#duplicate}

您可以重複使用現有作業的資訊以建立新請求。

要執行此操作，請按一下復製圖示，視需要編輯作業資訊，然後按一下 **[!UICONTROL 建立]** 來建立新請求。

![](assets/batch-duplicate.png)
