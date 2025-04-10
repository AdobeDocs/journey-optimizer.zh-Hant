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
source-git-commit: 1ee75284f3c5f0c7870e8bd8779d4daf9879aa40
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 48%

---

# 疑難排解您的歷程 {#troubleshooting}

在本節中，瞭解如何在測試或發佈之前疑難排解歷程。 下列所有檢查皆可在歷程處於測試模式或歷程為即時狀態時執行。建議您在測試模式中進行下列所有檢查，然後繼續發佈。在[此頁面](../building-journeys/testing-the-journey.md)上進一步瞭解測試模式。

作為管理員，您還可以直接從使用者介面發出真正的API呼叫，以測試自訂動作設定。 在[此頁面](../action/troubleshoot-custom-action.md)瞭解更多資訊。

## 請先檢查錯誤，然後再進行測試 {#checking-for-errors-before-testing}

在測試和發佈您的歷程之前，請先確認所有活動皆已正確設定。如果系統仍偵測到錯誤，則無法進行測試或發佈。


### 活動中的錯誤 {#activity-errors}

發生錯誤，而且畫布上的活動本身會顯示警告符號。將游標放在驚嘆號上，即可顯示錯誤訊息。如果您按一下活動，應該會看到錯誤的行並會顯示警告。例如：

* 如果必填欄位為空，則會顯示錯誤

  ![](assets/journey63.png)

* 在畫布中，當兩個活動中斷連線時，會顯示警告

  ![](assets/canvas-disconnected.png)

### 歷程中的錯誤 {#canvas-errors}

畫布上方的&#x200B;**[!UICONTROL 警示]**&#x200B;按鈕也會顯示錯誤。 此按鈕可讓您檢視系統偵測到的錯誤，這些錯誤會阻止測試模式啟動或歷程發佈。

系統偵測到兩種問題： **錯誤**&#x200B;和&#x200B;**警告**。 錯誤會封鎖發佈及測試啟動。警告指出未封鎖測試啟動或發佈的潛在問題。您會看到問題的說明，以及類型 ERR_XXX_XXX 的問題日誌 ID。這可協助識別問題。

![](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

與歷程相關的全域錯誤和警告會先出現在清單中。會依活動順序或外觀，由左至右地列出與特定活動相關的錯誤及警告。在警示清單底部，**[!UICONTROL 複製詳細資料]**&#x200B;按鈕可讓您複製有助於疑難排解問題的歷程相關技術資訊。

### 新增替代路徑 {#canvas-add-path}

您可以為下列歷程活動定義發生錯誤時的遞補動作： **[!UICONTROL 條件]**&#x200B;和&#x200B;**[!UICONTROL 動作]**。

當動作或條件發生錯誤時，個人的歷程就會停止。唯一能讓它繼續的方法是解決這個問題。 為避免中斷歷程，您還可以核取選項&#x200B;**[!UICONTROL 在逾時或活動屬性中的錯誤]**&#x200B;的情況下新增替代路徑。 請參閱[此章節](../building-journeys/using-the-journey-designer.md#paths)深入瞭解。


## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。如果您收到錯誤，則表示您的呼叫發生問題。再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。您可以諮詢管理員哪個是要點擊的正確 URL。

不會直接將事件從來源推送到歷程。 事實上，歷程依賴Adobe Experience Platform的串流獲取API。 因此，如果發生與事件相關的問題，您可以參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}，以疑難排解串流獲取API。

如果您的歷程無法啟用測試模式，錯誤為`ERR_MODEL_RULES_16`，請確定使用的事件包含使用通道動作時的[身分名稱空間](../audience/get-started-identity.md)。

身分名稱空間會用於唯一識別測試設定檔。 例如，如果使用電子郵件來識別測試設定檔，則應選取身分名稱空間&#x200B;**電子郵件**。 如果唯一識別碼是電話號碼，則應該選取識別名稱空間&#x200B;**電話**。

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

* [!DNL Journey Optimizer]已正確考慮傳送郵件的要求。 業務使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer]已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可以檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。
