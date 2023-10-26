---
solution: Journey Optimizer
product: journey optimizer
title: 權限層級
description: 瞭解允許使用者存取不同功能的高和低層級許可權。
topic: Administration
feature: Access Management
role: Admin, Architect, Developer
level: Experienced
keywords: 許可權，高階，低階，設定檔， admin console
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '1116'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每個角色都包含允許使用者存取不同功能的許可權。
它們可以分為兩種型別：

* **高階許可權**：代表可指派給的不同許可權 **[!UICONTROL 角色]**，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高層級許可權包含低層級許可權。 高層級許可權詳見 [此頁面](ootb-permissions.md).

* **低階許可權**：代表來自高階許可權的不同許可權。

例如， **[!DNL Journey administrator]** 角色已指派給 **[!DNL Manage journeys]** 許可權。 此許可權會產生低階許可權，可讓歷程管理員寫入、讀取和刪除歷程。

## 歷程資源 {#journey-capability}

* **[!DNL Manage journeys]** 高階許可權可讓使用者建立新歷程及編輯/刪除現有歷程，以及存取歷程畫布中用來建立歷程流程的物件。

+++ 其中包含下列低階許可權：

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

* **[!DNL Publish journeys]** 高階許可權可讓使用者發佈歷程。

+++ 其中包含下列低階許可權：
   * Journey Optimizer專用：
      * journeys.publish
      * journeys.read

+++

* **[!DNL View journeys]** 高階許可權可讓使用者瀏覽及檢視歷程。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * journeys.read

   * Adobe Experience Platform專用：
      * segments.read
      * profiles.read

+++

* **[!DNL Manage journeys events, data sources and actions]** 高階許可權可讓使用者設定事件和資料設定。

+++ 其中包含下列低階許可權：

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

* **[!DNL View journeys events, data sources and actions]** 高階許可權可讓使用者在歷程流程中使用事件和資料。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * journeys_events.read
      * journeys_data_sources.read
      * journeys_actions.read

   * Adobe Experience Platform專用：
      * schemas.read
      * datasets.read
      * identity_namespace.read

+++

* **[!DNL View journeys report]** 高階許可權可讓使用者以唯讀方式存取歷程報告。

+++ 其中包含下列低階許可權：

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

* **[!DNL Manage frequency rules]** 高階許可權可讓使用者讀取、建立、編輯、刪除和啟用/停用頻率規則。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * frequency_rules.read
      * frequency_rules.write
      * frequency_rules.delete

+++

* **[!DNL View frequency rules]** 高階許可權可讓使用者檢影片率規則。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * frequency_rules.read

+++

## 行銷活動資源 {#campaign-capability}

* **[!DNL Export suppression list]** 高階許可權可讓使用者將隱藏清單下載為CSV檔案。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * 隱藏清單匯出

   * Adobe Experience Platform專用：
      * profiles.read
      * datasets.read

+++

* **[!DNL Manage campaigns]** 高階許可權可讓使用者建立新的和編輯/刪除行銷活動

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：

      * campaign.read
      * campaign.write
      * campaign.delete
     <!--* experiments.read
      * experiments.write
      * experiments.delete-->

+++

* **[!DNL Publish campaigns]** 高階許可權可讓使用者發佈行銷活動。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：

      * campaign-read
      * campaign-publish
        <!--* experiments.activate-->

+++

* **[!DNL View campaigns report]** 高階許可權可讓使用者閱讀及編輯行銷活動報告。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * campaign.read
      * campaign-report.read
     <!--* experiments.read
      * experiments_report.read-->

+++

## 決定管理資源 {#decisions-permissions}

* **[!DNL Manage decisions]** 高階許可權可讓使用者建立新專案和編輯/刪除現有專案 **[!DNL Activity entities]**，以及管理用於這些活動中以做出決定的物件。

+++ 其中包含下列低階許可權：

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

* **[!DNL View decisions]** 高階許可權可讓使用者使用現有的活動和相關商業物件來做出決策。

+++ 其中包含下列低階許可權：

   * 特定決策管理：
      * activities.read
      * offers.read
      * placements.read
      * ranking_strategy.read

   * Adobe Experience Platform專用：
      * schemas.read
      * segment.read
      * datasets.read
      * datasets.write
      * datasets.delete

+++

* **[!DNL Manage offers]** 高階許可權可讓使用者建立、編輯和刪除所有優惠、元件、讀取決定和集合。

+++ 其中包含下列低階許可權：

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

* **[!DNL Manage ranking strategies]** 高階許可權可讓使用者讀取、建立、編輯和刪除排名策略。

+++ 其中包含下列低階許可權：

   * 特定決策管理：
      * ranking_strategy.read
      * ranking_strategy.write
      * ranking_strategy.delete
      * activities.read
      * offers.read
      * placements.read

+++

## 頻道設定資源 {#administration-permissions}

* **[!DNL Manage channel surface]** 高階許可權可讓使用者在沙箱層級建立、編輯和刪除跨頻道的頻道介面。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read
      * mobile_setting.read (來自Adobe Experience Platform Launch)

+++

* **[!DNL Manage IP pools]** 高階許可權可讓使用者建立、編輯和刪除相似性定義。

+++ 其中包含下列低階許可權：
   * Journey Optimizer專用：
      * IP_pools.read
      * IP_pools.write
      * IP_pools.delete

+++

* **[!DNL Manage landing page settings]** 高階許可權可讓使用者讀取、建立及編輯登陸頁面子網域和預設集設定。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：

      * landing_page_subdomain.read
      * landing_page_subdomain.write
      * landing_page_subdomain.delete
      * landing_page_preset.read
      * landing_page_preset.write
      * landing_page_preset.delete

+++

* **[!DNL Manage messages general settings]** 高階許可權可讓使用者在沙箱層級建立、編輯和刪除全域設定。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * messages_general_settings.read
      * messages_general_settings.write
      * messages_general_settings.delete

   * Adobe Experience Platform專用：
      * schemas.read

+++

* **[!DNL Manage messages presets]** 高階許可權可讓使用者讀取、建立、編輯和刪除內容品牌。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * messages_presets.read
      * messages_presets.write
      * messages_presets.delete
      * subdomains_delegation.read
      * IP_pools.read

   * 資料收集特定：
      * Mobile_setting.read

+++

* **[!DNL Manage PTR records]** 高階許可權可讓使用者讀取和編輯已根據子網域設定的PTR記錄。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * PTR_records.read
      * PTR_records.write
      * subdomains_delegation.read

+++

* **[!DNL Manage Seedlist]** 高階許可權可讓使用者讀取、建立、編輯和刪除Seedlist。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * seedlist.read
      * seedlist.write
      * seedlist.delete

+++

* **[!DNL Manage SMS subdomains]** 高階許可權可讓使用者讀取、建立、編輯和刪除SMS子網域。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * sms_subdomains.read
      * sms_subdomains.write
      * sms_subdomains.delete

+++

* **[!DNL Manage subdomains delegation]** 高階許可權可讓使用者建立、編輯和刪除子網域委派（包括IP集區）。

+++ 其中包含下列低階許可權：
   * Journey Optimizer專用：

      * subdomains_delegation.read
      * subdomains_delegation.write
      * subdomains_delegation.delete

+++

* **[!DNL Manage suppression]** 高階許可權可讓使用者定義將電子郵件地址新增至隱藏清單前的跳出次數，以及在隱藏清單中新增和刪除專案。

+++ 其中包含下列低階許可權：
   * Journey Optimizer專用：
      * suppression_rules.read
      * suppression_rules.write
      * suppression_rules.delete
      * suppression_list.write
      * suppression_list.delete

+++

* **[!DNL View PTR records]** 高階許可權可讓使用者檢視已根據子網域設定的PTR記錄。

+++ 其中包含下列低階許可權：
   * Journey Optimizer專用：

      * PTR_records.read
      * subdomains_delegation.read

+++

* **[!DNL View messages general settings]** 高階許可權可讓使用者檢視訊息的一般設定，例如執行地址。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * messages_general_settings.read

   * Adobe Experience Platform專用：
      * schemas.read

+++

* **[!DNL View messages presets]** 高階許可權可讓使用者檢視訊息預設集。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * messages_presets.read
      * subdomains_delegation.read
      * IP_pools.read

   * 資料收集特定：
      * Mobile_setting.read

+++
<!--
### [!DNL View channel surface] permission {#view-channel-surface}

The **[!DNL View channel surface]** high-level permission allows users to view channel surfaces in order to know which channel surfaces to use. 
  +++ It includes the following low-level permissions:  

* messages_presets.read
* subdomains_delegation.read
* IP_pools.read
* mobile_setting.read (from Adobe Experience Platform Data Collection)
-->


* **[!DNL View suppression list]** 高階許可權可讓使用者檢視隱藏清單內容和設定。

+++ 其中包含下列低階許可權：

   * Journey Optimizer專用：
      * suppression_list.view

   * Adobe Experience Platform專用：
      * profiles.read
      * datasets.read

+++

<!--
### Manage web subdomain permission {#web-subdomain}

The **[!DNL Manage web subdomain]** high-level permission allows users to read, create, edit, and delete web subdomains.

  +++ It includes the following low-level permissions: 
-->

