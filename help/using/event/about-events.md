---
title: 關於事件
description: 瞭解事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '829'
ht-degree: 51%

---

# 關於事件{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="關於事件"
>abstract="事件會連結至人員，它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等等）或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是Journey Optimizer在制定下一個最佳行動時會傾聽的。"

事件設定可讓您定義 [!DNL Journey Optimizer] 會接收以作為事件的資訊。您可以使用多個事件（在行程的不同步驟中），而多個行程可以使用同一事件。

>[!CAUTION]
>
>事件配置為 **強制** 必須由 **資料工程師**。

可以配置兩種類型的事件：

* **酉** 事件：這些事件與某人有關。 它們與人的行為有關（例如，一個人買了產品，去了商店，退出了網站等） 或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 [!DNL Journey Optimizer] 在歷程中會監聽的事件，以便協調下一個最佳動作。酉事件可以是基於規則或系統生成的。 要瞭解如何建立統一事件，請參閱 [頁](../event/about-creating.md)。

* **業務** 事件：與單一事件不同，業務事件是未與特定配置檔案連結的事件。 例如，它可以是新聞警報、體育更新、航班更改或取消、清單更新、天氣事件等。 雖然這些事件不是特定於配置檔案的，但它們可能對任意數量的配置檔案感興趣：訂閱特定新聞主題的個人、航班上的乘客、對庫存不足產品感興趣的購物者等。 業務事件始終基於規則。 在行程中刪除業務事件時，它會自動添加 **讀取段** 活動之後。 要瞭解如何建立業務事件，請參閱此 [頁](../event/about-creating-business.md)。


>[!NOTE]
>
>如果您編輯草稿或即時歷程中使用的事件，則只能變更名稱和說明，或是新增有效負載欄位。我們對草稿或即時歷程版本有嚴格限制，以免中斷歷程。

➡️ [在影片中探索此功能](#video)

## 事件ID類型{#event-id-type}

對於業務事件，事件ID類型始終基於規則。

對於酉事件，有兩種類型的事件ID:

* **規則型** 事件：此類型的事件不會產生 eventID。使用簡單運算式編輯器，您只需定義一個規則，系統會使用該規則來識別將觸發您歷程的相關事件。 此規則可以根據事件裝載中可用的任何欄位，例如設定檔的位置或新增至設定檔購物車的項目數。

   >[!CAUTION]
   >
   >已為規則型事件定義上限規則。 它將特定組織的合格事件數限制為每秒5000次。 它與Journey OptimizerSLA相對應。 請參閱您的Journey Optimizer授權和 [Journey Optimizer產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html)。

* **系統產生的** 事件：這些事件需要 eventID。建立事件時，會自動產生此 eventID 欄位。 推播事件的系統不應產生 ID，而應傳遞有效裝載預覽中可用的 ID。

Journey Optimizer要求將活動分流或批發到Adobe Experience Platform。 此資料不一定需要前往即時設定檔。 如果您想要在個別歷程中使用事件進行細分或查詢，建議您為設定檔啟用資料集。

## 資料週期 {#data-cycle}

事件屬於 POST API 呼叫。事件通過流接收API發送到Adobe Experience Platform。 透過交易訊息 API 傳送的事件 URL 目的地稱為「入口」。事件的有效負載遵從 XDM 格式。

負載包含流接收API工作所需的資訊（在標頭中）以及 [!DNL Journey Optimizer] 工作和用於旅行的資訊（例如，在車身中，報廢的購物車的數量）。 串流獲取共有兩種模式，分別是驗證和未驗證。如需串流獲取 API 的詳細資訊，請參閱[此連結](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant)。

在通過流接收API後，事件會流入名為Pipeline的內部服務，然後流入Adobe Experience Platform。 如果事件結構已啟用「即時客戶個人檔案服務」標幟，且資料集 ID 也具有「即時客戶個人檔案」標幟，就會流入「即時客戶個人檔案服務」。

對於系統生成的事件，管道將過濾具有包含負載的事件 [!DNL Journey Optimizer] 事件ID（請參閱下面的事件建立過程）由 [!DNL Journey Optimizer] 並包含在事件負載中。 對於基於規則的事件，系統使用eventID條件標識事件。 這些事件會由 [!DNL Journey Optimizer] 監聽，並會觸發相對應的歷程。

## 作法影片 {#video}

了解如何設定事件、指定串流端點和事件的裝載。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

瞭解業務事件的適用使用案例。 瞭解如何使用業務事件建立歷程，以及套用哪些最佳實務。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
