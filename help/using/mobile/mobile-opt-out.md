---
solution: Journey Optimizer
product: journey optimizer
title: 行動訊息的選擇退出管理
description: 瞭解如何使用SMS/RCS/MMS訊息管理選擇退出
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
TQID: https://experienceleague.adobe.com/mQVaZ8jb-hBBPxDnztkayDEI4vj0KvMTREI0KxOgAf0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 674
ht-degree: 14%

---

# 行動訊息的選擇退出管理 {#sms-opt-out}

根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 [進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

>[!IMPORTANT]
>
>行動訊息通訊可能會受到各種法律規範要求的約束，具體取決於其性質、您傳送行動訊息的位置以及收件者的位置。 雖然Adobe Journey Optimizer會處理短代碼、長代碼和免付費號碼的訊息，如以下所述，請洽詢您的法律顧問，以確保您的行動訊息通訊符合所有適用的法律規範要求。
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

請注意，如果客戶對行動訊息回應STOP，提供者會封鎖該特定傳送者ID （短代碼或長數字）的所有後續SMS，包括交易式訊息。 為確保異動SMS的傳送不會中斷，請使用先前未選取退出的個別傳送者ID。


>[!NOTE]
>
>如果您打算使用雙向SMS （以STOP、QUIT等回覆），請確定您先傳送至少一次單向SMS以建立電話號碼與設定檔對應。 提供者認證過期或設定錯誤會導致傳入關鍵字無法更新使用者設定檔，導致遺失或延遲選擇退出記錄。 傳入回應儲存在&#x200B;_AJO傳入活動事件資料集_&#x200B;系統資料集中。 [了解更多](../data/get-started-datasets.md#system-datasets)


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

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

  +++
