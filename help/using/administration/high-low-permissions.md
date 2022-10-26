---
solution: Journey Optimizer
product: journey optimizer
title: 權限層級
description: 了解高和低層權限
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每個產品設定檔都包含允許使用者存取不同功能的權限。
可分為兩種類型：

* **高級權限**:代表可指派給的不同權限 **[!UICONTROL 產品設定檔]** 在 [!DNL Admin console]，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**. 高階權限包含低階權限。

* **低階權限**:代表來自高階權限的不同權限。

例如， **[!DNL Journey administrator]** 已指派產品設定檔 **[!DNL Manage journeys]** 權限。 從此權限會產生低階權限，讓歷程管理員可編寫、讀取和刪除歷程。

## 歷程功能 {#journey-capability}

### [!DNL Manage journeys] 權限 {#manage-journeys}

此 **[!DNL Manage journeys]** 高階權限可讓使用者建立新的和編輯/刪除現有的歷程，以及存取歷程畫布中用來建立歷程流程的物件。

其中包含下列低階權限：

* Journey Optimizer特定：

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform特定：

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] 權限 {#publish-journeys}

此 **[!DNL Publish journeys]** 高階權限可讓使用者發佈歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 權限 {#view-journeys}

此 **[!DNL View journeys]** 高階權限可讓使用者瀏覽及檢視歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 權限 {#manage-journeys-events}

此 **[!DNL Manage journeys events, data sources and actions]** 高階權限可讓使用者設定事件和資料設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_events.write
   * journeys_events.delete
   * journeys_data_sources.read
   * journeys_data_sources.write
   * journeys_data_sources.delete
   * journeys_actions.read
   * journeys_actions.write
   * journeys_actions.delete

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys events, data sources and actions] 權限 {#view-journeys-event}

此 **[!DNL View journeys events, data sources and actions]** 高階權限可讓使用者在歷程流程中使用事件和資料。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### [!DNL View journeys report] 權限 {#view-journeys-report}

此 **[!DNL View journeys report]** 高階權限可讓使用者以唯讀的歷程報告。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys_report.read
   * messages_report.read

* Adobe Experience Platform特定：
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 決策管理能力 {#decisions-permissions}

### [!DNL Manage decisions] 權限 {#manage-decisioning}

此 **[!DNL Manage decisions]** 高階權限可讓使用者建立新項目，以及編輯/刪除現有項目 **[!DNL Activity entities]**，以及管理用於這些活動中以做出決策的物件。

其中包含下列低階權限：

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

* Adobe Experience Platform特定：
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] 權限 {#view-decisions}

此 **[!DNL View decisions]** 高級權限允許用戶使用現有活動和相關業務對象進行決策。

其中包含下列低階權限：

* 特定決策管理：
   * activities.read
   * offers.read
   * placements.read
   * ranking_strategy.read

* Adobe Experience Platform特定：
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] 權限 {#publish-decisions}

此 **[!DNL Publish offers decisioning]** 高階權限可讓使用者存取核准/取消核准優惠方案活動。

其中包含下列低階權限：

* 特定決策管理：
   * offers_activity.read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * ranking_strategy.read

* Adobe Experience Platform特定：
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] 權限 {#manage-ranking-strategies}

此 **[!DNL Manage ranking strategies]** 高階權限可讓使用者讀取、建立、編輯和刪除排名策略。

其中包含下列低階權限：

* 特定決策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理功能 {#administration-permissions}

### [!DNL Manage subdomains delegation] 權限 {#manage-subdomain}

此 **[!DNL Manage subdomains delegation]** 高級權限允許用戶建立、編輯和刪除子域委託（包括IP池）。

其中包含下列低階權限：

* subdomains_delegation_read
* subdomains_delegation.write
* subdomains_delegation.delete

### [!DNL Manage PTR records] 權限 {#manage-ptr}

此 **[!DNL Manage PTR records]** 高級權限允許用戶讀取和編輯基於子域配置的PTR記錄。

其中包含下列低階權限：

* PTR_records.read
* PTR_records.write
* subdomains_delegation_read

### [!DNL View PTR records] 權限 {#view-ptr}

此 **[!DNL View PTR records]** 高級權限允許用戶查看已基於子域配置的PTR記錄。

其中包含下列低階權限：

* PTR_records.read
* subdomains_delegation_read

### [!DNL Manage IP pools] 權限 {#manage-ip-pools}

此 **[!DNL Manage IP pools]** 高階權限可讓使用者建立、編輯和刪除相關性定義。

其中包含下列低階權限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

<!--
### [!DNL Manage messages general settings] permission {#manage-message-settings}

The **[!DNL Manage messages general settings]** high-level permission allows users to create, edit and delete global settings at the sandbox level.

It includes the following low-level permissions: 

* Journey Optimizer specific: 
  * messages_general_settings.read
  * messages_general_settings.write
  * messages_general_settings.delete
* Adobe Experience Platform specific:
  * schemas.read

### [!DNL View messages general settings] permission {#view-message-settings}

The **[!DNL View messages general settings]** high-level permission allows users to view messages general settings such as the execution address.

It includes the following low-level permissions:

* Journey Optimizer specific: 
  * messages_general_settings.read
* Adobe Experience Platform specific: 
  * schemas.read
-->

### [!DNL Manage channel surface] 權限 {#manage-channel-surface}

此 **[!DNL Manage channel surface]** 高階權限可讓使用者在沙箱層級建立、編輯和刪除各管道的管道表面。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation_read
   * IP_pools.read
   * mobile_setting.read(來自Adobe Experience Platform Launch)

### [!DNL View channel surface] 權限 {#view-channel-surface}

此 **[!DNL View channel surface]** 高級權限允許用戶查看通道曲面，以了解要使用的通道曲面。

其中包含下列低階權限：

* messages_presets.read
* subdomains_delegation_read
* IP_pools.read
* mobile_setting.read(從Adobe Experience Platform資料收集)

### [!DNL Manage suppression] 權限 {#manage-suppression}

此 **[!DNL Manage suppression]** 高級權限允許用戶在將電子郵件地址添加到隱藏清單之前定義跳出數，以及向隱藏清單添加和刪除條目。

其中包含下列低階權限：

* suppressing_rules.read
* suppressing_rules.write
* suppressing_rules.delete
* suppressing_list.write
* suppressing_list.delete

### [!DNL View suppression list] 權限 {#view-suppression-list}

此 **[!DNL View suppression list]** 高級權限允許用戶查看隱藏清單內容和設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * suppressing_list.view

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 權限 {#export-suppression-list}

此 **[!DNL Export suppression list]** 高級權限可讓使用者將隱藏清單下載為CSV檔案。

其中包含下列低階權限：

* Journey Optimizer特定：
   * suppressing_list.export

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] 權限 {#manage-landing-page-settings}

此 **[!DNL Manage landing page settings]** 高階權限可讓使用者讀取、建立和編輯登錄頁面子網域和預設集設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * landing_page_subdomain.read
   * landing_page_subdomain.write
   * landing_page_subdomain.delete
   * landing_page_preset.read
   * landing_page_preset.write
   * landing_page_preset.delete

### [!DNL Manage frequency rules] 權限 {#manage-frequency-rules}

此 **[!DNL Manage frequency rules]** 高階權限可讓使用者讀取、建立、編輯、刪除及啟用/停用頻率規則。

其中包含下列低階權限：

* Journey Optimizer特定：
   * frequency_rules.read
   * frequency_rules.write
   * frequency_rules.delete

### [!DNL View frequency rules] 權限 {#view-frequency-rules}

此 **[!DNL View frequency rules]** 高階權限可讓使用者檢視頻率規則。

其中包含下列低階權限：

* Journey Optimizer特定：
   * frequency_rules.read
