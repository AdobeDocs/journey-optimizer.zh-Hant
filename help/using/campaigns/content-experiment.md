---
title: 建立內容實驗
description: 瞭解如何在您的活動中建立內容實驗
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 0036c905b9344a6f99e8525acbe9caab5932f361
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---

# 建立內容實驗 {#content-experiment}

>[!AVAILABILITY]
>
>「內容」實驗功能目前僅適用於一組組織（有限可用性）。 如需詳細資訊，請聯絡您的 Adobe 代表。

內容實驗功能允許您定義多個傳遞處理。 興趣對象被隨機地分配到每個治療中，以確定哪個在興趣度量方面表現最佳。 您可以選擇更改電子郵件的內容、主題或發件人。

在下例中，交貨目標已分解為兩個組，每個組佔目標人口的45%，而拒絕組佔10%，他們將不接收交貨。

目標受眾中的每個人將收到一個版本的電子郵件，主題行是以下兩個版本之一：

* 直接宣傳新系列和形象10%的報價。
* 另一個只是在沒有任何影像的情況下，在沒有指定10%的折扣的情況下，宣傳特價。

此處的目標是查看收件人是否會根據收到的實驗與電子郵件進行交互。 因此，我們將選擇 **[!UICONTROL Email Opens]** 作為本內容實驗中的主要目標度量。

![](assets/content_experiment.png)

## 建立市場活動 {#campaign-experiment}

1. 從 **[!UICONTROL Campaigns]** 的 **[!UICONTROL Create Campaign]**。

   ![](assets/content_experiment_1.png)

1. 選擇 **[!UICONTROL Email]** 然後 **[!UICONTROL Surface]** 您想用於此交貨。 有關詳細資訊，請參閱 [通道曲面](../configuration/channel-surfaces.md) 的子菜單。

   ![](assets/content_experiment_2.png)

1. 按一下「**[!UICONTROL Create]**」。

1. 設定 **[!UICONTROL Properties]** 您的交貨：
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. 要啟動內容實驗，請切換 **[!UICONTROL Content experiment]** 的雙曲餘切值。 的 **[!UICONTROL Content experiment]** 的子菜單。

   ![](assets/content_experiment_3.png)

1. 設定 **[!UICONTROL Audience]** 和 **[!UICONTROL Schedule]** 交貨的參數。 [了解更多](create-campaign.md)

1. 按一下 **[!UICONTROL Edit content]** 開始個性化 **[!UICONTROL Treatments]**。

   ![](assets/content_experiment_4.png)

## 建立您的治療 {#treatment-experiment}

1. 從 **[!UICONTROL Edit content]** 的 **[!UICONTROL Subject line]** 郵件，然後按一下 **[!UICONTROL Save]**。

   對於此處理，我們直接在主題行中指定優惠。

   ![](assets/content_experiment_5.png)

1. 按一下 **[!UICONTROL Email designer]** 開始個性化送貨。

   ![](assets/content_experiment_6.png)

1. 設計完電子郵件後，按一下 **[!UICONTROL Save]** 回到 **[!UICONTROL Edit content]** 的子菜單。

1. 從 **[!UICONTROL More actions]** 按鈕 **[!UICONTROL Duplicate]**。

   也可以選擇從頭開始新治療，按一下 **[!UICONTROL Content experiment]** 按鈕 **[!UICONTROL Add treatment]**。

   ![](assets/content_experiment_7.png)

1. 更改 **[!UICONTROL Title]** 來讓他們更加與眾不同。

   ![](assets/content_experiment_8.png)

1. 選擇連結到新建立的電子郵件傳遞 **[!UICONTROL Treatment]**。

1. 添加 **[!UICONTROL Subject line]** 你送的。

   對於此處理，我們選擇不在 **[!UICONTROL Subject line]**。

   ![](assets/content_experiment_9.png)

1. 按一下 **[!UICONTROL Email designer]** 以進一步個性化處理B的交付（如果需要）。

一旦您的治療個性化，您就可以開始配置內容實驗。

## 配置內容實驗 {#configure-experiment}

1. 當兩個交貨都個性化時，從 **[!UICONTROL Edit content]** 窗口，選擇 **[!UICONTROL Configure content experiment]**。

   ![](assets/content_experiment_10.png)

1. 選擇要為實驗設定的目標。

   為了實驗，我們選擇 **[!UICONTROL Email open]** test：如果促銷代碼在主題行中，收件人將開啟其電子郵件。

   ![](assets/content_experiment_11.png)

1. 選擇以添加 **[!UICONTROL Holdout]** 組到您的交貨。 此組將不會從此市場活動接收任何內容。

   開啟切換欄將自動佔用人口的10%，如果需要，您可以調整此百分比。

   ![](assets/content_experiment_12.png)

1. 然後，您可以選擇為每個 **[!UICONTROL Treatment]** 或者乾脆開啟 **[!UICONTROL Distribute evenly]** 切換欄。

   ![](assets/content_experiment_13.png)

1. 按一下 **[!UICONTROL Save]** 的子菜單。

1. 內容實驗準備好後，可以按一下 **[!UICONTROL Review to activate]** 顯示市場活動的摘要。 如果任何參數不正確或缺少，則顯示警報。

   ![](assets/content_experiment_15.png)

1. 檢查市場活動配置是否正確，然後按一下 **[!UICONTROL Activate]** 啟動它。

   ![](assets/content_experiment_14.png)

## 試驗報告 {#experimentation-report}

![](assets/experimentation_report_3.png)

從您的活動 **[!UICONTROL Global report]**，也請參見Wiki頁。 **[!UICONTROL Experimentation]** 頁籤詳細列出與每個變型的執行方式以及在test期間是否存在最佳執行者相關的主要資訊。

有關此報告的更多詳細資訊，請參閱 [市場活動全局報表](../campaigns/content-experiment.md#experimentation-report) 的子菜單。

