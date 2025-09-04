---
solution: Journey Optimizer
product: journey optimizer
title: 疑難排解您的即時歷程執行
description: 瞭解如何疑難排解即時歷程執行中的錯誤
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 疑難排解，疑難排解，歷程，檢查，錯誤
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 36%

---

# 疑難排解您的即時歷程執行 {#troubleshooting-execution}

在本節中，瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何導覽歷程，以及是否傳送訊息。

您也可以在測試或發佈歷程之前疑難排解錯誤。 在此頁面[上瞭解如何](troubleshooting.md)。

如果您使用輸入動作，請在此頁面[瞭解如何疑難排解](troubleshooting-inbound.md)。

## 檢查是否已正確傳送事件 {#checking-that-events-are-properly-sent}

歷程的起點永遠是一個事件。您可以使用 Postman 等工具執行測試。

您可以檢查您透過這些工具傳送的 API 呼叫是否都已正確傳送。如果您收到錯誤，則表示您的呼叫發生問題。再次檢查有效負載、標題（特別是組織 Id）和目的地 URL。您可以諮詢管理員哪個是要點擊的正確 URL。

不會直接將事件從來源推送到歷程。 事實上，歷程依賴Adobe Experience Platform的串流獲取API。 因此，如果發生與事件相關的問題，您可以參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target="_blank"}，以疑難排解串流獲取API。

如果您的歷程無法啟用測試模式，錯誤為`ERR_MODEL_RULES_16`，請確定使用的事件包含使用通道動作時的[身分名稱空間](../audience/get-started-identity.md)。

身分名稱空間會用於唯一識別測試設定檔。 例如，如果使用電子郵件來識別測試設定檔，則應選取身分名稱空間&#x200B;**電子郵件**。 如果唯一識別碼是電話號碼，則應該選取識別名稱空間&#x200B;**電話**。

## 檢查是否有人進入歷程 {#checking-if-people-enter-the-journey}

歷程報告會即時衡量歷程中的人員入口。

如果您成功傳送事件，但未看到有人進入歷程，則表示在事件傳送與事件接收之間發生錯誤。

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

如果個人在歷程中的進度正常，但沒有收到應接收的訊息，您可以檢查：

* [!DNL Journey Optimizer]已正確考慮傳送郵件的要求。 業務使用者可以存取應傳送的訊息，並檢查最新執行的時間是否與歷程的執行時間對應。 他們也可以檢查收到的最新API呼叫/事件。
* [!DNL Journey Optimizer]已成功傳送訊息。 檢查歷程報告以確定沒有錯誤。

若是透過自訂動作傳送訊息，在歷程測試期間唯一可以檢查的事項，就是自訂動作系統的呼叫是否會導致錯誤。 如果呼叫與自訂動作相關聯的外部系統並未導致錯誤，但並未導致訊息傳送，則應在外部系統端進行一些調查。
