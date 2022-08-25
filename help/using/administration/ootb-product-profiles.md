---
title: 內建的產品設定檔
description: 瞭解內置產品配置檔案
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
exl-id: 5a968bd8-cf76-4242-aa80-3cfb3d551511
source-git-commit: 5087c5a13eda0b9b5894197b393788f82413690b
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 8%

---

# 內建的產品設定檔 {#ootb-product-profiles}

Adobe Journey Optimizer正在發佈一項新功能，即「內聯創作」，它允許您直接從旅途中建立和創作消息。 有關此新功能的詳細資訊，請參閱此頁。

>[!WARNING]
>
>如果已為 **[!DNL Message Manager]** 僅產品配置檔案，沒有 **[!DNL Journey manager]** 產品配置檔案，您需要為他們分配新的產品配置檔案，以便能夠繼續編輯內容。

此功能將影響以下權限：

| 權限名稱 | 將包含在 |
|:-:|:-:|
| **[!DNL View Messages]** | **[!DNL View Journeys]** |
| **[!DNL View Message reports]** | **[!DNL View Journeys Report]** |
| **[!DNL Manage Messages]** | **[!DNL Manage Journey]** |
| **[!DNL Publish Messages]** | **[!DNL Publish Journeys]** |
| **[!DNL Manage Messages Preview and Test]** | **[!DNL Manage Journeys]** |

**7月25日之後**，與消息相關的權限仍將可用，因為仍然可以訪問消息以啟用轉換，並且您仍可以將其另存為模板。

**截至9月6日**，將刪除與消息相關的權限，並且消息將不再可訪問。

## [!DNL Journey Administrator] {#journey-administrator}

的 **[!DNL Journey Administrator]** 產品配置檔案允許管理菜單，並可以管理和發佈「旅程和決策管理」。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |旅程| <ul><li> **[!DNL Manage journeys]**:讀取、建立、編輯和刪除旅程。</li><li>**[!DNL Publish journeys]**:發佈旅程。</li><li>**[!DNL Manage journeys events, data sources and actions]**:讀取、建立、編輯和刪除事件、源或操作。</li><li>**[!DNL View journeys report]**:閱讀和編輯旅程報告。</li></ul>|
|管理|<ul><li>**[!DNL Manage subdomains delegation]**:讀取、建立、編輯和刪除子域委派。</li><li>**[!DNL Manage IP pools]**:讀取、建立、編輯和刪除ip池。</li><li>**[!DNL Manage PTR records]**:讀取和編輯PTR記錄。</li><li>**[!DNL View PTR records]**:對PTR記錄的只讀訪問。</li><li>**[!DNL Manage channel surfaces]**:讀取、建立、編輯和刪除內容品牌。</li><li>**[!DNL Manage Landing page settings]**:建立、編輯和刪除登錄頁子域和登錄頁預設。</li><li> **[!DNL Manage messages general settings]**:讀取、建立、編輯和刪除消息常規設定。</li><li>**[!DNL Manage SMS settings]**:建立、編輯和刪除啟用SMS通道所需的API憑據和SMS通道曲面。</li><li>**[!DNL Manage suppression rules]**:訪問讀取、建立、編輯和刪除禁止規則。</li><li>**[!DNL View suppression list]**:讀取並導出本地抑制清單。</li><li>**[!DNL Manage alerts]**:啟用/禁用旅程和權利的警報。</li></ul>|
|決策管理|<ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除排名策略。</li></ul>|
|Adobe Experience Platform|<ul><li>**[!DNL Sandbox]**:授予對沙箱的訪問權限。</li><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除配置檔案。</li><li>**[!DNL Read datasets]**:對資料集的只讀訪問。</li><li>**[!DNL Read schemas]**:對架構的只讀訪問。</li><li>**[!DNL Read Identity namespace]**:對標識命名空間的只讀訪問。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>| |Journey Optimizer庫|<ul><li>**[!DNL Manage Library Items]**:添加和刪除中保存的表達式 [!DNL Journey Optimizer] 庫。</li></ul>|

## [!DNL Journey Approver] {#journey-approver}

的 **[!DNL Journey Approver]** 產品配置檔案允許用戶批准交貨並發佈。 他們稍後可以通過 **[!DNL Journey]** 報告。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |旅程| <ul><li>**[!DNL Manage journeys]**:讀取、建立、編輯和刪除旅程。</li><li>**[!DNL Publish journey]**:發佈旅程。</li><li>**[!DNL View journeys events, data sources and actions]**:只讀訪問行程事件、行程自定義操作和行程資料源。</li><li>**[!DNL View journeys report]**:閱讀、編輯行程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自定義報告和使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li>**[!DNL Manage segments]**:讀取、建立、編輯和刪除段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除配置檔案。</li><li>**[!DNL Read datasets]**:對資料集的只讀訪問。</li><li>**[!DNL Read schemas]**:對架構的只讀訪問。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:對通道曲面的只讀訪問。</li></ul>|

## [!DNL Journey Manager] {#journey-manager}

的 **[!DNL Journey Manager]** 產品配置檔案允許用戶建立和編輯 **[!UICONTROL Journeys]** 和所有能力 **[!UICONTROL Journeys]** 卻無法發表。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |旅程| <ul><li>**[!DNL Manage journeys]**:讀取、建立、編輯和刪除旅程。</li><li>**[!DNL View journeys events]**:只讀訪問行程事件、行程自定義操作和行程資料源。</li><li>**[!DNL View journeys report]**:閱讀，編輯行程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自定義報告和使用操作功能。</li></ul>| |Adobe Experience Platform| <ul><li> **[!DNL Manage segments]**:讀取、建立、編輯和刪除段。</li><li>**[!DNL Manage profiles]**:讀取、建立、編輯和刪除配置檔案。</li><li>**[!DNL Read datasets]**:對資料集的只讀訪問。</li><li>**[!DNL Read schemas]**:對架構的只讀訪問。</li><li>**[!DNL Manage merge policies]**:讀取、建立、編輯和刪除合併策略。</li></ul>|
|管理| <ul><li>**[!DNL View channel surfaces]**:對通道曲面的只讀訪問。</li></ul>|

## [!DNL Journey Viewer] {#journey-viewer}

的 **[!DNL Journey viewer]** 產品配置檔案允許對 **[!UICONTROL Journeys]** 和 **[!UICONTROL Decision management]** 功能。

分配給此產品配置檔案的用戶將無法編輯或發佈。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |旅程| <ul><li>**[!DNL View journeys]**:只讀訪問旅行。</li><li>**[!DNL View journeys event, data sources, actions]**:只讀訪問旅程事件和資料源。</li><li>**[!DNL View journeys report]**:只讀訪問行程報告。</li></ul>|
|決策管理| <ul><li>**[!DNL View decisions]**:對決策實體的只讀訪問。</li></ul>|

## [!DNL Decisioning manager] {#decisioning-manager}

的 **[!DNL Decisioning manager]** 產品配置檔案僅允許 **[!UICONTROL Decision management]** 的子菜單。 分配給此產品配置檔案的用戶將只能管理、查看和發佈決策。

此產品設定檔包含下列權限：

|功能 |權限| |-|-| |決策管理| <ul><li>**[!DNL Manage decisions]**:讀取、建立、編輯和刪除決策實體。</li><li>**[!DNL View decisions]**:對決策實體的只讀訪問。</li><li>**[!DNL Manage ranking strategies]**:讀取、建立、編輯和刪除自定義報告和使用操作功能。</li><li>**[!DNL Publish decisions]**:激活或停用決策活動。</li></ul>|
