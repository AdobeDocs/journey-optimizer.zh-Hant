---
title: 發行說明2022
description: Journey Optimizer2022年發行說明
source-git-commit: 4626237ce629dcaec8d20c89db3cb8b517671502
workflow-type: tm+mt
source-wordcount: '1069'
ht-degree: 97%

---

# 2022 年發行說明 {#release-notes-2022}

此頁列出了 [!DNL Journey Optimizer] 於2022年發佈。

最新發行說明可用 [此頁](release-notes.md)。

## 2022 年 4 月發行版本 {#april-2022-release}

### 改進項目

**登陸頁面**

* **核取方塊的新選項「選擇加入/選擇退出」** - 現在，您可以在訂閱項目登錄頁面中插入選擇加入/選擇退出的核取方塊。 使用者需要勾選方塊同意 (選擇加入)，並取消勾選方塊移除其同意 (選擇退出)。 [了解更多](../landing-pages/design-lp.md#define-lp-specific-content)

* **預先填寫登陸頁面欄位** - 現在，使用者可以使用個人資料預先填寫登陸頁面欄位。 [進一步了解](../landing-pages/create-lp.md#configure-primary-page)

**決定管理**

* **邊緣決策 API** - 邊緣決策 API 可以提供並轉譯受 Offer Decisioning 管理的個人化服務。 您可以使用 Offer Decisioning 使用者介面 (UI) 或 API 建立您的優惠方案與其他相關物件。 [進一步了解](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**管理**

* **PTR 提交期間** - PTR 編輯的生效期間現在為幾個小時。 [了解更多](../configuration/ptr-records.md#processing)

**電子郵件設計**

* 提供 **20 個新電子郵件範本**，可在 Journey Optimizer 設計您的電子郵件內容。

**使用者介面**

* **Journey Optimizer UI 內容說明** - 內容說明連結已新增到 Journey Optimizer 的多個頁面。 可用時，請按一下「i」圖示可針對目前功能及存取權限的相關文章查看快速說明。

**整合 Adobe Campaign Standard**

作為 Adobe Campaign Standard 的客戶，您現在可以使用 Journey Optimizer 傳送電子郵件、推播通知和 SMS。 使用新的內建動作在 Journey Optimizer 善用 Campaign Standard 異動訊息傳送功能。  [了解更多](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## 2022 年 3 月發行 {#march-2022-release}

### 改進項目

**歷程**

* 為避免統一設定檔綱要存在不必要的欄位，預設情況下不再為設定檔啟用「歷程步驟事件」綱要。 如有需要，可以啟用。 [了解更多](../reports/sharing-overview.md)
* 跟匯出工作有關的新步驟活動現在由 Journey Optimizer 傳送到 Adobe Experience Platform。 已在文件中新增查詢範例。 [進一步了解](../reports/query-examples.md)

**決定管理**

* 現在您可以指定在所有使用者或單個特定設定檔中套用優惠上限設定，以及指定在個別或所有投放位置上套用。[了解更多](../offers/offer-library/add-constraints.md#capping)
* 批次決策 API 允許組織在一次呼叫中對給定區段中的所有設定檔使用 Offer Decisioning 功能。 區段中每個設定檔提供的內容都放在 AEP 資料集，可用於自訂批次處理工作流程。 [進一步了解](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**管理**

* 您現在可以在訊息預設層及在/從電子郵件標題啟用/停用取消訂閱連結，並在訊息層級設定自訂取消訂閱 URL。 [了解更多](../configuration/message-presets.md#list-unsubscribe)
* 現在，可以透過生產或非生產沙箱的 [!DNL Journey Optimizer] 介面啟用或停用允許清單。 [進一步了解](../reports/allow-list.md#enable-allow-list)

**個人化**

* 您現在可以在程式庫中儲存 40 多組個人化運算式。 [了解更多](../personalization/personalization-library.md)

## 2022 年 2 月發佈內容 {#feb-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>訂閱項目登陸頁面</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在 Journey Optimizer 建立並設計登陸頁面，引導您的使用者存取線上表單，以便他們可以選擇加入或選擇退出接收您的通訊，或訂閱電子報等特定服務。</p>
<p>有關詳細資訊，請參閱<a href="../landing-pages/create-lp.md">詳細文件</a>及相關<a href="../landing-pages/lp-use-cases.md">使用範例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>全新個人化運算式資料庫</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer 現在提供資料庫，您可以在其中存取預先定義的個人化運算式。 這些運算式由管理員使用者設定。</p>
<p>如需詳細資訊，請參閱<a href="../personalization/personalization-library.md">詳細文件</a>。</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>傳遞資訊透過 UTM 追蹤參數追蹤郵件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>在 Journey Optimizer 訊息內容中，您現在可以將 UTM 參數加入連結：提供有關該連結的其他資料，幫助您確定某人按下連結的位置及原因。</p>
<p>如需詳細資訊，請參閱<a href="../configuration/message-presets.md#configure-email-settings">詳細文件</a>。</p-->
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* 為了最佳化效能，所有處於測試模式且一週內未觸發的歷程現在將切換回「草稿」狀態。 [閱讀全文](../building-journeys/testing-the-journey.md#important_notes)
* 已最佳化 Journey Optimizer 和 Adobe Campaign Classic 的整合，以便提高效能。 上限預設設定已變更為 4000 次呼叫 / 5 分鐘。	[閱讀全文](../action/acc-action.md#important-notes)

**報告**

* 現在可以根據狀態篩選傳遞：
   * 您現在可以從「訊息執行」清單排除傳遞清單中的證明。
   * 您可以選擇從即時/全域報告排除測試事件。

* 您現在可以存取有關最佳化傳送時間資料的報告：即時訊息的人數，以及經過 1 小時最佳化、2 小時最佳化等訊息的人數。

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**決策管理**

* 排名和 AI 排名現在分類在單一標籤。

## 2022 年 1 月發行版本 {#january-2022-release}

### 新功能

<table>
<thead>
<tr>
<th><strong>歷程 — 使用個人資料上限條件最佳化 IP 提升</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>當在歷程中設定<strong>條件</strong>活動時，您現在可以定義個人資料上限。 此新條件類型允許您為歷程路徑設定個人資料的最大數量。 當達到此限制後，輸入的個人資料將採用替代路徑。 這樣，您就可以提高傳遞量 (IP 提升)。 例如，您可能希望透過分割執行來加快網域上的傳遞量：在第 1 天傳送 1000 則訊息，在第 2 天傳送 2000 則訊息等。</p>
<p>有關詳細資訊，請參閱<a href="../building-journeys/condition-activity.md#profile_cap">詳細文件</a>及相關<a href="../building-journeys/ramp-up-deliveries-uc.md">使用範例</a>。</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>歷程 — 讀取區段改進</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>增量讀取</strong>選項已加入循環<strong>讀取區段</strong>活動。 此選項允許您僅將目標設定在自上次執行歷程以來進入區段的個人。 第一次執行始終將目標設定在所有區段成員。</p>
<p>如需詳細資訊，請參閱<a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">詳細文件</a>。
</td>
</tr>
</tbody>
</table>

### 改進項目

**歷程**

* Journey Optimizer 步驟事件現在可以連結到 [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=zh-Hant) 中的其他資料集。  內建「歷程步驟事件」方案中的 **profileID** 欄位現在定義為身分欄位。 [了解更多](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* 對於在已發佈訊息中直接或間接引用的優惠方案、遞補優惠、優惠收藏或優惠決定，現在將在對應訊息中自動反映您的更新，無需重新發佈。 [了解更多](../offers/offers-e2e.md#insert-decision-in-email)

* 在模擬給定測試設定檔將提供哪些服務時，您現在可以修改預設模擬設定，並針對用於疑難排解的模擬查看對應的代碼。 [進一步了解](../offers/offer-activities/simulation.md#define-simulation-settings)

**管理**

* 管理員現在可以使用 CNAME 設定子網域來編輯 PTR 記錄。 [進一步了解](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**個人化**

* **加入收藏夾** — 為了協助在使用個人化功能時提高效率，我們引進了儲存收藏夾的概念。 將不同屬性加入收藏夾功能表可快速存取您使用頻率最高的項目。 [了解更多](../personalization/personalize.md#fav)
