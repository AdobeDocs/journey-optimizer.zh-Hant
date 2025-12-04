---
solution: Journey Optimizer
product: journey optimizer
title: 文字訊息的選擇退出管理
description: 瞭解如何透過簡訊/多媒體簡訊管理選擇退出
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 38d537eb7a14f926cafd2769fd09821eebb1186a
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 14%

---

# 文字訊息的選擇退出管理 {#sms-opt-out}

根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

>[!IMPORTANT]
>
>文字訊息通訊可能會受到各種法律規範要求的約束，具體取決於其性質、您傳送文字訊息的位置以及收件者的位置。 雖然Adobe Journey Optimizer會處理短代碼、長代碼和免付費號碼的訊息，如以下所述，請洽詢您的法律顧問，以確保您的文字訊息通訊符合所有適用的法律規範要求。
>

## 原生傳入關鍵字 {#sms-native-keywords}

>[!NOTE]
>
> 搭配Journey Optimizer使用時，只有Sinch和Infobip支援原生關鍵字。

依預設，Adobe Journey Optimizer會針對短代碼、免付費和長代碼訊息處理以下標準英文回複訊息：

* **選擇退出**：停止、結束、取消、結束、取消訂閱、否。
* **選擇加入**：訂閱、是、取消停止、開始、繼續、繼續、開始。
* **說明**：說明。

這些關鍵字通常會觸發來自第三方提供者的自動標準回覆。 您可以直接向提供者或透過其文件網站確認。

使用Infobip時，請確定「轉送」動作已設為「提取」設定。

無需任何步驟，即可確保SMS選擇退出功能在Adobe Journey Optimizer中運作，因為關鍵字回應STOP、UNSTOP、START、QUIT、CANCEL、END和UNSUBSCRIBE會自動識別。 在Adobe Journey Optimizer中即時更新設定檔選擇退出狀態。

如果您在SMS API認證中定義自訂選擇退出關鍵字，這些關鍵字會覆寫以上列出的預設傳入關鍵字。 若要保留預設關鍵字（例如STOP、QUIT、CANCEL、END和UNSUBSCRIBE），請在簡訊設定的Opt-Out Keywords欄位中將其與自訂關鍵字一起明確納入。 否則，只會辨識您的自訂關鍵字，且預設關鍵字不再觸發選擇退出動作。

請注意，如果客戶對文字訊息回應STOP，提供者會封鎖該特定傳送者ID （短代碼或長數字）的所有後續SMS，包括交易式訊息。 為確保異動SMS的傳送不會中斷，請使用先前未選取退出的個別傳送者ID。


>[!NOTE]
>
>如果您打算使用雙向SMS （以STOP、QUIT等回覆），請確定您先傳送至少一次單向SMS以建立電話號碼與設定檔對應。 提供者認證過期或設定錯誤會導致傳入關鍵字無法更新使用者設定檔，導致遺失或延遲選擇退出記錄。


## 封鎖清單 {#sms-blocklists}

除了Adobe Journey Optimizer根據選擇退出狀態（用於與Twilio、Infobip或Sinch直接整合）停止傳送外，大部分的簡訊閘道提供者也會維護封鎖清單，確保您不會將簡訊傳送給選擇退出的個人。 如果您使用Sinch或Twilio以外的提供者，並透過[自訂頻道](../building-journeys/using-custom-actions.md)傳送SMS，您必須向提供者確認。


## 短程式碼 {#short-codes}

依預設，Adobe Journey Optimizer不會處理短程式碼的選擇加入或說明關鍵字。 為了確保符合業界法規與選擇退出處理規則，您必須確認您的短程式碼符合所有准則。

不過，Journey Optimizer不支援根據不同寄件者ID的傳入關鍵字執行全域選擇退出。

## 英數字元寄件者 ID {#alphanumeric}

英數字元寄件者 ID 僅用於單向傳訊，無法接收傳入訊息。 因此，Adobe Journey Optimizer的SMS STOP、START、HELP關鍵字不適用於Alpha寄件者ID。 您必須提供其他指示，如寫入支援團隊、呼叫支援電話熱線或傳送文字訊息給其他電話號碼或程式碼，以允許使用者選擇退出透過英數字元寄件者 ID 傳送的訊息。

## 影片 {#video-sms}

* 以下影片可協助您瞭解如何設定簡訊的雙重選擇加入。

  +++ 收看影片

  >[!VIDEO](https://video.tv.adobe.com/v/3440291/?captions=chi_hant&learn=on)

  +++
