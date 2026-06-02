---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 護欄和限制
description: 深入瞭解 Journey Optimizer 護欄
feature: Guardrails
role: User
level: Intermediate
mini-toc-levels: 2
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
TQID: https://experienceleague.adobe.com/k4DqGogrTZ9QrnqyFGwdgDeUI9ivpOd1iSI0c5comuU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2:
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 26e1073e2fef79ecdfd72ff1c2e5247ec2d62f8a
workflow-type: tm+mt
source-wordcount: 4622
ht-degree: 64%

---


# 護欄與限制 {#limitations}

當使用 [!DNL Adobe Journey Optimizer] 時，您將找到下列護欄和限制。

權益、產品限制和效能護欄全都列於 [Adobe Journey Optimizer 產品說明頁面上](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}。

>[!CAUTION]
>
>* [即時客戶輪廓資料、分段的護欄](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/guardrails){target="_blank"}也適用於 Adobe Journey Optimizer。
>
>* 另請參閱[即時客戶設定檔中資料攝取的護欄](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/ingestion/guardrails){target="_blank"}

## 主要限制一覽 {#quick-reference}

在您建置或發佈之前，請使用這個表格來查詢最重要的數值限制。 以下各節提供完整的詳細資訊和內容。

| 區域圖 | 限制 | 值 |
|---|---|---|
| **歷程** | 每個歷程最多[個活動](#journeys-guardrails-journeys) | **50** |
| **歷程** | [最多即時/暫停/試執行歷程](#journeys-guardrails-journeys) | **100** |
| **歷程** | [歷程執行個體大小](#journeys-guardrails-journeys) | **1 MB** |
| **歷程** | [歷程裝載大小（發佈）](#journey-payload-size) | **2 MB** （在90%時警告） |
| **歷程** | [全域歷程逾時](#journeys-guardrails-journeys) | **91天** |
| **歷程** | 每個設定檔[擱置的事件佇列](#journeys-guardrails-journeys) | **10個事件** |
| **歷程** | [同時讀取對象執行個體](#read-segment-g) | 所有沙箱中的&#x200B;**5** |
| **歷程** | [讀取對象沙箱輸送量](#read-segment-g) | **20,000個設定檔/秒** （共用） |
| **歷程** | [讀取對象工作逾時](#read-segment-g) | **12小時** |
| **頻道** | [每秒傳入要求](#inbound-guardrails) | **5,000 RPS** |
| **頻道** | [最大作用中傳入動作](#inbound-guardrails) | **500** |
| **頻道** | [異動訊息/秒（行銷活動）](#transactional-message-guardrails) | **500** |
| **頻道** | [每秒的傳入歷程事件](#events-g) | **5,000** |
| **自訂動作** | 每分鐘[次呼叫（回應&lt; 0.75秒）](#custom-actions-g) | 每個主機/沙箱&#x200B;**300,000 / min** |
| **自訂動作** | 每30秒[次呼叫（回應> 0.75秒）](#custom-actions-g) | 每個主機/沙箱&#x200B;**150,000 / 30 s** |
| **內容** | [電子郵件訊息內容於發佈](#message-content-size) | **2 MB** （1 MB以下的作者） |
| **內容** | [應用程式內訊息內容](#in-app-activity-limitations) | **2 MB** |
| **內容** | [視覺片段大小](#fragments-guardrails) | **100 KB** |
| **內容** | [運算式片段大小](#fragments-guardrails) | **200 KB** |
| **內容** | [歷程片段節點](#fragments-journey-g) | **20個節點/片段**，200個使用中/沙箱 |
| **客群** | 每個沙箱的[對象組合](#audience) | **10** |
| **資料集** | [設定檔存放區TTL （新組織/沙箱）](#datasets-guardrails) | **90天** |
| **資料集** | [資料湖TTL （新組織/沙箱）](#datasets-guardrails) | **13個月** |


## 系統與平台 {#system-platform}

### 支援的瀏覽器 {#browsers}

Adobe [!DNL Journey Optimizer] 介面的設計可在最新版 Google Chrome 中以最佳方式運作。 您在舊版或其他瀏覽器上使用某些功能時可能會遇到問題。

### 資料集護欄 {#datasets-guardrails}

自 2025 年 2 月起，將在 **新沙箱和新組織** 中，向 Journey Optimizer 系統產生的資料集，開放使用存留時間 (TTL) 護欄功能，如下所示：

* 設定檔存放區中的資料&#x200B;**90天**
* 資料湖中的資料為&#x200B;**13個月**

將在後續階段，開放&#x200B;**現有客戶沙箱**&#x200B;使用這項變更。 [進一步瞭解資料集存留時間 (TTL) 護欄](../data/datasets-ttl.md)

## 管道與傳訊 {#channel-guardrails}

本節涵蓋所有通訊管道的護欄，包括電子郵件、簡訊、傳入管道 (網頁、應用程式內、程式碼型、內容卡) 和交易型訊息。

>[!NOTE]
>
>在極少數情況下，特定區域的暫時中斷可能會導致有效的設定檔被排除在歷程之外，或導致郵件被錯誤標示為退回郵件。 服務恢復後，重新檢查歷程記錄，驗證同意設定檔欄位，並在需要時重新發佈歷程。 若發生 ISP 中斷，請參閱[本節](../configuration/manage-suppression-list.md#remove-from-suppression-list)以了解如何從禁止名單之中移除設定檔。

### 電子郵件護欄 {#message-guardrails}

下列防護措施適用於[電子郵件頻道](../email/get-started-email.md)：

* 您無法使用相同的傳送網域從[!DNL Adobe Journey Optimizer]和其他產品 (例如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]) 傳送電子郵件訊息。

在設計電子郵件訊息時，系統會檢查關鍵設定並顯示警告 (建議和最佳做法) 和錯誤 (封鎖會阻礙測試或啟用的問題) 的警示。 在[本節](../email/create-email.md#check-email-alerts)中進一步了解電子郵件警示和驗證需求。

#### 歷程發佈的訊息內容大小 {#message-content-size}

發佈包含電子郵件訊息的歷程時，後端處理後的訊息內容大小總計不得超過&#x200B;**2 MB**。 在發佈期間，系統會透過修補連結、影像和套用轉換來自動處理訊息內容，這會增加承載大小，超過編寫的內容大小。

>[!CAUTION]
>
>如果最終處理的訊息內容超過&#x200B;**2 MB**，歷程發佈將會失敗。 將您編寫的訊息內容保持在2 MB以下 — 最好在&#x200B;**1 MB**&#x200B;以下 — 以允許緩衝為300-400 KB的後端處理負荷。

**防止發佈失敗的最佳做法：**

* 將編寫的電子郵件內容保留在&#x200B;**1 MB**&#x200B;以下
* 將內容變化版本的數量減到最少
* 在將影像新增至訊息之前，請先最佳化及壓縮影像
* 移除未使用的資產及不必要的 HTML 元素
* 在將歷程發佈到生產環境之前測試訊息大小

如果歷程發佈因內容大小而失敗，請減少訊息內容並重新發佈歷程。

### SMS 護欄 {#sms-guardrails}

下列防護措施適用於 [SMS 頻道](../mobile/get-started-mobile.md)：

* MMS 適用的媒體檔案可透過支援的 URL 加入。 請確定媒體檔案已個別上傳。
* 訊息回饋同步目前不適用於 MMS。
* 同意管理在 MMS 的 SMS 通道層級運作。

### 傳入頻道護欄 {#inbound-guardrails}

* 若要在 [!DNL Journey Optimizer] 中使用[程式碼型體驗](../code-based/get-started-code-based.md)動作，並傳送您的應用程式可以使用的程式碼內容承載，請遵循[此頁面](../code-based/code-based-prerequisites.md)詳述的先決條件。

* 若要能夠在 [!DNL Journey Optimizer] 使用者介面中存取及編寫[網頁](../web/get-started-web.md)，請遵循[此頁面](../web/web-prerequisites.md)上列出的先決條件。

* 若要使用 [!DNL Journey Optimizer] 在歷程與行銷活動中傳送應用程式內訊息，請遵循[此頁面](../in-app/inapp-configuration.md)上列出的傳遞先決條件。

* 若要讓 Adobe Journey Optimizer 正確顯示內容卡，您必須設定[此頁面](../content-card/content-card-configuration-prereq.md)上列出的 Adobe Experience Platform 設定。

* Journey Optimizer支援每秒&#x200B;**5,000個傳入要求的尖峰數量**。 此護欄適用於所有傳入請求，這些請求可源自任何 Journey Optimizer 支援的傳入頻道 ([網頁](../web/get-started-web.md)、[應用程式內](../in-app/get-started-in-app.md)、[程式碼型體驗](../code-based/get-started-code-based.md)、[內容卡](../../rp_landing_pages/content-card-landing-page.md))。

* Journey Optimizer在任何時間支援最多&#x200B;**500個作用中的傳入動作**。 這些傳入動作若是即時行銷活動的一部分，或為即時歷程中使用的節點，則會計算在內。 達到此數目後，您必須停用使用傳入動作的舊版行銷活動或歷程，才能啟動新行銷活動或歷程。

#### 傳入管道的輪廓管理 {#profile-management-inbound}

[!DNL Journey Optimizer]傳入管道可鎖定假名輪廓，這表示輪廓尚未驗證或還處於未知狀態，因為它們之前從未在其他管道上有過互動。 例如，當根據類似 ECID 的臨時 ID 來鎖定所有訪客或客群時，就會發生這種情況。

這樣做會增加可互動輪廓總數，如果其超過您購買的可互動輪廓合約數量，可能會影響成本。 各個套件的授權量度都列在 [Journey Optimizer 產品說明](https://helpx.adobe.com/tw/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}頁面上。 您可以在[授權使用儀表板](../audience/license-usage.md)中檢查可互動輪廓的數量。

為了將您的可互動輪廓保持在合理限制內，Adobe 建議設定存留時間 (TTL)，以在指定時間範圍內未看到假名輪廓或未與之互動時，自動從即時客戶輪廓中刪除該輪廓。 Adobe建議將TTL值設為&#x200B;**14天**，以符合目前的Edge設定檔TTL。

>[!NOTE]
>
>在 [Experience Platform 文件](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}中了解如何設定假名輪廓的資料有效期。

### 交易型訊息護欄 {#transactional-message-guardrails}

Journey Optimizer在行銷活動中支援每秒&#x200B;**500個交易式訊息的尖峰數量**。

## 內容與資產 {#content-assets}

本節涵蓋內容建立與管理的護欄，包括登陸頁面、子網域和片段。

### AI助理護欄 {#ai-assistant-g}

**AI助理內容產生**&#x200B;的護欄和限制 — 包括支援的管道（電子郵件、推播、網頁、簡訊）和個人化編輯器限制 — 列於[此頁面](../content-management/gs-generative.md#generative-guardrails)。

### 登陸頁面護欄 {#lp-guardrails}

下列防護措施適用於[登陸頁面](../landing-pages/get-started-lp.md)：

* 一個主頁面只能使用一個&#x200B;**表單**&#x200B;元件。
* 此&#x200B;**表單**&#x200B;元件無法在子頁面中使用。
* 您無法將預覽文字新增至登陸頁面。
* 在設計登陸主要頁面時，您無法選取&#x200B;**自行編碼**&#x200B;選項。

### 子網域護欄 {#subdomain-guardrails}

[本頁](../configuration/delegate-subdomain.md#guardrails)詳細說明了套用至 Journey Optimizer 子網域委派的護欄和限制。

### 片段護欄 {#fragments-guardrails}

下列防護措施適用於[片段](../content-management/fragments.md)：

* 若要建立、編輯、封存和發佈片段，您需要&#x200B;**[!DNL Content Library Manager]**&#x200B;產品設定檔中包含的&#x200B;**[!DNL Manage library items]**&#x200B;和&#x200B;**[發佈片段]**&#x200B;權限。 [了解更多](../administration/ootb-product-profiles.md#content-library-manager)
* 視覺片段僅可用於電子郵件管道。
* 運算式片段不適用於應用程式內管道。
* 視覺化片段不能超過&#x200B;**100 KB**。 運算式片段不能超過&#x200B;**200 KB**。
* 若要在歷程或行銷活動中使用片段，它現在必須處於&#x200B;**即時**&#x200B;狀態。
* 片段中不支援[內容屬性](../personalization/personalization-build-expressions.md)。
* 視覺片段在使用主題和手動樣式模式之間不相容。 為了能夠在您想要套用主題的內容中使用片段，此片段必須在使用主題模式中建立。 [進一步了解主題](../email/apply-email-themes.md)
* 在歷程或行銷活動中啟用追蹤時，如果您將連結新增至片段，且此片段用於訊息中，則會追蹤這些連結，例如訊息中包含的所有其他連結。 [進一步了解連結和追蹤](../email/message-tracking.md)

## 客群和輪廓 {#audiences-profiles}

本節涵蓋客群管理、輪廓處理和可互動輪廓考量事項的護欄。

### 客群和輪廓護欄 {#audience}

* 您最多可以在指定的沙箱中發佈&#x200B;**10個對象組合**。 如果您達到此臨界值，則需要刪除構成以釋放空間，才能發佈新的構成。

  請在[此頁面](../audience/get-started-audience-orchestration.md)深入了解有關客群構成的詳細資訊。

* 擷取資料時，電子郵件區分大小寫。 這意味著可能會建立重複的輪廓 (例如，John.Greene@luma.com 是一個輪廓、john.greene@luma.com 是另一個輪廓)，並在您的 [!DNL Journey Optimizer] 歷程和行銷活動中定位對應的收件者時使用。

* 使用傳入管道定位目標假名輪廓 (未驗證的訪客) 時，請考慮設定自動刪除輪廓的存留時間 (TTL)，以管理可互動輪廓計數和相關成本。 [了解更多](#profile-management-inbound)

## 決策管理 {#decision-management}

### 決策與決策管理護欄 {#decisioning-guardrails}

決策和決策管理部分詳細說明了使用決策或決策管理時需要牢記的護欄與限制：

* [決策護欄與限制](../experience-decisioning/decisioning-guardrails.md)
* [決策管理護欄與限制](../offers/decision-management-guardrails.md)

## 歷程 {#journeys-guardrails}

本節涵蓋歷程的護欄和限制，包括一般歷程限制、歷程元件 (動作、事件、資料來源)、歷程活動以及自訂動作和運算式編輯器等特定功能。

### 一般歷程護欄 {#journeys-guardrails-journeys}

* 歷程中的活動數限製為&#x200B;**50**。 活動數會顯示於歷程畫布的左上方區段。

  由於歷程接近此限制，編輯和發佈效能可能會降低，並且可能會發生儲存或驗證失敗。 如果發生此情況，請使用[跳轉活動](../building-journeys/jump.md)將您的歷程分割為較小的子歷程，或在新版本中重新建立它。 無法增加活動限制。

* 根據預設，一次的即時/暫停/試執行歷程數限製為&#x200B;**100**。 目前的歷程數目會顯示在歷程畫布上方。

  當您發佈歷程時，我們會自動縮放和調整，以確保輸送量與穩定性達到最高。 當您一次接近 100 個即時歷程的里程碑時，您會看到此成果的 UI 中出現通知。 如果您看到此通知，並需要一次將歷程擴充至 100 個即時歷程以上，請建立客戶服務支援服務單，我們將協助您達成目標。

* 在歷程中使用對象資格時，該對象資格活動最多可能需要&#x200B;**10分鐘**&#x200B;才能生效，並聆聽進入或退出對象的設定檔。

* 設定檔的歷程執行個體大小上限為&#x200B;**1 MB**。 在歷程執行過程中收集的所有資料都會儲存在該歷程執行個體中。 因此，來自傳入事件的資料、從 Adobe Experience Platform 擷取的輪廓資訊、自訂動作回應等會儲存在該歷程執行個體中，並影響歷程大小。 當歷程以事件開始時，建議限制該事件裝載的大小上限（例如低於&#x200B;**800 KB**），以免在歷程執行中經過幾個活動後達到該限制。 當達到該限制時，輪廓處於錯誤狀態並將從歷程中排除。

* 對於每個設定檔和歷程版本，歷程執行階段在處理一個事件時，會保留最多&#x200B;**10個擱置事件**&#x200B;的內部佇列。 如果達到此限制，則會出於 `maxInstanceStackEventsReached` 原則捨棄其他事件，直到堆疊耗盡為止。 檢視[由於封鎖歷程執行個體而捨棄的事件](../building-journeys/troubleshooting-execution.md#max-instance-stack-events-reached)。

* 除了歷程活動中使用的逾時之外，還有一個不會顯示在介面且無法變更的全域歷程逾時。 此全域逾時會在個人進入歷程&#x200B;**91天**&#x200B;後停止個人進度。 [閱讀更多](../building-journeys/journey-properties.md#global_timeout)

>[!TIP]
>
>**這對您來說意味著什麼：** **50活動限制**&#x200B;和&#x200B;**100即時歷程限制**&#x200B;是大多數團隊在縮放時首先遇到的兩個護欄。 規劃提早分割歷程，並將讀取對象開始時間隔開至少5至10分鐘，以避免沙箱輸送量競爭。

#### 歷程承載大小驗證 {#journey-payload-size}

當您儲存或發佈歷程時，Journey Optimizer 會驗證歷程承載總大小，以保留穩定性和績效。

| 藍本 | 臨界值 | 行為 |
|---|---|---|
| 承載小於限制的90% | 低於警告 | 歷程已成功儲存和發佈。 未顯示警告或錯誤。 |
| 有效負載為限制的90-99% | 警告（軟式） | 歷程儲存並發佈時出現警告： **警告**：歷程裝載大小接近限制。 最大節點：&#39;[NodeName]&#39; (類型：&#39;[NodeType]&#39;，大小：[N] 位元組)。 |
| 裝載≥限制的100% | **錯誤（硬式）** | 已封鎖儲存或發佈。 傳回&#x200B;**HTTP 413要求實體太大**。 錯誤：歷程裝載大小超過限制。 最大節點：&#39;[NodeName]&#39; (類型：&#39;[NodeType]&#39;，大小：[N] 位元組)。 |

**預設設定**

* **預設要求大小上限**： **2 MB** （2,000,000位元組）。 某些組織可能有 Adobe 設定的自訂限制。
* **警告臨界值**：上限的 90%。
* **錯誤臨界值**：上限的 100%。

**疑難排解與建議**

* 檢閱警告或錯誤中反白顯示的最大節點。
* 簡化條件、減少資料對應，以及移除不必要的步驟或參數。
* 如有需要，請考慮將歷程分割為較小的歷程。
* 如果您認為您的組織需要更高的限制，請聯絡您的 Adobe 代表。

若要在發佈之前監視您歷程的目前裝載大小，請使用歷程屬性面板中的&#x200B;**[!UICONTROL 目前歷程裝載大小]**&#x200B;指標。 [瞭解如何檢查您的歷程承載的大小](../building-journeys/journey-properties.md#journey-payload-size)

### 授權套件比較 {#select-package-limitations}

>[!NOTE]
>
>以下的Select套件限制不適用於讀取對象或業務事件歷程。 如果您需要具有多個動作、條件或等待活動的更複雜的歷程邏輯，請考慮升級您的授權套件或在適用的情況下使用讀取客群歷程。

對於使用&#x200B;**Select**&#x200B;授權套件的客戶，下列額外限制尤其適用於單一歷程（以事件或對象資格開始的歷程）：

| 限制 | 錯誤代碼 | 說明 |
|---|---|---|
| 只允許一個動作 | `ERR_PKG_SELECT_8` | 單一歷程只能包含&#x200B;**一個**&#x200B;動作活動。 同一個歷程中不允許有多個電子郵件、推播、簡訊或其他動作活動。 |
| 不允許的條件 | `ERR_PKG_SELECT_7` | 條件活動不能用於單一歷程。 歷程必須遵循單一線性路徑，不含分支邏輯。 |
| 無等待活動 | `ERR_PKG_SELECT_6` | 無法將等待活動新增到單一歷程。 動作必須立即執行且無延遲。 |
| 逾時/錯誤轉換必須移至結束節點 | `ERR_PKG_SELECT_2` | 如果您為動作（例如電子郵件動作）設定逾時或錯誤轉變，這些路徑必須直接指向結束節點。 它們無法連線到歷程中的其他活動或動作。 |

>[!TIP]
>
>**這對您有何意義：**&#x200B;如果您位於Select套件並且需要分支邏輯、等待活動或多個動作，您必須改用讀取對象歷程，或聯絡您的Adobe代表以升級套件。

### 一般動作 {#general-actions-g}

下列防護措施適用於您旅程的[行動](../building-journeys/about-journey-activities.md)：

* 如果出現錯誤，將系統地執行三次重試。 您無法根據收到的錯誤訊息調整重試次數。 除 HTTP 401、403 和 404 外，會對所有 HTTP 錯誤執行重試。
* 內建的&#x200B;**反應**&#x200B;事件可讓您對開箱即用的動作做出反應。 請在[此頁面](../building-journeys/reaction-events.md)了解更多。 如果要對透過自訂動作傳送的訊息做出反應，則需設定專用事件。
* 您無法同時進行兩個動作，必須逐一新增。
* 對於作用中的[&#128279;](../building-journeys/publish-journey.md#journey-create-new-version)歷程版本中，設定檔無法在同一歷程中同時出現多次。 如果啟用重新進入，輪廓可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](../building-journeys/end-journey.md)

### 歷程版本 {#journey-versions-g}

下列防護措施適用於[歷程版本](../start/user-interface.md)：

* 從 v1 中的事件活動開始的歷程無法從其他版本中的事件開始。 您無法透過&#x200B;**客群資格篩選**&#x200B;事件開始歷程。
* 在 v1 中以&#x200B;**客群資格篩選**&#x200B;活動開始的歷程，在後續版本中必須一律以&#x200B;**客群資格篩選**&#x200B;開始。
* 在&#x200B;**客群資格篩選** (第一個節點) 中選擇的客群與命名空間在新版本中無法變更。
* 所有歷程版本中的重新進入規則必須相同。
* 以&#x200B;**讀取客群**&#x200B;開始的歷程在後續版本中無法以另一個事件開始。
* 您無法建立使用增量讀取方式的新讀取客群歷程版本。 您必須重複歷程。

### 自訂動作 {#custom-actions-g}

下列防護措施適用於您旅程的[自訂動作](../action/action.md)：

| 護欄 | 值 | 附註 |
|---|---|---|
| 上限限制 — 回應&lt; 0.75秒 | 每個主機和每個沙箱&#x200B;**300,000次呼叫/分鐘** | 滑動視窗。 針對每個沙箱和每個端點強制執行。 |
| 上限限制 — 回應> 0.75秒 | **150,000次呼叫/ 30秒**&#x200B;每個主機和每個沙箱 | 滑動視窗。 端點延遲超過0.75秒時套用的個別限制。 |
| URL型別 | 僅限靜態 | 不支援自訂動作URL中的動態引數。 |
| 支援的HTTP方法 | POST、PUT、GET | 不支援其他方法。 |
| 查詢引數/標頭名稱格式 | 不得以`.`或`$`開頭 | 以這些字元開頭的名稱會遭到拒絕。 |
| url中的IP位址 | 不允許 | 請使用主機名稱而非IP位址。 |
| 內部Adobe位址 | 不允許 | URL和API中不允許`.adobe.*`位址。 |
| 內建自訂動作 | 無法移除 | 內建自訂動作是永久性的。 |
| 裝載格式 | 僅限JSON | 要求和回應裝載均需要JSON格式。 請參閱[此頁面](../action/about-custom-action-configuration.md#custom-actions-limitations)。 |
| 最小端點輸送量 | 200 TPS | 自訂動作鎖定的任何端點都必須支援至少200個TPS。 |

>[!TIP]
>
>**這對您有何意義：**&#x200B;預設的300,000個呼叫/分鐘上限可保護您的外部端點，避免因歷程輸送量而受限。 如果您的端點可以處理更多負載，您可以使用[上限API](../configuration/capping.md)或[節流API](../configuration/throttling.md)來提高此限制。 如果您需要更高的組織限制，請聯絡您的Adobe代表。

此限制是根據客戶使用情況來設定，可保護自訂動作鎖定為目標的外部端點。 如有需要，您可以透過上限/節流 API 定義較高的上限或節流限制來覆寫此設定。 請參閱[此頁面](../configuration/external-systems.md)。

### 活動 {#events-g}

下列防護措施適用於您旅程的[事件](../event/about-events.md)：

* Journey Optimizer支援所有沙箱每秒&#x200B;**5,000個傳入歷程事件**&#x200B;的尖峰數量。 請[在此頁面](../event/about-events.md#event-thoughput)深入了解此限制。
* 事件觸發的歷程最多可能需要&#x200B;**5分鐘**&#x200B;才能處理歷程中的第一個動作。
* 對於系統產生的事件，必須先在 Journey Optimizer 中設定用於啟動客戶歷程的串流資料，才能取得唯一的協調流程 ID。 此協調流程 ID 必須附加至傳入 Adobe Experience Platform 的串流裝載。 此限制不適用於規則型事件。
* 業務事件不能與單一事件或客群資格篩選活動結合使用。
* 單一歷程 (從事件或客群資格篩選開始) 包含可防止同一事件多次錯誤觸發歷程的護欄。 設定檔重新進入預設會暫時封鎖&#x200B;**5分鐘**。 例如，如果某個事件在 12:01 觸發特定設定檔的歷程，而另一個事件在 12:03 達到時間限制 (無論是相同事件或是不同事件觸發相同歷程)，則此設定檔的歷程將不會再次開始。
* Journey Optimizer 需將事件串流至資料收集核心服務 (DCCS)，才能觸發歷程。 批次擷取的事件、透過&#x200B;**查詢服務**&#x200B;插入的事件，或來自內部 Journey Optimizer 資料集的事件 (訊息意見回饋、電子郵件追蹤等等) 不能用於觸發歷程。 對於無法取得串流事件的使用案例，請根據這些事件建置對象，然後改為使用&#x200B;**讀取對象**&#x200B;活動。 技術上可使用客群資格篩選，但不建議使用，因為它可能會根據所使用的操作導致下游挑戰。

### 資料來源 {#data-sources-g}

下列防護措施適用於您旅程的[資料來源](../datasource/about-data-sources.md)：

* 可在客戶歷程中利用外部資料來源即時查詢外部資料。 這些來源必須可透過 REST API 使用、支援 JSON 並且能夠處理大量請求。
* 內部 Adobe 地址 (`.adobe.*`) 不允許在 URL 及 API 中使用。

>[!NOTE]
>
>現已支援回應，對於外部資料來源使用案例，您應該使用自訂動作，而非資料來源。

### 歷程與輪廓建立 {#journeys-limitation-profile-creation}

在 Adobe Experience Platform 中建立/更新以 API 為基礎的輪廓會有延遲。 對於第95個百分位數的請求，服務等級目標(SLT)從擷取到統一設定檔的延遲小於1分鐘，每秒請求量為&#x200B;**20K (RPS)**。

如果在建立輪廓的同時觸發歷程，並立即從輪廓服務檢查/擷取資訊，則可能無法正常運作。

您可以從以下兩種解決方案中選擇一種：

* 在第一個事件後新增等待活動，為 Adobe Experience Platform 提供執行擷取至輪廓服務所需的時間。

* 設定不會立即運用輪廓的歷程。 例如，如果歷程的設計是要確認帳戶的建立，則體驗事件可能包含傳送第一個確認訊息 (名字、姓氏、電子郵件地址等) 所需的資訊。

### 補充識別碼 {#supplemental}

特定護欄適用於在歷程中使用補充識別碼。 它們會在[本頁面](../building-journeys/supplemental-identifier.md#guardrails)中列出。

### 運算式編輯器 {#expression-editor}

下列護欄適用於[歷程運算式編輯器](../building-journeys/expression/expressionadvanced.md)：

* 從讀取客群、客群資格篩選或業務事件活動開始的歷程中，無法使用體驗事件欄位群組。 您必須建立新的客群，才能在歷程中使用`inaudience`條件。
* 無法在運算式編輯器中使用`timeSeriesEvents`屬性。 若想在設定檔等級存取體驗事件，請根據`XDM ExperienceEvent`結構描述建立新的欄位群組。

### 歷程活動 {#activities}

#### 客群資格鑑定活動 {#audience-qualif-g}

下列護欄適用於[客群鑑定](../building-journeys/audience-qualification-events.md)歷程活動：

* 客群資格篩選活動無法與 Adobe Campaign 活動搭配使用。
* 客群資格鑑定歷程不支援補充識別碼。

在[本節](../building-journeys/entry-management.md#journey-processing-rate)中深入了解歷程處理速率和輸送量限制。

其他護欄 — 包括串流與批次對象的建議以及構成對象限制 — 列於[此頁面](../building-journeys/audience-qualification-events.md#audience-qualification-guardrails)。

#### 行銷活動 {#ac-g}

下列護欄適用於 **[!UICONTROL Campaign v7/v8]** 和 **[!UICONTROL Campaign Standard]** 活動：

* Adobe Campaign 活動不能與讀取客群或客群資格篩選活動搭配使用。
* **[!UICONTROL Campaign Standard]** 活動不能與其他管道活動搭配使用：卡片、程式碼型體驗、電子郵件、推播、簡訊、應用程式內訊息、網頁。
* **[!UICONTROL Campaign v7/v8]** 活動可與同一歷程中的原生管道活動搭配使用。

#### 反應事件 {#reaction-events-g}

特定護欄適用於&#x200B;**[!UICONTROL 反應]**&#x200B;事件，包括必須在頻道動作後立即放置活動，以及無法追蹤不同歷程中傳送的訊息。 它們會列出於[此頁面](../building-journeys/reaction-events.md#guardrails-limitations)。

#### 應用程式內活動 {#in-app-activity-limitations}

下列護欄適用於&#x200B;**[!UICONTROL 應用程式內訊息]**&#x200B;動作。 請在[此頁面](../in-app/create-in-app.md)深入了解有關應用程式內訊息的更多資訊。

* 此功能目前不適用於醫療保健客戶。

* 個人化只能包含輪廓屬性。

* 應用程式內活動無法搭配 **[!UICONTROL Campaign Standard]** 活動使用。

* 應用程式內顯示會繫結至歷程期限，這表示當輪廓的歷程結束時，該歷程中的所有應用程式內訊息將不再顯示該輪廓。 因此，無法直接從歷程活動停止應用程式內訊息。 而是必須結束整個歷程，才能停止將應用程式內訊息顯示給輪廓。

* 在測試模式中，應用程式內顯示取決於歷程的有效期限。 為避免歷程在測試期間過早結束，請調整&#x200B;**[!UICONTROL 等待]**&#x200B;活動的&#x200B;**[!UICONTROL 等待時間]**&#x200B;值。

* **[!UICONTROL 回應]**&#x200B;活動無法用於對應用程式內開啟或點按做出反應。

* 啟動延遲可能發生在使用者輪廓到達畫布中的應用程式內活動的時刻和他們開始看到該應用程式內訊息的時刻之間。

* 應用程式內訊息內容大小限製為&#x200B;**2 MB**。 包含大型影像可能會阻礙發佈過程。

#### 內容決活動 {#content-decision-g}

特定護欄適用於&#x200B;**[!UICONTROL 內容決定]**&#x200B;活動，包括更新的同意政策在決定政策中生效之前的48小時延遲。 它們會列出於[此頁面](../building-journeys/content-decision.md#guardrails)。

#### 跳轉活動 {#jump-g}

特定護欄適用於&#x200B;**[!UICONTROL 跳轉]**&#x200B;活動。 它們會列出於[此頁面](../building-journeys/jump.md#jump-limitations)。

#### 讀取客群活動 {#read-segment-g}

下列護欄適用於[讀取對象](../building-journeys/read-audience.md)歷程活動：

| 護欄 | 值 | 附註 |
|---|---|---|
| 並行執行個體（所有沙箱+歷程） | **5** | 避免排程超過5個同時開始的讀取對象歷程；將它們分散開5到10分鐘。 |
| 沙箱輸送量 | **20,000個設定檔/秒** （共用） | 在沙箱中的所有讀取對象活動中共用。 如果達到限制，工作可能會排入佇列。 |
| 每個活動可設定的輸送量 | **500-20,000個設定檔/秒** | 在沙箱共用限制內為每個活動設定。 |
| 作業處理逾時 | **12小時** | 系統會自動清理無法在12小時內處理的工作，且這些工作不會執行。 |
| 重試視窗 | 最多&#x200B;**1小時** （10分鐘間隔） | 擷取匯出作業時會套用重試。 歷程最多可在排程時間後1小時執行。 |
| 補充ID讀取率 | 每個歷程執行個體每秒&#x200B;**500個設定檔** | 適用於使用補充ID時。 |
| 每個歷程讀取對象例項 | **1** | 歷程只能有一個讀取對象活動。 |
| 對象型別 | 串流對象一律為最新狀態 | 批次對象在每日批次評估時間每天僅評估一次。 |
| 設定檔屬性重新整理 | 已在&#x200B;**等待**&#x200B;活動重新整理 | 在歷程專案上，設定檔會使用批次快照值。 當設定檔達到等待活動時，屬性會重新整理。 |
| 歷程中的定位 | 第一個活動或業務事件後 | 「讀取對象」活動只能作為歷程中的第一個活動，或是在業務活動活動之後。 |
| 搭配Adobe Campaign使用 | 不支援 | 「讀取對象」活動無法與Adobe Campaign活動搭配使用。 |
| 多個對象 | 不直接支援 | 「讀取對象」活動在每個歷程中只能鎖定一個對象。 若要使用多個對象，請先將其合併。 [了解做法](../audience/get-started-audience-orchestration.md) |

>[!TIP]
>
>**這對您來說意味著什麼：** 5個並行執行個體的限制是整個組織的硬性上限。 如果您有多個團隊排程讀取對象歷程，請謹慎協調開始時間。 錯過12小時處理時段的作業會無訊息地捨棄 — 一律在歷程記錄中確認成功執行。

另請參閱讀取客群活動的[建議與設定](../building-journeys/read-audience.md#must-read)。

#### 更新輪廓活動 {#update-profile-g}

特定護欄套用於&#x200B;**[!UICONTROL 更新輪廓]**&#x200B;活動。 它們會列出於[此頁面](../building-journeys/update-profiles.md)。

#### 歷程暫停 {#pause-g}

特定護欄適用於&#x200B;**暫停歷程**，包括組織中所有暫停歷程的最長暫停期間&#x200B;**14天**&#x200B;和&#x200B;**10,000,000設定檔上限**。 它們會列出於[此頁面](../building-journeys/journey-pause.md#journey-pause-guardrails)。

#### 歷程試運行 {#dry-run-g}

特定護欄適用於&#x200B;**歷程練習**，包括計算可參與的設定檔和即時歷程配額。 它們會列出於[此頁面](../building-journeys/journey-dry-run.md#journey-dry-run-limitations)。

#### 歷程片段 {#fragments-journey-g}

特定護欄適用於&#x200B;**歷程片段**，包括每個片段&#x200B;**最多** 20個節點，以及每個沙箱&#x200B;**最多** 200個作用中片段。 它們會列出於[此頁面](../building-journeys/journey-fragments.md#guardrails)。

#### 使用波段傳送 {#waves-g}

特定護欄適用於在歷程&#x200B;**中傳送的**&#x200B;波浪，包括2-10波浪範圍以及波浪之間的&#x200B;**30分鐘最小間隔**。 它們會列出於[此頁面](../building-journeys/send-using-waves.md#limitations-guardrails)。

#### 歷程模擬 {#simulation-g}

特定護欄適用於&#x200B;**歷程模擬**。 它們會列出於[此頁面](../building-journeys/simulate-journey.md#limitations)。

## 行銷活動協調 {#campaign-orchestration}

### 行銷活動協調護欄 {#orchestration-guardrails}

本節詳細說明使用行銷活動協調時要牢記的護欄和限制：[護欄和限制](../orchestrated/guardrails.md)。
