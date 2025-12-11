---
solution: Journey Optimizer
product: journey optimizer
title: 歷程進入和退出條件
description: 透過真實世界的範例和最佳實務，瞭解如何有效管理設定檔進入和退出歷程的時間
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: 登入，退出，條件，歷程，設定檔，重新進入，最佳實務
version: Journey Orchestration
source-git-commit: 970712614b0d4da37d9ecbe45701f93147b1428c
workflow-type: tm+mt
source-wordcount: '1445'
ht-degree: 1%

---


# 使用歷程進入和退出條件 {#entry-exit-criteria-guide}

在客戶體驗協調中，若要在適當的時間提供適當的訊息，就必須精確控制客戶何時進入及退出您的歷程。 瞭解並正確設定登入和退出標準，可區分成功、吸引人的行銷活動與錯過的機會或訊息疲勞。

本指南提供在Adobe Journey Optimizer中管理歷程進入與退出標準的實用指引、真實世界的範例和最佳作法。

## 什麼是登入與退出條件？ {#what-are-criteria}

**進入條件**&#x200B;決定[客戶設定檔](../audience/get-started-profiles.md)有資格進入特定歷程的條件。 設定檔可以根據以下條件輸入：

* **[客戶行為](../event/about-events.md)** — 客戶採取的動作會即時觸發歷程專案，例如進行購買、放棄購物車或開啟行動應用程式。

* **[設定檔屬性](../audience/get-started-profiles.md)** — 客戶特性會根據其設定檔中儲存的資料（如忠誠度等級、地點、年齡或通訊偏好設定）來決定適用性。

* **[外部事件](../event/about-creating-business.md)** — 同時影響多個客戶的業務或環境觸發程式，例如低庫存警示、天氣狀況或價格變更。

* **[對象成員資格](../audience/about-audiences.md)** — 屬於特定對象區段，可為高價值客戶、非作用中使用者或新訂閱者等群組啟用目標歷程。

**退出條件**&#x200B;定義設定檔何時及如何從歷程中離開或移除：

* **歷程完成** — 設定檔到達所有歷程路徑的[結尾](end-journey.md)時，就會自動結束，完成設計的體驗。

* **成功量度成就** — 設定檔完成[歷程目標](success-metrics.md)時結束，例如進行購買或下載應用程式，消除不必要的後續通訊。

* **以條件為基礎** — 當符合[特定條件](condition-activity.md)時（例如在一段設定的期間內不活動或設定檔屬性變更），設定檔會結束。

* **以事件為基礎** — 設定檔會在[發生特定事件時結束](../event/about-events.md)，例如訂閱取消或產品退貨。

* **對象取消資格** — 設定檔不再符合[目標對象條件](../audience/about-audiences.md)時結束，以確保訊息仍然相關。

## 為什麼登入與退出條件很重要 {#why-they-matter}

正確定義登入與退出條件可帶來顯著的商業價值：

* **關聯性**：只有適當的客戶才會進入歷程，透過在最佳時間鎖定最適當的對象來提高參與度和轉換率。

* **效率**：避免客戶停留在不相關的歷程中，減少不必要的通訊、營運成本及客戶煩惱。

* **Personalization**：根據即時資料和行為啟用體驗的動態量身打造，建立更有意義的客戶互動。

* **法規遵循**：協助管理頻率上限並避免過度通訊，在維持品牌信譽的同時，遵循客戶偏好和法規要求。

## 進入和退出歷程的真實範例 {#real-world-examples}

以下為示範登入與退出標準在實務中運作方式的常見案例：

**新訂閱者的歡迎行銷活動**

* **專案**：設定檔在訂閱電子報時進入歷程
* **退出**：設定檔完成歡迎系列的電子郵件後，或設定時間後未參與時，就會退出
* **權益**：確保新訂閱者能及時收到上線，同時避免重複傳送訊息

**放棄的購物車復原**

* **登入**：如果客戶將專案新增至購物車但未在24小時內完成結帳，則會進入歷程
* **結束**：設定檔完成購買時結束，或未購買則在7天後結束
* **優點**：透過及時提醒來推動轉換，而不會傳送無興趣的客戶

**熟客方案參與度**

* **登入**：客戶在達到特定忠誠度點數臨界值後加入歷程
* **退出**：設定檔在兌現獎勵後結束，或如果閒置60天
* **優點**：讓高價值客戶與個人化優惠保持互動，並避免溝通疲勞

**產品意見回饋集合**

* **專案**：客戶在收到產品傳遞確認事件後進入歷程
* **結束**：在提交意見回饋後，設定檔結束；如果沒有回應，則在10天後結束
* **優點**：立即擷取有價值的意見回饋，而不會因持續要求而煩惱客戶

## 如何設定歷程進入條件 {#configure-entry}

>[!BEGINSHADEBOX]

**在這裡瞭解您需要瞭解的有關進入條件的所有內容：**

* **[事件型觸發器](../event/about-events.md)**：使用「設定檔建立」、「交易完成」或自訂事件等事件來開始歷程。 [在](../event/about-creating.md)管理&#x200B;**[!UICONTROL >]**&#x200B;事件&#x200B;**[!UICONTROL 中設定事件]**，定義[事件結構描述和欄位](../event/experience-event-schema.md)，然後在&#x200B;**[!UICONTROL 歷程設計器]**&#x200B;中從[事件](using-the-journey-designer.md)調色盤新增事件。

* **[以對象為基礎的專案](read-audience.md)**：以一次性批次或重複排程的方式，將歷程鎖定在屬於特定對象的設定檔中。 在[對象](../audience/creating-a-segment-definition.md)功能表中建立&#x200B;**[!UICONTROL 對象]**，然後新增&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動並[設定排程](journey-properties.md#schedule)。

* **[對象資格專案](audience-qualification-events.md)**：設定檔符合或退出特定對象時，即時觸發歷程。 定義[串流對象](../audience/about-audiences.md)，從&#x200B;**[!UICONTROL 事件]**&#x200B;調色盤新增&#x200B;**[!UICONTROL 對象資格]**&#x200B;事件，並選擇觸發程式型別。

* **[屬性篩選器](condition-activity.md)**：使用AND/OR邏輯，結合事件或對象與設定檔屬性和內容，以調整專案條件。 使用[條件](conditions.md)參照[設定檔屬性](../audience/get-started-profiles.md)、事件或[外部資料](../datasource/about-data-sources.md)。

* **[時間視窗與排程](journey-properties.md#schedule)**：設定暫時性限制，讓歷程保持及時且相關。 在讀取對象活動[上設定](read-audience.md)排程，使用[等待活動](wait-activity.md)，並新增[以時間為基礎的條件](conditions.md)來控制時間。

>[!ENDSHADEBOX]

## 如何設定歷程退出條件 {#configure-exit}

>[!BEGINSHADEBOX]

**在這裡瞭解您需要瞭解的有關退出條件的所有內容：**

* **[歷程完成](end-journey.md)**：設定檔在到達最後一個歷程步驟後自動結束。 設計結束於&#x200B;**[!UICONTROL 結束]**&#x200B;活動的歷程路徑。

* **[成功量度成就](journey-properties.md#exit-criteria)**：定義成功量度（例如購買或訂閱）並在完成時退出設定檔。 按一下「**[!UICONTROL 顯示退出條件]**」圖示，選取「**[!UICONTROL 新增退出條件]**」，然後選擇「[事件](../event/about-events.md)」或「[對象](../audience/about-audiences.md)」作為退出觸發器。

* **[非使用狀態逾時](wait-activity.md)**：如果未在設定的時間範圍內發生任何參與，則結束設定檔。 使用[退出條件](journey-properties.md#exit-criteria)搭配檢查上次參與日期的對象、設定[等待活動](wait-activity.md)並定義持續時間，以及使用[條件](condition-activity.md)來檢查活動。

* **[重新進入規則](entry-management.md)**：根據您的行銷活動策略，決定設定檔是否可以多次或僅一次重新進入歷程。 設定歷程&#x200B;**[!UICONTROL 內容]**&#x200B;中的&#x200B;**[!UICONTROL 重新進入]**&#x200B;設定以設定等待期間、啟用強制重新進入，或使用[補充識別碼](supplemental-identifier.md)進行內容特定重新進入。

>[!ENDSHADEBOX]

## 詳細歷程範例 {#journey-examples}

如需包含完整技術細節的逐步實作指引，請探索這些記錄的使用案例：

* **[客戶上線歷程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)** — 使用對象資格、事件逾時和以目標為基礎的退出，建置個人化的歡迎體驗

* **[捨棄的購物車復原](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)** — 使用事件觸發的歷程、教戰手冊及頻道路由，復原損失的銷售

* **[重新參與行銷活動](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)** — 利用行為目標定位和付費媒體啟用來贏回非作用中客戶

* **[傳送訊息給訂閱者](message-to-subscribers-uc.md)** — 目標訂閱清單包含「讀取對象」和個人化內容

* **[傳送多頻道訊息](journeys-uc.md)** — 結合電子郵件和推播與反應事件和多路徑邏輯

* **[只在工作日傳送電子郵件](weekday-email-uc.md)** — 使用以時間為基礎的條件和等待公式來排程通訊

>[!TIP]
>
>瀏覽[歷程使用案例資料庫](jo-use-cases.md)中的所有可用使用案例，以取得更多模式和實作，包括[加速傳送](ramp-up-deliveries-uc.md)、[體驗事件模式](exp-event-lookup.md)和[從即時歷程中移除設定檔](journey-pause.md#apply-an-exit-criteria-in-a-paused-journey)。

## 管理登入和退出的最佳實務 {#best-practices}

**清除定義**

* 在建立歷程以協調行銷與分析團隊之前，先記錄您的登入和退出邏輯
* 建立流程圖以顯示進入點、歷程路徑和退出條件
* 清楚地定義商業規則：「設定檔在X發生時或Y天后結束」
* 使用描述性標籤：「退出 — 購買完成」而非「退出1」
* [為報告及篩選一致地標籤歷程](../start/search-filter-categorize.md#tags)

**避免歷程重疊**

* [在啟動類似的歷程之前稽核使用中的歷程](journey-ui.md)以避免衝突
* 運用[衝突管理](../conflict-prioritization/conflicts.md)和[優先順序分數](../conflict-prioritization/priority-scores.md)來解決重疊並排定歷程優先順序
* 相互補充而非競爭的設計歷程

>[!NOTE]
>
>對於進階案例，例如當設定檔符合較高優先順序的歷程資格時自動移除設定檔，請使用[歷程上限與仲裁](../conflict-prioritization/journey-capping.md)，而不是退出條件。

**監視和最佳化**

* 使用[歷程報告](../reports/journey-global-report-cja.md)追蹤每個歷程的進入率、退出率和完成率
* 監視[成功量度](success-metrics.md)：透過成功量度完成與逾時結束的百分比
* 在啟動之前，針對各種設定檔案例測試[登入與退出條件](testing-the-journey.md)
* 根據資料調整：如果高頻率結束，請檢閱進入條件相關性；如果低成功量度完成，則分析內容和時間
* 每季檢閱所有作用中的歷程

**遵守頻率上限**

* 設定適當的[重新進入等待期間](entry-management.md)或停用一次性歷程的重新進入
* 使用[頻率限定規則](../conflict-prioritization/rule-sets.md)來防止過度通訊
* 監視報告中的頻率量度以確保法規遵從性

>[!NOTE]
>
>若要跨多個歷程管理頻率限制和歷程專案上限，請使用[歷程上限和仲裁](../conflict-prioritization/journey-capping.md)以及頻道的[頻率上限](../conflict-prioritization/channel-capping.md)。

## 結論 {#conclusion}

歷程登入和退出條件是Adobe Journey Optimizer提供個人化、及時且有效客戶體驗的基礎。 透過謹慎地設計這些條件，行銷人員可以提升參與度、減少摩擦，並建立更強大的客戶關係。

從明確對應客戶觸發器和退出點開始、徹底測試並監控結果，以持續改進您的歷程協調。

## 相關資源 {#related-resources}

**技術檔案**

* [設定檔入口管理](entry-management.md) — 入口控制的詳細技術指南
* [歷程屬性和退出條件](journey-properties.md) — 完整的設定參考
* [歷程結束的方式](end-journey.md) — 歷程生命週期管理
* [補充識別碼](supplemental-identifier.md) — 進階重新進入案例
* [歷程設計器](using-the-journey-designer.md) — 建置和設計歷程

**教學課程與範例**

* [歷程使用案例](jo-use-cases.md) — 完成歷程範例和模式
* [客戶入門影片](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* [捨棄的購物車視訊](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* [社群部落格：登入與退出條件](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/mastering-journey-entry-and-exit-criteria-in-adobe-journey/ba-p/760958)

**相關功能**

* [對象資格鑑定事件](audience-qualification-events.md)
* [成功量度和目標](success-metrics.md)
* [衝突管理](../conflict-prioritization/conflicts.md)
* [頻率上限](../conflict-prioritization/rule-sets.md)
* [測試歷程](testing-the-journey.md)
* [條件活動](condition-activity.md)
* [反應事件](reaction-events.md)
* [等待活動](wait-activity.md)
