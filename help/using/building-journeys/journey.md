---
solution: Journey Optimizer
product: journey optimizer
title: 開始使用歷程
description: 開始使用歷程
feature: Journeys
role: User
level: Beginner
exl-id: 73cfd48b-72e6-4b72-bbdf-700a32a34bda
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 26%

---


# 開始使用歷程{#jo-general-principle}

使用 [!DNL Journey Optimizer] 使用儲存在事件或資料來源中的內容資料，建立即時協調使用案例。

設計由下列功能提供支援的多步驟進階案例：

* 傳送在收到事件時觸發的即時&#x200B;**單一傳遞**，或使用 Adobe Experience Platform 分段&#x200B;**批次**&#x200B;傳遞。

* 利用來自事件的&#x200B;**情境資料** 、來自 Adobe Experience Platform 的資訊，或來自協力廠商 API 服務的資料。

* 使用 **內建動作** 發送設計在 [!DNL Journey Optimizer] 或建立 **自訂動作** 如果您使用協力廠商系統來傳送訊息。

* 使用&#x200B;**歷程設計器**，建立您的多步驟使用案例：輕鬆拖放登入事件或讀取區段活動、新增條件及傳送個人化訊息。

## 建立歷程的步驟{#steps-journey}

使用Adobe Journey Optimizer來設計和協調從單一畫布的個人化歷程。

Adobe Journey Optimizer包含全通路協調畫布，可讓行銷人員協調行銷外展與一對一客戶互動。 使用者介面可讓您輕鬆將活動從浮動視窗拖放至畫布中，以建立您的歷程。

![](assets/interface-journeys.png)

了解如何在 [本頁](journey-gs.md).

全通路歷程設計程式可協助您使用直覺式的拖放介面，以鎖定目標對象、根據即時客戶或業務互動進行更新，以及全通路訊息來建立多步驟歷程。

![](assets/journey38.png)

深入了解 [本節](using-the-journey-designer.md).

身為資料工程師，設定歷程的步驟（包括資料來源、事件和動作）在 [本節](../configuration/about-data-sources-events-actions.md).


## 使用案例{#uc-journey}

了解如何在下列端對端使用案例中建立歷程。

業務使用案例:

* [傳送多頻道訊息](journeys-uc.md)
* [使用 Campaign v7/v8 傳送訊息](ajo-ac.md)
* [傳送訊息給訂閱者](message-to-subscribers-uc.md)

技術使用案例:

* [使用自訂動作以動態方式傳遞集合](collections.md)
* [加快傳遞速度](ramp-up-deliveries-uc.md)
* [使用外部資料來源和自訂動作限制輸送量](limit-throughput.md)

## 歷程版本{#journey-versions}

在歷程清單中，所有歷程版本都會以版本號碼顯示。 請參閱[此頁面](../building-journeys/using-the-journey-designer.md)。

當您搜尋歷程時，最新版本會在首次開啟應用程式時出現在清單頂端。 然後，您可以定義所要的排序，而應用程式會將其保留為使用者偏好設定。 歷程的版本也會顯示在歷程版本介面的頂端、畫布上方。

![](assets/journeyversions1.png)

>[!NOTE]
>
>一個設定檔通常無法在同一歷程中同時出現多次。 如果啟用重新進入，設定檔可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](end-journey.md)。

如果您需要修改至即時歷程，請建立新版本的歷程。

1. 開啟您最新版的即時歷程，按一下 **[!UICONTROL 建立新版本]** 並確認。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下 **[!UICONTROL 發佈]** 並確認。

   ![](assets/journeyversions3.png)

從歷程發佈之時，個人就會開始進入歷程的最新版本。 已輸入舊版的使用者會保留在舊版中，直到完成歷程為止。 如果他們稍後重新進入相同的歷程，將會進入最新版本。

歷程版本可個別停止。 所有版本的歷程都具有相同名稱。

當您發佈新版本的歷程時，舊版會自動結束，並切換至 **已關閉** 狀態。 旅行中的入口是不可能的。 即使您停止最新版本，舊版仍會保持關閉狀態。

>[!NOTE]
>
>進一步了解歷程版本護欄和限制，位於 [本頁](../start/guardrails.md#journey-versions-limitations)