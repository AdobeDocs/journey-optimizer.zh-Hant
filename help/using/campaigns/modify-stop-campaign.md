---
solution: Journey Optimizer
product: journey optimizer
title: 修改或停止行銷活動
description: 瞭解如何修改、停止或複製Journey Optimizer的即時活動
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: 管理市場活動、狀態、時間表、訪問、優化程式
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# 管理行銷活動 {#modify-stop-campaign}

激活市場活動後，您可以隨時修改或停止它。 這些操作僅適用於定期執行的市場活動。

此外，您還可以複製即時市場活動（執行一次或循環執行）以建立新市場活動，並存檔已完成或停止的市場活動。

## 存取行銷活動 {#access}

可從 **[!UICONTROL 市場活動]** 的子菜單。

預設情況下，清單顯示所有市場活動 **[!UICONTROL 草稿]**。 **[!UICONTROL 計畫]**, **[!UICONTROL 實況]** 狀態。 要顯示已停止、已完成和存檔的市場活動，您需要清除篩選器。

![](assets/create-campaign-list.png)

此外，您還可以根據市場活動類型和渠道或建立市場活動時分配給市場活動的標籤來篩選清單。 [瞭解如何為市場活動分配標籤](create-campaign.md#create)

## 市場活動狀態 {#statuses}

市場活動可以具有多種狀態：

* **[!UICONTROL 草稿]**:市場活動正在編輯，尚未激活。
* **[!UICONTROL 激活]**:活動正在激活。
* **[!UICONTROL 實況]**:活動已激活。
* **[!UICONTROL 計畫]**:市場活動配置為在特定開始日期激活。
* **[!UICONTROL 已停止]**:市場活動已手動停止。 您不能再激活或重新使用它。 [瞭解如何停止活動](modify-stop-campaign.md#stop)
* **[!UICONTROL 已完成]**:市場活動已完成。 在激活市場活動3天後，或在市場活動結束日期（如果市場活動已定期執行）自動分配此狀態。
* **[!UICONTROL 存檔]**:市場活動已存檔。 [瞭解如何存檔市場活動](modify-stop-campaign.md#archive)

>[!NOTE]
>
>「開啟草稿版本」表徵圖 **[!UICONTROL 實況]** 或 **[!UICONTROL 計畫]** 狀態表示已建立市場活動的新版本，但尚未激活。 [了解更多](modify-stop-campaign.md#modify)。

## 修改定期市場活動 {#modify}

要修改和建立定期市場活動的新版本，請執行以下步驟：

1. 開啟市場活動，然後按一下 **[!UICONTROL 修改市場活動]** 按鈕

1. 將建立市場活動的新版本。 您可以通過按一下 **[!UICONTROL 開啟即時版本]**。

   ![](assets/create-campaign-draft.png)

   在市場活動清單中，具有正在進行的草稿版本的激活市場活動在中顯示一個特定表徵圖 **[!UICONTROL 狀態]** 的雙曲餘切值。 按一下此表徵圖可開啟市場活動的草稿版本。

   ![](assets/create-campaign-edit-list.png)

1. 更改準備好後，您可以激活市場活動的新版本(請參閱： [複查並激活市場活動](create-campaign.md#review-activate))。

   >[!IMPORTANT]
   >
   >激活草稿將替換活動的即時版本。

## 停止定期市場活動 {#stop}

要停止定期市場活動，請開啟它，然後按一下 **[!UICONTROL 停止市場活動]** 按鈕

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>停止市場活動不會停止正在進行的發送，但如果發送已在進行，它將停止計畫的發送或下一次發生。

<!-- inbound campaign (inapp): can stop and resume -->

## 複製市場活動 {#duplicate}

您可以複製即時市場活動以建立新市場活動。 要執行此操作，請開啟市場活動，然後按一下 **[!UICONTROL 重複]**。

![](assets/create-campaign-duplicate.png)

## 存檔市場活動 {#archive}

隨著時間的推移，市場活動清單不斷增長，最終使瀏覽已完成和停止的市場活動變得更加困難。

為防止出現這種情況，您可以存檔已完成和停止的不再需要的市場活動。 要執行此操作，請按一下省略號按鈕，然後選擇 **[!UICONTROL 存檔]**。

![](assets/create-campaign-archive.png)

然後，可以使用清單中的專用過濾器來檢索存檔的市場活動。 [瞭解如何訪問市場活動](get-started-with-campaigns.md#access)
