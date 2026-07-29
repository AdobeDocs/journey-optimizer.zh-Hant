---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2:
  - id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794
  - id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0
  - id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: c58b70fa5f792e2fa1448034559ad7210e3e10d4
workflow-type: tm+mt
source-wordcount: 967
ht-degree: 21%

---


# 搶鮮版發行說明 {#e-release-notes}

Adobe Journey Optimizer 持續提供新功能、現有功能的增強功能並修正錯誤。 所有變更都會在每月底整合於[發行說明](release-notes.md)。

<!--
## June '26 pre-release notes {#june-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published once changes are live in production. While most changes are delivered on the release date, a few may roll out later — refer to the Availability Date listed for each entry for details.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: June 16-17, 2026

### Journeys {#june-26-journeys}

The following capabilities and improvements are coming to journeys in this release.

<table>
<thead>
<tr>
<th><strong>Channel optimization (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add multiple outbound channels (Email, Push, SMS) to a single journey action and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available: manual ranking, customer profile preference (XDM attribute), and AI model-based ranking using propensity scores. When the top-ranked channel is unavailable, the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../building-journeys/channel-optimization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

* **Increased live journey limit and new guardrails** - You can now have up to **200 active journeys**, increased from the previous limit of 100.



### Orchestrated campaigns {#june-26-oc}

The following capabilities and improvements are coming to orchestrated campaigns in this release.

-->

## 2026年7月發行前注意事項 {#july-26-rn}

**至發行日期之前，下方搶鮮版發行說明如有變更，恕不另行通知**。 連結、畫面和更新的文件會在變更上線生產時發佈。 雖然大多數變更會在發行日期提供，但有些可能會稍後推出。

另請參閱 [Adobe Experience Platform 預發行說明](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}。

**發行日期**： 2026年7月28至29日

<!--

### Onboarding {#july-26-onboarding}

Journey Optimizer introduces the Onboarding Assistant, a new capability in this release.

<table>
<thead>
<tr>
<th><strong>Onboarding Assistant</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Transitioning to Adobe Journey Optimizer from another marketing platform is easier with guided capabilities that help you move existing email content and journeys into Journey Optimizer. A dedicated workspace lets you reuse what you have instead of rebuilding from scratch.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<GIF placeholder: to be added>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

-->

### 歷程 {#july-26-journeys}

下列改善專案已新增至此版本中的歷程。

<!-- Documentation link: TBD -->

### 行銷活動 {#july-26-campaigns}

下列功能和改善專案已新增至此版本中的行銷活動。

<table>
<thead>
<tr>
<th><strong>API觸發的電子郵件中的個人化PDF附件</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在支援在API觸發的行銷活動中，每封電子郵件最多附加5個收件者特定PDF。 PDF檔案會從Azure或AWS儲存空間中安全地擷取，並在傳送時附加，每個檔案的位置都直接在API裝載中傳遞。 這可讓現有的上游檔案產生系統維持原狀，由Journey Optimizer處理傳送。</p>
<p>支援的使用案例包括發票、對帳單、票證、合約、出貨標籤，以及依收件者而異的類似檔案。 個人化PDF附件僅適用於API觸發的行銷活動，在歷程或其他行銷活動型別（動作、協調）中不支援。</p>
<p>PDF附件附加元件支援較大的附件數量與大小；如需詳細資訊，請聯絡您的Adobe代表。</p>
<p></p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Inbound experience simulation in Action campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now simulate inbound channel actions in Action campaigns before going live. Use simulation mode to test your configuration with simulated users and preview the rendered experience, including a generated URL and QR code, so you can validate rules, decisioning, and content rendering end-to-end.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
[GIF placeholder: to be added]
[Documentation link: TBD]
</td>
</tr>
</tbody>
</table>

-->

### 協調的行銷活動 {#july-26-oc}

下列改善專案已新增至此版本中的協調行銷活動。


<!--
* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.
-->

<!--
### Optimization {#july-26-optimization}

<table>
<thead>
<tr>
<th><strong>Channel optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now configure a journey or campaign action to include multiple outbound channels (Email, Push, SMS) and let Journey Optimizer automatically deliver through the best channel for each customer. Three optimization modes are available:</p>
<ul>
<li>Manual ranking: specify your preferred channel order.</li>
<li>Customer preference: use the customer's preferred channel from their profile (Experience Data Model Consents & Preferences attribute).</li>
<li>AI model-based ranking: use machine learning propensity scores to infer the most effective channel per customer.</li>
</ul>
<p>When the top-ranked channel is unavailable (not opted-in, frequency-capped, or not configured), the system falls back to the next available channel.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>
-->

<!--
<table>
<thead>
<tr>
<th><strong>Quiet Hours support for orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now apply quiet hours to Orchestrated campaigns. Quiet hours let you define time-based exclusions to prevent messages from being sent during specific periods, helping you respect customer preferences and compliance requirements across campaign orchestration use cases.</p>
<Documentation link: TBD>
</td>
</tr>
</tbody>
</table>

* **Ability to Manage Profile Target Dimensions** - You can now delete a Profile Target Dimension or edit and swap its configured identity namespace, providing greater control and flexibility over your data setups.

* **Support for Line** - You can now add LINE actions directly into your Orchestrated campaigns. This new activity allows you to build and deliver highly personalized content, including text, stickers, images, videos, location data, and rich Flex Messages, to engage your customers seamlessly on the LINE platform. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

* **New Orchestrated campaigns public APIs** - New API specifications are now available for Orchestrated campaigns. These APIs allow you to programmatically create, manage, and trigger orchestrated campaigns, enabling deeper integration with external systems and automation pipelines.

* **Personalize email sender details per recipient and campaign** - Orchestrated campaigns now support personalization of email header fields, including From name, From address, and Reply-To, using profile attributes or relational data. This allows sender details to reflect the relevant advisor, location, or branch for each recipient, rather than routing all sends through a single corporate address. Header values can be set at the channel level and overridden per campaign using contextual data for more precise control. Documentation link: TBD

* **Target dimension simplification in Orchestrated campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.

-->

### 管道 {#july-26-channels}

下列功能和改進專案已新增到此版本中的管道。

<table>
<thead>
<tr>
<th><strong>自訂傳出頻道</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer現在推出自訂管道，這項新功能可讓管理員透過無程式碼管道產生器，將任何外寄的HTTP傳訊管道（例如WeChat、Kakao Talk、Messenger或專屬提供者）直接帶入Journey Optimizer。</p >
<p>設定之後，便可在各種行銷活動、歷程和精心安排的行銷活動中使用自訂管道，並提供與原生管道相同的完整功能集：使用運算式編輯器進行個人化、內容實驗、預覽和校樣、現成可用的報告，以及同意和治理實施。</p>
<p>這填補了先前由自訂動作填補的空白，這些動作僅限於歷程，且缺乏專用頻道功能。</p>
<p>自訂傳出頻道目前以「有限可用性」的形式提供。 若想取得存取權，請聯絡您的 Adobe 代表。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

* **輸送量的效能附加元件 — 推播** — 在API觸發的行銷活動中提供新的高輸送量異動訊息模式。 此模式專為大規模即時交易型傳訊而設計，最高可支援每秒 5,000 筆交易，而且可用性更高。 此功能先前僅適用於電子郵件頻道，現在也可用於推播頻道，適用於已購買Adobe高輸送量異動訊息附加元件產品的組織。 如需詳細資訊，請聯絡您的Adobe代表。<!-- Documentation link: TBD -->



### 決策 {#july-26-decisioning}

下列改善專案已新增至此版本中的決策。

* **優惠層級的Personalization** — 決策專案自訂屬性現在可以在傳送時使用設定檔、情境和對象資料進行個人化。 如此一來，行銷人員就不需要針對次要內容變數維持重複的優惠方案，而能夠管理較少、較靈活的決策專案。<!-- Documentation link: TBD -->

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 內容管理 {#july-26-content}

下列改善專案已新增至此版本的內容管理。

* **電子郵件範本**&#x200B;的`<head>`支援運算式片段 — 現在可以在電子郵件範本的`<head>`中使用運算式片段。 這可讓您集中處理單一片段中的樣式或任何自訂程式碼，並在多個範本中重複使用。 更新並重新發佈片段時，所有根據範本建立的電子郵件都會自動繼承最新的程式碼，無需手動個別更新每封電子郵件。<!-- Documentation link: TBD -->
<!-- Documentation link: TBD -->



<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 個人化 {#july-26-personalization}

下列改善專案已新增至此版本中的個人化。

* **管理完整/基本URL個人化的網域** — 您現在可以直接從Adobe Journey Optimizer中的管理設定建立和管理核准的完整和基本URL個人化的網域，而無需連絡Adobe支援。<!-- Documentation link: TBD -->

<!-- Documentation link: TBD -->

### 電子郵件設計工具 {#july-26-email}

下列功能已新增至此版本的電子郵件通道。

<table>
<thead>
<tr>
<th><strong>電子郵件設計工具中的模組</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>電子郵件設計工具現在包含現成可用的版面模組 (例如頁首、產品卡、資訊區塊和頁尾) 資料庫，您可以將這些模組直接拖放到電子郵件畫布中。</p>
<p>每個模組都預先設定了可編輯的屬性 (影像、標題、文字、按鈕、連結)，並可透過 WYSIWYG 介面完全自訂，因此無需您從頭開始建立結構，即可加速電子郵件的建立。</p>
<!-- GIF placeholder: to be added -->
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>


### 管理 {#july-26-administration}

下列功能已新增至此版本的管理中。

<table>
<thead>
<tr>
<th><strong>Web應用程式防火牆IP白名單</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer現在支援將登入頁面列入Web應用程式防火牆IP白名單，方便組織強制要求所有傳入要求都透過其設定的Web應用程式防火牆基礎架構專門路由。 透過這項增強功能，客戶可設定Journey Optimizer以拒絕任何略過Web應用程式防火牆層的直接請求，確保一致套用Imperva等工具中定義的安全性原則。</p>
<p>此功能可加強具有嚴格網路存取需求之企業的安全狀況，讓企業能夠完全控制其Journey Optimizer託管登陸頁面的流量。</p>
<!-- Documentation link: TBD -->
</td>
</tr>
</tbody>
</table>

### 可用性改進功能 {#july-26-usability}

此版本即將推出下列可用性改善。

* 內容範本中SMS、推播、應用程式內和程式碼基底頻道的&#x200B;**快速啟動捷徑** — 「內容範本」清單中的&#x200B;**更多動作**&#x200B;按鈕現在提供其他頻道特定捷徑。 對於SMS範本，請快速編輯訊息或檢查字元計數/區段。 對於推播範本，請編輯標題、本文或媒體。 針對應用程式內範本，請編輯訊息標頭、訊息本文或媒體URL。 對於程式碼基底通道範本，請直接編輯程式碼。 這些捷徑可擴充現有的電子郵件頻道快速啟動捷徑。<!-- Documentation link: TBD -->
