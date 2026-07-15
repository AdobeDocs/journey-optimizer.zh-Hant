---
title: 測試您的自訂頻道
description: 瞭解如何測試連線、模擬內容，以及在啟用之前在Adobe Journey Optimizer中校訂您的自訂頻道訊息。
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 2%

---


# 測試您的自訂頻道 {#test-custom-channel}

在啟用使用自訂頻道的歷程或行銷活動之前，請驗證您的端點是否可連線、驗證是否有效，以及個人化權杖是否可正確解析您的目標設定檔。

## 測試來自管道產生器的連線 {#test-connection}

當自訂管道處於&#x200B;**[!UICONTROL 草稿]**&#x200B;狀態時，請使用管道產生器中的&#x200B;**[!UICONTROL 測試]**&#x200B;按鈕，將測試請求傳送至您的端點，並在啟用之前驗證端對端連線。 [了解更多](create-custom-channel.md#test-connection)

此測試會確認：

* 可從[!DNL Journey Optimizer]的輸出IP連線到端點。
* 設定的驗證認證是否有效。
* 端點會傳回HTTP 2xx回應。

檢查外部系統的記錄，確認已收到測試請求，其中包含預期的標頭和裝載結構。

## 模擬測試設定檔的內容 {#simulate-content}

**[!UICONTROL 模擬內容]**&#x200B;功能會針對測試設定檔解析個人化運算式，讓您能夠檢查在傳送任何實際訊息之前會傳送的確切裝載。

1. 在歷程動作或行銷活動版本畫面中，按一下&#x200B;**[!UICONTROL 模擬內容]**。

1. 按一下&#x200B;**[!UICONTROL 新增測試設定檔]**&#x200B;並選取一或多個設定檔。 [瞭解如何建立測試輪廓](../audience/creating-test-profiles.md)

1. 在預覽面板中檢閱已解析的裝載。 對於每個測試設定檔，請驗證：

   * 所有個人化權杖（例如`{{profile.person.name.firstName}}`）已取代為設定檔中的預期值。
   * 沒有未解析的Token剩餘（顯示為空白字串或常值`{{...}}`語法）。
   * 必填的裝載欄位已填入。
   * 協助程式函式會產生預期的格式化輸出。

>[!TIP]
>
>使用代表不同受眾區段的多個設定檔進行測試，以擷取邊緣案例，例如，在個人化欄位中缺少選擇性屬性、非拉丁字元集或null值的設定檔。

## 傳送校樣 {#send-proof}

若要在啟用之前驗證端對端傳送，請傳送證明給一組測試收件者：

1. 在&#x200B;**[!UICONTROL 模擬內容]**&#x200B;面板中，切換至&#x200B;**[!UICONTROL 傳送校樣]**&#x200B;標籤。

1. 新增您要使用的設定檔。 您可以上傳含有未定義為[!DNL Journey Optimizer]中測試設定檔之設定檔的CSV檔案。

1. 按一下&#x200B;**[!UICONTROL 傳送證明]**。 [!DNL Journey Optimizer]會使用每個所選設定檔的個人化裝載呼叫您的外部端點。

1. 檢查您的外部系統，以確認已收到證明承載。 對於傳訊頻道（例如WeChat或Kakao Talk），請確認訊息出現在目標裝置或傳訊應用程式上。

使用與電子郵件校樣相同的驗證模式顯示校樣結果：傳送校樣之前會顯示必填欄位、型別不匹配和結構描述驗證錯誤。

進一步瞭解如何在[行銷活動](../campaigns/create-campaign.md#send-proof)和[歷程](../building-journeys/testing-the-journey.md)中傳送校樣。

## 在歷程測試模式下測試 {#test-journey}

若要進行端對端歷程驗證，請在&#x200B;**[!UICONTROL 測試模式]**&#x200B;中啟用歷程：

1. 在歷程畫布上，按一下右上角區域中的&#x200B;**[!UICONTROL 測試]**。

1. 針對對象觸發的歷程，設定觸發事件或選取測試設定檔。

1. 按一下&#x200B;**[!UICONTROL 觸發事件]**，或讓設定檔透過&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動進入。

1. 觀察畫布中的流量。 當設定檔到達自訂通道動作節點時，[!DNL Journey Optimizer]會使用個人化裝載呼叫您的外部端點。

1. 檢查外部系統的記錄，確認已正確收到請求。

1. 完成時，按一下&#x200B;**[!UICONTROL 停止測試]**。

深入瞭解如何在[測試模式](../building-journeys/testing-the-journey.md)中測試歷程。

## 模擬歷程 {#simulate-journey}

[!DNL Journey Optimizer]的&#x200B;**模擬**&#x200B;模式可讓您使用模擬的使用者（類似暫時的設定檔實體，不會在Adobe Experience Platform中持續存在）來端對端驗證您的歷程，而不需要預先建立的測試設定檔。

對於自訂管道，模擬會解析個人化運算式，並呈現每個模擬使用者的裝載預覽，因此您可以在上線前驗證內容是否正確。

若要使用自訂頻道模擬歷程：

1. 在歷程畫布上，按一下右上角區域中的&#x200B;**[!UICONTROL 模擬]**。

1. 手動新增模擬使用者，或使用AI支援的&#x200B;**[!UICONTROL 快速模擬]**&#x200B;選項產生模擬使用者。

1. 設定任何必要的進入事件，然後透過歷程觸發模擬使用者。

1. 當模擬使用者到達自訂管道動作節點時，請在預覽面板中檢查已解析的裝載，以確認個人化權杖和裝載結構正確無誤。

>[!NOTE]
>
>模擬可用於草稿和即時歷程，並使用不會計入設定檔配額或實際端點呼叫的臨時模擬使用者。

[進一步瞭解歷程模擬](../building-journeys/simulate-journey-gs.md)

## 啟動前檢查清單 {#checklist}

在啟用您的歷程或行銷活動之前，請確認下列專案：

* 來自Channel Builder的連線測試成功（端點可連線，驗證有效）。
* 模擬裝載顯示所有測試設定檔的預期值。
* 承載中不會保留任何未解析的個人化權杖。
* 所有必要的裝載欄位皆已填入。
* 您的外部系統已正確傳送和接收校樣。
* 歷程動作活動（如果已設定）上的錯誤路徑會如預期處理失敗案例。

測試完成後，請繼續啟用。 [了解做法](create-custom-experience.md#activate)
