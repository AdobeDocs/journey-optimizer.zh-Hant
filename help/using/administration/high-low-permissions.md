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
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: 控制組
topic: 管理
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}

![](../assets/do-not-localize/permissions.png)

每個產品設定檔都包含允許使用者存取不同功能的權限。
可分為兩種類型：

* **高階權限**:代表可在中指派給的 **[!UICONTROL Product profile]** 不同 [!DNL Admin console]權限， **[!UICONTROL Publish journeys]** 例如和 **[!UICONTROL Manage subdomains delegation]**。高階權限包含低階權限。

* **低階權限**:代表來自高階權限的不同權限。

例如， **[!UICONTROL Journey administrator]**&#x200B;產品設定檔會獲派&#x200B;**[!UICONTROL Manage journeys]**&#x200B;權限。 從此權限會產生低階權限，讓歷程管理員可編寫、讀取和刪除歷程。

## 歷程功能 {#journey-capability}

### 管理歷程權限 {#manage-journeys}

**[!UICONTROL Manage journeys]**&#x200B;高階權限可讓使用者建立新的和編輯/刪除現有的歷程，以及存取歷程畫布中使用以建立歷程流程的物件。

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

**[!UICONTROL Publish journeys]**&#x200B;高階權限可讓使用者發佈歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.publish
   * journeys.read

### 檢視歷程權限 {#view-journeys}

**[!UICONTROL View journeys]**&#x200B;高階權限可讓使用者瀏覽及檢視歷程。

其中包含下列低階權限：

* Journey Optimizer特定：
   * journeys.read

* Adobe Experience Platform特定：
   * segments.read
   * profiles.read

### 管理歷程事件、資料來源和動作權限 {#manage-journeys-events}

**[!UICONTROL Manage journeys events, data sources and actions]**&#x200B;高級權限允許用戶配置事件和資料配置。

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

**[!UICONTROL View journeys events, data sources and actions]**&#x200B;高階權限可讓使用者在歷程流程中使用事件和資料。

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

**[!UICONTROL View journeys report]**&#x200B;高階權限可讓使用者以唯讀的歷程報告。

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

**[!UICONTROL Manage messages]**&#x200B;高級權限允許用戶建立和編輯/刪除消息。

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

**[!UICONTROL Manage messages preview and test]**&#x200B;高階權限可讓使用者預覽個人化訊息。

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

**[!UICONTROL Publish messages]**&#x200B;高階權限可讓使用者發佈訊息。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.publish

* Adobe Experience Platform特定：
   * profiles.read
   * schemas.read
   * datasets.read

### 檢視訊息權限 {#view-messages}

**[!UICONTROL View messages]**&#x200B;高級權限允許用戶只讀消息。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages.read
   * messages_presets.read

* Adobe Experience Platform特定：
   * schemas.read
   * segments.read

### 檢視訊息報表權限 {#view-message-reports}

**[!UICONTROL View messages report]**&#x200B;高階權限可讓使用者以唯讀方式使用電子郵件及推送報表。

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

**[!UICONTROL Manage decisions]**&#x200B;高級權限允許用戶建立新的和編輯/刪除現有的&#x200B;**[!UICONTROL Activity entities]**，以及管理這些活動中用於做出決策的對象。

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

**[!UICONTROL View decisions]**&#x200B;高級權限允許用戶使用現有活動和相關業務對象進行決策。

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

**[!UICONTROL Publish offers decisioning]**&#x200B;高階權限可讓使用者存取核准/取消核准優惠方案活動。

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

**[!UICONTROL Manage ranking strategies]**&#x200B;高階權限可讓使用者讀取、建立、編輯和刪除自訂訊息報表，以及使用動作功能。

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

**[!UICONTROL Manage subdomains delegation]**&#x200B;高級權限允許用戶建立、編輯和刪除子域委派（包括IP池）。

其中包含下列低階權限：

* subdomains_delegation_read
* subdomains_delegation.write
* subdomains_delegation.delete

### 查看PTR記錄權限 {#view-ptr}

**[!UICONTROL View PTR records]**&#x200B;高級權限允許用戶查看已基於子域配置的PTR記錄，並包括以下低級權限：

* PTR_records.read
* subdomains_delegation_read

### 管理IP池權限 {#manage-ip-pools}

**[!UICONTROL Manage IP pools]**&#x200B;高階權限可讓使用者建立、編輯和刪除相關性定義。

其中包含下列低階權限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### 管理郵件一般設定權限 {#manage-message-settings}

**[!UICONTROL Manage messages general settings]**&#x200B;高階權限可讓使用者在沙箱層級建立、編輯和刪除全域設定。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete

* Adobe Experience Platform特定：
   * schemas.read

### 檢視訊息一般設定權限 {#view-message-settings}

**[!UICONTROL View messages general settings]**&#x200B;高級權限允許用戶查看消息常規設定，如隱藏規則或執行地址。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_general_settings.read
* Adobe Experience Platform特定：
   * schemas.read

### 管理郵件預設集權限 {#manage-message-presets}

**[!UICONTROL Manage messages presets]**&#x200B;高階權限可讓使用者在沙箱層級建立、編輯和刪除各管道的訊息預設集。

其中包含下列低階權限：

* Journey Optimizer特定：
   * messages_presets.read
   * messages_presets.write
   * messages_presets.delete
   * subdomains_delegation_read
   * IP_pools.read
   * mobile_setting.read(來自Adobe Experience Platform Launch)

### 檢視訊息預設集權限 {#view-message-presets}

**[!UICONTROL View messages presets]**&#x200B;高級權限允許用戶查看郵件預設集，以便了解建立郵件時要使用的郵件預設集。

其中包含下列低階權限：

* messages_presets.read
* subdomains_delegation_read
* IP_pools.read
* mobile_setting.read(來自Adobe Experience Platform Launch)

### 管理隱藏規則權限 {#manage-suppression-rules}

**[!UICONTROL Manage suppression rules]**&#x200B;高階權限可讓使用者在將使用者的電子郵件地址新增至隱藏清單之前定義跳出數。

其中包含下列低階權限：

* suppressing_rules.read
* suppressing_rules.write
* suppressing_rules.delete

### 查看隱藏清單權限 {#view-suppresion-list}

**[!UICONTROL View suppression list]**&#x200B;高級權限允許用戶查看包括消息預設集和一般消息設定在內的消息配置。

其中包含下列低階權限：

* Journey Optimizer特定：
   * suppressing_list.view
* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read

### 導出隱藏清單權限 {#export-suppression-list}

**[!UICONTROL Export suppression list]**&#x200B;高級權限允許用戶配置消息配置，包括消息預設集和一般消息設定。

其中包含下列低階權限：

* Adobe Experience Platform特定：
   * profiles.read
   * datasets.read
