---
solution: Journey Optimizer
product: journey optimizer
title: 簡訊選擇退出管理
description: 瞭解如何透過簡訊管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 63237c02f632d289dba845acdcd0859f2d6de9c9
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 31%

---

# 簡訊選擇退出管理 {#sms-opt-out}

根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

>[!IMPORTANT]
>
>文字訊息通訊可能會受到各種法律規範要求的約束，具體取決於其性質、您傳送文字訊息的位置以及收件者的位置。 雖然Adobe Journey Optimizer會處理長程式碼和免付費號碼的訊息，如以下所述，請洽詢您的法律顧問，以確保您的文字訊息通訊符合所有適用的法律規範要求。
>

## 原生傳入關鍵字{#sms-native-keywords}

依預設，Adobe Journey Optimizer會針對免付費和長程式碼訊息處理下列標準英文回複訊息：STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE。 請注意，搭配Journey Optimizer使用時，只有Sinch支援原生關鍵字。

這些關鍵字通常會觸發來自第三方提供者的自動標準回覆。 您可以直接向提供者或透過其文件網站確認。

無需任何步驟，即可確保SMS選擇退出功能在Adobe Journey Optimizer中運作，因為關鍵字回應STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE會自動識別。 在Adobe Journey Optimizer中即時更新設定檔選擇退出狀態。


## 封鎖清單{#sms-blocklists}

除了Adobe Journey Optimizer根據選擇退出狀態（用於與Twilio或Sinch直接整合）停止傳送外，大部分的SMS閘道提供者也會維護封鎖清單，確保SMS訊息不會傳送給選擇退出的個人。 如果您使用Sinch或Twilio以外的提供者，並透過傳送簡訊 [自訂頻道](../building-journeys/using-custom-actions.md)，您必須向提供者確認。


## 短程式碼 {#short-codes}

依預設，Adobe Journey Optimizer不會處理短程式碼的選擇加入或說明關鍵字。 為了確保符合業界法規與選擇退出處理規則，您必須確認您的短程式碼符合所有准則。

不過，Journey Optimizer不支援根據不同寄件者ID的傳入關鍵字執行全域選擇退出。

## 英數字元寄件者 ID {#alphanumeric}

英數字元寄件者 ID 僅用於單向傳訊，無法接收傳入訊息。 因此，Adobe Journey Optimizer 的 SMS STOP、START、HELP 關鍵字不適用於 Alpha 傳送者 ID。 您必須提供其他指示，如寫入支援團隊、呼叫支援電話熱線或傳送文字訊息給其他電話號碼或程式碼，以允許使用者選擇退出透過英數字元寄件者 ID 傳送的訊息。

## 影片 {#video-sms}

若要深入瞭解原生輸入關鍵字如何支援 (START、STOP 和 UNSTOP) 的運作方式，請參閱下列影片：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
