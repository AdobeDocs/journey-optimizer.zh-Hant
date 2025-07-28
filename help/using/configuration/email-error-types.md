---
solution: Journey Optimizer
product: journey optimizer
title: 電子郵件錯誤型別
description: 使用Journey Optimizer傳送傳遞內容時，存取所有可能的電子郵件錯誤清單。
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 重試，退回，軟，已忽略，硬，最佳化器，錯誤
hide: true
hidefromtoc: true
source-git-commit: 817f7c88bfc2b40a7ce39575b4ad02fb372d429d
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 10%

---


# 電子郵件錯誤型別 {#email-error-types}

傳送失敗的可能原因有多種。 下表詳細說明傳送包含[!DNL Journey Optimizer]的電子郵件傳遞時可能發生的所有錯誤，以及其說明和錯誤型別。

這些錯誤可在[AJO訊息回饋事件資料集](../data/datasets-query-examples.md#message-feedback-event-dataset)中找到，此資料集包含訊息傳遞記錄，包括來自[!DNL Journey Optimizer]的所有訊息傳遞資訊，以及來自電子郵件ISP的回饋記錄（退信）。

| 錯誤標籤 | 錯誤型別 | 技術值 | 說明 |
| --- | --- | --- | --- |
| **未決定** | 已忽略 | 1 | 無法分類從ISP接收的SMTP退回訊息。 |
| **無效的收件者** | 硬退回 | 10 | 收件者的地址無效。 |
| **收件者已拒絕** | 硬退回 | 15 | 收件者的ISP已拒絕訊息，如果未抑制收件者，ISP可能會封鎖寄件者。 |
| **軟退信** | 軟退回 | 20 | 訊息發生暫時性失敗。 在未來的重試中可能會成功。 |
| **DNS失敗** | 軟退回 | 21 | 郵件傳遞發生暫時性DNS失敗。 在未來的重試中可能會成功。 |
| **郵箱已滿** | 軟退回 | 22 | 收件者的信箱已滿，郵件發生暫時傳遞失敗。 |
| **太大** | 已忽略 | 23 | 郵件發生暫時傳遞失敗，因為郵件大小超過收件者的限制。 |
| **逾時** | 已忽略 | 24 | 訊息傳遞失敗，可能是因為訊息有效性過期，或是傳送給ISP所花的時間太長。 |
| **管理失敗** | 管理 | 25 | 由於電子郵件傳送基礎結構中的某些原則設定，傳遞失敗。 |
| **一般退回：沒有RCPT** | 已忽略 | 30 | 無法傳遞郵件，因為未識別收件者。 |
| **一般退回** | 已忽略 | 40 | 訊息由於未指定的原因發生暫時傳送失敗。 |
| **郵件區塊** | 已忽略 | 50 | 由於ISP的高容量或速率限制，傳遞遇到暫時性失敗。 |
| **垃圾郵件區塊** | 已忽略 | 51 | 傳遞遇到暫時性失敗，因為ISP將寄件者的網域或IP視為已知的垃圾郵件來源。 |
| **垃圾郵件內容** | 已忽略 | 52 | 由於ISP將電子郵件內容分類為垃圾訊息，因此傳遞遇到暫時性失敗。 |
| **拒絕轉送** | 軟退回 | 54 | 無法接受此訊息，因為目的地網域未被列入允許轉送清單。 |
| **自動回覆** | 已忽略 | 60 | 除非啟用轉寄，否則接收時[!DNL Journey Optimizer]會捨棄這些郵件。 |
| **暫時性失敗** | 已忽略 | 70 | 傳遞將以節流率重試，或可能在暫停時延遲。 |
| **挑戰 — 回應** | 軟退回 | 100 | 傳遞可能會永久失敗，因為[!DNL Journey Optimizer]不支援挑戰 — 回應驗證機制。 |
