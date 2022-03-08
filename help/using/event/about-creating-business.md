---
title: 設定業務事件
description: 瞭解如何建立業務事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: 51254efaab08a572def118d475dc18f74c9d29b7
workflow-type: tm+mt
source-wordcount: '1041'
ht-degree: 12%

---

# 設定業務事件 {#configure-a-business-event}

與單一事件不同，業務事件不與特定的簡檔關聯。 事件ID類型始終基於規則。 閱讀有關中業務事件的更多資訊 [此部分](../event/about-events.md)。

基於讀段的行程可以在事件發生時由調度器定期或由業務事件一次性觸發。

業務事件可以是「產品回到庫存」、「公司股價達到一定值」等。

>[!NOTE]
>
>您還可以查看業務事件使用案例 [教程](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/use-case-business-event.html)。

## 重要備註 {#important-notes}

* 只有時間系列方案可用。 「體驗事件」、「決策事件」和「行程步驟事件」架構不可用。 事件架構必須包含主標識。 必鬚根據需要設定以下欄位： `_id` 和 `timestamp`
* 商務活動只能作為旅程的第一步而丟棄。
* 將業務事件作為行程的第一步放置時，行程的調度器類型將是「業務事件」。
* 業務事件後，只能刪除讀段活動。 它將自動添加為下一步。
* 要允許執行多個業務事件，請在 **[!UICONTROL Execution]** 的下界。
* 觸發業務事件後，將延遲將段從15分鐘導出到最多1小時。
* 在測試業務事件時，您必須傳遞事件參數和test配置檔案的標識符，該配置檔案將輸入test行程。 此外，在測試基於業務事件的行程時，您只能觸發單個配置檔案入口。 請參閱[本節](../building-journeys/testing-the-journey.md#test-business)。在test模式下，沒有可用的「代碼視圖」模式。
* 如果新業務活動到來，當前在旅途中的個人會如何？ 它的行為方式與當新的重複發生時個體仍處於循環過程中時的行為方式相同。 他們的道路結束了。 因此，如果市場營銷人員預期商業活動頻繁，就必須注意避免長途旅行。

## 多個業務事件 {#multiple-business-events}

以下是在一行中接收多個業務事件時適用的幾個重要說明。

**在行程處理期間接收業務事件時的行為是什麼？**

商業活動遵循與單一活動一樣的重新入場規則。 如果旅程允許重新入場，將處理下一個商務活動。

**哪些護欄可以避免過載實例化段？**

在即拍業務事件的情況下，對於給定行程，在1小時時間窗口期間重複利用由第一事件作業推送的資料。 對於預定行程，沒有護欄。 瞭解有關 [Adobe Experience Platform分段處檔案](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html)。

## 開始業務活動 {#gs-business-events}

以下是配置業務事件的第一步：

1. 在「管理」(ADMINISTRATION)菜單部分，選擇 **[!UICONTROL Configurations]**。 在  **[!UICONTROL Events]** ，按一下 **[!UICONTROL Manage]**。 畫面隨即顯示事件清單。

   ![](../assets/jo-event1.png)

1. 按一下 **[!UICONTROL Create Event]** 以建立新事件。事件設定窗格會在畫面右側開啟。

   ![](../assets/jo-event2.png)

1. 輸入事件名稱。 也可以添加說明。

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 在 **[!UICONTROL Type]** ，選擇 **業務**。

   ![](../assets/jo-event3bis-business.png)

1. 使用此事件的歷程次數會顯示在 **[!UICONTROL Used in]** 欄位中。您可以按一下 **[!UICONTROL View journeys]** 圖示，以顯示使用此事件的歷程清單。

1. 定義架構和負載欄位：這是您選擇事件資訊（通常稱為有效負載）旅行預期接收的地方。 接著，您就可以在歷程中使用這項資訊。請參閱[本節](../event/about-creating-business.md#define-the-payload-fields)。

   ![](../assets/jo-event5-business.png)

   只有時間系列方案可用。 「體驗事件」、「決策事件」和「行程步驟事件」架構不可用。 事件架構必須包含主標識。 必鬚根據需要設定以下欄位： `_id` 和 `timestamp`

   ![](../assets/test-profiles-4.png)

1. 在 **[!UICONTROL Event ID condition]** 的子菜單。 使用簡單表達式編輯器，定義系統將用於標識將觸發行程的事件的條件。
   ![](../assets/jo-event6-business.png)

   在示例中，我們根據產品的id編寫了條件。 這意味著，每當系統收到符合此條件的事件時，它都會將其傳遞到行程。

   >[!NOTE]
   >
   >在簡單表達式編輯器中，並非所有運算子都可用，它們取決於資料類型。 例如，對於欄位的字串類型，可以使用&quot;contains&quot;或&quot;equal to&quot;。

1. 按一下「**[!UICONTROL Save]**」。

   ![](../assets/journey7-business.png)

   條件現在已設定完畢，且準備好放入歷程中。若要接收事件，則需要完成其他設定步驟。請參閱[此頁面](../event/additional-steps-to-send-events-to-journey-orchestration.md)。

## 定義負載欄位 {#define-the-payload-fields}

有效負載定義允許您選擇系統希望從行程中的事件接收的資訊以及確定與事件關聯的人員的密鑰。 負載基於Experience CloudXDM欄位定義。 有關XDM的詳細資訊，請參閱 [Adobe Experience Platform文檔](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}。

1. 從清單中選擇XDM架構，然後按一下 **[!UICONTROL Fields]** 或 **[!UICONTROL Edit]** 表徵圖

   ![](../assets/journey8-business.png)

   將顯示架構中定義的所有欄位。 欄位清單因方案而異。 您可以搜索特定欄位，或使用篩選器顯示所有節點和欄位，或僅顯示選定欄位。 根據架構定義，某些欄位可能是必需的並且預先選定。 不能取消選擇它們。 預設情況下，對於要由行程正確接收的事件，必須選擇的所有欄位。

   ![](../assets/journey9-business.png)

   >[!NOTE]
   >
   > 確保選擇了以下欄位： `_id` 和 `timestamp`

1. 選擇要從事件接收的欄位。 這些是業務用戶在旅途中將利用的欄位。

1. 選擇完所需欄位後，按一下 **[!UICONTROL Save]** 按 **[!UICONTROL Enter]**。

   所選欄位的數量顯示在 **[!UICONTROL Fields]** 的子菜單。

   ![](../assets/journey12-business.png)

## 預覽負載 {#preview-the-payload}

負載預覽允許您驗證負載定義。

1. 按一下 **[!UICONTROL View Payload]** 表徵圖，預覽系統所需的負載。

   ![](../assets/journey13-business.png)

   您可以注意到，所選欄位將顯示。

   ![](../assets/journey14-business.png)

1. 檢查預覽以驗證負載定義。

1. 然後，您可以與負責事件發送的人員共用負載預覽。 此負載可以幫助他們設計推送到的事件的設定 [!DNL Journey Optimizer]。 請參閱[此頁面](../event/additional-steps-to-send-events-to-journey-orchestration.md)。
