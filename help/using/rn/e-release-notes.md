---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: a0bba0ee8c2f7623d7cf7053b0c8dfc215b45fe0
workflow-type: tm+mt
source-wordcount: 744
ht-degree: 18%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

## 2026年8月發行前注意事項 {#august-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年8月18至19日

<!--
### Onboarding {#august-26-onboarding}

The following capability is coming to onboarding in this release.

<table>
<thead>
<tr>
<th><strong>Guided capabilities for onboarding emails and journeys (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 歷程 {#august-26-journeys}

下列功能和改進功能將新增到此版本的歷程。

<table>
<thead>
<tr>
<th><strong>歷程層級保留（可用性限制）</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以直接從歷程屬性設定歷程的保留群組。 保留是目標受眾中可設定的百分比，會排除在進入歷程之外且不會收到任何通訊。 將保留設定檔與Customer Journey Analytics報告中的作用中設定檔進行比較，即可測量歷程帶來的增量提升度（實際影響）。</p>
<p> 此功能僅適用於一組組織 (可用性限制)。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **在歷程運算式編輯器中加入新的dateDiff函式** — 歷程運算式編輯器現在包含`dateDiff`函式，該函式會以天數計算兩個日期之間的差異。 此函式適用於以時間為基礎的邏輯，例如建立截止日期、計算客戶生命週期持續時間或在歷程條件中建立倒數計時器。<!-- Documentation link: TBD -->

* **歷程標題中的開始和結束日期** — 當在歷程上設定開始和/或結束日期時，它們現在會出現在狀態徽章旁邊的歷程標題中。 顯示的標籤會根據每個日期是近期到來或已過去而調整。<!-- Documentation link: TBD -->

### 管道 {#august-26-channels}

此版本中的Campaigns即將進行下列改進：

* **即時活動執行中繼資料(executionMetadata)** - API觸發的即時活動行銷活動（交易和行銷）現在支援每個收件者的可選executionMetadata欄位。 這可讓您將自訂索引鍵/值資料（例如訂單ID、忠誠度層級或區域代碼）附加至執行。

### 行銷活動 {#august-26-camp}

此版本中的行銷活動推出下列功能和改善。

<table>
<thead>
<tr>
<th><strong>Action Campaigns中的傳入體驗模擬</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>您現在可以在上線前在「動作行銷活動」中模擬傳入頻道動作。 使用模擬模式透過模擬使用者測試您的設定並預覽呈現的體驗，包括產生的URL和QR碼，因此您可以端對端驗證規則、決策和內容呈現。</p>
<p>此功能目前為私人測試版，僅供有限的組織使用。 請聯絡您的 Adobe 代表以取得更多資訊。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **Action Campaign編寫流程重新設計** - Adobe Journey Optimizer Action Campaign編寫流程已重新設計，以提供更直覺、更有效率且順暢的使用者體驗。

* **動作行銷活動的資料夾** — 您現在可以將動作行銷活動整理到資料夾中，以改善介面中的導覽和管理。<!-- Documentation link: TBD -->

<!--* **Brand alignment score in Action Campaign dashboard** - You can now assess your brand alignment score directly within your Action Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.  Documentation link: TBD -->

* **覆寫動作行銷活動中的預設執行欄位** — 您現在可以覆寫動作行銷活動引數中針對電子郵件、簡訊和WhatsApp傳遞全域設定的預設執行欄位（先前可在歷程層級使用）。<!-- Documentation link: TBD -->

### 決策 {#august-26-decisioning}

此版本中的決定即將提供下列功能和改善。

<table>
<thead>
<tr>
<th><strong>Web Channel中的決策支援</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning現在可用於Web管道。 您可以直接在網頁視覺化編輯器中使用決定原則，將最相關的選件傳送給每位訪客。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **決策中的版位層級頻率上限** — 決策中的頻率上限規則現在可以將範圍限定於個別版位，讓您更能掌控優惠方案在指定介面中的顯示頻率。 有兩種模式可供使用：版位特定上限，定義只適用於所選版位中顯示優惠方案的上限；以及每次版位上限，會針對出現優惠方案的每個版位獨立套用上限，因此每個版位都會維持其自己的上限計數器。 請注意，與位置相關的上限不適用於使用以Adobe Experience Platform資料為基礎的規則來設定上限的優惠方案。<!-- Documentation link: TBD -->

### 管理 {#august-26-administration}

此版本中的管理即將進行下列改進。

* **自訂子網域的Feedback Loop OTP程式** — 直接在產品UI中顯示Yahoo寄件者中心一次性密碼(OTP)，已改善Feedback Loop (FBL)自訂子網域設定程式。 使用者現在可以自動擷取及顯示Yahoo寄件者中心網域擁有權驗證期間產生的OTP。<!-- Documentation link: TBD -->

<!--

## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->


