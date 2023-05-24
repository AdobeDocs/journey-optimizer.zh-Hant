---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程
feature: Journeys
role: User
level: Beginner
keywords: 旅程，發現，開始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 28%

---


# 開始使用歷程{#jo-general-principle}

使用 [!DNL Journey Optimizer] 使用儲存在事件或資料源中的上下文資料構建即時業務流程使用案例。

設計由下列功能提供支援的多步驟進階案例：

* 傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用 Adobe Experience Platform 分段&#x200B;**批次**&#x200B;傳遞。

* 利用來自事件的&#x200B;**情境資料** 、來自 Adobe Experience Platform 的資訊，或來自協力廠商 API 服務的資料。

* 使用 **內置操作** 發送設計為 [!DNL Journey Optimizer] 建立 **自定義操作** 使用第三方系統發送消息。

* 使用&#x200B;**歷程設計器**，建立您的多步驟使用案例：輕鬆拖放登入事件或讀取區段活動、新增條件及傳送個人化訊息。


>[!NOTE]
>
>旅行護欄和限制在 [此頁](../start/guardrails.md)

## 建立行程的步驟{#steps-journey}

使用Adobe Journey Optimizer設計並協調單一畫布的個性化旅程。 建立行程的主要步驟如下：

![](assets/journey-creation-process.png)

Adobe Journey Optimizer包括一個人口協調佈景，使營銷人員能夠將營銷推廣與一對一的客戶參與協調起來。 用戶介面允許您輕鬆地將活動從調色板拖放到畫布中，以構建您的旅程。

![](assets/interface-journeys.png)

瞭解如何開始和建立您的第一次 [此頁](journey-gs.md)。

通道行程設計器幫助您構建多步行程，目標受眾、基於即時客戶或業務交互的更新，以及使用直觀的拖放介面的通道消息。

![](assets/journey38.png)

更多內容 [此部分](using-the-journey-designer.md)。

作為資料工程師，配置您的行程的步驟（包括資料源、事件和操作）在中詳細介紹 [此部分](../configuration/about-data-sources-events-actions.md)。


## 使用案例{#uc-journey}

瞭解如何在以下端到端使用案例中構建行程。

業務使用案例:

* [傳送多頻道訊息](journeys-uc.md)
* [使用 Campaign v7/v8 傳送訊息](ajo-ac.md)
* [傳送訊息給訂閱者](message-to-subscribers-uc.md)

技術使用案例:

* [使用自訂動作以動態方式傳遞集合](collections.md)
* [加快傳遞速度](ramp-up-deliveries-uc.md)
* [使用外部資料來源和自訂動作限制輸送量](limit-throughput.md)

## 歷程版本{#journey-versions}

在行程清單中，所有行程版本都以版本號顯示。 請參閱[此頁面](../building-journeys/using-the-journey-designer.md)。

搜索行程時，首次開啟應用程式時，最新版本會出現在清單頂部。 然後，您可以定義所需的排序，應用程式將將其保留為用戶首選項。 行程版本也顯示在行程版本介面的頂部，位於畫布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常而言，設定檔無法在同一歷程中同時出現多次。如果啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](end-journey.md)。

如果需要修改到即時行程，請建立新版本的行程。

1. 開啟您的即時旅程的最新版本，按一下 **[!UICONTROL 建立新版本]** 確認一下。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從旅程的最新版本建立新版本。

1. 進行修改，按一下 **[!UICONTROL 發佈]** 確認一下。

   ![](assets/journeyversions3.png)

從旅程發表那一刻起，個人就會開始流入旅程的最新版本。 已輸入先前版本的人會一直保留到完成旅程。 如果以後重新進入同一行程，他們將進入最新版。

行程版本可以單獨停止。 所有版本的旅程都具有相同名稱。

當您發佈新版本的行程時，舊版本將自動結束並切換到 **已關閉** 狀態。 這趟旅程不可能有入口。 即使您停止最新版本，舊版本也會保持關閉狀態。
