---
solution: Journey Optimizer
product: journey optimizer
title: 關於事件
description: 了解事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# 關於事件{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="關於事件"
>abstract="事件會連結至人員。 它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等） 或某人發生的事（例如，某人達到10,000個忠誠點數）。 這是Journey Optimizer在歷程中會監聽的事項，以便協調下一個最佳動作。"

事件設定可讓您定義資訊 [!DNL Journey Optimizer] 會作為事件接收。 您可以使用多個事件（在歷程的不同步驟中），而數個歷程可以使用相同的事件。

>[!CAUTION]
>
>事件設定為 **強制** 和必須由 **資料工程師**.

您可以設定兩種事件：

* **單一** 事件：這些事件會連結至人員。 它們與人的行為相關（例如，某人購買產品、造訪商店、離開網站等） 或某人發生的事（例如，某人達到10,000個忠誠點數）。 這就是 [!DNL Journey Optimizer] 會在歷程中監聽，以便協調下一個最佳動作。 單一事件可以是規則型事件或系統產生的事件。 若要了解如何建立統一事件，請參閱 [頁面](../event/about-creating.md).

* **企業** 事件：業務事件是與單一事件不同，不連結至特定設定檔的事件。 例如，它可以是新聞警報、運動更新、航班變更或取消、庫存更新、天氣事件等。 雖然這些事件不是設定檔專屬的事件，但可能對任何數量的設定檔都感興趣：訂閱特定新聞主題的個人、航班上的乘客、對無存貨產品感興趣的購物者等。 業務事件一律以規則為基礎。 當您在歷程中放置業務事件時，會自動新增 **讀取區段** 活動之後。 若要了解如何建立業務活動，請參閱 [頁面](../event/about-creating-business.md).


>[!NOTE]
>
>如果您編輯草稿或即時歷程中使用的事件，則只能變更名稱、說明或新增裝載欄位。 我們嚴格限制草稿或即時歷程的版本，以避免中斷歷程。

單一歷程（從事件或區段資格開始）包含防止同一事件多次錯誤觸發歷程的護欄。 設定檔重新進入預設會暫時封鎖5分鐘。 例如，如果某個事件在12:01對特定設定檔觸發歷程，而另一個事件在12:03到達（無論是相同事件或是不同事件觸發相同歷程），該歷程將不會對此設定檔重新開始。

➡️ [在影片中探索此功能](#video)

## 事件ID類型{#event-id-type}

對於業務事件，事件ID類型一律為規則型。

對於單一事件，有兩種事件ID:

* **規則型** 事件：此類型的事件不會產生eventID。 使用簡單運算式編輯器，您只需定義一個規則，系統將使用該規則來識別將觸發您歷程的相關事件。 此規則可以根據事件裝載中可用的任何欄位，例如設定檔的位置或新增至設定檔購物車的項目數。

   >[!CAUTION]
   >
   >已為規則型事件定義上限規則。 此量度會將歷程可處理的合格事件數限制為指定組織的每秒5000次。 它對應至Journey Optimizer SLA。 請參閱您的Journey Optimizer授權和 [Journey Optimizer產品說明](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **系統產生** 事件：這些事件需要eventID。 建立事件時，會自動產生此eventID欄位。 推送事件的系統不應產生ID，而應傳遞有效負載預覽中可用的ID。

Journey Optimizer需要將事件串流或批次處理至Adobe Experience Platform。 此資料不一定需要前往即時設定檔。 如果您想要在個別歷程中使用事件進行分段或查詢，建議您為設定檔啟用資料集。

## 資料週期 {#data-cycle}

事件是POST API呼叫。 事件會透過串流獲取API傳送至Adobe Experience Platform。 透過交易訊息API傳送之事件的URL目的地稱為「入口」。 事件的裝載會遵循XDM格式。

裝載包含串流獲取API運作（在標題中）所需的資訊，以及 [!DNL Journey Optimizer] 用於歷程的工作和資訊（在內文中，例如捨棄購物車的金額）。 串流獲取共有兩種模式，分別是驗證和未驗證。 如需串流獲取API的詳細資訊，請參閱 [此連結](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

在透過串流獲取API到達目的地後，事件會流入名為Pipeline的內部服務，然後流入Adobe Experience Platform。 如果事件結構已啟用「即時客戶個人檔案服務」標幟，且資料集ID也具有「即時客戶個人檔案」標幟，便會流入「即時客戶個人檔案服務」。

對於系統產生的事件，管道會篩選具有包含之裝載的事件 [!DNL Journey Optimizer] eventID（請參閱下方的事件建立程式），由 [!DNL Journey Optimizer] 和包含在事件裝載中。 對於規則型事件，系統會使用eventID條件來識別事件。 這些事件由 [!DNL Journey Optimizer] 且會觸發對應的歷程。

## 作法影片 {#video}

了解如何設定事件、指定串流端點和事件的裝載。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

了解業務事件的適用使用案例。 了解如何使用業務活動建立歷程，以及套用哪些最佳實務。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
