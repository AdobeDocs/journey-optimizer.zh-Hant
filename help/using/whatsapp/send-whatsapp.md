---
solution: Journey Optimizer
product: journey optimizer
title: 檢查並測試您的WhatsApp訊息
description: 瞭解如何在Journey Optimizer中檢查並傳送您的WhatsApp訊息
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 2%

---

# 檢查並傳送 WhatsApp 訊息 {#send-whatsapp}

## 預覽您的WhatsApp訊息 {#preview-whatsapp}

定義訊息內容後，您可以使用測試設定檔，或從CSV / JSON檔案上傳的範例輸入資料，或手動新增以預覽其內容。 如果您已插入個人化內容，您可以檢查此內容在訊息中的顯示方式。

若要這麼做，請按一下&#x200B;**[!UICONTROL 模擬內容]**，然後使用測試設定檔資料檢查您的訊息。

有關如何預覽及測試內容的詳細資訊，請參閱[內容管理](../content-management/preview-test.md)區段。

## 驗證您的內容 {#whatsapp-validate}

您必須檢查編輯器上半區段的警示。 其中一些是簡單的警告，但其他警告可能會阻止您傳送訊息。 可能會發生兩種型別的警報：警告和錯誤。

* **警告**&#x200B;參考建議和最佳實務。 例如，如果您的文字訊息為空白，則會顯示警告訊息。

* **錯誤**&#x200B;會阻止您測試或啟動歷程，或發佈行銷活動，只要這些錯誤未解決。 例如，當主旨行遺失時，錯誤訊息會警告您。

## 傳送您的WhatsApp訊息 {#whatsapp-send}

>[!IMPORTANT]
>
> 如果您的行銷活動受核准政策的約束，您將需要請求核准才能傳送您的文字訊息。 [了解更多](../test-approve/gs-approval.md)

當您的WhatsApp訊息準備就緒時，請完成您的[歷程](../building-journeys/publish-journey.md)或[行銷活動](../campaigns/review-activate-campaign.md)的設定以進行傳送。

## 分析WhatsApp互動 {#whatsapp-channel-context}

Journey Optimizer會擷取從WhatsApp頻道傳回的其他互動資料，並將其儲存在`whatsAppChannelContext`欄位群組下的&#x200B;**報告 — 電子郵件追蹤體驗事件資料集**&#x200B;中。 使用這些欄位來建置[對象](../audience/about-audiences.md)、執行[查詢](../data/get-started-queries.md)，以及分析WhatsApp參與。 [進一步瞭解系統資料集](../data/get-started-datasets.md#system-datasets)。

擷取下列欄位：

| 欄位 | 說明 |
|-|-|
| `messageType` | WhatsApp訊息型別（例如，`templateBased`、`response`）。 |
| `inboundMessage` | 傳入回覆內容（例如，`stop`、`start`、`subscribe`）。 |
| `inboundNumber` | 接收傳入訊息的寄件者ID。 |
| `channelType` | 管道類別（`Utility`、`Marketing`或`Promotional`）。 |
| `profileNumber` | 接收傳入訊息的來源電話號碼。 |
| `origTimestamp` | Meta / WhatsApp的原始時間戳記。 |
| `status` | 傳遞狀態包含標準化的提供者意見（`sent`、`delivered`、`bounce`、`error`、`delay`、`duplicate`、`denylist`、`exclude`或`unknown`）以及原始提供者狀態訊息。 |
| `reactionEvent` | 使用者回應的內容：回應的表情符號，或特定訊息的回複訊息文字。 |
| `reactionMessageID` | 要回應之原始郵件的ID。 |
| `reactionActionName` | 回應動作的型別（`react`、`unreact`或`reply`）。 |
| `interactiveSelectedTitle` | 使用者從WhatsApp互動訊息中選取的標題。 |
| `interactiveType` | 互動式訊息型別（`list reply`、`button reply`或`button`）。 |
| `interactiveSelectedDescription` | 所選WhatsApp互動式選項的說明。 |
| `interactiveSelectedID` | 從WhatsApp選取的選項ID。 |

若要查詢此資料集，請使用查詢服務中的`ajo_email_tracking_experience_event_dataset`資料表。 如需查詢模式和相關使用案例，請參閱[資料集查詢範例](../data/datasets-query-examples.md)。
