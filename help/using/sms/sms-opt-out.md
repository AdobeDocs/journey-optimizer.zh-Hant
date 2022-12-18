---
solution: Journey Optimizer
product: journey optimizer
title: 簡訊選擇退出管理
description: 了解如何使用SMS訊息管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 96%

---

# 簡訊選擇退出管理 {#sms-opt-out}

根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [深入了解隱私權和選擇退出管理](../privacy/opt-out.md)

預設情況下，Adobe Journey Optimizer 會根據 Sinch 和 Twilio 等原生整合的行業標準，處理 STOP、UNSTOP 和 START 等標準英文回覆訊息，以實現免付費和長程式碼訊息。 這些關鍵字通常會觸發您協力廠商提供者 (例如 Twilio、Sinch 等) 的自動標準回覆。 您可以直接向提供者或透過其文件網站確認。

無需任何步驟，即可確保 SMS 選擇退出功能在 Adobe Journey Optimizer 中運作，因為關鍵字回應 STOP、UNSTOP 和 START 將會自動識別。

除了 Adobe Journey Optimizer 根據選擇退出狀態 (用於與 Twilio 或 Sinch 直接整合) 停止傳送外，大部分的 SMS 閘道提供者也會維護封鎖清單，確保 SMS 訊息不會傳送給已選擇退出的個人。 如果您使用 Sinch 或 Twilio 以外的提供者，並透過[自訂頻道](../building-journeys/using-custom-actions.md)傳送 SMS，您需要向提供者確認。

>[!IMPORTANT]
>
>文字訊息行銷活動可能會受到各種法律法規遵循要求的約束，具體取決於您的文字訊息行銷活動的性質、您傳送訊息的位置，以及收件者的位置。 <br>雖然 Adobe Journey Optimizer 會處理上述長程式碼和免付費號碼的訊息，但您應諮詢法律顧問，以確保您的文字訊息傳送行銷活動符合所有適用的法律規範要求。

## 短程式碼 {#short-codes}

預設情況下，Adobe Journey Optimizer 不會處理短程式碼的選擇退出、選擇加入或說明關鍵字。

您必須確保您的短程式碼符合選擇退出處理的所有產業規則和法規。

## 英數字元寄件者 ID {#alphanumeric}

英數字元寄件者 ID 僅用於單向傳訊，無法接收傳入訊息。 因此，Adobe Journey Optimizer 的 SMS STOP、START、HELP 關鍵字不適用於 Alpha 傳送者 ID。 您必須提供其他指示，如寫入支援團隊、呼叫支援電話熱線或傳送文字訊息給其他電話號碼或程式碼，以允許使用者選擇退出透過英數字元寄件者 ID 傳送的訊息。

## 影片 {#video-sms}

若要深入瞭解原生輸入關鍵字如何支援 (START、STOP 和 UNSTOP) 的運作方式，請參閱下列影片：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
