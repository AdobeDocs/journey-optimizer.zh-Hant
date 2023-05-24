---
solution: Journey Optimizer
product: journey optimizer
title: 簡訊選擇退出管理
description: 瞭解如何使用SMS消息管理退出選項
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

根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [瞭解有關隱私和退出管理的更多資訊](../privacy/opt-out.md)

>[!IMPORTANT]
>
>文本消息通信可能受各種法律合規性要求的約束，具體取決於其性質、您發送文本消息的位置以及收件人的位置。 儘管Adobe Journey Optimizer處理下面詳細介紹的長代碼和免費號碼消息，但請咨詢您的法律顧問，確保您的簡訊通信符合所有適用的法律合規要求。

## 本機入站關鍵字{#sms-native-keywords}

預設情況下，Adobe Journey Optimizer會處理以下免費和長代碼消息的標準英文回復消息：停止、取消、開始、退出、取消、結束和取消訂閱。 請注意，與Journey Optimizer一起使用時，只有Sinch支援Native關鍵字。

這些關鍵字通常會觸發來自第三方提供商的自動標準答復。 您可以直接向提供者或透過其文件網站確認。

無需執行任何步驟來確保SMS選擇退出功能在Adobe Journey Optimizer工作，因為關鍵字響應STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE將自動識別。 配置檔案選擇退出狀態在Adobe Journey Optimizer即時更新。


## 塊清單{#sms-blocklists}

除了Adobe Journey Optimizer根據選擇退出狀態（與Twilio或Sinch直接整合）停止發送外，大多數SMS網關提供商還維護一個阻止清單，確保SMS消息不會發送給選擇退出的個人。 如果您使用的是Sinch或Twilio以外的提供商，並通過 [定制通道](../building-journeys/using-custom-actions.md)，您需要向提供商確認。


## 短程式碼 {#short-codes}

預設情況下，短代碼號的opt-in或help關鍵字不由Adobe Journey Optimizer處理。 為確保遵守行業法規和選擇退出處理規則，必須驗證您的簡短代碼是否遵守所有准則。

但是，Journey Optimizer確實支援基於具有不同發件人ID的傳入關鍵字的全局退出。

## 英數字元寄件者 ID {#alphanumeric}

英數字元寄件者 ID 僅用於單向傳訊，無法接收傳入訊息。 因此，Adobe Journey Optimizer 的 SMS STOP、START、HELP 關鍵字不適用於 Alpha 傳送者 ID。 您必須提供其他指示，如寫入支援團隊、呼叫支援電話熱線或傳送文字訊息給其他電話號碼或程式碼，以允許使用者選擇退出透過英數字元寄件者 ID 傳送的訊息。

## 影片 {#video-sms}

若要深入瞭解原生輸入關鍵字如何支援 (START、STOP 和 UNSTOP) 的運作方式，請參閱下列影片：

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
