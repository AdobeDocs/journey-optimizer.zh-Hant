---
title: 設定業務事件
description: 了解如何建立業務活動
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 39eb40e1-d7f5-4a8e-9b64-c620940d5ff2
source-git-commit: b219f900d8349c46c01a0dd3110e441694e47b5f
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 12%

---

# 設定業務事件 {#configure-a-business-event}

與單一事件不同，業務事件不會連結至特定設定檔。 事件ID類型一律為規則型。 有關[此部分](../event/about-events.md)中業務事件的詳細資訊。

事件發生時，排程器可定期或由業務事件一次性觸發以讀取區段為基礎的歷程。

業務事件可以是「產品回頭有存貨」、「公司股價達到一定值」等。

## 重要備註

* 事件架構必須包含主要身分。
* 業務事件只能視為歷程的第一步。
* 將業務事件拖放為歷程的第一步時，歷程的排程器類型將是「業務事件」。
* 在業務事件後，只能捨棄讀取區段活動。 系統會自動新增為下一個步驟。
* 若要允許執行多個業務事件，請啟動歷程屬性的&#x200B;**[!UICONTROL Execution]**&#x200B;區段中的對應選項。
* 觸發業務事件後，將區段從15分鐘匯出至最多1小時會有延遲。
* 測試業務事件時，您必須傳遞事件參數以及測試設定檔的識別碼，以便在測試中輸入歷程。 此外，在測試以業務事件為基礎的歷程時，您只能觸發單一設定檔入口。 請參閱[本節](../building-journeys/testing-the-journey.md#test-business)。在測試模式中，沒有可用的「程式碼檢視」模式。
* 如果新的業務事件到達，目前處於歷程中的個人會發生什麼事？ 其運作方式與當新週期發生時，個人仍處於循環歷程中的情況相同。 他們的路終了。 因此，如果行銷人員預期會發生頻繁的業務事件，就必須注意避免建立過長的歷程。

## 多個業務事件

以下是幾個重要附註，當連續收到多個業務事件時適用。

**歷程處理期間收到業務事件時的行為為何？**

商務活動遵循重新進入規則的方式與單一活動相同。 如果歷程允許重新進入，則會處理下一個業務事件。

**避免過載實體化段的護欄是什麼？**

對於業務事件，主題的可重用性設定為1小時。 這表示對於指定的歷程，在1小時的時間範圍內，不會建立新的匯出工作。 由第一個事件作業推送的資料會重複使用。 對於已排程的歷程，沒有護欄。

## 開始使用業務活動

以下是設定業務事件的前幾個步驟：

1. 在「管理」菜單部分，選擇&#x200B;**[!UICONTROL Configurations]**。 在&#x200B;**[!UICONTROL Events]**&#x200B;區段中，按一下&#x200B;**[!UICONTROL Manage]**。 畫面隨即顯示事件清單。

   ![](../assets/jo-event1.png)

1. 按一下 **[!UICONTROL Create Event]** 以建立新事件。事件設定窗格會在畫面右側開啟。

   ![](../assets/jo-event2.png)

1. 輸入事件名稱。 您也可以新增說明。

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >請勿使用空格或特殊字元。請勿使用超過 30 個字元。

1. 在&#x200B;**[!UICONTROL Type]**&#x200B;欄位中，選擇&#x200B;**Business**。

   ![](../assets/jo-event3bis-business.png)

1. 使用此事件的歷程次數會顯示在 **[!UICONTROL Used in]** 欄位中。您可以按一下 **[!UICONTROL View journeys]** 圖示，以顯示使用此事件的歷程清單。

1. 定義結構和裝載欄位：這是您選取歷程預期會收到的事件資訊（通常稱為裝載）的位置。 接著，您就可以在歷程中使用這項資訊。請參閱[本節](../event/about-creating-business.md#define-the-payload-fields)。

   ![](../assets/jo-event5-business.png)

   只有時間序列結構可用。 無法使用體驗事件、決策事件和歷程步驟事件結構。 事件架構必須包含主要身分。

   ![](../assets/test-profiles-4.png)

1. 在&#x200B;**[!UICONTROL Event ID condition]**欄位內按一下。 使用簡單運算式編輯器，定義系統將使用的條件，以識別將觸發您歷程的事件。
   ![](../assets/jo-event6-business.png)

   在範例中，我們根據產品的id撰寫條件。 這表示每當系統收到符合此條件的事件時，都會將其傳遞至歷程。

   >[!NOTE]
   >
   >在簡單運算式編輯器中，並非所有運算子都可用，它們取決於資料類型。 例如，對於欄位的字串類型，您可以使用「包含」或「等於」。

1. 按一下「**[!UICONTROL Save]**」。

   ![](../assets/journey7-business.png)

   條件現在已設定完畢，且準備好放入歷程中。若要接收事件，則需要完成其他設定步驟。請參閱[此頁面](../event/additional-steps-to-send-events-to-journey-orchestration.md)。

## 定義裝載欄位 {#define-the-payload-fields}

有效負載定義可讓您選擇系統預期從歷程中的事件接收的資訊，以及識別與事件相關聯之人員的金鑰。 裝載以Experience CloudXDM欄位定義為基礎。 如需XDM的詳細資訊，請參閱[Adobe Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hant){target=&quot;_blank&quot;}。

1. 從清單中選取XDM架構，然後按一下&#x200B;**[!UICONTROL Fields]**&#x200B;欄位或&#x200B;**[!UICONTROL Edit]**&#x200B;圖示。

   ![](../assets/journey8-business.png)

   架構中定義的所有欄位都會顯示。 欄位清單因結構而異。 您可以搜尋特定欄位，或使用篩選器來顯示所有節點和欄位，或僅顯示選取的欄位。 根據架構定義，某些欄位可能是必填欄位，且已預先選取。 您無法取消選取它們。 依預設，會選取所有對於歷程正確接收事件而言為必要的欄位。

   ![](../assets/journey9-business.png)

1. 選取您要從事件接收的欄位。 這些是業務使用者在歷程中將利用的欄位。

1. 選擇完所需欄位後，按一下&#x200B;**[!UICONTROL Save]**&#x200B;或按&#x200B;**[!UICONTROL Enter]**&#x200B;鍵。

   選定欄位的數量顯示在&#x200B;**[!UICONTROL Fields]**&#x200B;欄位中。

   ![](../assets/journey12-business.png)

## 預覽裝載 {#preview-the-payload}

有效負載預覽可讓您驗證有效負載定義。

1. 按一下&#x200B;**[!UICONTROL View Payload]**&#x200B;圖示可預覽系統預期的有效負載。

   ![](../assets/journey13-business.png)

   您可以注意到已顯示選取的欄位。

   ![](../assets/journey14-business.png)

1. 檢查預覽以驗證有效負載定義。

1. 接著，您可以將裝載預覽與事件傳送的負責人共用。 此裝載可協助他設計推送至[!DNL Journey Optimizer]之事件的設定。 請參閱[此頁面](../event/additional-steps-to-send-events-to-journey-orchestration.md)。
