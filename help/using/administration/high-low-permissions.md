---
solution: Journey Optimizer
product: journey optimizer
title: 權限層級
description: 瞭解允許使用者存取不同功能的高階和低階許可權。
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: 許可權，高階，低階，設定檔， admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '1301'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}


每個角色都包含允許使用者存取不同功能的許可權。

它們可以分為兩種型別：

* **高階許可權**：代表可指派給&#x200B;**[!UICONTROL 角色]**&#x200B;的不同許可權，例如&#x200B;**[!DNL Publish journeys]**&#x200B;和&#x200B;**[!DNL Manage subdomains delegation]**。 高階許可權包括低階許可權。 在[此頁面](ootb-permissions.md)上詳細說明了高階許可權。

* **低階許可權**：代表來自高階許可權的不同許可權。

例如，**[!DNL Journey administrator]**&#x200B;角色已指派&#x200B;**[!DNL Manage journeys]**&#x200B;許可權。 此許可權會產生低階許可權，可讓歷程管理員寫入、讀取和刪除歷程。

![](assets/do-not-localize/permissions.png){width="70%"}


## 歷程資源 {#journey-capability}

* **[!DNL Manage journeys]**&#x200B;高階許可權可讓使用者建立新的和編輯/刪除現有的歷程，以及存取歷程畫布中用來建立歷程流程的物件。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * journeys.read
      * journeys.write
      * journeys.delete
      * messages.read

   * Adobe Experience Platform專用：

      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read

+++

* **[!DNL Publish journeys]**&#x200B;高階許可權可讓使用者發佈歷程。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]**&#x200B;高階許可權可讓使用者瀏覽及檢視歷程。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * journeys.read

   * Adobe Experience Platform專用：
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]**&#x200B;高階許可權可讓使用者設定事件和資料設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * journeys_events.read
      * journeys_events.write
      * journeys_events.delete
      * journeys_data_sources.read
      * journeys_data_sources.write
      * journeys_data_sources.delete
      * journeys_actions.read
      * journeys_actions.write
      * journeys_actions.delete

   * Adobe Experience Platform專用：
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys events, data sources and actions]**&#x200B;高階許可權可讓使用者在歷程流程中使用事件和資料。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read

   * Adobe Experience Platform專用：
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]**&#x200B;高階許可權可讓使用者以唯讀方式存取歷程報告。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * journeys_report.read
      * messages_report.read

   * Adobe Experience Platform專用：
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++

## Journey Optimizer規則資源 {#journey-rules-capability}

* **[!DNL Manage frequency rules]**&#x200B;高階許可權可讓使用者讀取、建立、編輯、刪除和啟用/停用頻率規則。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]**&#x200B;高階許可權可讓使用者檢影片率規則。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * frequency_rules.read

+++

## 行銷活動資源 {#campaign-capability}

* **[!DNL Export suppression list]**&#x200B;高階許可權可讓使用者將隱藏清單下載為CSV檔案。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * 隱藏清單匯出

   * Adobe Experience Platform專用：
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]**&#x200B;高階許可權可讓使用者建立新的和編輯/刪除行銷活動

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]**&#x200B;高階許可權可讓使用者發佈行銷活動。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]**&#x200B;高階許可權可讓使用者閱讀及編輯行銷活動報告。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## 決定管理資源 {#decisions-permissions}

* **[!DNL Manage decisions]**&#x200B;高階許可權可讓使用者建立新的和編輯/刪除現有的&#x200B;**[!DNL Activity entities]**，以及管理這些活動中用來做決定的物件。

+++ 此許可權包括下列低階許可權：

   * 特定決策管理：
      * activities.read
      * activities.write
      * activities.delete
      * offers.read
      * offers.write
      * offers.delete
      * placements.read
      * placements.write
      * placements.delete
      * ranking_strategy.read

   * Adobe Experience Platform專用：
      * datasets.read
      * datasets.write
      * datasets.delete
      * schemas.read
      * profile.read
      * segments.read

+++

* **[!DNL View decisions]**&#x200B;高階許可權可讓使用者使用現有的活動和相關商業物件來做出決定。

+++ 此許可權包括下列低階許可權：

   * 特定決策管理：
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Adobe Experience Platform專用：
      * schemas.read
      * segment.read
      * datasets.read

+++

* **[!DNL Manage offers]**&#x200B;高階許可權可讓使用者建立、編輯和刪除所有優惠、元件、讀取決定和集合。

+++ 此許可權包括下列低階許可權：

   * 特定決策管理：
      * offers_activity.read
      * offers.read
      * offers.Write
      * offers.Delete
      * placements.Read
      * placements.Write
      * placements.Delete
      * ranking_strategy.read

   * Adobe Experience Platform專用：
      * schemas.read
      * segment.read
      * datasets.read
      * profiles.read

+++

* **[!DNL Manage ranking strategies]**&#x200B;高階許可權可讓使用者讀取、建立、編輯和刪除排名策略。

+++ 此許可權包括下列低階許可權：

   * 特定決策管理：
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## 頻道設定資源 {#administration-permissions}

<!--
* **[!DNL Manage Experience decisions]** high-level permission allows users to read, create, edit, and delete Decisioning entities.

  +++ This permission includes the following low-level permissions:  

  * Experience decisions specific:
    * ranking_strategy.read
    * offeritem.read
    * offeritem.write
    * offeritem.delete
    * itemCollection.read
    * itemCollection.write
    * itemCollection.delete
    * SelectionStrategy.read
    * SelectionStrategy.write
    * SelectionStrategy.delete
    * Decisionpolicy.read
    * Decisionpolicy.write
    * Decisionpolicy.delete
  +++
-->

* **[!DNL Manage file routing]**&#x200B;高階許可權可讓使用者建立、編輯和刪除檔案路由設定。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：

      * file_routing.read
      * file_routing.write
      * file_routing.delete

+++

* **[!DNL Manage IP pools]**&#x200B;高階許可權可讓使用者建立、編輯和刪除相似性定義。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]**&#x200B;高階許可權可讓使用者讀取、建立及編輯登陸頁面子網域和預設集設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]**&#x200B;高階許可權可讓使用者在沙箱層級建立、編輯和刪除全域設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Adobe Experience Platform專用：
      * schemas.read

+++

* **[!DNL Manage messages presets]**&#x200B;高階許可權可讓使用者在沙箱層級讀取、建立、編輯和刪除跨頻道的頻道設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * 資料收集特定：
      * Mobile_setting.read <!--(from Adobe Experience Platform Launch)-->

+++

* **[!DNL Manage PTR records]**&#x200B;高階許可權可讓使用者讀取和編輯已根據子網域設定的PTR記錄。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]**&#x200B;高階許可權可讓使用者讀取、建立、編輯及刪除Seedlist。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]**&#x200B;高階許可權可讓使用者讀取、建立、編輯及刪除SMS子網域。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegations]**&#x200B;高階許可權可讓使用者建立、編輯和刪除子網域委派（包括IP集區）。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]**&#x200B;高階許可權可讓使用者定義電子郵件地址新增至隱藏清單前的跳出次數，以及新增和刪除隱藏清單中的專案。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View file routing]**&#x200B;高階許可權可讓使用者檢視檔案路由設定。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：

      * file_routing.read

+++

* **[!DNL View messages general settings]**&#x200B;高階許可權可讓使用者檢視訊息的一般設定，例如執行位址。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * messages_general_settings.read

   * Adobe Experience Platform專用：
      * schemas.read

+++

* **[!DNL View messages presets]**&#x200B;高階許可權可讓使用者檢視訊息預設集。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * 資料收集特定：
      * Mobile_setting.read

+++

* **[!DNL View PTR records]**&#x200B;高階許可權可讓使用者檢視已根據子網域設定的PTR記錄。

+++ 此許可權包括下列低階許可權：
   * Journey Optimizer專用：

      * PTR_records.read
      * subdomains_delegation.read

+++

<!--
### [!DNL View channel configuration] permission {#view-channel-surface}

The **[!DNL View channel configuration]** high-level permission allows users to view channel configurations in order to know which channel configurations to use. 
  +++ This permission includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]**&#x200B;高階許可權可讓使用者檢視隱藏清單內容與設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：
      * suppression_list.view

   * Adobe Experience Platform專用：
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ This permission includes the following low-level permissions: 
-->

## AI協助資源 {#ai-permissions}

* **[!DNL Generate content]**&#x200B;高階許可權可讓使用者存取Journey Optimizer中的AI助理。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * ai-assistant-generated-content.generate

+++

## 協調的行銷活動資源 {#ai-orchestrated-campaign}

* **[!DNL Manage orchestrated campaigns]**&#x200B;高階許可權可讓使用者建立新的及編輯/刪除協調的行銷活動。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * orchestrated_campaigns.read
      * orchestrated_campaigns.write
      * orchestrated_campaigns.delete
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.write
      * cjm-message.delete
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * cjm-message-preview-test.write
      * experiment.read
      * experiment.write
      * experiment.delete

   * Adobe Experience Platform專用：

      * identity-graph.read
      * segments.read
      * profiles.read
      * datasets.read
      * schemas.read
      * sandboxes.view

+++

* **[!DNL Manage orchestrated campaigns admin]**&#x200B;高階許可權可讓使用者在Adobe Experience Platform設定檔與關聯式存放區實體之間建立新連結，以及編輯/刪除連結與調解。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * cjm-orchestrated-campaign-admin.read
      * cjm-orchestrated-campaign-admin.write
      * cjm-orchestrated-campaign-admin.delete

+++

* **[!DNL Publish orchestrated campaigns]**&#x200B;高階許可權可讓使用者發佈協調的行銷活動。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * cjm-orchestrated-campaign.read
      * cjm-orchestrated-campaign.publish
      * cjm-web-subdomain.read
      * cjm-message.read
      * cjm-message.publish
      * cjm-library-item.read

   * Adobe Experience Platform專用：

      * sandboxes.view

+++

* **[!DNL View orchestrated campaigns]**&#x200B;高階許可權可讓使用者檢視協調的行銷活動及其內容。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * cjm-message-general-setting.read
      * cjm-message-preset.read
      * experiment.read

   * Adobe Experience Platform專用：

      * sandboxes.view
      * segments.read
      * profiles.read

+++

* **[!DNL View orchestrated campaigns admin]**&#x200B;高階許可權可讓使用者檢視管理員設定，但無法編輯設定。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * cjm-orchestrated-campaign-admin.read

+++

* **[!DNL View orchestrated campaigns report]**&#x200B;高階許可權可讓使用者在即時和商務報告中檢視協調的行銷活動績效。

+++ 此許可權包括下列低階許可權：

   * Journey Optimizer專用：

      * cjm-orchestrated-campaign-reports.read
      * cjm-message-report.read
      * cjm-channel-report.read
      * cjm-orchestrated-campaign.read
      * cjm-message.read
      * cjm-library-item.read
      * experiment.read
      * experiment-report.read

   * Adobe Experience Platform專用：

      * sandboxes.view
      * datasets.read
      * queries.read
      * queries.write
      * queries.delete

+++
