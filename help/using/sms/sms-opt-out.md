---
solution: Journey Optimizer
product: journey optimizer
title: SMS選擇退出管理
description: 了解如何使用SMS訊息管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# SMS選擇退出管理 {#sms-opt-out}

根據業界標準和法規，所有SMS行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [深入了解隱私權和選擇退出管理](../privacy/opt-out.md)

依預設，Adobe Journey Optimizer會根據Sinch和Twilio等原生整合的業界標準，處理免付費和長程式碼訊息的標準英文回覆訊息，例如STOP、UNSTOP和START。 這些關鍵字通常會觸發您第三方提供者（例如Twilio、Sinch等）的自動標準回覆。 您可以直接向提供者或透過其檔案網站確認。

無需任何步驟，即可確保SMS選擇退出功能在Adobe Journey Optimizer中正常運作，因為系統會自動辨識關鍵字回應STOP、UNSTOP和START。

除了Adobe Journey Optimizer根據選擇退出狀態停止傳送（用於與Twilio或Sinch直接整合）外，大部分的SMS閘道提供者也會維護封鎖清單，確保SMS訊息不會傳送給已選擇退出的個人。 如果您使用Sinch或Twilio以外的提供者，並透過 [自訂頻道](../building-journeys/using-custom-actions.md)，您需要向提供者確認。

>[!IMPORTANT]
>
>簡訊行銷活動可能會受到各種法律法規遵循要求的約束，具體取決於您的簡訊行銷活動的性質、您發送簡訊的位置，以及收件者的位置。 <br>雖然Adobe Journey Optimizer將依照上述所述處理長碼和免付費號碼的訊息，您應諮詢您的法律顧問，以確保您的文字訊息行銷活動符合所有適用的法律規範要求。

## 短代碼 {#short-codes}

依預設，Adobe Journey Optimizer不會處理短程式碼的選擇退出、選擇加入或說明關鍵字。

您必須確保您的簡短程式碼符合選擇退出處理的所有產業規則和法規。

## 字母數字發件人ID {#alphanumeric}

英數字元寄件者ID僅用於單向傳訊，無法接收傳入訊息。 因此，Adobe Journey Optimizer的SMS STOP、START、HELP關鍵字不適用於Alpha傳送者ID。 您必須提供其他指示，如寫入支援團隊、呼叫支援電話線或發簡訊給其他電話號碼或代碼，以允許用戶選擇退出通過字母數字發件人ID發送的郵件。

## 影片 {#video-sms}

若要進一步了解SMS原生傳入關鍵字支援（START、STOP及UNSTOP）的運作方式，請參閱下列影片：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
