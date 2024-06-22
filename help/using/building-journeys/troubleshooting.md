---
solution: Journey Optimizer
product: journey optimizer
title: 歷程疑難排解
description: 瞭解如何疑難排解歷程中的錯誤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 疑難排解，疑難排解，歷程，檢查，錯誤
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 135dd7528e87a6fde7e148745ef2f49104809bc1
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 63%

---

# 疑難排解您的歷程 {#troubleshooting}

在本節中，瞭解如何在測試或發佈之前疑難排解歷程。 下列所有檢查皆可在歷程處於測試模式或歷程為即時狀態時執行。建議您在測試模式中進行下列所有檢查，然後繼續發佈。請參閱[此頁面](../building-journeys/testing-the-journey.md)。

## 請先檢查錯誤，然後再進行測試 {#checking-for-errors-before-testing}

在測試和發佈您的歷程之前，請先確認所有活動皆已正確設定。如果系統仍偵測到錯誤，則無法進行測試或發佈。

發生錯誤，而且畫布上的活動本身會顯示警告符號。將游標放在驚嘆號上，即可顯示錯誤訊息。如果您按一下活動，應該會看到錯誤的行並會顯示警告。例如，如果強制欄位為空，則會顯示錯誤。

![](assets/journey63.png)

例如，在畫布中，當兩個活動中斷連線時，則會顯示警告。

![](assets/canvas-disconnected.png)

在 **[!UICONTROL 測試]** 切換及 **[!UICONTROL 發佈]** 按鈕時，會顯示警告符號。 此警告符號會顯示系統偵測到的錯誤，而且可防止測試模式啟動或歷程發佈。在大多數情況下，系統偵測到的錯誤會連結到活動上的可見錯誤，但有時候會連結到其他問題。在這種情況下，您可以顯示這些問題，嘗試識別用於說明錯誤的問題。如果您無法識別問題，可以複製詳細資料並傳送給管理員或支援人員。 請注意，會封鎖測試的錯誤和封鎖發佈的錯誤是類似的。

系統偵測到兩種問題：錯誤及警告。錯誤會封鎖發佈及測試啟動。警告指出未封鎖測試啟動或發佈的潛在問題。您會看到問題的說明，以及類型 ERR_XXX_XXX 的問題日誌 ID。這將有助於技術支援人員找出問題。

兩種不同的顏色可以顯示在旁邊的符號上 **[!UICONTROL 測試]** 切換及 **[!UICONTROL 發佈]** 按鈕。 出現錯誤時，符號會以紅色顯示。若出現警告，則會顯示為橘色。

![](assets/journey75.png)

與歷程相關的全域錯誤和警告會先出現在清單中。會依活動順序或外觀，由左至右地列出與特定活動相關的錯誤及警告。此 **[!UICONTROL 複製詳細資料]** 按鈕會複製支援團隊可用於疑難排解的歷程相關技術資訊。

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法就是勾選方塊 **[!UICONTROL 在逾時或錯誤的情況下新增替代路徑]**. 請參閱[本節](../building-journeys/using-the-journey-designer.md#paths)。

## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。如果您收到錯誤，則表示您的呼叫發生問題。再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。您可以諮詢管理員哪個是要點擊的正確 URL。

不會直接將事件從來源推送到歷程。 事實上，歷程依賴Adobe Experience Platform的串流獲取API。 因此，若發生事件相關問題，您可以參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"} 適用於串流獲取API的疑難排解。

## 檢查是否有人進入歷程 {#checking-if-people-enter-the-journey}

歷程報告會即時衡量歷程中的人員入口。

如果您成功傳送活動，但在歷程中看不到任何入口，則表示在活動傳送以及在歷程中的事件接收之間發生錯誤。

您可以透過下列問題開始進行疑難排解：

* 您確定您預期會發生傳入事件的歷程處於測試模式或是即時狀態？
* 在從有效負載預覽複製有效負載之前，您是否已儲存事件？
* 您的事件有效負載是否包含事件 ID？
* 您是否點按了正確的 URL？
* 您是否依照串流獲取 API 有效負載結構，而在事件設定窗格中使用有效負載結構預覽？請參閱[此頁面](../event/about-creating.md#preview-the-payload)。
* 您在事件標題中是否使用正確的機碼值組？

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

## 檢查人們如何導覽歷程 {#checking-how-people-navigate-through-the-journey}

歷程報告會衡量歷程中個人的進度。 可輕鬆識別人員停止的位置及原因。

以下是一些要檢查的事項：

* 是否是因為某個條件排除此人？例如，條件是 &quot;gender = male&quot;，但人員是女性。如果條件並非太複雜，則可由業務使用者執行此檢查。
* 是否是因為呼叫資料來源未回應？當歷程處於測試模式時，可在測試模式日誌中看到此資訊。當歷程為即時狀態時，管理員可測試直接呼叫資料來源並檢查收到的答案。管理員也可以複製歷程並進行測試。

## 檢查訊息是否成功傳送 {#checking-that-messages-are-sent-successfully}

如果個人在歷程中的進度正常，但並未收到應接收的訊息，您可以檢查：

* [!DNL Journey Optimizer] 已正確考量傳送訊息的要求。 業務使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer] 已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可以檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。
