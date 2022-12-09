---
solution: Journey Optimizer
product: journey optimizer
title: 歷程疑難排解
description: 了解如何疑難排解歷程中的錯誤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---

# 疑難排解您的歷程{#troubleshooting}

在本節中，您會了解如何先疑難排解歷程，再進行測試或發佈。 下列所有檢查皆可在歷程處於測試模式或歷程為即時狀態時執行。 建議您在測試模式中進行下列所有檢查，然後繼續發佈。 請參閱 [本頁](../building-journeys/testing-the-journey.md).

## 測試前檢查錯誤{#checking-for-errors-before-testing}

在測試和發佈您的歷程之前，請確認所有活動皆已正確設定。 如果系統仍檢測到錯誤，則無法執行測試或發佈。

出現錯誤，畫布上的活動本身會顯示警告符號。 將游標放在驚嘆號上以顯示錯誤訊息。 如果按一下活動，應該會看到錯誤的行並出現警告。 例如，如果必填欄位空白，則會顯示錯誤。

![](assets/journey63.png)

例如，在畫布中，當兩個活動中斷連線時，會顯示警告。

![](assets/canvas-disconnected.png)

在 **[!UICONTROL Test]** 切換和 **[!UICONTROL Publish]** 按鈕，將顯示警告標誌。 此警告符號會顯示系統偵測到的錯誤，並防止測試模式啟動或歷程發佈。 大多數情況下，系統偵測到的錯誤會連結至活動上可見的錯誤，但有時會連結至其他問題。 在此情況下，您可以顯示問題，嘗試識別用於錯誤說明的問題。 如果您無法識別問題，則可以複製詳細資訊並傳送給管理員或支援。 請注意，封鎖測試的錯誤和封鎖發佈的錯誤類似。

系統偵測到兩種問題：錯誤和警告。 錯誤會封鎖發佈並測試啟動。 警告指出未封鎖測試啟動或發佈的潛在問題。 您會看到問題的說明，以及類型ERR_XXX_XXX的問題日誌ID。 這將有助於技術支援人員識別問題。

在 **[!UICONTROL Test]** 切換和 **[!UICONTROL Publish]** 按鈕。 出現錯誤時，符號會以紅色顯示。 若出現警告，則會顯示為橘色。

![](assets/journey75.png)

與歷程相關的全域錯誤和警告會先出現在清單中。 會依活動順序或外觀，從左到右列出與特定活動相關的錯誤和警告。 此 **[!UICONTROL Copy details]** 按鈕會複製支援團隊可用於疑難排解之歷程的相關技術資訊。

當動作或條件中發生錯誤時，個人的歷程就會停止。 唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL Add an alternative path in case of a timeout or an error]**. 請參閱 [本節](../building-journeys/using-the-journey-designer.md#paths).

## 檢查是否已正確傳送事件{#checking-that-events-are-properly-sent}

歷程的起點永遠是事件。 您可以使用Postman等工具執行測試。

您可以檢查您透過這些工具傳送的API呼叫是否正確傳送。 如果您收到錯誤，表示您的呼叫有問題。 再次檢查裝載、標題（尤其是組織ID）和目的地URL。 您可以詢問管理員要點擊的正確URL為何。

事件不會直接從來源推播至歷程。 事實上，歷程需仰賴Adobe Experience Platform的串流獲取API。 因此，若發生事件相關問題，您可以參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}，以疑難排解串流獲取API。

## 檢查是否有人進入歷程{#checking-if-people-enter-the-journey}

歷程報告會即時測量歷程中的人員入口。

如果您成功傳送活動，但在歷程中看不到任何入口，表示活動傳送與歷程中的活動接收之間發生錯誤。

以下是管理員應檢查的一些事項：

* 您確定您預期傳入事件的歷程處於測試模式或即時狀態？
* 在從有效負載預覽複製有效負載之前，您是否已儲存事件？
* 您的事件裝載是否包含事件ID?
* 您是否點擊了正確的URL?
* 您是否使用事件設定窗格中的裝載結構預覽，按照串流獲取API裝載結構操作？ 請參閱 [本頁](../event/about-creating.md#preview-the-payload).
* 您在事件標題中是否使用正確的索引鍵值配對？

   ```
   X-gw-ims-org-id - your organization's ID
   Content-type - application/json
   ```

## 檢查人們如何導覽歷程{#checking-how-people-navigate-through-the-journey}

歷程報告會衡量歷程中個人的進度。 很容易識別人員停止的位置和原因。

以下是一些要檢查的事項：

* 是否是因為某個條件排除了此人？ 例如，條件是「性別=男性」，而人是女性。 如果條件不太複雜，則業務使用者可以執行此檢查。
* 是否是因為呼叫資料來源未回應？ 當歷程處於測試模式時，可在測試模式記錄中看到此資訊。 當歷程為即時狀態時，管理員可測試對資料來源的直接呼叫，並檢查收到的答案。 管理員也可以複製歷程並加以測試。

## 檢查是否成功發送消息{#checking-that-messages-are-sent-successfully}

如果個人在歷程中以正確的方式流動，但未收到應該收到的訊息，您可以檢查：

* [!DNL Journey Optimizer] 已正確考慮傳送訊息的要求。 商務使用者可存取應傳送的訊息，並檢查最新執行時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer] 已成功發送消息。 檢查歷程報表，確認沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。
