---
solution: Journey Optimizer
product: journey optimizer
title: 新增個人化優惠方案
description: 瞭解如何向您的郵件添加個性化優惠
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 提供，決策，電子郵件，個性化，決策
exl-id: 1e648eca-b5ca-4767-b45d-c179243e347f
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 1%

---

# 新增個人化優惠方案 {#deliver-personalized-offers}

在 [!DNL Journey Optimizer] 電子郵件中，您可以插入將利用決策管理引擎的決策，以便選擇向客戶提供的最佳服務。

例如，您可以添加一個將在電子郵件中顯示特殊折扣優惠的決定，該折扣優惠會因收件人的忠誠度而有所不同。

>[!IMPORTANT]
>
>如果更改了在行程消息中使用的優惠決定，則需要取消發佈行程並重新發佈。  這將確保將更改納入旅程的消息，並確保消息與最新更新一致。

* 有關如何建立和管理產品的詳細資訊，請參閱 [此部分](../offers/get-started/starting-offer-decisioning.md)。
* 對於 **全端到端示例** 顯示如何配置優惠、在決策中使用優惠以及在電子郵件中利用此決策、簽出 [此部分](../offers/offers-e2e.md#insert-decision-in-email)。

➡️ [瞭解如何在此視頻中添加個性化服務](#video-offers)

## 在電子郵件中插入決定 {#insert-offers}

>[!CAUTION]
>
>開始前，必須 [定義聘用決定](../offers/offer-activities/create-offer-activities.md)。

要在電子郵件中插入決定，請執行以下步驟：

1. 建立電子郵件，然後開啟電子郵件設計器以配置其內容。

1. 添加 **[!UICONTROL 提供決定]** 內容元件。

   ![](assets/deliver-offer-component.png)

   瞭解如何在 [此部分](content-components.md)。

1. 的 **[!UICONTROL 提供決定]** 頁籤。 按一下 **[!UICONTROL 選擇優惠決定]**:

   1. 在顯示的窗口中，選擇與要顯示的優惠相對應的位置。

      [放置](../offers/offer-library/creating-placements.md) 是用來展示您優惠的容器。 在本示例中，我們將使用「電子郵件頂部影像」位置。 此位置已在「提供庫」中建立，以顯示位於消息頂部的影像類型提供。

   1. 與所選放置顯示匹配的決定。 選擇要在內容元件中使用的決定，然後按一下 **[!UICONTROL 添加]**。

      >[!NOTE]
      >
      >清單中只顯示與所選放置相容的決定。 在此示例中，只有一個服務活動與「電子郵件頂部影像」位置匹配。

      ![](assets/deliver-offer-placement.png)

現在，該決定已添加到元件中。 保存更改後，您的優惠隨時可以顯示到相關配置檔案中，以作為行程的一部分發送消息。

>[!NOTE]
>
>當您更新消息中直接或間接引用的聘用、回退聘用、聘用集合或聘用決定時，更新將自動反映在相應消息中。

## 通過電子郵件預覽優惠 {#preview-offers-in-email}

您可以使用 **[!UICONTROL 優惠]** 或內容元件箭頭。

![](assets/deliver-offer-preview.png)

要在客戶配置檔案中顯示作為決策一部分的不同優惠，請執行以下步驟。

>[!NOTE]
>
>您需要有test配置檔案才能預覽郵件。 瞭解如何 [建立test配置檔案](../segment/creating-test-profiles.md)。

1. 選擇用於預覽優惠的test配置檔案：

   1. 按一下 **[!UICONTROL 「模擬內容」按鈕]** 按鈕，然後選擇用於從 **[!UICONTROL 標識命名空間]** 的子菜單。

      >[!NOTE]
      >
      >在此示例中，我們使用 **電子郵件** 命名空間。 瞭解有關Adobe Experience Platform標識命名空間的詳細資訊 [此部分](../segment/get-started-identity.md)。

   1. 在 **[!UICONTROL 標識值]** 欄位中，輸入用於標識test配置檔案的值。 在此示例中，輸入test配置檔案的電子郵件地址。

   <!--For example enter smith@adobe.com and click the **[!UICONTROL Add profile]** button.-->

   1. 添加其他配置檔案，以便根據配置檔案資料test消息的不同變型。

      ![](assets/deliver-offer-test-profiles.png)


1. 按一下 **[!UICONTROL 預覽]** 頁籤test消息，然後選擇test配置檔案。 顯示與所選簡檔（女性）對應的要約。

   ![](assets/deliver-offer-test-profile-female-preview.png)

   您可以選擇其他test配置檔案來預覽郵件每個變體的電子郵件內容。 在消息內容中，現在顯示與所選test配置檔案（現在是人）相對應的服務。

瞭解有關詳細步驟的詳細資訊，以在中查看消息預覽 [此部分](#preview-your-messages)。

## 操作說明影片{#video-offers}

瞭解如何將決策管理元件添加到 [!DNL Journey Optimizer]。

>[!VIDEO](https://video.tv.adobe.com/v/334088?quality=12)
