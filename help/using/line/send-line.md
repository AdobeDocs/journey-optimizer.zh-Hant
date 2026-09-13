---
solution: Journey Optimizer
product: journey optimizer
title: 預覽、驗證及傳送您的LINE訊息
description: 瞭解如何預覽和驗證LINE訊息、解決警告和錯誤、必要時請求核准，以及在歷程或行銷活動中啟動或發佈
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# 預覽、驗證及傳送您的LINE訊息 {#send-line}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;預覽並驗證您的LINE訊息、解決警告和錯誤、必要時要求核准，以及完成歷程或行銷活動設定以傳送訊息。

>[!ENDSHADEBOX]

## 開始之前 {#before-you-start}

開始之前，請確定：

* 已為您的組織啟用LINE。 如果LINE無法使用，請聯絡您的Adobe代表以請求啟用。
* Journey Optimizer中提供LINE頻道設定。 請參閱[設定LINE頻道](./line-configuration.md)。
* 您已將LINE動作新增至歷程或行銷活動，並定義訊息內容。 請參閱[建立LINE訊息](./create-line.md)。

## 預覽您的LINE訊息 {#preview-line}

定義訊息內容之後，使用&#x200B;**[!UICONTROL 模擬內容]**&#x200B;在傳送訊息之前先預覽訊息。

您可以使用下列任一選項：

| 模擬選項 | 使用它可以 |
| --- | --- |
| **[!UICONTROL 模擬內容]** | 使用範例輸入資料或AI自動產生來測試內容變異。 |
| **[!UICONTROL 模擬內容]** > **[!UICONTROL 模擬內容（AEP設定檔）]** | 使用測試設定檔預覽訊息。 |

檢閱每個變數，並確認訊息內容和個人化值顯示如預期。

如需預覽和測試內容的詳細資訊，請參閱[預覽和測試內容](../content-management/preview-test.md)。

## 驗證您的內容 {#line-validate}

繼續之前，請先檢閱訊息編輯器頂端顯示的警示。

Journey Optimizer會顯示兩種警報：

* **警告**&#x200B;是建議或最佳實務建議。 它們不會阻止您測試或傳送訊息。
* **錯誤**&#x200B;會識別在您測試或啟動歷程，或發佈行銷活動之前必須解決的問題。

請先解決所有錯誤，然後再繼續。 當警告指出訊息可能無法提供預期的客戶體驗時，請解決該警告。

## 需要時要求核准 {#line-approval}

如果您的行銷活動受核准政策的約束，請在傳送訊息之前請求核准。

請參閱[瞭解如何要求核准](../test-approve/gs-approval.md)。

## 傳送您的LINE訊息 {#line-send}

當訊息準備就緒時，請返回包含LINE動作的歷程或行銷活動並完成其設定：

* **歷程：**&#x200B;完成歷程設定，然後啟動歷程。
* **促銷活動：**&#x200B;請完成促銷活動設定，然後發佈促銷活動。

如果您無法啟動歷程或發佈行銷活動，請返回訊息編輯器並解決任何剩餘的錯誤。

## 相關任務 {#related-tasks}

* [開始使用 LINE](./get-started-line.md)
* [建立 LINE 訊息](./create-line.md)
* [設定LINE頻道](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
