---
solution: Journey Optimizer
product: journey optimizer
title: 暫停歷程
description: 瞭解如何暫停並繼續即時歷程
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="可用性限制" type="Informative"
keywords: 發佈，歷程，即時，有效性，檢查
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 3%

---

# 暫停歷程 {#journey-pause}

您可以隨時暫停即時歷程、執行所有需要的變更，然後再次繼續。 歷程最多可暫停14天。 您可以選擇歷程是否在暫停期間結束時繼續，或者歷程是否完全停止。


>[!AVAILABILITY]
>
>此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。


## 主要優點 {#journey-dry-run-benefits}

暫停和繼續歷程可讓行銷人員在不中斷客戶體驗的情況下暫時暫停即時歷程，以提供更優異的控制力和彈性。 暫停時，不會傳送任何通訊，而且設定檔會維持在暫停狀態，直到歷程繼續為止。

此功能減少在錯誤或更新期間（例如：變更訊息內容）傳送意外訊息的風險，支援更安全的歷程管理，並提高從業人員的信心。 直接在UI中檢視暫停的歷程及其狀態，可進一步增強透明度和作業靈敏度。

>[!CAUTION]
>
>暫停和恢復歷程的許可權僅限於具有&#x200B;**[!DNL Publish journeys]**&#x200B;高階許可權的使用者。 在[本節](../administration/permissions-overview.md)中進一步瞭解如何管理[!DNL Journey Optimizer]使用者的存取權。

## 護欄和推薦

* 歷程版本最多可暫停14天。
* 暫停的歷程會以即時方式納入所有商業規則中。
* 設定檔到達動作活動時，會在暫停的歷程中「捨棄」。 如果他們在歷程暫停期間堅持等待，並在恢復時退出，則會繼續歷程且不會被捨棄。
* 即使暫停後，隨著事件繼續處理，這些事件也會計為5ktps配額，之後節流會成為單一專案。
* 已進入歷程但在暫停期間被捨棄的設定檔，仍會計為可參與的設定檔。
* 當設定檔在暫停的歷程中保留時，在繼續時會重新整理設定檔屬性
* 條件仍會在暫停的歷程中執行，因此如果歷程因資料品質問題而暫停，則可以使用錯誤的資料評估動作節點之前的任何條件。
* 對於以增量閱聽眾為基礎的讀取閱聽眾歷程，會考慮暫停的持續時間。 例如，對於每日歷程，如果它在2日暫停並在當月5日繼續，則6日的執行將接管從1日到6日符合資格的所有設定檔。 對象資格或事件型歷程則非如此（如果在暫停期間收到對象資格或事件，則會捨棄這些事件）。
* 暫停的歷程計入即時歷程配額。
* 歷程全域逾時仍適用於暫停的歷程。 例如，如果設定檔處於歷程中90天且歷程已暫停，則此設定檔仍將在第91天結束歷程。
* 歷程繼續時，有新的&#x200B;**繼續**&#x200B;歷程狀態可用。 當您按一下&#x200B;**繼續**&#x200B;時，它會再次開始聆聽歷程事件。  歷程中的設定檔延遲一段時間，無法繼續。 當歷程從&#x200B;**繼續**&#x200B;到&#x200B;**即時**，這表示所有設定檔都已繼續。 因此，**繼續**&#x200B;可能需要一些時間。
* 如果設定檔保留在歷程中，而且此歷程在XX天后自動繼續，則設定檔會繼續歷程且不會捨棄。 如果您想要刪除它們，您必須手動繼續歷程。
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## 如何暫停歷程 {#journey-pause-steps}

您可以暫停任何即時歷程。

若要暫停您的歷程，請依照下列步驟進行：

1. 開啟您要暫停的歷程。
1. 按一下歷程畫布右上角的&#x200B;**...更多**&#x200B;按鈕，然後選取&#x200B;**暫停**。

   ![暫停歷程按鈕](assets/pause-journey-button.png)

1. 選取如何管理目前位於歷程中的設定檔。

   ![暫停歷程選項](assets/pause-confirm.png){width="50%" align="left"}

   您可以：

   * 保留設定檔
   * 捨棄設定檔

1. 按一下&#x200B;**暫停**&#x200B;按鈕確認。

歷程最多可暫停14天。

## 如何繼續暫停的歷程 {#journey-resume-steps}

暫停的歷程可以隨時手動繼續。

若要繼續歷程，請遵循下列步驟：

1. 開啟您要繼續的歷程。
1. 按一下歷程畫布右上角的&#x200B;**...更多**&#x200B;按鈕，然後選取&#x200B;**繼續**。




