---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用行銷活動
description: 深入了解 Journey Optimizer 的行銷活動
Feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: 行銷活動、如何進行、開始、最佳化程式
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 100%

---

# 開始使用行銷活動 {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="建立行銷活動"
>abstract="使用 **Adobe Journey Optimizer**，透過各種管道將一次性內容傳遞至特定對象。當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。"


>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="行銷活動"
>abstract="建立行銷活動以跨不同管道向特定對象提供一次性內容。建立行銷活動之前，請務必備妥管道表面 (即訊息預設集) 和 Adobe Experience Platform 對象以供使用。"

使用 Journey Optimizer 行銷活動，透過各種頻道將一次性內容傳遞至特定對象。 當使用歷程時，動作會依序執行。 透過行銷活動，可同時執行動作 (立即執行或根據指定的排程執行)。

您可建立兩種類型的行銷活動：

* **已排程的 Campaign**&#x200B;允許針對促銷優惠方案、參與行銷活動、公告、法律注意事項知或原則更新等行銷案例進行簡單的臨時批次通訊。
* **API 觸發的行銷活動**&#x200B;允許行銷通訊以在適當時間和對象聯絡，或允許與個人聯絡異動/操作訊息，如密碼重設，其中可能不僅需要使用設定檔屬性，還要使用其為 REST API 承載的觸發程序之中的即時內容資料，來進行個人化。

建立行銷活動的主要步驟如下：

![](assets/create-campaign-process.png)

➡️ [在影片中探索此功能](#video)

## 開始之前 {#campaign-prerequisites}

開始在 Journey Optimizer 建立第一個行銷活動之前，請先檢查下列必要條件：

1. **您需要適當的權限**。行銷活動僅適用於具有行銷活動相關&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;存取權的使用者，例如 Campaign 管理員、Campaign 核准者、Campaign 主管和/或 Campaign 檢視者。

   如果您無法存取行銷活動，則必須延長您的權限。 如果您有權存取貴組織的 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}，請依照下列步驟操作。否則請聯絡您的 Journey Optimizer 管理員。

   +++了解如何指派行銷活動權限

   若要將對應的&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;指派給使用者：

   1. 從 [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}，選取 [!DNL Adobe Experience Platform] 產品。

   1. 瀏覽至&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;索引標籤，選取與內建行銷活動相關的&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;之一：Campaign 管理員、Campaign 核准者、Campaign 經理或 Campaign 檢視者。

      深入了解 Journey Optimizer 行銷活動&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;及&#x200B;**[!UICONTROL 權限]**，[請參閱本頁面](../administration/ootb-product-profiles.md)。

      ![](assets/do-not-localize/admin_1.png)

   1. 按一下&#x200B;**[!UICONTROL 新增使用者]**，將選定的&#x200B;**[!UICONTROL 產品設定檔]**&#x200B;指派給您的使用者。

      ![](assets/do-not-localize/admin_2.png)

   1. 輸入您的使用者名稱、群組或電子郵件地址，然後按一下&#x200B;**[!UICONTROL 儲存]**。

   您的使用者現在可以存取&#x200B;**[!UICONTROL 行銷互動]**。

+++

1. **您需要對象**。建立行銷活動之前必須有可用的對象。 [在此頁面中](../audience/about-audiences.md)了解更多有關對象的資訊。
1. **需要管道表面**。若要選取管道，您必須建立相對應的管道表面 (即預設)，使其可供使用。[在本頁](../configuration/channel-surfaces.md)深入了解管道表面。

## 操作說明影片 {#video}

了解如何建立您的第一個行銷活動。

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
