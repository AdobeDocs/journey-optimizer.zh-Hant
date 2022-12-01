---
solution: Journey Optimizer
product: journey optimizer
title: 建立 SMS 訊息
description: 了解如何在Journey Optimizer中建立SMS訊息
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b7b333e96e0f4b32a0f94c3f1e67f0f3d3fc2816
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 7%

---

# 建立 SMS 訊息 {#create-sms-bis}

>[!NOTE]
>
>根據行業標準及法規，所有簡訊行銷訊息都必須包含讓收件者輕鬆取消訂閱的方式。 若要這麼做，SMS收件者可以使用選擇加入和選擇退出關鍵字回覆。

## 在歷程或行銷活動中建立SMS訊息 {#sms-content}

若要開始個人化SMS訊息，請遵循下列步驟：

>[!BEGINTABS]

>[!TAB 將SMS訊息新增至歷程]

1. 開啟您的歷程，然後從浮動視窗的「動作」區段拖放SMS活動。

1. 提供訊息的基本資訊（標籤、說明、類別），然後選擇要使用的訊息表面。

   如需如何設定歷程的詳細資訊，請參閱。

您現在可以開始從 **[!UICONTROL 編輯內容]** 按鈕。

>[!TAB 新增SMS訊息至促銷活動]

1. 建立新的排程或API觸發促銷活動，請選取 **[!UICONTROL 簡訊]** 作為您的動作，並選取 **[!UICONTROL 應用程式表面]** 來使用。

1. 按一下&#x200B;**[!UICONTROL 建立]**。

1. 從 **[!UICONTROL 屬性]** 區段，編輯您的促銷活動 **[!UICONTROL 標題]** 和 **[!UICONTROL 說明]**.

1. 在 **[!UICONTROL 動作追蹤]** 區段，指定是否要追蹤SMS訊息中連結的點按次數。

1. 按一下 **[!UICONTROL 選取對象]** 按鈕，從可用的Adobe Experience Platform區段清單中定義要鎖定的對象。

1. 在 **[!UICONTROL 身分命名空間]** 欄位中，選擇要使用的命名空間，以識別所選區段中的個人。

1. 促銷活動設計為在特定日期或循環頻率上執行。 了解如何設定 **[!UICONTROL 排程]** 你的競選團隊。

1. 從 **[!UICONTROL 動作觸發器]** 菜單，選擇 **[!UICONTROL 頻率]** 簡訊：

   * 一次
   * 每日
   * 每週
   * 月

您現在可以開始從 **[!UICONTROL 編輯內容]** 按鈕。

>[!ENDTABS]

## 定義您的SMS內容{#sms-content}

1. 在歷程或行銷活動設定畫面中，按一下 **[!UICONTROL 編輯內容]** 按鈕來設定SMS內容。

1. 按一下 **[!UICONTROL 訊息]** 欄位來開啟運算式編輯器。

1. 使用運算式編輯器來定義內容並新增動態內容。 您可以使用任何屬性，例如設定檔名稱或城市。

1. 按一下 **[!UICONTROL 儲存]** 並在預覽中檢查您的訊息。

1. 當您的SMS訊息準備就緒時，請完成的設定以傳送訊息。

## 驗證您的簡訊{#sms-preview}

>[!NOTE]
>
> 為了獲得更好的傳遞能力，您應始終使用提供商支援的格式的電話號碼。 例如， Twilio和Sinch僅支援E.164格式的電話號碼。

定義訊息內容後，您就可以使用測試設定檔來預覽和測試。 如果已插入，則可以使用測試設定檔資料檢查此內容在訊息中的顯示方式。

若要視覺化您的SMS訊息在行動裝置上的顯示方式，請按一下 **[!UICONTROL 模擬內容]** 標籤。 深入了解中的內容模擬。

您也必須檢查編輯器上方區段的警報。  其中有些是簡單警告，但有些警告可能會阻止您使用訊息。 了解更多。
