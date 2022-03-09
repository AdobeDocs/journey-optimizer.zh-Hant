---
title: 權限層級
description: 瞭解高級權限和低級權限
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b286f9d-43ef-4b80-b4ee-136da857bb95
source-git-commit: 2a27c19766c84d8c65e8b21ba381754758d60cae
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# 權限層級 {#high-low-permissions}

![](assets/do-not-localize/permissions.png)

每個產品配置檔案都由允許用戶訪問不同功能的權限組成。
可分為兩類：

* **高級權限**:表示可分配給的不同權限 **[!UICONTROL Product profile]** 的 [!DNL Admin console]，例如 **[!DNL Publish journeys]** 和 **[!DNL Manage subdomains delegation]**。 高級權限包含低級權限。

* **低級別權限**:表示來自高級權限的不同權限。

例如， **[!DNL Journey administrator]** 已分配產品配置檔案 **[!DNL Manage journeys]** 權限。 從此權限將產生低級權限，使「旅程」管理員能夠寫入、讀取和刪除旅程。

## 行程能力 {#journey-capability}

### [!DNL Manage journeys] 權限 {#manage-journeys}

的 **[!DNL Manage journeys]** 高級權限允許用戶建立新和編輯/刪除現有的Journeys，以及訪問在Journey畫布中用於構建Journey流的對象。

它包括以下低級權限：

* Journey Optimizer特別：

   * journeys.read
   * journeys.write
   * journeys.delete
   * messages.read

* Adobe Experience Platform特別：

   * segments.read
   * profiles.read
   * datasets.read
   * schemas.read

### [!DNL Publish journeys] 權限 {#publish-journeys}

的 **[!DNL Publish journeys]** 高級權限允許用戶發佈行程。

它包括以下低級權限：

* Journey Optimizer特別：
   * journeys.publish
   * journeys.read

### [!DNL View journeys] 權限 {#view-journeys}

的 **[!DNL View journeys]** 高級權限允許用戶瀏覽和查看行程。

它包括以下低級權限：

* Journey Optimizer特別：
   * journeys.read

* Adobe Experience Platform特別：
   * segments.read
   * profiles.read

### [!DNL Manage journeys events, data sources and actions] 權限 {#manage-journeys-events}

的 **[!DNL Manage journeys events, data sources and actions]** 高級權限允許用戶配置事件和資料配置。

它包括以下低級權限：

* Journey Optimizer特別：
   * roymers_events_read
   * reyormes_events_write
   * roymers_events_delete
   * journeys_data_sources_read
   * journeys_data_sources_write
   * journeys_data_sources_delete
   * reagners_actions_read
   * rougners_actions_write
   * journeys_actions_delete

* Adobe Experience Platform特別：
   * schemas.read
   * datasets.read
   * identity_namespace_read

### [!DNL View journeys events, data sources and actions] 權限 {#view-journeys-event}

的 **[!DNL View journeys events, data sources and actions]** 高級權限允許用戶使用行程流中的事件和資料。

它包括以下低級權限：

* Journey Optimizer特別：
   * roymers_events_read
   * journeys_data_sources_read
   * reagners_actions_read

* Adobe Experience Platform特別：
   * schemas.read
   * datasets.read
   * identity_namespace_read

### [!DNL View journeys report] 權限 {#view-journeys-report}

的 **[!DNL View journeys report]** 高級權限允許用戶只讀行程報告。

它包括以下低級權限：

* Journey Optimizer特別：
   * rougners_report_read
   * messages_report_read

* Adobe Experience Platform特別：
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete

## 消息功能 {#message-capability}

### [!DNL Manage messages] 權限 {#manage-messages}

的 **[!DNL Manage messages]** 高級權限允許用戶建立和編輯/刪除消息。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages.write
   * messages.read
   * messages.delete
   * messages_presets_read

* Adobe Experience Platform特別：
   * segments.read
   * schemas.read

### [!DNL Manage messages preview and test] 權限 {#mange-messages-preview}

的 **[!DNL Manage messages preview and test]** 高級權限允許用戶預覽個性化消息。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages.publish
   * messages_preview_and_test.write
   * messages.publish

* Adobe Experience Platform特別：
   * profiles.read
   * profiles.write
   * schemas.read
   * datasets.write
   * datasets.read
   * identity_namespace_read
   * segments.read
   * queries.write
   * merge_policies_read

### [!DNL Publish messages] 權限 {#publish-messages}

的 **[!DNL Publish messages]** 高級權限允許用戶發佈消息。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages.publish

* Adobe Experience Platform特別：
   * profiles.read
   * schemas.read
   * datasets.read

### [!DNL View messages] 權限 {#view-messages}

的 **[!DNL View messages]** 高級權限允許用戶只讀消息。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages.read
   * messages_presets_read

* Adobe Experience Platform特別：
   * schemas.read
   * segments.read

### [!DNL View messages report] 權限 {#view-message-reports}

的 **[!DNL View messages report]** 高級權限允許用戶只讀電子郵件和推送報告。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages_report_read
   * datasets.read
   * queries.read
   * queries.write
   * queries.delete
   * journey.read

## 決策管理能力 {#decisions-permissions}

### [!DNL Manage decisions] 權限 {#manage-decisioning}

的 **[!DNL Manage decisions]** 高級權限允許用戶建立新權限和編輯/刪除現有權限 **[!DNL Activity entities]**，以及管理這些活動中用於做出決策的對象。

它包括以下低級權限：

* 具體決策管理：
   * activities.read
   * activities.write
   * activities.delete
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * 排名_策略_讀取

* Adobe Experience Platform特別：
   * datasets.read
   * datasets.write
   * datasets.delete
   * schemas.read
   * profile.read
   * segments.read

### [!DNL View decisions] 權限 {#view-decisions}

的 **[!DNL View decisions]** 高級權限允許用戶使用現有活動和相關業務對象做出決策。

它包括以下低級權限：

* 具體決策管理：
   * activities.read
   * offers.read
   * placements.read
   * 排名_策略_讀取

* Adobe Experience Platform特別：
   * schemas.read
   * segment.read
   * datasets.read
   * datasets.write
   * datasets.delete

### [!DNL Publish offers decisioning] 權限 {#publish-decisions}

的 **[!DNL Publish offers decisioning]** 高級權限允許用戶訪問批准/取消批准聘用活動。

它包括以下低級權限：

* 具體決策管理：
   * offis_activity_read
   * offers.read
   * offers.write
   * offers.delete
   * placements.read
   * placements.write
   * placements.delete
   * 排名_策略_讀取

* Adobe Experience Platform特別：
   * schemas.read
   * segment.read
   * datasets.read
   * profiles.read

### [!DNL Manage ranking strategies] 權限 {#manage-decisions}

的 **[!DNL Manage ranking strategies]** 高級權限允許用戶讀取、建立、編輯和刪除自定義消息報告和使用操作功能。

它包括以下低級權限：

* 具體決策管理：
   * 排名_策略_讀取
   * 排名_策略_寫入
   * 排名_策略_刪除
   * activities.read
   * offers.read
   * placements.read

## 管理能力 {#administration-permissions}

### [!DNL Manage subdomains delegation] 權限 {#manage-subdomain}

的 **[!DNL Manage subdomains delegation]** 高級權限允許用戶建立、編輯和刪除子域委託（包括IP池）。

它包括以下低級權限：

* 子域_委派_讀取
* 子域_委派_寫入
* 子域_委派_刪除

### [!DNL Manage PTR records] 權限 {#manage-ptr}

的 **[!DNL Manage PTR records]** 高級權限允許用戶讀取和編輯基於子域配置的PTR記錄。

它包括以下低級權限：

* PTR_records.read
* PTR_records.write
* 子域_委派_讀取

### [!DNL View PTR records] 權限 {#view-ptr}

的 **[!DNL View PTR records]** 高級權限允許用戶查看基於子域配置的PTR記錄。

它包括以下低級權限：

* PTR_records.read
* 子域_委派_讀取

### [!DNL Manage IP pools] 權限 {#manage-ip-pools}

的 **[!DNL Manage IP pools]** 高級權限允許用戶建立、編輯和刪除關聯定義。

它包括以下低級權限：

* IP_pools.read
* IP_pools.write
* IP_pools.delete

### [!DNL Manage messages general settings] 權限 {#manage-message-settings}

的 **[!DNL Manage messages general settings]** 高級權限允許用戶在沙盒級別建立、編輯和刪除全局設定。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages_general_settings.read
   * messages_general_settings.write
   * messages_general_settings.delete
* Adobe Experience Platform特別：
   * schemas.read

### [!DNL View messages general settings] 權限 {#view-message-settings}

的 **[!DNL View messages general settings]** 高級權限允許用戶查看消息常規設定，如執行地址。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages_general_settings.read
* Adobe Experience Platform特別：
   * schemas.read

### [!DNL Manage messages presets] 權限 {#manage-message-presets}

的 **[!DNL Manage messages presets]** 高級權限允許用戶在沙盒級別跨通道建立、編輯和刪除消息預設。

它包括以下低級權限：

* Journey Optimizer特別：
   * messages_presets_read
   * messages_presets_write
   * messages_presets_delete
   * 子域_委派_讀取
   * IP_pools.read
   * mobile_setting.read(來自Adobe Experience Platform Launch)

### [!DNL View messages presets] 權限 {#view-message-presets}

的 **[!DNL View messages presets]** 高級權限允許用戶查看消息預設，以便知道在建立消息時要使用哪些消息預設。

它包括以下低級權限：

* messages_presets_read
* 子域_委派_讀取
* IP_pools.read
* mobile_setting.read(來自Adobe Experience Platform資料收集)

### [!DNL Manage suppression] 權限 {#manage-suppression}

的 **[!DNL Manage suppression]** 高級權限允許用戶在將電子郵件地址添加到禁止使用清單之前定義禁止使用的次數，以及向禁止使用清單添加和刪除條目。

它包括以下低級權限：

* suppression_rules_read
* suppression_rules_write
* suppression_rules_delete
* suppression_list.write
* suppression_list.delete

### [!DNL View suppression list] 權限 {#view-suppression-list}

的 **[!DNL View suppression list]** 高級權限允許用戶查看禁止顯示清單內容和設定。

它包括以下低級權限：

* Journey Optimizer特別：
   * suppression_list_view

* Adobe Experience Platform特別：
   * profiles.read
   * datasets.read

### [!DNL Export suppression list] 權限 {#export-suppression-list}

的 **[!DNL Export suppression list]** 高級權限允許用戶將禁止顯示清單作為CSV檔案下載。

它包括以下低級權限：

* Journey Optimizer特別：
   * suppression_list.export

* Adobe Experience Platform特別：
   * profiles.read
   * datasets.read

### [!DNL Manage landing page settings] 權限 {#manage-landing-page-settings}

的 **[!DNL Manage landing page settings]** 高級權限允許用戶讀取、建立和編輯登錄頁子域和預設設定。

它包括以下低級權限：

* Journey Optimizer特別：
   * landing_page_subdomain_read
   * landing_page_subdomain_write
   * landing_page_subdomain_delete
   * landing_page_preset_read
   * landing_page_preset_write
   * landing_page_preset_delete
