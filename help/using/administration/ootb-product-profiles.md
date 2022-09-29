---
title: 內建的產品設定檔
description: 了解內建的產品設定檔
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 8ca0d2bbd01451de613d8ae985e10a711fcc6316
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 9%

---

# 內建的產品設定檔 {#ootb-product-profiles}


## 關於訊息相關權限{#message-permissions}

Adobe Journey Optimizer推出新的內嵌撰寫功能，可讓您直接從歷程或行銷活動建立及撰寫訊息。

此功能會影響權限，如下所示：

| 權限名稱 | 將包含在 |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**7月25日之後**，相關權限 **訊息** 仍可用，因為仍可存取訊息以啟用轉變，您仍可將其儲存為範本。

**截至9月6日**，相關權限 **訊息** 將會移除，且訊息將無法再存取。

>[!WARNING]
>
>如果您已將使用者指派給 **[!DNL Message Manager]** 僅限產品設定檔，沒有 **[!DNL Journey manager]** 產品設定檔中，您需要為其指派新的產品設定檔，才能繼續編輯內容。


## [!DNL Campaign Administrator] {#campaign-administrator}

此 **[!DNL Campaign Administrator]** 產品設定檔可讓管理功能表管理及發佈促銷活動與決策管理。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |促銷活動| <ul><li> **[!DNL Manage campaigns]**:閱讀、建立、編輯和刪除促銷活動。</li><li>**[!DNL Publish campaigns]**:發佈促銷活動。</li><li>**[!DNL View campaigns report]**:讀取和編輯促銷活動報表。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:讀取、建立、編輯和刪除子網域委派。</li><li>**[!DNL Manage IP pools]**:讀取、建立、編輯和刪除ip池。</li><li>**[!DNL Manage PTR records]**:讀取和編輯PTR記錄。</li><li>**[!DNL View PTR records]**:對PTR記錄的只讀訪問。</li><li> **[!DNL Manage messages general settings]**:讀取、建立、編輯和刪除消息常規設定。</li><li>**[!DNL Manage messages presets]**:閱讀、建立、編輯和刪除內容品牌。</li><li>**[!DNL Manage suppression rules]**:訪問讀取、建立、編輯和刪除隱藏規則。</li><li>**[!DNL Export suppression list]**:以CSV檔案形式存取匯出隱藏清單。</li><li>**[!DNL View suppression list]**:讀取並導出本地隱藏清單。</li><li>**[!DNL Manage alerts]**:啟用/停用促銷活動、訊息和權益的警報。</li><li>**[!DNL Manage landing page settings]**:讀取、建立、編輯和刪除登錄頁面設定。</li><li>**[!DNL Manage SMS settings]**:讀取、建立、編輯和刪除SMS設定。</li></ul>|
|決策管理|<ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除排名策略。</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予沙箱的存取權。</li><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Read Identity namespace]**:唯讀存取身分命名空間。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|

## [!DNL Campaign Approver] {#campaign-approver}

此 **[!DNL Campaign Approver]** 產品設定檔可讓使用者核准傳遞並發佈。 他們稍後可以透過 **[!DNL Campaigns]** 報表。

|功能 |權限| |-|-| |促銷活動| <ul><li>**[!DNL Manage campaigns]**:閱讀、建立、編輯和刪除促銷活動。</li><li>**[!DNL Publish campaigns]**:發佈促銷活動。</li><li>**[!DNL View Campaigns report]**:閱讀、編輯歷程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自訂訊息報表，以及使用動作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:對訊息預設集的唯讀存取。</li></ul>|

## [!DNL Campaign Manager] {#campaign-manager}

此 **[!DNL Campaign Manager]** 產品設定檔可讓使用者建立和編輯 **[!UICONTROL 行銷活動]** 以及連結到 **[!UICONTROL 行銷活動]** 但無法發佈。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |促銷活動| <ul><li>**[!DNL Manage campaigns]**:閱讀、建立、編輯和刪除促銷活動。</li><li>**[!DNL View campaigns report]**:閱讀、編輯歷程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自訂訊息報表，以及使用動作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View messages presets]**:對訊息預設集的唯讀存取。</li></ul>|

## [!DNL Campaign Viewer] {#campaign-viewer}

此 **[!DNL Campaign Viewer]** 產品設定檔可讓您以唯讀方式存取 **[!UICONTROL 行銷活動]** 和 **[!UICONTROL 決策管理]** 功能。

指派給此產品設定檔的使用者將無法編輯或發佈。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |促銷活動| <ul><li>**[!DNL View campaigns]**:行銷活動的唯讀存取。</li><li>**[!DNL View campaigns report]**:「促銷活動」報表的唯讀存取。</li></ul>|
|決策管理| <ul><li>**[!DNL View decisions]**:對決策實體的唯讀存取。</li></ul>|

## [!DNL Journey Administrator] {#journey-administrator}

此 **[!DNL Journey Administrator]** 產品設定檔可讓管理功能表管理及發佈歷程與決策管理。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |歷程| <ul><li> **[!DNL Manage journeys]**:讀取、建立、編輯和刪除歷程。</li><li>**[!DNL Publish journeys]**:發佈歷程。</li><li>**[!DNL Manage journeys events, data sources and actions]**:讀取、建立、編輯和刪除事件、源或操作。</li><li>**[!DNL View journeys report]**:閱讀及編輯歷程報告。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:讀取、建立、編輯和刪除子網域委派。</li><li>**[!DNL Manage IP pools]**:讀取、建立、編輯和刪除ip池。</li><li>**[!DNL Manage PTR records]**:讀取和編輯PTR記錄。</li><li>**[!DNL View PTR records]**:對PTR記錄的只讀訪問。</li><li>**[!DNL Manage channel surfaces]**:閱讀、建立、編輯和刪除內容品牌。</li><li>**[!DNL Manage Landing page settings]**:建立、編輯和刪除登錄頁面子網域和登錄頁面預設集。</li><li> **[!DNL Manage messages general settings]**:讀取、建立、編輯和刪除消息常規設定。</li><li>**[!DNL Manage SMS settings]**:建立、編輯和刪除啟用SMS通道所需的API憑證和SMS通道介面。</li><li>**[!DNL Manage suppression rules]**:訪問讀取、建立、編輯和刪除隱藏規則。</li><li>**[!DNL View suppression list]**:讀取並導出本地隱藏清單。</li><li>**[!DNL Manage alerts]**:啟用/停用歷程和權益的警報。</li></ul>|
|決策管理|<ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除排名策略。</li></ul>| |Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予沙箱的存取權。</li><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Read Identity namespace]**:唯讀存取身分命名空間。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>| |Journey Optimizer程式庫|<ul><li>**[!DNL Manage Library Items]**:新增和刪除 [!DNL Journey Optimizer] 程式庫。</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

此 **[!DNL Journey Approver]** 產品設定檔可讓使用者核准傳遞並發佈。 他們稍後可以透過 **[!DNL Journey]** 報表。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |歷程| <ul><li>**[!DNL Manage journeys]**:讀取、建立、編輯和刪除歷程。</li><li>**[!DNL Publish journey]**:發佈歷程。</li><li>**[!DNL View journeys events, data sources and actions]**:歷程事件、歷程自訂動作和歷程資料來源的唯讀存取。</li><li>**[!DNL View journeys report]**:閱讀、編輯歷程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自訂報表及使用動作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:對通道曲面的只讀訪問。</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

此 **[!DNL Journey Manager]** 產品設定檔可讓使用者建立和編輯 **[!UICONTROL 歷程]** 以及連結到 **[!UICONTROL 歷程]** 但無法發佈。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |歷程| <ul><li>**[!DNL Manage journeys]**:讀取、建立、編輯和刪除歷程。</li><li>**[!DNL View journeys events]**:歷程事件、歷程自訂動作和歷程資料來源的唯讀存取。</li><li>**[!DNL View journeys report]**:閱讀、編輯歷程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自訂報表及使用動作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:讀取、建立、編輯和刪除區段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Read datasets]**:資料集的唯讀存取權。</li><li>**[!DNL Read schemas]**:綱要的唯讀存取權。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:對通道曲面的只讀訪問。</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

此 **[!DNL Journey viewer]** 產品設定檔可讓您以唯讀方式存取 **[!UICONTROL 歷程]** 和 **[!UICONTROL 決策管理]** 功能。

指派給此產品設定檔的使用者將無法編輯或發佈。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |歷程| <ul><li>**[!DNL View journeys]**:歷程的唯讀存取。</li><li>**[!DNL View journeys event, data sources, actions]**:對歷程事件和資料來源的唯讀存取。</li><li>**[!DNL View journeys report]**:對歷程報表的唯讀存取。</li></ul>|
|決策管理| <ul><li>**[!DNL View decisions]**:對決策實體的唯讀存取。</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

此 **[!DNL Decisioning manager]** 產品設定檔僅允許 **[!UICONTROL 決策管理]** 功能表。 指派給此產品設定檔的使用者將只能管理、檢視和發佈決策。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL View decisions]**:決策實體的唯讀存取權。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自訂報表及使用動作功能。</li><li>**[!DNL Publish decisions]**:啟用或停用決策活動。</li></ul>|
