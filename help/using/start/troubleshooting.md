---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer疑難排解
description: Journey Optimizer疑難排解問題
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# 疑難排解 {#ajo-troubleshooting}


以下為Adobe Journey Optimizer的疑難排解文章清單。 每個疑難排解區段都提供常見問題的解答和問題的解決方案。

另請參閱[Adobe Experience Platform常見問題集和疑難排解檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}。

## 電子郵件管道 {#ajo-troubleshooting-email}

### 電子郵件設計 {#ajo-troubleshooting-design}

+++ 如何使用主題避免Adobe Journey Optimizer中的電子郵件格式問題？

在Adobe Journey Optimizer (AJO)中，修改電子郵件標頭中的預設CSS區塊可能會導致未預期的格式問題，尤其是在移除內容片段後。 這些問題在行動裝置上較為明顯，並可能導致版面配置轉移或樣式不一致。 若要防止此情況，請使用「主題」功能安全地套用自訂CSS，而不變更系統產生的CSS樣式。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"}以瞭解如何解決此問題。

在此頁面[上進一步瞭解電子郵件格式](../email/get-started-email-design.md)。

+++


+++ 為什麼具有可編輯欄位的片段無法運作？

在Adobe Journey Optimizer中，具有可編輯欄位的片段在新增至範本時可能會無法正確載入或意外重複。 該問題通常會影響各個環境的特定片段。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"}以瞭解如何解決此問題。

在此頁面[上進一步瞭解可自訂的片段](../content-management/customizable-fragments.md)。

+++

+++ 為什麼電子郵件範本和內容會從未發佈的歷程中消失？

在未發佈的歷程中編輯電子郵件範本時，某些電子郵件的內容和範本可能會意外消失。 這可能會造成重工和延遲。 若要降低此問題的風險，請避免同時編輯、限制開啟的標籤數量，並經常儲存變更。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}以瞭解如何解決此問題。

在此頁面[上進一步瞭解範本](../email/use-email-templates.md)。

+++

+++ 個人資料可以在Adobe Journey Optimizer中有多個推播權杖嗎？

在Journey Optimizer中實作推播通知時，單一設定檔實際上可以有多個與不同裝置相關聯的推播權杖。 在推播通知行銷活動中，Journey Optimizer的設計用途是管理這些代號，並確保可透過所有關聯裝置存取目標設定檔。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，深入瞭解推播權杖管理。

在此頁面[上進一步瞭解推播設定](../push/push-configuration.md)。

+++

### 電子郵件追蹤與報告 {#ajo-troubleshooting-tracking}

+++ 如何防止報告中遺失電子郵件追蹤連結？

當電子郵件URL使用動態變數且開頭不是http，或當邏輯陳述式放在URL欄位中時，Adobe Journey Optimizer中遺失連結追蹤就會發生。 若要解決此問題，請確保所有URL都以http開頭，避免在URL欄位中使用邏輯，並將複雜的個人化邏輯移至HTML內容或預先處理的屬性。


請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"}以瞭解如何解決此問題。

在此頁面[上進一步瞭解電子郵件追蹤](../email/message-tracking.md)。

+++

### 電子郵件傳送 {#ajo-troubleshooting-sending}

+++ 設定API觸發的交易式電子郵件行銷活動時，如何解決郵件交換器錯誤？ 

如果您在Adobe Journey Optimizer中為API觸發的交易式電子郵件促銷活動建立通道設定時遇到郵件交換器(MX)錯誤，可能是因為&#x200B;**DNS設定錯誤**&#x200B;或&#x200B;**DMARC原則限制**。 若要解決此問題，請確定您的DNS已正確設定，並確認您的網域符合&#x200B;**網域型訊息驗證、報告及一致性(DMARC)**&#x200B;需求。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"}以瞭解如何解決此問題。

在此頁面[上進一步瞭解電子郵件DMARC原則](../configuration/dmarc-record-update.md)。

另請參閱[API觸發的行銷活動檔案](../campaigns/api-triggered-campaigns.md)。
+++

## 推播頻道 {#ajo-troubleshooting-push}

+++ 個人資料可以在Adobe Journey Optimizer中有多個推播權杖嗎？

在Journey Optimizer中實作推播通知時，單一設定檔實際上可以有多個與不同裝置相關聯的推播權杖。 在推播通知行銷活動中，Journey Optimizer的設計用途是管理這些代號，並確保可透過所有關聯裝置存取目標設定檔。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"}，深入瞭解推播權杖管理。

在此頁面[上進一步瞭解推播設定](../push/push-configuration.md)。

+++

+++ 為何按一下推送訊息時無法將我重新導向至已設定的網頁URL？  

如果推送訊息未重新導向至預期的Web URL，可能是因為不正確的點按動作設定或停用推送通知設定。 請確定推送訊息的&#x200B;**點按動作**&#x200B;已正確設定，且推送通知的&#x200B;**自動顯示和追蹤**&#x200B;已啟用以解決此問題。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"}，以進一步瞭解此問題。

在此頁面[上進一步瞭解推播設定](../push/push-configuration.md)。

+++


## 簡訊頻道 {#ajo-troubleshooting-sms}

+++ 即使同意設定為`marketing.sms.value=y`，為什麼交易式SMS沒有傳遞？

如果收件者對SMS回應&#x200B;**STOP**，將會封鎖該短號碼的所有未來訊息，包括異動訊息。 為確保異動SMS的傳送不會中斷，請設定並透過收件者先前未選擇退出的&#x200B;**個別短號碼**&#x200B;傳送。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"}，以進一步瞭解此問題。

在此頁面[上進一步瞭解簡訊選擇退出設定](../sms/sms-opt-out.md)。

+++


## 資料管理 {#ajo-troubleshooting-data-management}

+++ 當您建立新沙箱時，存留時間(TTL)設定如何套用至設定檔和資料湖資料集？

在Adobe Journey Optimizer中布建新沙箱的組織提出了存留時間(TTL)設定如何套用至設定檔和資料湖資料集的問題。 本文說明TTL設定不會影響現有沙箱，並僅自動套用至新布建的沙箱。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}，瞭解如何處理TTL。

在此頁面[上進一步瞭解資料集存留時間](../data/datasets-ttl.md)。

+++


## 設定檔與對象管理 {#ajo-troubleshooting-audiences}

+++ 如何解決對象計數差異？

Adobe Journey Optimizer的&#x200B;**讀取對象**&#x200B;功能中已處理的專案數可能低於預期的對象數。 此問題通常因名稱空間設定不正確而發生，導致設定檔被排除在歷程之外。 解決方法包含檢查和修正名稱空間設定、檢閱相關檔案，以及調整優先順序以確保在Adobe Journey Optimizer中更順暢的操作。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"}以瞭解如何解決此問題。

另請參閱[這篇關於過時對象計數的文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}。

在此頁面&#x200B;**瞭解歷程**&#x200B;中[讀取對象](../building-journeys/read-audience.md)活動的詳細資訊。

+++

+++ 為何設定檔更新會失敗？

在Adobe Journey Optimizer中，某些欄位值在歷程中執行&#x200B;**更新設定檔**&#x200B;活動後可能無法正確更新。 在某些情況下，更新的欄位可能會消失或恢復到其以前的狀態。 若要解決此問題，請檢查衝突的規則或條件、檢閱許可權設定、為&#x200B;**更新設定檔**&#x200B;活動使用唯一的資料集，並確保沒有其他擷取程式同時寫入相同的設定檔。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}，瞭解解決此問題的步驟。

在此頁面&#x200B;**的歷程**&#x200B;中進一步瞭解[更新設定檔](../building-journeys/update-profiles.md)活動。

另請參閱有關資料擷取[的](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}Adobe Experience Platform檔案。

+++

+++ 為什麼進入歷程的設定檔計數和相關聯對象中的設定檔計數不相符？

如果在歷程執行時無法使用當天的快照，則當歷程使用前一天的設定檔快照時，可能會發生差異。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"}，瞭解解決此問題的步驟。

深入瞭解[此Journey Optimizer社群貼文](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}。

另請參閱[Adobe Experience Platform排程API檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"}，以檢查您的每日工作排程時間。

+++


+++ 如何解決對象人口問題？

當元件或資源遺失（通常是因為權益、布建或許可權設定錯誤）時，可能會發生對象人口問題。 若要修正這些問題，請先驗證權益、確保正確布建並檢閱許可權。 如果問題仍然存在，請升級案例並與支援團隊協調以取得完整的解決方案。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"}，瞭解解決此問題的步驟。

在此頁面&#x200B;**的歷程**&#x200B;中進一步瞭解[更新設定檔](../building-journeys/update-profiles.md)活動。

另請參閱[Adobe Real-Time CDP設定檔檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}。

+++

+++ 如何解決Adobe Journey Optimizer中對象變更後的歷程觸發問題？ 

如果歷程在修改其關聯對象（例如變更合併原則）後停止觸發，您可能會遇到行銷活動流程中斷的情況。 若要解決此問題，請&#x200B;**使用更新的對象設定複製並重新發佈歷程**，以確保觸發器正常運作。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"}，瞭解解決此問題的步驟。

瞭解如何在此頁面[上複製歷程](../building-journeys/journey-ui.md#duplicate-a-journey)。

+++


## 歷程

### 活動

+++ 為什麼我的事件沒有觸發預期的歷程？  

即使符合所有條件，當事件是&#x200B;**透過查詢服務**&#x200B;建立，而不是串流至&#x200B;**資料收集核心服務(DCCS)**&#x200B;時，事件仍可能無法觸發歷程。 若要解決此問題，請檢閱事件設定，確定事件已直接串流至DCCS **，並使用**&#x200B;測試模式&#x200B;**驗證功能。**

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"}，瞭解解決此問題的步驟。

在此頁面[上進一步瞭解事件](../event/about-events.md)。

另請參閱[歷程事件護欄](../start/guardrails.md#events)。

+++

## 決策 {#ajo-troubleshooting-decisioning}

+++ 如何解決建立優惠方案集合時的問題？

尚未為您的組織布建&#x200B;**目錄**&#x200B;時，通常會發生建立優惠方案集合的困難。 若要解決此問題，請在嘗試建立優惠方案集合之前，確認所有必要的目錄皆已正確布建。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"}，瞭解解決此問題的步驟。

在此頁面[上進一步瞭解優惠收藏](../offers/offer-library/creating-collections.md)。

+++


## 多語言 {#ajo-troubleshooting-multilingual}

+++ 如何解決此問題`Message validation error (CJMMAS - 1069-500)`？

在Adobe Journey Optimizer中，連結至多語言功能的訊息驗證錯誤(CJMMAS - 1069-500)會導致歷程無法設為測試模式或發佈。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"}，瞭解解決此問題的步驟。

在此頁面[上進一步瞭解多語言內容](../content-management/multilingual-gs.md)。

++


## 設定 {#ajo-troubleshooting-config}

### 安全性 {#ajo-troubleshooting-security}

+++ 如何為自訂動作啟用TLS v1.3？  

若要在連線到協力廠商系統時維持&#x200B;**資料完整性和安全性**，請確定您的自訂動作已啟用傳輸層安全性(**TLS**) v1.3。 這有助於保護通訊並防止潛在的安全漏洞。


請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"}以瞭解更多資訊。

在此頁面[上進一步瞭解多語言內容](../action/about-custom-action-configuration.md)。

+++

### 儀表板 {#ajo-troubleshooting-dashboards}

+++ 為什麼我無法直接從Adobe Journey Optimizer中的查詢建立儀表板？ 

在Adobe Journey Optimizer中，無法直接從查詢建立儀表板。 若要建置儀表板，請使用Adobe Experience Platform中可用的&#x200B;**儀表板建立功能**，以便您有效地視覺化及分析查詢資料。

請參閱[此疑難排解文章](https://experienceleague.adobe.com/zh-hant/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"}以瞭解更多資訊。

++