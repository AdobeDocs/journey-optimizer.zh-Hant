---
title: 重試次數
description: 瞭解在將地址發送到禁止顯示清單之前如何執行重試
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# 重試次數 {#retries}

當電子郵件由於臨時原因而失敗時 **軟彈跳** 錯誤，執行多次重試。 每個錯誤都會增加一個錯誤計數器。 當此計數器達到限制閾值時，地址將添加到禁止清單。

>[!NOTE]
>
>瞭解有關中錯誤類型的詳細資訊 [傳遞失敗類型](../reports/suppression-list.md#delivery-failures) 的子菜單。

在預設配置中，閾值設定為5個錯誤。

* 對於同一交貨，在第五個交貨時 [重試時間](#retry-duration)，地址將被隱藏。

* 如果存在不同的遞送並且至少24小時之外出現兩個錯誤，則每次錯誤時誤差計數器遞增，並且在第五次嘗試時地址也被抑制。

如果重試後傳遞成功，則重新初始化地址的錯誤計數器。

如果預設值5不適合您的需要，則可以按照以下步驟修改錯誤閾值。

1. 前往 **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Suppression list]**。

1. 選取 **[!UICONTROL Edit suppression rules]** 按鈕。

   ![](assets/suppression-list-edit-retries.png)

1. 根據需要編輯允許的連續軟邊界數。

   ![](assets/suppression-list-edit-soft-bounces.png)

   必須輸入介於1和20之間的整數值，這意味著最小重試次數為1，最大重試次數為20。

   >[!CAUTION]
   >
   >超過10的任何值都可能導致交付能力信譽問題，以及ISP的IP限制或阻止清單。 [瞭解有關可交付性的更多資訊](../reports/deliverability.md)

## 重試時段 {#retry-duration}

的 **重試時間** 是重試傳遞中遇到臨時錯誤或軟彈回的任何電子郵件的時間段。

預設情況下，將為 **3.5天** 或 **84小時**)。

但是，為了確保不再需要重試嘗試時不再執行，可以在建立或編輯時根據需要更改此設定 [消息預設](message-presets.md) 應用到電子郵件通道。

例如，對於與密碼重置相關的事務性電子郵件，您可以將重試週期設定為24小時，並且包含僅有效一天的連結。 同樣，對於午夜銷售，您可能需要定義6小時的重試期。

>[!NOTE]
>
>重試期限不能超過84小時。 市場營銷電子郵件的最小重試時間為6小時，事務性電子郵件的重試時間為10分鐘。

瞭解如何在中建立郵件預設時調整電子郵件重試參數 [此部分](message-presets.md#create-message-preset)。

