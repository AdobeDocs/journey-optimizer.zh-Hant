---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer 搶鮮版發行說明
description: Adobe Journey Optimizer 搶鮮版發行說明
feature: Release Notes
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
TQID: https://experienceleague.adobe.com/951PJzmmITN1nSUapVomlYnPws9pS0TosI1Gl3R9yL4
hide: true
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a7b2bfc5-be71-4740-b371-76fa6be8df02
subfeature_v2: id: eac3bd2c-b027-4dfa-80d2-0bd752ae4794id: e437f8db-d1f7-44c0-bdc0-b0a361adc4c0id: c4e1378f-bb85-43a2-8b7c-1623ad3b14b5
source-git-commit: 6e665528805269903885ba9ba3f958de3f4374f4
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 32%

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


### 行銷活動 {#july-26-campaigns}

下列功能和改善專案已新增至此版本中的行銷活動。

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
</td>
</tr>
</tbody>
</table>
-->

### 協調的行銷活動 {#july-26-oc}

下列改善專案已新增至此版本中的協調行銷活動。

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

* **Send messages in waves** - You can now schedule outbound messages from orchestrated campaigns to be delivered in controlled batches over time. Ideal for high-volume or time-sensitive campaigns, wave sending also supports better deliverability and helps maintain a strong sender reputation by reducing the risk of being flagged as spam.

-->

### 管道 {#july-26-channels}

下列功能和改進專案已新增到此版本中的管道。

### 決策 {#july-26-decisioning}

下列改善專案已新增至此版本中的決策。

<!--
* **Placement-level frequency capping in Decisioning** - Frequency capping rules in Decisioning can now be scoped to individual placements, giving you finer control over how often an offer is shown in a given surface. Two modes are available: placement-specific capping (define a cap that applies only when the offer is displayed in a selected placement) and per-placement capping (apply a cap independently across every placement where the offer appears, so each placement maintains its own capping counter). Documentation link: TBD
-->

### 內容管理 {#july-26-content}

下列改善專案已新增至此版本的內容管理。

<!--
### Integrations {#july-26-integrations}

The following improvements have been added to integrations in this release.

* **Real-time countdown timers for Adobe Experience Manager Dynamic Media integration** - Marketers can now build countdown timers as Dynamic Media templates in Adobe Experience Manager and pull them directly into Journey Optimizer. Timers render live at the moment of open, so every recipient sees an accurate countdown, not a static image. Configure dates, styling, and fallback values right within the Journey Optimizer editor to power flash sales and limited-time offers. [Documentation link: TBD]
-->

### 個人化 {#july-26-personalization}

下列改善專案已新增至此版本中的個人化。


### 電子郵件設計工具 {#july-26-email}

下列功能已新增至此版本的電子郵件通道。


### 管理 {#july-26-administration}

下列功能已新增至此版本的管理中。


### 可用性改進功能 {#july-26-usability}

此版本即將推出下列可用性改善。

* 內容範本中SMS、推播、應用程式內和程式碼基底頻道的&#x200B;**快速啟動捷徑** — 「內容範本」清單中的&#x200B;**更多動作**&#x200B;按鈕現在提供其他頻道特定捷徑。 對於SMS範本，請快速編輯訊息或檢查字元計數/區段。 對於推播範本，請編輯標題、本文或媒體。 針對應用程式內範本，請編輯訊息標頭、訊息本文或媒體URL。 對於程式碼基底通道範本，請直接編輯程式碼。 這些捷徑可擴充現有的電子郵件頻道快速啟動捷徑。<!-- Documentation link: TBD -->
