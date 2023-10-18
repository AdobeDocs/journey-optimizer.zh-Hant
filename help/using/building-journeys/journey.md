---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程
feature: Journeys, Get Started, Overview
role: User
level: Beginner, Intermediate
keywords: 歷程，探索，開始
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 27%

---


# 開始使用歷程{#jo-general-principle}

使用 [!DNL Journey Optimizer] 可讓您善用儲存在事件或資料來源中的內容資料，建置即時協調流程使用案例。

設計由下列功能提供支援的多步驟進階案例：

* 傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用 Adobe Experience Platform 對象&#x200B;**批次**&#x200B;傳遞。

* 利用來自事件的&#x200B;**情境資料** 、來自 Adobe Experience Platform 的資訊，或來自協力廠商 API 服務的資料。

* 使用 **內建動作** 傳送設計的訊息： [!DNL Journey Optimizer] 或建立 **自訂動作** 如果您使用協力廠商系統來傳送訊息。

* 使用&#x200B;**歷程設計工具**，建置多步驟使用案例：輕鬆拖放進入事件或讀取對象活動、新增條件及傳送個人化訊息。


>[!NOTE]
>
>中詳細說明了歷程護欄和限制 [此頁面](../start/guardrails.md)

## 建立歷程的步驟{#steps-journey}

使用Adobe Journey Optimizer從單一畫布設計及編排個人化歷程。 建立歷程的主要步驟如下：

![](assets/journey-creation-process.png)

Adobe Journey Optimizer包含全通路協調畫布，可讓行銷人員協調行銷外聯活動與一對一客戶參與。 使用者介面可讓您輕鬆將活動從浮動視窗拖放至畫布，以建立您的歷程。

![](assets/interface-journeys.png)

瞭解如何開始並建立您的第一個歷程 [此頁面](journey-gs.md).

全頻道歷程設計器可協助您使用直覺式的拖放介面，透過目標受眾建立多步驟歷程、根據即時客戶或業務互動進行更新，以及全頻道訊息。

![](assets/journey38.png)

詳細內容： [本節](using-the-journey-designer.md).

身為資料工程師，設定歷程（包括資料來源、事件和動作）的步驟已詳細說明，請參閱 [本節](../configuration/about-data-sources-events-actions.md).


## 使用案例{#uc-journey}

瞭解如何在下列端對端使用案例中建立歷程。

業務使用案例:

* [傳送多頻道訊息](journeys-uc.md)
* [使用 Campaign v7/v8 傳送訊息](ajo-ac.md)
* [傳送訊息給訂閱者](message-to-subscribers-uc.md)

技術使用案例:

* [使用自訂動作以動態方式傳遞集合](collections.md)
* [加快傳遞速度](ramp-up-deliveries-uc.md)
* [使用外部資料來源和自訂動作限制輸送量](limit-throughput.md)

## 歷程版本{#journey-versions}

在歷程清單中，所有歷程版本都會連同版本號碼一起顯示。 請參閱[此頁面](../building-journeys/using-the-journey-designer.md)。

當您搜尋歷程時，最新版本會在應用程式首次開啟時出現在清單頂端。 然後，您可以定義所需的排序，應用程式會將其保留為使用者偏好設定。 歷程的版本也會顯示在畫布上方的歷程版本介面頂端。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常而言，設定檔無法在同一歷程中同時出現多次。如果啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](end-journey.md)。

如果您需要修改為即時歷程，請建立歷程的新版本。

1. 開啟最新版本的即時歷程，按一下 **[!UICONTROL 建立新版本]** 並確認。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下 **[!UICONTROL 發佈]** 並確認。

   ![](assets/journeyversions3.png)

從發佈歷程的那一刻起，個人就會開始進入歷程的最新版本。 已輸入舊版的人會保留在舊版中，直到歷程結束。 如果他們稍後重新進入相同的歷程，則會進入最新版本。

歷程版本可個別停止。 所有版本的歷程都有相同的名稱。

當您發佈新版本的歷程時，會自動結束舊版本並切換至 **已關閉** 狀態。 歷程中無法進入。 即使您停止最新版本，先前版本仍會保持關閉狀態。
