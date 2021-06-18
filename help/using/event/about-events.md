---
title: 關於事件
description: 了解事件
feature: 事件
topic: 管理
role: Administrator
level: Intermediate
source-git-commit: 6e2526bd3c80ad2bff59502c6537a3e2213f7bf7
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 31%

---

# 關於事件{#concept_gfj_fqt_52b}

>[!CONTEXTUALHELP]
>id="jo_events"
>title="關於事件"
>abstract="事件會連結至人員，它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等等）或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 [!DNL Journey Optimizer] 在歷程中會監聽的事件，以便協調下一個最佳動作。"

事件設定可讓您定義 [!DNL Journey Optimizer] 會接收以作為事件的資訊。您可以使用多個事件（在歷程的不同步驟中），而數個歷程可以使用相同的事件。

>[!CAUTION]
>
>事件配置為&#x200B;**mandative**，必須由&#x200B;**技術用戶**&#x200B;執行。

您可以設定兩種事件：

* **** Unitaryevents:這些事件會連結至人員。它們與人的行為相關（例如，某人購買產品、造訪商店、離開網站等） 或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 [!DNL Journey Optimizer] 在歷程中會監聽的事件，以便協調下一個最佳動作。一般事件可依規則或系統產生。 若要了解如何建立統一事件，請參閱此[page](../event/about-creating.md)。

* **** 業務七：業務事件是與單一事件不同，不連結至特定設定檔的事件。例如，它可以是新聞警報、運動更新、航班變更或取消、庫存更新、天氣事件等。 雖然這些事件不是設定檔專屬的事件，但可能對任何數量的設定檔都感興趣：訂閱特定新聞主題的個人、航班上的乘客、對無存貨產品感興趣的購物者等。 業務事件一律以規則為基礎。 當您在歷程中放置業務事件時，緊接在之後自動新增&#x200B;**讀取區段**&#x200B;活動。 若要了解如何建立業務事件，請參閱此[page](../event/about-creating-business.md)。


>[!NOTE]
>
>如果您編輯草稿或即時歷程中使用的事件，則只能變更名稱和說明，或是新增有效負載欄位。我們對草稿或即時歷程版本有嚴格限制，以免中斷歷程。

## 事件ID類型{#event-id-type}

對於業務事件，事件ID類型一律為規則型。

對於單一事件，有兩種事件ID:

* **規則基** 礎事件：此類型的事件不會產生eventID。使用簡單運算式編輯器，您只需定義一個規則，系統將使用該規則來識別將觸發您歷程的相關事件。 此規則可以根據事件裝載中可用的任何欄位，例如設定檔的位置或新增至設定檔購物車的項目數。

   >[!CAUTION]
   >
   >已為規則型事件定義上限規則。 此量度會將歷程可處理的合格事件數限制為指定組織(ORG)的每秒5000次。 它對應於Journey Optimizer SLA。 請參閱此[page](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html)。

* **系統生** 成事件：這些事件需要eventID。建立事件時，會自動產生此eventID欄位。 推送事件的系統不應產生ID，而應傳遞有效負載預覽中可用的ID。

Journey Optimizer需要將事件串流或批次傳入Adobe Experience Platform。 此資料不一定需要前往即時設定檔。 如果您想要在個別歷程中使用事件進行分段或查詢，建議您為設定檔啟用資料集。

## 資料週期 {#section_r1f_xqt_pgb}

事件屬於 POST API 呼叫。事件會透過串流獲取API傳送至Adobe Experience Platform。 透過交易訊息 API 傳送的事件 URL 目的地稱為「入口」。事件的有效負載遵從 XDM 格式。

有效負載包含串流獲取API運作（在標題中）所需的資訊，以及[!DNL Journey Optimizer]運作所需的資訊，以及用於歷程（在正文中，例如捨棄購物車的金額）的資訊。 串流獲取共有兩種模式，分別是驗證和未驗證。如需串流獲取 API 的詳細資訊，請參閱[此連結](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hant)。

在透過串流獲取API到達目的地後，事件會流入名為Pipeline的內部服務，然後流入Adobe Experience Platform。 如果事件結構已啟用「即時客戶個人檔案服務」標幟，且資料集 ID 也具有「即時客戶個人檔案」標幟，就會流入「即時客戶個人檔案服務」。

對於系統產生的事件，Pipeline會篩選由[!DNL Journey Optimizer]提供且包含[!DNL Journey Optimizer] eventID之有效負載（請參閱下方的事件建立程式）的事件。 對於規則型事件，系統會使用eventID條件來識別事件。 這些事件會由 [!DNL Journey Optimizer] 監聽，並會觸發相對應的歷程。
