---
solution: Journey Optimizer
product: journey optimizer
title: 發佈此歷程
description: 瞭解如何發佈歷程
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 發佈，歷程，即時，有效性，檢查
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
source-git-commit: 5bdacef2196592776c6b37708b0df0986460ca1f
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 41%

---

# 發佈您的歷程 {#publishing-the-journey}

若要啟用歷程並允許新設定檔進入歷程，您必須發佈歷程。 發佈可讓歷程上線且正常運作。 發佈之前，您必須確保歷程完整且有效，並修正任何錯誤，因為歷程包含錯誤時無法發佈。

➡️ [在影片中探索此功能](#video)

## 發佈程式 {#journey-publication}

發佈歷程的步驟詳述如下：

1. 發佈歷程之前，請確定歷程有效且沒有錯誤。 如果歷程包含任何錯誤，則無法發佈歷程。

   * 瞭解如何在[此頁面](testing-the-journey.md)上測試您的歷程。
   * 在[本節](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)中瞭解如何疑難排解您的歷程錯誤。

1. 若要發佈歷程，請按一下右上角下拉式功能表中的&#x200B;**[!UICONTROL 發佈]**&#x200B;選項。

   >[!NOTE]
   >
   > 如果您的歷程受限於核准政策，您必須先請求核准才能發佈。 [了解更多](../test-approve/gs-approval.md)


   ![](assets/journeyuc1_18.png)

發佈歷程時，它處於&#x200B;**唯讀**&#x200B;模式。 當歷程為唯讀時，您只能修改活動標籤和說明、歷程的名稱和歷程的說明。 如果您需要對已發佈的歷程進行更多修改，請建立歷程的[新版本](journey-ui.md#journey-versions)。

當您停止歷程時，其會永久停止：在歷程中流動的所有人員會永久停止，且歷程會停止允許新入口。 如果您需要再次執行歷程，必須複製歷程並發佈新歷程。


>[!IMPORTANT]
>
>如果對歷程訊息中使用的優惠決定進行變更，您需要取消發佈歷程並重新發佈。  這將確保將變更納入歷程的訊息中，並且該訊息與最新更新一致。


## 歷程版本 {#journey-versions}

在歷程清單中，所有歷程版本都會連同版本號碼一起顯示。當您搜尋歷程時，最新版本會在應用程式首次開啟時出現在清單頂端。然後，您可以定義所需的排序，應用程式會將其保留為使用者偏好設定。歷程的版本也會顯示在畫布上方的歷程版本介面頂端。

![](assets/journeyversions1.png)

>[!NOTE]
>
>通常，對於歷程的所有作用中版本，設定檔無法在同一歷程中同時出現多次。 如果啟用重新進入，輪廓可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。[閱讀全文](entry-management.md)。

### 建立歷程的新版本 {#journey-create-new-version}

如果您需要修改為即時歷程，請建立歷程的新版本。 若要建立現有歷程的新版本，請遵循下列步驟：

1. 開啟最新版本的即時歷程，按一下&#x200B;**[!UICONTROL 建立新版本]**&#x200B;並確認。

   ![](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下&#x200B;**[!UICONTROL 發佈]**&#x200B;並確認。

從發佈歷程的那一刻起，個人就會開始進入歷程的最新版本。 已進入舊版本的人會保留在舊版本中，直到歷程結束。如果他們稍後重新進入相同的歷程，則會進入最新版本。

歷程版本可個別停止。所有版本的歷程都有相同的名稱。

當您發佈歷程的新版本時，舊版本會自動結束並切換到&#x200B;**已關閉**&#x200B;狀態。歷程無法進入。即使您停止最新版本，先前版本仍會保持關閉狀態。


>[!NOTE]
>
>特定護欄和限制適用於歷程的版本設定。 請在[此頁面](../start/guardrails.md#journey-versions-journey-versions-g)了解更多。


## 作法影片 {#video}

透過此影片瞭解如何發佈歷程：

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)