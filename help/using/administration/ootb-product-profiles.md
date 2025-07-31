---
solution: Journey Optimizer
product: journey optimizer
title: Journey Optimizer內建角色
description: 瞭解內建角色
feature: Access Management
topic: Administration
role: Admin, User
level: Intermediate
keywords: 許可權，製作，訊息
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: ee2e07353762a81aadd3d63580c528f617599623
workflow-type: tm+mt
source-wordcount: '1175'
ht-degree: 7%

---

# 內建角色 {#ootb-product-profiles}

內建角色是一組統一許可權，可讓使用者存取介面中的特定功能或物件。 如需建立角色的可用許可權清單，請參閱[此頁面](ootb-permissions.md)。

## [!DNL Content Library Manager] {#content-library-manager}

**[!DNL Content Library Manager]**&#x200B;角色只允許存取&#x200B;**[!UICONTROL 內容範本]**&#x200B;功能表。 指派給此角色的使用者將只能存取範本資料庫以建立內容，而無需存取歷程或行銷活動。

此角色包含下列許可權：

| 功能 | 權限 |
|-|-|
| Journey Optimizer資料庫 | <ul><li>**[!DNL Manage library items]**：讀取、建立、編輯和刪除Journey Optimizer資料庫專案，包括內容範本和片段。</li><li>**[!DNL Manage simulate content]**：存取預覽和校訂的&#x200B;**[!UICONTROL 模擬內容]**&#x200B;選項。</li><li>**[!DNL Publish Fragment]**：發佈內容片段。</li></ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂報告，並使用動作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li><li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li><li> **[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li><li>**[!DNL View datasets]**：資料集的唯讀存取權。</li><li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li></ul> |

## [!DNL Decisioning manager] {#decisioning-manager}

**[!DNL Decisioning manager]**&#x200B;角色只允許存取&#x200B;**[!UICONTROL 決定管理]**&#x200B;功能表。 指派給此角色的使用者將只能管理、檢視和發佈決定。

此角色包含下列許可權：

| 功能 | 權限 |
|-|-|
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂報告，並使用動作功能。</li><li>**[!DNL View decisions]**：決策實體的唯讀存取權。</li><li>**[!DNL Publish decisions]**：啟用或停用決策活動。</li><!--li>**[!DNL Manage Experience decisions]**: read, create, edit, and delete Decisioning entities.</li--></ul> |

## [!DNL Campaign Administrator] {#campaign-administrator}

**[!DNL Campaign Administrator]**&#x200B;角色可讓管理功能表管理和發佈行銷活動與決定管理。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 行銷活動 | <ul><li> **[!DNL Manage campaigns]**：讀取、建立、編輯和刪除行銷活動。</li><li>**[!DNL Publish campaigns]**：發佈行銷活動。</li><li>**[!DNL View campaigns report]**：讀取並編輯行銷活動報告。</li></ul> |
| 頻道設定 | <ul> <li>**[!DNL Export suppression list]**：存取將隱藏清單匯出為CSV檔案的許可權。</li> <li>**[!DNL Manage alerts]**：啟用/停用行銷活動、訊息和權益的警示。</li> <li>**[!DNL Manage IP pools]**：讀取、建立、編輯和刪除ip集區。</li> <li>**[!DNL Manage landing page settings]**：讀取、建立、編輯和刪除登入頁面設定。</li> <li>**[!DNL Manage messages general settings]**：讀取、建立、編輯和刪除訊息一般設定。</li> <li>**[!DNL Manage messages presets]**：讀取、建立、編輯和刪除內容品牌。</li> <li>**[!DNL Manage PTR records]**：讀取和編輯PTR記錄。</li> <li>**[!DNL Manage SMS settings]**：讀取、建立、編輯及刪除SMS設定。</li> <li>**[!DNL Manage subdomains delegation]**：讀取、建立、編輯和刪除子網域委派。</li> <li>**[!DNL Manage suppression rules]**：存取讀取、建立、編輯和刪除隱藏規則。</li> <li>**[!DNL View PTR records]**：對PTR記錄的唯讀存取權。</li> <li>**[!DNL View suppression list]**：讀取和匯出本機隱藏清單。</li> </ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決定。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除排名策略。</li></ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li> <li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li> <li>**[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li> <li>**[!DNL View datasets]**：資料集的唯讀存取權。</li> <li>**[!DNL Read Identity namespace]**：身分名稱空間的唯讀存取權。</li> <li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li> <li>**[!DNL Sandbox]**：授與沙箱的存取權。</li> </ul> |

## [!DNL Campaign Approver] {#campaign-approver}

**[!DNL Campaign Approver]**&#x200B;角色可讓使用者核准傳遞並發佈。 他們稍後可以使用&#x200B;**[!DNL Campaigns]**&#x200B;報告檢查傳送是否成功。

| 資源 | 權限 |
|-|-|
| 行銷活動 | <ul><li>**[!DNL Manage campaigns]**：讀取、建立、編輯和刪除行銷活動。</li><li>**[!DNL Publish campaigns]**：發佈行銷活動。</li><li>**[!DNL View campaigns report]**：讀取、編輯行銷活動報告。</li></ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂訊息報告，並使用動作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li><li>**[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li><li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL View datasets]**：資料集的唯讀存取權。</li><li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li></ul> |
| 頻道設定 | <ul><li>**[!DNL View messages presets]**：訊息預設集的唯讀存取權。</li></ul> |

## [!DNL Campaign Manager] {#campaign-manager}

**[!DNL Campaign Manager]**&#x200B;角色可讓使用者建立和編輯&#x200B;**[!UICONTROL 行銷活動]**&#x200B;以及連結至&#x200B;**[!UICONTROL 行銷活動]**&#x200B;的每個功能，但將無法發佈。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 行銷活動 | <ul><li>**[!DNL Manage campaigns]**：讀取、建立、編輯和刪除行銷活動。</li><li>**[!DNL View campaigns report]**：讀取、編輯歷程報告。</li></ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂訊息報告，並使用動作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li><li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li><li> **[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li><li>**[!DNL View datasets]**：資料集的唯讀存取權。</li><li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li></ul> |
| 頻道設定 | <ul><li>**[!DNL View messages presets]**：訊息預設集的唯讀存取權。</li></ul> |

## [!DNL Campaign Viewer] {#campaign-viewer}

**[!DNL Campaign Viewer]**&#x200B;角色允許對&#x200B;**[!UICONTROL 行銷活動]**&#x200B;和&#x200B;**[!UICONTROL 決定管理]**&#x200B;功能的唯讀存取。

指派給此角色的使用者將無法編輯或發佈。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 行銷活動 | <ul><li>**[!DNL View campaigns]**：行銷活動的唯讀存取權。</li><li>**[!DNL View campaigns report]**：行銷活動報告的唯讀存取權。</li></ul> |
| 決策管理 | <ul><li>**[!DNL View decisions]**：決策實體的唯讀存取權。</li></ul> |

## [!DNL Journey Administrator] {#journey-administrator}

**[!DNL Journey Administrator]**&#x200B;角色可讓管理功能表管理和發佈歷程與決定管理。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 歷程 | <ul> <li>**[!DNL Manage journeys]**：讀取、建立、編輯和刪除歷程。</li> <li>**[!DNL Manage journeys events, data sources and actions]**：讀取、建立、編輯和刪除事件、來源或動作。</li> <li>**[!DNL Publish journeys]**：發佈歷程。</li> <li>**[!DNL View journeys report]**：讀取及編輯歷程報告。</li> </ul> |
| 頻道設定 | <ul> <li>**[!DNL Manage alerts]**：啟用/停用歷程和權益的警報。</li> <li>**[!DNL Manage IP pools]**：讀取、建立、編輯和刪除ip集區。</li> <li>**[!DNL Manage Landing page settings]**：建立、編輯和刪除登陸頁面子網域和登陸頁面預設集。</li> <li>**[!DNL Manage messages general settings]**：讀取、建立、編輯和刪除訊息一般設定。</li> <li>**[!DNL Manage messages presets]**：讀取、建立、編輯和刪除內容品牌。</li> <li>**[!DNL Manage PTR records]**：讀取和編輯PTR記錄。</li> <li>**[!DNL Manage SMS settings]**：建立、編輯及刪除啟用SMS頻道所需的API認證和SMS頻道設定。</li> <li>**[!DNL Manage subdomains delegation]**：讀取、建立、編輯和刪除子網域委派。</li> <li>**[!DNL Manage suppression rules]**：存取讀取、建立、編輯和刪除隱藏規則。</li> <li>**[!DNL View PTR records]**：對PTR記錄的唯讀存取權。</li> <li>**[!DNL View suppression list]**：讀取和匯出本機隱藏清單。</li> </ul> |
| 決策管理 | <ul> <li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決定。</li> <li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除排名策略。</li> </ul> |
| Adobe Experience Platform | <ul> <li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li> <li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li> <li>**[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li> <li>**[!DNL View datasets]**：資料集的唯讀存取權。</li> <li>**[!DNL Read Identity namespace]**：身分名稱空間的唯讀存取權。</li> <li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li> <li>**[!DNL Sandbox]**：授與沙箱的存取權。</li> </ul> |
| Journey Optimizer資料庫 | <ul> <li>**[!DNL Manage Library Items]**：新增並刪除[!DNL Journey Optimizer]資料庫中已儲存的運算式。</li> </ul> |
| 資料治理 | <ul> <li>**[!DNL Manage data usage policies]**：讀取、建立、編輯和刪除資料使用原則。</li> <li>**[!DNL Manage usage label]**：讀取、建立及刪除使用標籤。</li> <li>**[!DNL View data usage policies]**：資料使用原則的唯讀存取權。</li> <li>**[!DNL View user activity log]**：讀取和匯出稽核記錄。</li> </ul> |

## [!DNL Journey Approver] {#journey-approver}

**[!DNL Journey Approver]**&#x200B;角色可讓使用者核准傳遞並發佈。 他們稍後可以使用&#x200B;**[!DNL Journey]**&#x200B;報告檢查傳送是否成功。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 歷程 | <ul><li>**[!DNL Manage journeys]**：讀取、建立、編輯和刪除歷程。</li><li>**[!DNL Publish journey]**：發佈歷程。</li><li>**[!DNL View journeys events, data sources and actions]**：歷程事件、歷程自訂動作和歷程資料來源的唯讀存取權。</li><li>**[!DNL View journeys report]**：讀取、編輯歷程報告。</li></ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂報告，並使用動作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li><li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li><li>**[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li><li>**[!DNL View datasets]**：資料集的唯讀存取權。</li><li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li></ul> |
| 頻道設定 | <ul><li>**[!DNL View channel configurations]**：通道設定的唯讀存取權。</li></ul> |

## [!DNL Journey Manager] {#journey-manager}

**[!DNL Journey Manager]**&#x200B;角色可讓使用者建立和編輯&#x200B;**[!UICONTROL 歷程]**&#x200B;以及連結至&#x200B;**[!UICONTROL 歷程]**&#x200B;的每個功能，但將無法發佈。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 歷程 | <ul><li>**[!DNL Manage journeys]**：讀取、建立、編輯和刪除歷程。</li><li>**[!DNL View journeys events]**：歷程事件、歷程自訂動作和歷程資料來源的唯讀存取權。</li><li>**[!DNL View journeys report]**：讀取、編輯歷程報告。</li></ul> |
| 決策管理 | <ul><li>**[!DNL Manage decisions]**：讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**：讀取、建立、編輯和刪除自訂報告，並使用動作功能。</li></ul> |
| Adobe Experience Platform | <ul><li>**[!DNL Manage merge policies]**：讀取、建立、編輯和刪除合併原則。</li><li>**[!DNL Manage profiles]**：讀取、建立、編輯和刪除設定檔。</li><li> **[!DNL Manage segments]**：讀取、建立、編輯和刪除區段定義。</li><li>**[!DNL View datasets]**：資料集的唯讀存取權。</li><li>**[!DNL View schemas]**：結構描述的唯讀存取權。</li></ul> |
| 頻道設定 | <ul><li>**[!DNL View channel configurations]**：通道設定的唯讀存取權。</li></ul> |

## [!DNL Journey Viewer] {#journey-viewer}

**[!DNL Journey viewer]**&#x200B;角色允許對&#x200B;**[!UICONTROL 歷程]**&#x200B;和&#x200B;**[!UICONTROL 決定管理]**&#x200B;功能的唯讀存取。

指派給此角色的使用者將無法編輯或發佈。

此角色包含下列許可權：

| 資源 | 權限 |
|-|-|
| 歷程 | <ul><li>**[!DNL View journeys]**：歷程的唯讀存取權。</li><li>**[!DNL View journeys event, data sources, actions]**：對歷程事件和資料來源的唯讀存取權。</li><li>**[!DNL View journeys report]**：歷程報告的唯讀存取權。</li></ul> |
| 決策管理 | <ul><li>**[!DNL View decisions]**：決策實體的唯讀存取權。</li></ul> |

<!--
## [!DNL Orchestrated Campaign Administrators] {#orchestrated-campaign-administrator}

The **[!DNL Orchestrated Campaign Administrator]** role allows the administration menus with the possibility to manage and publish Orchestrated Campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated Campaigns| <ul><li> **[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete orchestrated campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish orchestrated campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read and edit orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Export suppression list]**: access to export suppression list as a CSV file.</li> <li>**[!DNL Manage alerts]**: enable/disable alerts for campaigns, messages and entitlements.</li> <li>**[!DNL Manage custom dashboards]**: read, create, edit, and delete custom dashboards.</li><li>**[!DNL Manage IP pools]**: read, create, edit, and delete ip pool.</li> <li>**[!DNL Manage landing page settings]**: read, create, edit, and delete landing page settings.</li> <li>**[!DNL Manage messages general settings]**: read, create, edit, and delete message general settings.</li> <li>**[!DNL Manage messages presets]**: read, create, edit, and delete content branding.</li> <li>**[!DNL Manage orchestrated campaign administrator]**: Read, create, edit and delete links and reconciliations between Adobe Experience Platform Profiles and Relational store entities.</li><li>**[!DNL Manage PTR records]**: read and edit PTR records.</li> <li>**[!DNL Manage SMS settings]**: read, create, edit, and delete SMS settings.</li> <li>**[!DNL Manage subdomains delegation]**: read, create, edit, and delete subdomain delegation.</li> <li>**[!DNL Manage suppression rules]**: access read, create, edit and delete suppression rules.</li> <li>**[!DNL View PTR records]**: read-only access to PTR records.</li> <li>**[!DNL View suppression list]**: read and export local suppression list.</li> </ul>|
|Decision management|<ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisions.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete ranking strategies.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View Identity namespace]**: read-only access to identity namespace.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL View sandbox]**: grant access to sandboxes.</li> </ul>|

## [!DNL Orchestrated Campaign Approver] {#orchestrated-campaign-approver}

The **[!DNL Orchestrated Campaign Approver]** role allows users to publish Orchestrated campaigns. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL Publish orchestrated campaigns]**: publish campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaign reports.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL Publish messages]**: publish messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform|<ul> <li>**[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li> <li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li> <li>**[!DNL View datasets]**: read-only access to datasets.</li> <li>**[!DNL View schemas]**: read-only access to schemas.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li> <li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations|<ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li> <li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li> </ul>|

## [!DNL Orchestrated Campaign Manager] {#orchestrated-campaign-manager}

The **[!DNL Orchestrated Campaign Manager]** role allows users to create and edit **[!UICONTROL Orchestrated campaigns]** and every capability linked to **[!UICONTROL Orchestrated campaigns]** but will not be able to publish them.

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL Manage orchestrated campaigns]**: read, create, edit, and delete campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read orchestrated campaigns report.</li></ul>|
|Messages| <ul><li>**[!DNL Manage messages]**: read, create, edit, and delete messages.</li><li>**[!DNL Manage messages preview and test]**: preview and test messages before sending.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL Manage decisions]**: read, create, edit, and delete decisioning entities.</li><li>**[!DNL Manage ranking strategies]**: read, create, edit, and delete custom messages reports and use action features.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL Manage merge policies]**: read, create, edit, and delete merge policies.</li><li>**[!DNL Manage profiles]**: read, create, edit, and delete profiles.</li><li> **[!DNL Manage segments]**: read, create, edit, and delete segment definitions.</li><li>**[!DNL View datasets]**: read-only access to datasets.</li>  <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li><li>**[!DNL View schemas]**: read-only access to schemas.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View messages presets]**: read-only access to messages presets.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

## [!DNL Orchestrated Campaign Viewer] {#orchestrated-campaign-viewer}

The **[!DNL Campaign Viewer]** role allows read-only access to the **[!UICONTROL Orchestrated campaigns]** capabilities. 

Users assigned to this role will not be able to edit or publish. 

This role includes the following permissions:

| Resources | Permissions|
|-|-|
|Orchestrated campaigns| <ul><li>**[!DNL View orchestrated campaigns]**: read-only access to campaigns.</li><li>**[!DNL View orchestrated campaigns report]**: read-only access to campaigns reports.</li></ul>|
|Messages|<ul><li>**[!DNL View messages]**: view messages.</li><li>**[!DNL View messages report]**: view and edit message reports.</li></ul>|
|Decision management| <ul><li>**[!DNL View decisions]**: read-only access to decisions entities.</li></ul>|
|Adobe Experience Platform| <ul><li>**[!DNL Enable AI Assistant]**: enable or access AI-powered campaign and audience features.</li> <li>**[!DNL View operational insights]**: read-only access to system-level insights and monitoring dashboards.</li></ul>|
|Channel configurations| <ul><li>**[!DNL Manage custom dashboards]**: create, edit, and delete custom dashboards.</li><li>**[!DNL View orchestrated campaigns admin]**: Read-only access to links and reconciliations between Adobe Experience Platform Profiles and Relational store entities section.</li></ul>|

-->