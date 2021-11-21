---
title: 權限層級
description: 了解高和低層權限
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Control Groups
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: da885bd5e29ff3454fef1c6b362f0e646fe8c39a
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

每個產品設定檔都包含允許使用者存取不同功能的權限。
可分為兩種類型：

* **高級權限**:代表可指派給的不同權限 **[!UICONTROL Product profile]** 在 [!DNL Admin console]，例如 **[!UICONTROL Publish journeys]** 和 **[!UICONTROL Manage subdomains delegation]**. 高階權限包含低階權限。

* **低階權限**:代表來自高階權限的不同權限。

例如， **[!UICONTROL Journey administrator]** 已指派產品設定檔 **[!UICONTROL Manage journeys]** 權限。 從此權限會產生低階權限，讓歷程管理員可編寫、讀取和刪除歷程。

## 歷程功能 {#journey-capability}

### 管理歷程權限 {#manage-journeys}

此 **[!UICONTROL Manage journeys]** 高階權限可讓使用者建立新的和編輯/刪除現有的歷程，以及存取歷程畫布中用來建立歷程流程的物件。

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

### 發佈歷程權限 {#publish-journeys}

此 **[!UICONTROL Publish journeys]** 高階權限可讓使用者發佈歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### 檢視歷程權限 {#view-journeys}

此 **[!UICONTROL View journeys]** 高階權限可讓使用者瀏覽及檢視歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### 管理歷程事件、資料來源和動作權限 {#manage-journeys-events}

此 **[!UICONTROL Manage journeys events, data sources and actions]** 高階權限可讓使用者設定事件和資料設定。

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

### 檢視歷程事件、資料來源和動作權限 {#view-journeys-event}

此 **[!UICONTROL View journeys events, data sources and actions]** 高階權限可讓使用者在歷程流程中使用事件和資料。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys_events.read
   * journeys_data_sources.read
   * journeys_actions.read

* Adobe Experience Platform特定：
   * schemas.read
   * datasets.read
   * identity_namespace.read

### 檢視歷程報表權限 {#view-journeys-report}

此 **[!UICONTROL View journeys report]** 高階權限可讓使用者以唯讀的歷程報告。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys_report.read
   * messages_report.read

* Adobe Experience Platform特定：
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 訊息功能 {#message-capability}

### 管理訊息權限 {#manage-messages}

此 **[!UICONTROL Manage messages]** 高階權限可讓使用者建立和編輯/刪除訊息。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets.read

* Adobe Experience Platform特定：
   * segments.read
   * schemas.read

### 管理訊息預覽和測試權限 {#mange-messages-preview}

此 **[!UICONTROL Manage messages preview and test]** 高階權限可讓使用者預覽個人化訊息。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace.read
   * segments.read
   * queries.write
   * merge_policies.read

### 發佈訊息權限 {#publish-messages}

此 **[!UICONTROL Publish messages]** 高階權限可讓使用者發佈訊息。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * schemas.read
   * datasets.read

### 檢視訊息權限 {#view-messages}

此 **[!UICONTROL View messages]** 高級權限允許用戶只讀郵件。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.read
   * messages_presets.read

* Adobe Experience Platform特定：
   * schemas.read
   * segments.read

### 檢視訊息報表權限 {#view-message-reports}

此 **[!UICONTROL View messages report]** 高階權限可讓使用者以唯讀電子郵件和推送報表。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_report.read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 決策管理能力 {#decisions-permissions}

### 管理決策權限 {#manage-decisioning}

此 **[!UICONTROL Manage decisions]** 高階權限可讓使用者建立新項目，以及編輯/刪除現有項目 **[!UICONTROL Activity entities]**，以及管理用於這些活動中以做出決策的物件。

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

### 查看決策權限 {#view-decisions}

此 **[!UICONTROL View decisions]** 高級權限允許用戶使用現有活動和相關業務對象進行決策。

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

### 發佈優惠方案決策權限 {#publish-decisions}

此 **[!UICONTROL Publish offers decisioning]** 高階權限可讓使用者存取核准/取消核准優惠方案活動。

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

### 管理排名策略權限 {#manage-decisions}

此 **[!UICONTROL Manage ranking strategies]** 高階權限可讓使用者讀取、建立、編輯和刪除自訂訊息報表，以及使用動作功能。

其中包含下列低階權限：

* 特定決策管理：
   * ranking_strategy.read
   * ranking_strategy.write
   * ranking_strategy.delete
   * activities.read
   * offers.read
   * placements.read

## 管理功能 {#administration-permissions}

### 管理子網域委派權限 {#manage-subdomain}

此 **[!UICONTROL Manage subdomains delegation]** 高級權限允許用戶建立、編輯和刪除子域委託（包括IP池）。

其中包含下列低階權限：

* subdomains_delegation_read
* subdomains_delegation.write
* subdomains_delegation.delete

### 查看PTR記錄權限 {#view-ptr}

此 **[!UICONTROL View PTR records]** 高級權限允許用戶查看已基於子域配置的PTR記錄。

其中包含下列低階權限：

* PTR_records.read
* subdomains_delegation_read

### 管理IP池權限 {#manage-ip-pools}

此 **[!UICONTROL Manage IP pools]** 高階權限可讓使用者建立、編輯和刪除相關性定義。

其中包含下列低階權限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### 管理郵件一般設定權限 {#manage-message-settings}

此 **[!UICONTROL Manage messages general settings]** 高階權限可讓使用者在沙箱層級建立、編輯和刪除全域設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform特定：
   * schemas.read

### 檢視訊息一般設定權限 {#view-message-settings}

此 **[!UICONTROL View messages general settings]** 高級權限允許用戶查看消息的一般設定，如執行地址。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_general_settings.read
* Adobe Experience Platform特定：
   * schemas.read

### 管理郵件預設集權限 {#manage-message-presets}

此 **[!UICONTROL Manage messages presets]** 高階權限可讓使用者在沙箱層級建立、編輯和刪除各管道的訊息預設集。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation_read
   * IP_pools.read
   * mobile_setting.read(來自Adobe Experience Platform Launch)

### 檢視訊息預設集權限 {#view-message-presets}

此 **[!UICONTROL View messages presets]** 高級權限允許用戶查看郵件預設集，以便了解建立郵件時要使用哪些郵件預設集。

其中包含下列低階權限：

* messages_presets.read
* subdomains_delegation_read
* IP_pools.read
* mobile_setting.read(來自Adobe Experience Platform Launch)

### 管理隱藏權限 {#manage-suppression}

此 **[!UICONTROL Manage suppression]** 高級權限允許用戶在將電子郵件地址添加到隱藏清單之前定義跳出數，以及向隱藏清單添加和刪除條目。

其中包含下列低階權限：

* suppressing_rules.read
* suppressing_rules.write
* suppressing_rules.delete
* suppressing_list.write
* suppressing_list.delete

### 查看隱藏清單權限 {#view-suppresion-list}

此 **[!UICONTROL View suppression list]** 高級權限允許用戶查看隱藏清單內容和設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * suppressing_list.view
* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### 導出隱藏清單權限 {#export-suppression-list}

此 **[!UICONTROL Export suppression list]** 高級權限可讓使用者將隱藏清單下載為CSV檔案。

其中包含下列低階權限：

* Journey Optimizer特定：
   * suppressing_list.export
* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read
