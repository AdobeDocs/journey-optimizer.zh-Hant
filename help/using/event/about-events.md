---
solution: Journey Optimizer
product: journey optimizer
title: 使用歷程事件
description: 瞭解如何使用歷程中的事件
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: 事件，事件，歷程，定義，開始
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 2f2b53fd74a51e96e61ddaf9e489c07bd359294f
workflow-type: tm+mt
source-wordcount: '989'
ht-degree: 56%

---

# 使用歷程事件 {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="歷程事件"
>abstract="事件會連結至人員，它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等等）或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 Journey Optimizer 在歷程中會監聽的事件，以便協調下一個最佳動作。"

事件設定可讓您定義 [!DNL Journey Optimizer] 會接收以作為事件的資訊。您可以使用多個事件（在歷程的不同步驟中），而數個歷程則可以使用相同事件。

>[!CAUTION]
>
>事件設定為 **強制** 而且必須由 **資料工程師**.

您可以設定兩種事件：

* **單一** 事件：這些事件會連結至人員。 它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等等） 或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是什麼 [!DNL Journey Optimizer] 將在歷程中聆聽，以協調下一個最佳動作。 單一事件可以是規則型或系統產生。 若要瞭解如何建立單一事件，請參閱本 [頁面](../event/about-creating.md).

* **企業** 事件：與單一事件相反，業務事件是指未連結至特定設定檔的事件。 例如，可以是新聞警報、運動更新、航班變更或取消、詳細目錄更新、天氣事件等。 雖然這些事件不是設定檔所特有，但任何數量的設定檔都可能有興趣：訂閱特定新聞主題的個人、航班上的乘客、對無存貨產品感興趣的購物者等。 業務事件一律以規則為基礎。 將業務事件拖放到歷程中時，會自動新增 **讀取對象** 活動之後。 若要瞭解如何建立商業活動，請參閱此 [頁面](../event/about-creating-business.md).


>[!NOTE]
>
>如果您編輯草稿或即時歷程中使用的事件，則只能變更名稱和說明，或是新增有效負載欄位。我們對草稿或即時歷程版本有嚴格限制，以免中斷歷程。

單一歷程 (從事件或對象資格開始) 包含可防止同一事件多次錯誤觸發歷程的護欄。 在預設情況下，設定檔重新進入時會暫時封鎖 5 分鐘。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。

➡️ [在影片中探索此功能](#video)

## 事件ID型別{#event-id-type}

對於業務事件，事件ID型別一律以規則為基礎。

單一事件有兩種事件ID：

* **規則型** 事件：此類型的事件不會產生 eventID。使用簡單運算式編輯器，您只需定義一個規則，系統會使用該規則來識別將觸發您歷程的相關事件。 此規則可以根據事件裝載中可用的任何欄位，例如設定檔的位置或新增至設定檔購物車的項目數。

  >[!CAUTION]
  >
  >已為規則型事件定義上限規則。 對於指定組織，這會將歷程可處理的合格事件數限製為每秒5000。 它對應於Journey Optimizer SLA。 請參閱您的Journey Optimizer授權及 [Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html).

* **系統產生的** 事件：這些事件需要 eventID。建立事件時，會自動產生此 eventID 欄位。 推播事件的系統不應產生 ID，而應傳遞有效裝載預覽中可用的 ID。

>[!NOTE]
>
>Journey Optimizer 需將事件串流至資料收集核心服務 (DCCS)，才能觸發歷程。 批次收錄的事件，或來自內部 Journey Optimizer 資料集的事件 (訊息意見回饋、電子郵件追蹤等等) 無法用來觸發歷程。 對於無法取得串流事件的使用案例，請根據這些事件建置對象，然後改為使用&#x200B;**讀取對象**&#x200B;活動。 技術上可使用對象資格，但可能根據使用動作而造成下游挑戰。 此資料不一定需要前往即時設定檔。 如果您想要在個別歷程中使用事件進行細分或查詢，建議您為設定檔啟用資料集。

## 資料週期 {#data-cycle}

事件屬於 POST API 呼叫。事件會透過串流擷取API傳送至Adobe Experience Platform。 透過交易訊息API傳送之事件的URL目的地稱為「入口」。 事件的有效負載遵從 XDM 格式。

有效負載包含串流獲取API運作（在標題中）所需的資訊，以及所需的資訊。 [!DNL Journey Optimizer] 用於工作和用於歷程的資訊（在正文中，例如捨棄購物車的金額）。 串流獲取共有兩種模式，分別是驗證和未驗證。如需串流獲取 API 的詳細資訊，請參閱[此連結](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant)。

在透過串流獲取API到達目的地之後，事件會流入名為Pipeline的內部服務，再流入Adobe Experience Platform。 如果事件結構已啟用「即時客戶個人檔案服務」標幟，且資料集 ID 也具有「即時客戶個人檔案」標幟，就會流入「即時客戶個人檔案服務」。

對於系統產生的事件，Pipeline會篩選其裝載包含下列內容的事件 [!DNL Journey Optimizer] eventIDs （請參閱下方的事件建立程式），由 [!DNL Journey Optimizer] 並包含在事件裝載中。 對於規則型事件，系統會使用eventID條件來識別事件。 這些事件會由 [!DNL Journey Optimizer] 監聽，並會觸發相對應的歷程。

## 作法影片 {#video}

了解如何設定事件、指定串流端點和事件的裝載。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

瞭解業務事件的適用使用案例。 瞭解如何使用業務事件建立歷程，以及套用哪些最佳實務。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
