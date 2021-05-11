---
title: 關於事件
description: 瞭解活動
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 32%

---

# 關於事件{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="關於事件"
>abstract="事件會連結至人員，它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等等）或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 [!DNL Journey Optimizer] 在歷程中會監聽的事件，以便協調下一個最佳動作。"

事件設定可讓您定義 [!DNL Journey Optimizer] 會接收以作為事件的資訊。您可以使用多個事件（在歷程的不同步驟中），而數個歷程可以使用相同的事件。

>[!CAUTION]
>
>事件配置為&#x200B;**強制**，且必須由&#x200B;**技術用戶**&#x200B;執行。

您可以設定兩種事件：

* **** Unitaryevents:這些事件會連結至某個人。它們與人的行為有關（例如，某人購買產品、造訪商店、退出網站等） 或是某人發生的事（例如，某人達到 10,000 點忠誠點數）。這是 [!DNL Journey Optimizer] 在歷程中會監聽的事件，以便協調下一個最佳動作。單一事件可以是規則型事件或系統產生的事件。 要瞭解如何建立統一事件，請參閱此[頁](../event/about-creating.md)。

* **企** 業代表：商業事件是與單一事件不同的事件，不連結至特定個人檔案的事件。例如，它可以是新聞警報、運動更新、航班變更或取消、庫存更新、氣象事件等。 雖然這些事件並非個人檔案專屬，但可能對任何數量的個人檔案感興趣：訂閱特定新聞主題的個人、航班上的乘客、對無存貨產品感興趣的購物者等。 業務事件一律以規則為基礎。 當您將業務事件拖曳至歷程中時，它會在之後自動新增&#x200B;**讀取區段**&#x200B;活動。 要瞭解如何建立業務事件，請參閱此[頁](../event/about-creating-business.md)。


>[!NOTE]
>
>如果您編輯草稿或即時歷程中使用的事件，則只能變更名稱和說明，或是新增有效負載欄位。我們對草稿或即時歷程版本有嚴格限制，以免中斷歷程。

## 事件ID類型{#event-id-type}

對於商業事件，事件ID類型一律以規則為基礎。

對於單一事件，事件ID有兩種類型：

* **以規則為基** 礎的事件：此類型的事件不會產生eventID。使用簡單運算式編輯器，您只需定義規則，系統將使用該規則來識別將觸發歷程的相關事件。 此規則可以根據事件裝載中可用的任何欄位，例如描述檔位置或新增至描述檔購物車的項目數。

   >[!CAUTION]
   >
   >會為規則型事件定義上限規則。 它可將特定組織(ORG)的歷程可處理的合格事件數限制為每秒5000個。 它對應於Journey Optimizer的SLA。 請參閱此[頁](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html)。

* **系統生成** 事件：這些事件需要eventID。建立事件時會自動產生此eventID欄位。 推送事件的系統不應產生ID，而應傳遞裝載預覽中可用的ID。

## 資料週期 {#section_r1f_xqt_pgb}

事件屬於 POST API 呼叫。事件會透過串流擷取API傳送至Adobe Experience Platform。 透過交易訊息 API 傳送的事件 URL 目的地稱為「入口」。事件的有效負載遵從 XDM 格式。

裝載包含串流擷取API運作所需的資訊（在標題中），以及[!DNL Journey Optimizer]運作所需的資訊和歷程所需的資訊（在內文中，例如已放棄購物車的數量）。 串流獲取共有兩種模式，分別是驗證和未驗證。如需串流獲取 API 的詳細資訊，請參閱[此連結](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html)。

在透過串流擷取API到達後，事件會流入名為Pipeline的內部服務，然後流入Adobe Experience Platform。 如果事件結構已啟用「即時客戶個人檔案服務」標幟，且資料集 ID 也具有「即時客戶個人檔案」標幟，就會流入「即時客戶個人檔案服務」。

對於系統產生的事件，Pipeline會篩選包含[!DNL Journey Optimizer] eventIDs的裝載（請參閱下面的事件建立程式）的事件，這些事件由[!DNL Journey Optimizer]提供並包含在事件裝載中。 對於規則型事件，系統會使用eventID條件來識別事件。 這些事件會由 [!DNL Journey Optimizer] 監聽，並會觸發相對應的歷程。
