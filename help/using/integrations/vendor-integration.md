---
solution: Journey Optimizer
product: journey optimizer
title: 廠商整合
description: 搭配任何公開有效API的外部平台使用Adobe Journey Optimizer整合，加上經過工程測試的供應商模式，讓您在設計設定時獲得信賴度。
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: 整合，廠商，協力廠商
source-git-commit: eab38d6c5f07af0f2dc403abaf0deb3a09f0d392
workflow-type: tm+mt
source-wordcount: '9327'
ht-degree: 5%

---

# 可用的廠商

>[!BEGINSHADEBOX]

目錄：

* [使用整合](integrations.md)
* [開始使用廠商整合](vendor-integration-gs.md)
* **[可用的廠商](vendor-integration.md)**
* [常見問題集](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## 內容與CMS {#content-and-cms}

### 有內容 {#contentful}

>[!BEGINSHADEBOX]

「內容」是指透過REST或GraphQL用於結構化專案和資產的Headless CMS，因此Journey Optimizer可以在傳送或開啟時提取內容。

典型的使用案例包括電子郵件中本地化的主圖區塊、替代文字和CTA，以及動態模組中的產品或促銷專案。 另一個常見模式是依ID擷取特定專案，以進行個人化傳訊。

>[!ENDSHADEBOX]

+++ 進一步瞭解內容功能的必要條件和限制。

適用下列先決條件：

* 具有傳送API存取權及讀取導向API金鑰的充滿內容的空間。
* 清除內容型別和欄位ID；使用Journey Optimizer中的管理員存取權來建立整合。


下列限制和排除專案適用：

* 廣泛列出或分頁的內容性API並不適合這種模式；偏好以特定專案或資產為目標的擷取呼叫。
* 回寫或雙向同步處理不在本範例的範圍之內。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用內容傳送API和您的傳送Token設定&#x200B;**GET**、貼上範例JSON、對應欄位、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用內容傳送API (CDA) URL設定端點： `https://cdn.contentful.com/spaces/{space_id}/environments/{environment_id}/entries/{entry_id}`

1. 選取HTTP方法： **GET**。

1. 新增驗證。 將&#x200B;**`access_token`** **查詢**&#x200B;引數設定為您的內容傳送API Token，如下列&#x200B;**整合欄位範例**&#x200B;所示。 內容也接受`Authorization: Bearer`標題中的相同權杖；使用任何支援的整合欄位。

1. 視需要新增路徑變數（例如，專案ID、地區設定）。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 選取個人化的必要欄位。

1. 視需要設定逾時和快取。

1. 測試連線並啟動。

下表列出此整合請求的範例值。

+++ 整合欄位範例

整合欄位範例（與空間和環境的[內容傳送API](https://www.contentful.com/developers/docs/references/content-delivery-api/){target="_blank"}一致）：

| 欄位 | 價值 |
| -- | -- |
| **URL** | `https://cdn.contentful.com/spaces/{{spaceID}}/environments/{{environment_id}}/entries/{{entry_id}}` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |
| **HTTP方法** | `GET` |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `spaceID` | `spaceID` | `<YOUR_SPACE_ID>` |
| `environment_id` | `environment_id` | `<YOUR_ENV_ID>` |
| `entry_id` | `entry_id` | `<YOUR_ENTRY_ID>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | `access_token` | `<YOUR_API_KEY>` | 查詢引數 |

+++

### Sitecore {#sitecore}

>[!BEGINSHADEBOX]

Sitecore Content Hub和相關雲端API支援DAM樣式的下載和中繼資料流程；以下範例模式以ID下載訂單為中心。

典型的使用案例包括電子郵件內容中的資產或下載中繼資料，以及與Sitecore中管理的DAM工作流程保持一致。

>[!ENDSHADEBOX]

+++ 進一步瞭解Sitecore的先決條件和限制。

適用下列先決條件：

* 租使用者URL和認證（每個API表面的持有者或權杖）。
* Journey Optimizer中的管理員存取權以建立整合。

下列限制和排除專案適用：

* 主機名稱和路徑因Sitecore產品而異。 僅使用您的租使用者公開的端點。
* OAuth存取權杖、重新整理和生命週期都必須遵循Sitecore安全性原則。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 在下載順序路徑上設定&#x200B;**GET**、根據Sitecore設定授權標頭、從內容對應`id`、貼上範例JSON、對應欄位，以及針對資產延遲調整逾時。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Content Hub API設定端點（範例：依ID下載訂單）。 範例URL模式：

   `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{id}`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

在Journey Optimizer中設定此範例呼叫時，請使用下列欄位。 在[Sitecore檔案](https://doc.sitecore.com/){target="_blank"}中確認您產品（Content Hub、XM Cloud等）的主機名稱和API版本。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://xmapps-api.sitecorecloud.io/api/v1/downloadorders/{{id}}` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `id` | `id` | `<id_of_download_order>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| Authorization | Authorization | 常數 | 持有人`<token>` | 是（開啟） |
| If-Modified-Since | If-Modified-Since | 變數 | 2019-08-24T14:15:22Z | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | X-Auth-Token | `<token>` | Header |

+++

### Salsify {#salsify}

>[!BEGINSHADEBOX]

Salsify是一種PIM，具有適用於產品、管道和數位資產的API。

典型的使用案例包括電子郵件中的產品屬性或媒體URL，以及符合聯合目錄資料的訊息傳送。

>[!ENDSHADEBOX]

+++ 深入瞭解Salsify的先決條件和限制。

適用下列先決條件：

* API權杖和組織內容；可從設定檔或內容解析的產品ID。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 非常大的目錄：如果整合需要每個實體的擷取，請避免大量列出端點。
* 「銷售」角色許可權可限制屬性可見性。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 比起大量目錄呼叫、設定持有人驗證、貼上範例JSON、對應欄位、測試、啟動，偏好使用單一產品擷取。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Salsify Product API設定端點。 範例URL模式：

   `https://api.salsify.com/v1/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

有些較舊的參考重複使用Salsify的下載順序樣式路徑；您的租使用者可能會改用`https://app.salsify.com/api/v1/orgs/{org_id}/products/{salsify_id}`或類似專案。 在[Salsify developers](https://developers.salsify.com/){target="_blank"}中確認。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://app.salsify.com/api/v1/orgs/{{org_id}}/products/{{salsify_id}}` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `org_id` | `org_id` | `<org_id>` |
| `salsify_id` | `salsify_id` | `<salsify_id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設引數） | Content-Type | 常數 | application/json | 是（開啟） |
| Authorization | Authorization | 常數 | `Bearer <YOUR_TOKEN_HERE>` | 是（開啟） |
| If-Modified-Since | If-Modified-Since | 變數 | 2019-08-24T14:15:22Z | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | `apiKey` | `<your_api_key>` | Header |

+++

### Contentstack {#contentstack}

>[!BEGINSHADEBOX]

Contentstack是Headless CMS；REST傳送通常用於Journey Optimizer中的JSON欄位對應。

典型的使用案例是將橫幅或促銷活動的專案與包含地區設定的引數搭配使用。

>[!ENDSHADEBOX]

+++ 深入瞭解Contentstack的先決條件和限制。

適用下列先決條件：

* 棧疊API金鑰、傳遞Token、環境名稱和內容型別UID。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 此模式使用REST JSON進行欄位對應；GraphQL傳送會遵循不同的整合路徑。
* 使用與生產環境相適應的傳遞權杖；預覽和發佈的流程不可互換。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 根據Contentstack需要新增`api_key`和`access_token`標頭、包含`environment`查詢引數、貼上範例JSON、對應欄位、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用內容傳送API設定端點。 範例URL模式：

   `https://cdn.contentstack.io/v3/content_types/{content_type_uid}/entries/{entry_uid}`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

整合欄位範例。 請參閱[Contentstack內容傳送API](https://www.contentstack.com/docs/developers/apis/content-delivery-api/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://cdn.contentstack.io/v3/content_types/{{content_type_uid}}/entries/{{entry_uid}}` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |
| 標頭 | 不需要額外的標頭。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `content_type_uid` | 內容型別UID | `<your_content_type_uid>` |
| `entry_uid` | 進入UID | `<your_entry_uid>` |

**驗證**

| 金鑰名稱 | 索引鍵值 | 新增至 |
| --- | --- | --- |
| `api_key` | `<YOUR_STACK_API_KEY>` | Header |
| `access_token` | `<YOUR_DELIVERY_TOKEN>` | Header |

Contentstack需要&#x200B;**兩個**&#x200B;金鑰做為傳遞要求的標頭。

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `environment` | 環境名稱 | 變數 | `<your_environment_name>` | 是（開啟） |

+++

### Akeneo {#akeneo}

>[!BEGINSHADEBOX]

Akeneo PIM會公開產品、屬性和媒體的REST API。

典型的使用案例包括電子郵件模組中的受管控產品資料以及歷程中特定頻道的屬性。

>[!ENDSHADEBOX]

+++ 進一步瞭解Akeneo的先決條件和限制。

適用下列先決條件：

* PIM基底URL和OAuth使用者端；產品UUID或識別碼策略。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* PIM回應可能會很大。 僅對應個人化所需的屬性。
* 寫入作業不在典型的唯讀個人化範例的範圍內。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用&#x200B;**GET**&#x200B;搭配持有人權杖、在查詢旗標中僅要求所需的屬性選項、貼上範例JSON、對應最小屬性集、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Akeneo REST API設定端點。 範例URL模式：

   `https://{pim-host}/api/rest/v1/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例模式： `https://{pim-host}/api/rest/v1/products-uuid/{uuid}`與`Accept: application/json`。 請參閱[Akeneo API](https://api.akeneo.com/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{your-akeneo-domain}}.com/api/rest/v1/products-uuid/{{uuidProduct}}` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `uuidProduct` | UUID | `<product_uuid>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Authorization | Authorization | 常數 | `Bearer <YOUR_TOKEN>` | 是（開啟） |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `with_attribute_options` | 包含屬性選項 | 變數 | 假 | 否（關閉） |
| `with_quality_scores` | 包含品質分數 | 變數 | 假 | 否（關閉） |
| `with_completenesses` | 包含完整性 | 變數 | 假 | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | `Bearer <YOUR_ACCESS_TOKEN>` | Header |

+++

### 木蘭花 {#magnolia}

>[!BEGINSHADEBOX]

依部署而定，Magnolia提供Headless和REST傳送端點。

典型的使用案例是為行銷模組提供內容節點或片段。

>[!ENDSHADEBOX]

+++ 進一步瞭解Magnolia的先決條件和限制。

適用下列先決條件：

* 執行個體URL和權杖或基本驗證；工作區和傳遞路徑。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* REST傳遞URL取決於已安裝的Magnolia模組和設定。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用您的模組公開的公開傳送URL模式、根據Magnolia指引進行驗證（匿名傳送與受保護內容的Token）、貼上範例JSON、對應欄位、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Magnolia REST （傳送）設定端點。 範例URL模式：

   `https://{author-or-public}/.rest/delivery/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例模式： `https://{domain}/magnoliaAuthor/.rest/delivery/...`或公開傳遞導覽樣式URL。 您的路徑取決於已安裝的模組。 請參閱[Magnolia檔案](https://docs.magnolia-cms.com/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `http://{{your-domain}}/magnoliaAuthor/.rest/delivery/<myEndpoint>/travel/@nodes` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 常數 | application/json | 是（開啟） |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | `<bearer_token>` | Header |

注意：傳送API是用於不需要登入的內容之其餘匿名角色。 為了安全存取受保護的資料，建議使用更健全的方法，例如API Token或OAuth 2.0。

+++


## 忠誠度和獎勵 {#loyalty-and-rewards}

### 武謝里菲 {#voucherify}

>[!BEGINSHADEBOX]

Voucherify提供促銷活動和熟客REST API （行銷活動、憑單、熟客方案）。

典型的使用案例包括讀取內容中優惠方案的忠誠度或促銷狀態，以及顯示適當的層級或平衡。

>[!ENDSHADEBOX]

+++ 深入瞭解Voucherify的先決條件和限制。

適用下列先決條件：

* 應用程式ID和密碼（依地區/叢集）；清楚說明您呼叫的忠誠度或行銷活動端點。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 避免在面對客戶的錯誤或訊息內容中公開內部促銷活動或行銷活動識別碼。
* 套用應用程式層級的速率限制。 依據驗證指引設定重試和快取。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 設定叢集的基底URL、新增必要的標頭(`X-APP-ID`、`X-APP-TOKEN`)、使用篩選器或ID限制清單端點、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用忠誠度/REST API設定端點。 根據[Voucherify](https://docs.voucherify.io/){target="_blank"}，設定您地區的&#x200B;**叢集**&#x200B;主機和路徑。 範例URL模式：

   `https://{cluster}.voucherify.io/`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

整合欄位範例。 完整參考： [Voucherify API](https://docs.voucherify.io/reference/introduction){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{cluster}}.voucherify.io/v1/loyalties/{{campaignId}}/members` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `cluster` | `cluster` | `<your_cluster>` |
| `campaignId` | `campaignId` | `<loyalty_campaign_Id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| X-APP-ID | X-APP-ID | 常數 | `<YOUR-APP-ID>` | 是（開啟） |
| X-Voucherify-Channel | X-Voucherify-Channel | 常數 | Voucherify檔案 | 否（關閉） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `limit` | `limit` | 變數 | 10 | 否（關閉） |
| `page` | `page` | 變數 | 1 | 否（關閉） |
| `customer` | `customer` | 變數 | `<customer_identifier>` | 否（關閉） |
| `created_at` | `created_at` | 變數 | `<iso8601_date>` | 否（關閉） |
| `updated_at` | `updated_at` | 變數 | `<iso8601_date>` | 否（關閉） |
| `order` | `order` | 變數 | `<sort_field>` | 否（關閉） |
| `code` | `code` | 變數 | `<loyalty_card_code>` | 否（關閉） |
| `ids` | `ids` | 變數 | `<array_of_ids>` | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | X-APP-TOKEN | `<YOUR-APP-TOKEN>` | Header |

+++

### Talon.One {#talon-one}

>[!BEGINSHADEBOX]

Talon.One是促銷和忠誠度規則引擎，使用REST API來處理工作階段、效果和設定檔。

典型的使用案例包括個人化內容中的購物車或設定檔層級的促銷活動，以及忠誠度進度或獎勵顯示。

>[!ENDSHADEBOX]

+++ 進一步瞭解Talon.One的先決條件和限制。

適用下列先決條件：

* API金鑰和部署特定的基底URL；應用程式或促銷活動範圍的識別碼。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 工作階段密集型流程可能需要仔細對應至整合請求模型。
* 請參閱Talon.One速率限制和冪等指引。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 在您需要的設定檔或成就路徑上使用&#x200B;**GET**，將`Authorization: ApiKey-v1 <key>`設為紀錄，貼上範例JSON，對應欄位，測試，啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Talon.One整合API設定端點。 範例URL模式：

   `https://{your-domain}.talon.one/v1/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{your-deployment}}.talon.one/v1/customer_profiles/{{integrationId}}/achievements/{{achievementId}}` |
| **HTTP方法** | `GET` |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `your-deployment` | `your-deployment` | `<your_deployment>` |
| `integrationId` | `integrationId` | `<integrationId>` |
| `achievementId` | `achievementId` | `<achievementId>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `progressStatus` | `progressStatus` | 變數 | 進行中/已完成/已過期 | 否（關閉） |
| `startDate` | `startDate` | 變數 | 2024-05-29T15:04:05+07:00 | 否（關閉） |
| `endDate` | `endDate` | 變數 | 2024-05-29T15:04:05+07:00 | 否（關閉） |
| `pageSize` | `pageSize` | 變數 | `<default_page_size>` | 否（關閉） |
| `skip` | `skip` | 變數 | `<items_to_skip>` | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | ApiKey-v1 `<YOUR_API_KEY>` | Header |

+++

### 安塔沃 {#antavo}

>[!BEGINSHADEBOX]

Antavo是一種企業忠誠度平台，具有適用於成員、獎勵和事件的REST API。

典型的使用案例包括電子郵件或推播中的點數、層級或獎勵，以及忠誠度狀態所驅動的優惠。

>[!ENDSHADEBOX]

+++ 深入瞭解Antavo的先決條件和限制。

適用下列先決條件：

* 棧疊URL和API認證；視需要程式或商店識別碼。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 客戶PII必須根據Antavo合約和您的隱私權政策處理。
* 使用Antavo確認您環境的API版本和穩定端點。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用供應商的驗證（例如查詢中的API金鑰）設定&#x200B;**GET**，避免公開PII違反原則、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Antavo Enterprise API設定端點。

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例整合欄位使用&#x200B;**暫存**&#x200B;主機；生產使用您的Antavo棧疊主機名稱。 請參閱[Antavo檔案](https://antavo.com/docs/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://api.staging.antavo.com/customers/{{customer_id}}/activities/offers` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `customer_id` | `customer_id` | `<customer_id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| 接受 | 接受 | 常數 | application/json | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | `api_key` | `<YOUR_API_KEY>` | 查詢參數 |

+++

### Salesforce忠誠度 {#salesforce-loyalty}

>[!BEGINSHADEBOX]

Salesforce忠誠度管理會公開Salesforce平台上的REST API，供成員、計畫和交易使用。

典型的使用案例包括顯示歷程中的層級、點數或好處，以及根據CRM和忠誠度資料調整訊息。

>[!ENDSHADEBOX]

+++ 進一步瞭解Salesforce忠誠度的必要條件和限制。

適用下列先決條件：

* Salesforce例項、連線的應用程式或整合使用者，以及適合您組織的OAuth。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* Salesforce API限制和OAuth權杖重新整理必須設計到您的整合中。
* 欄位層級安全性和共用規則控管API回應中顯示的欄位。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用您的團隊核准的忠誠度整合端點、完成Salesforce OAuth、貼上範例JSON、對應欄位、遵守複合API限制、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Salesforce忠誠度管理REST設定端點。 範例URL模式：

   `https://{instance}.salesforce.com/services/data/vXX.X/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

使用針對您組織的API版本記錄的熟客方案管理&#x200B;**成員設定檔** GET作業；路徑包含方案和成員識別碼。 檢視[Salesforce開發人員](https://developer.salesforce.com/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{your-instance}}.my.salesforce.com/services/data/{{version}}/connect/loyalty/management/members` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |
| `version` | `version` | `version` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| 接受 | 接受 | 常數 | application/json | 否（關閉） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `membershipNumber` | `membershipNumber` | 變數 | `<membership_number>` | 否（關閉） * |
| `membershipId` | `membershipId` | 變數 | `<membership_id>` | 否（關閉） * |
| `posMemId` | `posMemId` | 變數 | `<pos_mem_id>` | 否（關閉） * |

\*至少需要三者之一。

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | `<access_token>` | Header |

+++

### 毛細管 {#capillary}

>[!BEGINSHADEBOX]

Capillary提供零售棧疊中常見的忠誠度和參與API。

典型的使用案例包括個人化歷程中的點、層級或優惠。

>[!ENDSHADEBOX]

+++ 深入瞭解Capillary的先決條件和限制。

適用下列先決條件：

* API主機和驗證（通常為已簽署的要求；請遵循毛細血管檔案）。
* 端點的程式識別碼。

下列限制和排除專案適用：

* 驗證配置和區域主機會因部署而異。 請用「毛細管」確認您的棧疊。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 視需要設定標頭，例如`CAP-API-ACCESS-TOKEN`、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Capillary API設定端點。

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例： `https://ushc.intouch.capillarytech.com/api/v3/rewards/{reward_id}` （主機因地區而異）。 使用[毛細管](https://capillarytech.com/){target="_blank"}驗證主機和驗證配置。


| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://ushc.intouch.capillarytech.com/api/v3/rewards/{{reward_id}}` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `reward_id` | 獎勵ID | `<your_reward_id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type | Content-Type | 常數 | application/json | 是（開啟） |
| CAP-API-ACCESS-TOKEN | 存取權杖 | 常數 | `<YOUR_ACCESS_TOKEN>` | 是（開啟） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | CAP-API-ACCESS-TOKEN | `<YOUR_ACCESS_TOKEN>` | Header |

+++


## 範本和傳訊 {#templates-and-messaging}

### 樣板 {#stensul}

>[!BEGINSHADEBOX]

Stensul是用於核准範本的電子郵件建立平台；Journey Optimizer可以透過其API使用範本中繼資料和結構化區域。

典型的使用案例包括匯入核准的範本並將區域對應至設定檔屬性，以及針對可擴充的行銷活動組建重複使用受管控區塊。

>[!ENDSHADEBOX]

+++ 進一步瞭解Stensul的必要條件和限制。

適用下列先決條件：

* 具有API存取權的範本帳戶和具有已定義權杖的已發佈範本。
* Journey Optimizer中的管理員存取權以建立整合。

下列限制和排除專案適用：

* 就地編輯WYSIWYG中的Journey Optimizer樣板範本在此不說明。
* 範本裝載中的大型或複雜HTML可能需要安全性審查和淨化。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入整合名稱。

1. 使用樣板範本API URL設定端點。 範例URL模式：

   `https://api.stensul.com/v1/templates/{template_id}`

1. 設定驗證（API金鑰或每個模具API檔案的OAuth）。

1. 定義路徑變數，例如範本ID。

1. 貼上用於欄位偵測的範例JSON回應。

1. 將必要的範本欄位對應至Journey Optimizer個人化欄位。

1. 測試連線並啟動。

### 萬用字元 {#marigold}

>[!BEGINSHADEBOX]

Marigold會公開忠誠度和參與API；主機會因地理位置而異（歐盟與美國的模組主機名稱）。

典型的使用案例是使用Marigold計畫的忠誠度或偏好設定資料來豐富訊息。

>[!ENDSHADEBOX]

+++ 進一步瞭解Marigold的先決條件和限制。

適用下列先決條件：

* 來自您合約的基本URL和認證；可能的話，請使用最低許可權的API使用者。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 端點因Marigold產品而異。 驗證Marigold是否支援您的部署。
* 回應中的個人資料必須符合您的DPA和保留政策。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 指向您地區的Marigold主機、設定驗證（下列範例使用包含金鑰和密碼的`X-Api-Key`）、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Marigold REST API設定端點。

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

1. Marigold根據客戶執行個體所在的地理區域使用2個端點：

   * 歐洲： `https://{{customername}}.module.slgnt.eu`
   * 美國： `https://{{customername}}.module.slgnt.us`

下表列出此整合請求的範例值。

+++ 整合欄位範例

基礎主機依存於區域（例如`https://{{customername}}.module.slgnt.eu`或`https://{{customername}}.module.slgnt.us`）。 使用Marigold確認您部署的路徑。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{customername}}.module.slgnt.{{locale}}/Portal/Api/organizations/{{organization}}/content/{{api_name}}` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `customername` | `customername` | `<your_name>` |
| `locale` | `locale` | `eu` / `us` |
| `organization` | `organization` | `<your_organization>` |
| `api_name` | `api_name` | `<api_name>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | X-Api-Key | `<apiKey>:<apiSecret>` | Header |

+++

### Adobe Target Recommendations {#adobe-target-recommendations}

>[!BEGINSHADEBOX]

Adobe Target包含適用於伺服器端或整合式體驗的建議與傳送API，但須視權利而定。

典型的使用案例包括將建議插入您在Journey Optimizer中撰寫的體驗，以及將索引鍵與設定檔或Experience Platform內容對齊。

>[!ENDSHADEBOX]

+++ 進一步瞭解Adobe Target Recommendations的先決條件和限制。

適用下列先決條件：

* 目標與建議；IMS組織和支援的驗證。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 推薦和傳遞API需要特定引數（例如mbox或產品識別碼）。 請依照Adobe Target檔案操作。
* 調整傳送磁碟區及使用案例的延遲和快取。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 傳遞呼叫通常是具有JSON內文的&#x200B;**POST**。 根據[目標驗證](https://experienceleague.adobe.com/zh-hant/docs/target-dev/developer/api/configure-authentication){target="_blank"}設定OAuth、貼上範例回應、對應欄位、在預期的磁碟區下測試。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Target Recommendations/傳送API設定端點。

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{client}}.tt.omtrdc.net/rest/v1/delivery` |
| 原則 | 視需要設定原則層級的詳細資訊。 |
| **HTTP方法** | `POST` |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `client` | `client` | `<client_name>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| 使用者端 | 使用者端 | 變數 | `<customer_client_code>` | 是（開啟） |
| sessionId | sessionId | 變數 | ` <session_identifier>` | 是（開啟） |

**驗證**

參考[Target驗證組態](https://experienceleague.adobe.com/zh-hant/docs/target-dev/developer/api/configure-authentication)並將JSON新增至承載。

**要求承載**

```Sample Request Payload JSON
{
  "id": {
    "tntId": "<YOUR_TENANT_ID>"
  },
  "context": {
    "channel": "web",
    "address": {
      "url": "https://example.com/store.html"
    },
    "screen": {
      "width": 1200,
      "height": 1400
    }
  },
  "experienceCloud": {
    "analytics": {
      "logging": "server_side",
      "supplementalDataId": "<supDataId>",
      "trackingServer": "sstats.adobe.com"
    }
  },
  "execute": {
    "pageLoad": {
      "parameters": {
        "pageType": "checkout",
        "preferredCurrency": "$"
      }
    },
    "mboxes": [
      {
        "index": 1,
        "name": "orderConfirmPage"
      }
    ]
  },
  "prefetch": {
    "views": [
      {
        "parameters": {
          "ad": "view"
        }
      }
    ],
    "mboxes": {
      "index": 1,
      "name": "SummerOffer"
    }
  }
}
```

+++


## 資料、天氣和作業 {#data-weather-and-operations}

### AccuWeather {#accuweather}

>[!BEGINSHADEBOX]

AccuWeather會公開預測和位置REST API，讓訊息可包含天氣感知程式碼片段。

典型的使用案例包括電子郵件或推播中的簡短預測，以及使用與設定檔或內容繫結的預測值量身打造內容。

>[!ENDSHADEBOX]

+++ 進一步瞭解AccuWeather的先決條件和限制。

適用下列先決條件：

* API訂閱和金鑰；位置金鑰或城市搜尋流程。
* Journey Optimizer中的管理員存取權以建立整合。

下列限制和排除專案適用：

* 確認AccuWeather訂閱層級的JSON回應圖形；整合會從JSON回應對應欄位。
* 觀察AccuWeather速率限制和建議的快取。
* 解決`locationKey`通常需要在預測呼叫之前有單獨的地理位置或城市搜尋請求。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 除非您的訂閱另有需求，否則請使用&#x200B;**GET**，從設定檔/內容附加`apiKey`查詢引數、對應`locationKey`和其他變數、貼上範例JSON、對應欄位，然後測試。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用每日預測API設定端點。 範例URL模式：

   `https://dataservice.accuweather.com/forecasts/v1/daily/{days}day/{locationKey}`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++整合欄位範例

整合欄位範例。 詳細資訊和層級在[AccuWeather API](https://developer.accuweather.com/apis){target="_blank"}中說明。 您經常使用個別的位置搜尋呼叫（例如`.../locations/v1/cities/search?q={{cityName}}`）來解析`locationKey`。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://dataservice.accuweather.com/forecasts/v1/daily/{{days}}day/{{locationKey}}` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `days` | `days` | `15` |
| `locationKey` | `locationKey` | `<desired_location_key>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `format` | `format` | 變數 | json | 否（關閉） |
| `language` | `language` | 變數 | en-US | 否（關閉） |
| `details` | `details` | 變數 | False | 否（關閉） |
| `metric` | `metric` | 變數 | False | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | `apiKey` | `<YOUR_API_KEY>` | 查詢參數 |

+++

### 船站 {#shipstation}

>[!BEGINSHADEBOX]

ShipStation為承運商、標籤和追蹤提供運送和訂單API。

典型的使用案例包括交易式訊息中的訂單狀態、追蹤連結或傳遞ETA。

>[!ENDSHADEBOX]

+++ 深入瞭解ShipStation的先決條件和限制。

適用下列先決條件：

* API金鑰和密碼（每個ShipStation檔案的基本驗證）。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 請勿在訊息內容中公開ShipStation API金鑰；僅將認證保留在整合設定中。
* 分頁清單端點可能不適合整合；儘可能偏好單一資源GET。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 鎖定您需要的資源（訂單與出貨）、根據[ShipStation API](https://www.shipstation.com/docs/api/){target="_blank"}進行驗證、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用ShipStation REST API設定端點。 範例URL模式：

   `https://ssapi.shipstation.com/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

下列&#x200B;**取得計時器**&#x200B;範例說明一個ShipStation自動化計時呼叫。 在Journey Optimizer中重製時，請使用ShipStation整合指南中的確切路徑和驗證。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://dashboard.sendtric.com/api/v1/timers/{{id}}` |
| **HTTP方法** | `POST` |
| **原則** | 視需要設定原則層級的詳細資訊。 |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | apiKey | `<your_api_key>` | Header |

**要求承載**

```Sample Request Payload
{
    "external_batch_id": "se-28529731",
    "batch_notes": "This is my batch",
    "shipment_ids": [
      "se-28529731"
    ],
    "rate_ids": [
      "se-28529731"
    ]
}
```

+++

### RevenueCat {#revenuecat}

>[!BEGINSHADEBOX]

RevenueCat提供應用程式的訂閱狀態和權益API。

典型的使用案例是在原則允許的生命週期行銷活動中反映訂閱狀態。

>[!ENDSHADEBOX]

+++ 深入瞭解RevenueCat的先決條件和限制。

適用下列先決條件：

* 機密API金鑰和應用程式識別碼；設定檔與RevenueCat客戶ID之間的穩定對應。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 保護秘密API金鑰，並遵循您的輪換原則。
* 訂閱和權益資料是敏感的。 符合隱私權與同意要求。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 呼叫下面模型化的REST **GET**、使用機密金鑰標頭進行驗證、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用RevenueCat REST API設定端點。 範例URL模式：

   `https://api.revenuecat.com/v1/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例模式：使用RevenueCat的&#x200B;**「從[RevenueCat檔案](https://docs.revenuecat.com/){target="_blank"}取得產品** （或同等產品/權益GET）」以及專案的基本URL和版本。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://api.revenuecat.com/projects/{{project_id}}/products/{{product_id}}` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `project_id` | `project_id` | `<project_id>` |
| `product_id` | `product_id` | `<product_id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `country` | `country` | 變數 | `<iso_country_code>` | 否（關閉） |
| `locale` | `locale` | 變數 | `<locale_code>` | 否（關閉） |
| `parentId` | `parentId` | 變數 | `<parent_category_id>` | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | `Bearer <token>` | Header |

+++

### Databricks {#databricks}

>[!BEGINSHADEBOX]

Databricks透過lakehouse資料提供SQL和REST API；較早的草稿結合陳述式執行指引與&#x200B;**jobs/get**&#x200B;範例。

典型的使用案例是使用受控資料表中的小型、非正規化屬性，以進行具有嚴格最低許可權的個人化。

>[!ENDSHADEBOX]

+++ 進一步瞭解Databricks的必要條件和限制。

適用下列先決條件：

* 每個組織原則的Workspace主機、權杖或OAuth；具有最小範圍的服務主體。
* Journey Optimizer中的管理員存取權。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 偏好較窄的讀取路徑；如果您使用&#x200B;**POST**&#x200B;陳述式執行，包括API所需的JSON內文、貼上範例成功回應以進行對應、仔細測試延遲、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Databricks SQL陳述式執行API設定端點。 範例URL模式：

   `https://{workspace-host}/api/2.0/sql/statements/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++整合欄位範例

下面的&#x200B;**GET**&#x200B;工作範例是說明性的；對於SQL驅動的個人化，偏好使用您的工作區支援的[陳述式執行API](https://docs.databricks.com/api/workspace/statementexecution){target="_blank"}模式。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://<databricks-instance>/api/2.0/jobs/get` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |
| Authentication | OAuth |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `job_id` | `job_id` | 變數 | `12` | 是 |

+++

## 評論、同意和社交 {#reviews-consent-and-social}

### 旁白 {#bynder}

>[!BEGINSHADEBOX]

Bynder是具有REST API的DAM；整合功能通常會將OAuth 2.0用於唯讀中繼資料或資產URL。

典型的使用案例包括將資產中繼資料或傳送URL提取至訊息中，以及讓Bynder中的創意核准與歷程保持一致。

>[!ENDSHADEBOX]

+++ 進一步瞭解Bynder的先決條件和限制。

適用下列先決條件：

* 入口網站網域和OAuth使用者端（或核准的權杖方法）。
* 唯讀存取的範圍；Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 分頁和OAuth權杖重新整理必須遵循Bynder的API規則。
* 大型分頁回應：僅對應個人化所需的欄位。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 在選取的端點上設定&#x200B;**GET** （常見的模式為使用者清單）、根據[Bynder](https://developer.bynder.com/){target="_blank"}完成OAuth、避擴音取不必要的資料頁面、對應欄位、測試，然後啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Bynder API v4設定端點。 範例URL模式：

   `https://{your-bynder-domain}/api/v4/users/`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

整合欄位範例。 如需OAuth 2.0裝載詳細資料，請參閱[Bynder API檔案](https://developer.bynder.com/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{your-bynder-domain}}/api/v4/users/` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `your-bynder-domain` | `your-bynder-domain` | `<your-bynder-domain>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| Authorization | Authorization | 常數 | 持有人`<token>` | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `includeInActive` | `includeInActive` | 變數 | False | 否（關閉） |
| `limit` | `limit` | 變數 | 100 | 否（關閉） |
| `page` | `page` | 變數 | 1 | 否（關閉） |

**驗證**

| 類型 | 承載 |
| --- | --- |
| OAuth 2.0 | OAuth 2.0裝載（請參閱Bynder檔案） |

```
{
    "type": "oauth2",
    "endpoint": {
        "uri": ""
    },
    "method": "get",
    "response": {
        "type": "json"
    },
    "request": {
        "header": [
            {
                "key": "client_id",
                "value": ""
            },
            {
                "key": "client_secret",
                "value": ""
            }
        ],
        "queryParams": [
            {
                "key": "grant_type",
                "value": ""
            },
            {
                "key": "scope",
                "value": ""
            }
        ],
        "payload": {
            "type": "json",
            "content": {}
        }
    },
    "credentialPaths": [
        "header.client_id",
        "header.client_secret",
        "queryParam.scope"
    ],
    "tokenPath": "message.token",
    "policy": {
        "timeoutInMilliseconds": 30000,
        "cache": {
            "enabled": true,
            "ttlInSeconds": 300
        },
        "retry": {
            "enabled": false
        }
    },
    "locationConfig": {
        "key": "x-token",
        "location": "query"
    }
}
```

+++

### Trustpilot {#trustpilot}

>[!BEGINSHADEBOX]

Trustpilot會提供適用於業務的API，並在您的使用案例和合約允許的情況下，稽核摘要資料。

典型的使用案例是顯示符合Trustpilot條款的行銷內容中的評論計數或評等。

>[!ENDSHADEBOX]

+++ 深入瞭解Trustpilot的先決條件和限制。

適用下列先決條件：

* API金鑰和核准的使用案例；用於查詢的商業識別碼。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 使用Trustpilot資料必須符合Trustpilot品牌和資料使用政策。
* 速率限制適用於稽核摘要和相關端點。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用必要的查詢驗證設定&#x200B;**GET**、從設定檔或內容對應識別碼、貼上範例JSON、對應欄位、測試、啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Trustpilot API設定端點。 範例URL模式：

   `https://api.trustpilot.com/v1/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

針對您的整合模式，使用來自[Trustpilot開發人員](https://developers.trustpilot.com/){target="_blank"}的類別清單操作；引數會因資源而異。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://api.trustpilot.com/v1/categories` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `country` | `country` | 變數 | `<iso_country_code>` | 否（關閉） |
| `locale` | `locale` | 變數 | `<locale_code>` | 否（關閉） |
| `parentId` | `parentId` | 變數 | `<parent_category_id>` | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | apiKey | `<your_api_key>` | Header |

+++

### Bazaarvoice {#bazaarvoice}

>[!BEGINSHADEBOX]

Bazaarvoice提供評等、評論和UGC API。

典型的使用案例是當原則允許時，在電子郵件中顯示稽核摘要或評分。

>[!ENDSHADEBOX]

+++ 進一步瞭解Bazaarvoice的先決條件和限制。

適用下列先決條件：

* 來自您合約的API密碼金鑰和使用者端識別碼。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 分級和評論的顯示必須遵循Bazaarvoice內容原則。
* 每個API金鑰套用速率限制和快取規則。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用&#x200B;**GET**&#x200B;搭配`passkey`做為Conversations API上的查詢引數，設定`Accept: application/json`，貼上範例JSON，對應欄位，測試，啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Bazaarvoice交談API設定端點。 範例URL模式：

   `https://api.bazaarvoice.com/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例進入點： `https://api.bazaarvoice.com/data/products.json`具有版本和篩選查詢引數。 請參閱[Bazaarvoice開發人員](https://developer.bazaarvoice.com/){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://api.bazaarvoice.com/data/products.json` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**驗證**

| 類型 | 索引鍵值 | 位置 |
| --- | --- | --- |
| 密碼 | `<YOUR_ACCESS_TOKEN>` | 查詢參數 |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `apiversion` | apiversionNumber | 常數 | 5.4 | 是（開啟） |
| `filter` | `filter` | 變數 | 識別碼:47950830 | 否（關閉） |
| `stats` | `stats` | 變數 | 全部 | 否（關閉） |

+++

### OneTrust {#onetrust}

>[!BEGINSHADEBOX]

OneTrust會公開隱私權和同意API （產品專屬的URL和結構描述）。

典型的使用案例是讀取架構和法律審查允許的情況下的條件式內容的同意或偏好設定訊號。

>[!ENDSHADEBOX]

+++ 深入瞭解OneTrust的先決條件和限制。

適用下列先決條件：

* API認證和區域基底URL；傳訊中所使用欄位的法律核准。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 同意和偏好設定資料受到高度規範。 與隱私權與法律團隊協調。
* API路徑和裝載會因OneTrust產品而異。 使用說明檔案說明您的訂閱。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 使用已發佈的結構描述或偏好設定中心路徑您的訂閱檔案，視需要完成OAuth、貼上範例JSON、對應欄位、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用OneTrust API設定端點。 您的租使用者、產品和路徑來自您訂閱的[OneTrust](https://developer.onetrust.com/){target="_blank"}檔案。 範例URL模式：

   `https://{tenant}.my.onetrust.com/api/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://customer.my.onetrust.com/api/consentmanager/v2/preferencecenters/{{preferencecenterid}}/schema` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| **驗證** | OAuth |

**路徑引數**

| 參數 | 名稱 | 值 |
| --- | --- | --- |
| `preferencecenterid` | `preferencecenterid` | `<pref-id>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `state` | `state` | 常數 | 已發佈 | 是 |

+++

#### 偏好設定中心結構（已發佈）

範例（片段）： `https://{tenant}.my.onetrust.com/api/consentmanager/v2/preferencecenters/{preferencecenterid}/schema?state=PUBLISHED`。 確認[OneTrust Developer](https://developer.onetrust.com/){target="_blank"}中的確切路徑。

### Meta {#meta}

>[!BEGINSHADEBOX]

Meta Graph和Marketing API會公開目錄和促銷活動物件，以進行授權的業務整合。

典型的使用案例是使用權杖和原則允許的Meta屬性來豐富內容。

>[!ENDSHADEBOX]

+++ 進一步瞭解Meta的先決條件和限制。

適用下列先決條件：

* 具有正確許可權的系統使用者或應用程式權杖；Business Manager一致性。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* 短期存取權杖需要適用於伺服器端整合的更新或長期策略。
* 遵守Meta平台條款；請勿在訊息裝載中記錄代號或其他秘密。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 圖表呼叫通常是有版本化路徑的&#x200B;**GET**；處理權杖到期、貼上範例JSON、對應欄位、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Meta Graph API設定端點。 範例URL模式：

   `https://graph.facebook.com/vXX.X/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

整合欄位範例。 如需版本設定和存取權杖，請參閱[Graph API](https://developers.facebook.com/docs/graph-api){target="_blank"}。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://graph.facebook.com/{{API_VERSION}}/{{PRODUCT_CATALOG_ID}}/products` |
| **HTTP方法** | `GET` |
| 回應裝載 | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |
| 原則 | 視需要設定原則層級的詳細資訊。 |
| Authentication | OAuth |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `API_VERSION` | `API_VERSION` | `v19.0` |
| `PRODUCT_CATALOG_ID` | `PRODUCT_CATALOG_ID` | `12345` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| 接受 | 接受 | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `fields` | `fields` | 變數 | id | 無 |
| `filter` | `filter` | 變數 | — | 無 |

+++

### Aprimo {#aprimo}

>[!BEGINSHADEBOX]

Aprimo結合行銷作業和適用於記錄、資產和中繼資料的DAM API。

典型的使用案例包括動態內容中的已核准記錄或資產欄位，以及受規管行業中的受管DAM工作流程。

>[!ENDSHADEBOX]

+++ 進一步瞭解Aprimo的先決條件和限制。

適用下列先決條件：

* 租使用者URL和認證（根據您的設定，為OAuth或API金鑰）。
* Journey Optimizer中的管理員存取權。

下列限制和排除專案適用：

* Aprimo欄位層級安全性必須符合您在Journey Optimizer中對應的屬性。
* 大型HAL或JSON裝載：將對應欄位限製為最小必要集。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 在所需的記錄路徑上使用&#x200B;**GET**、傳送必要的標頭（例如`API-VERSION`）、貼上範例JSON （傳回的HAL或JSON）、對應最小欄位集、測試、啟用。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Aprimo DAM /記錄API設定端點。 使用您&#x200B;**租使用者**&#x200B;的API基底URL和記錄路徑（根據Aprimo）。 範例URL模式：

   `https://{tenant}.dam.aprimo.com/`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://productstrategy1.dam.aprimo.com/api/core/record/{{recordID}}` |
| **HTTP方法** | `GET` |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `recordId` | `recordId` | `<record_identifier>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |
| API版本 | API版本 | 常數 | 1 | 是（開啟） |
| 接受 | 接受 | 常數 | application/hal+json OR application/json | 否（關閉） |
| select-record | select-record | 變數 | `<selection_type>` | 否（關閉） |
| select-record-fields | select-record-fields | 變數 | `<field_list>` | 否（關閉） |
| select-field | select-field | 變數 | `<field_selection>` | 否（關閉） |

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | Authorization | 持有人`<token>` | Header |

+++

### Epsilon (Epsilon3) {#epsilon}

>[!BEGINSHADEBOX]

Epsilon會根據企業合約公開API；基本URL和驗證來自您的帳戶團隊（以下事件API範例為說明性）。

典型的使用案例是透過支援的JSON API公開忠誠度或優惠屬性。

>[!ENDSHADEBOX]

+++ 深入瞭解Epsilon (Epsilon3)的先決條件和限制。

適用下列先決條件：

* 來自Epsilon的認證和端點；Journey Optimizer中的管理員存取。

下列限制和排除專案適用：

* 端點與主機因客戶而異。 若沒有Epsilon帳戶團隊的檔案，請勿部署。

+++

使用以下程式，在Journey Optimizer中設定這項整合。 請參閱&#x200B;**範例整合欄位**&#x200B;以取得請求詳細資訊，並在您環境的廠商檔案中確認這些值。

1. 遵循[使用整合](integrations.md)。 請勿猜測公開URL。 使用Epsilon的規格，貼上範例JSON，對應欄位，測試，啟動。

1. 在Journey Optimizer中，移至&#x200B;**[!UICONTROL 組態]** > **[!UICONTROL 管理]**，然後選取&#x200B;**[!UICONTROL 建立整合專案]**。

1. 輸入不含空格的整合名稱。

1. 使用Epsilon API設定端點（根據您的整合規格）。 基本URL和資源路徑由Epsilon帳戶小組提供。 範例URL模式：

   `https://{your-instance}.epsilon3.io/api/...`

1. 選取設定表格中顯示的HTTP方法，通常是GET，除非另有說明。

1. 請完全依照表格和廠商檔案中的指定，設定驗證（標頭、查詢引數或OAuth）。

1. 定義路徑、查詢和標題引數，並視需要將變數對應至設定檔或內容資料。

1. 貼上JSON回應範例，以偵測並對應欄位。

1. 在回應裝載對應中選取個人化所需的欄位。

1. 根據預期的磁碟區設定逾時、重試和快取原則。

1. 測試連線，然後啟動整合。

下表列出此整合請求的範例值。

+++ 整合欄位範例

範例模式： `https://{your-instance}.epsilon3.io/api/v1/planning/events`具有`start`和`end`查詢引數以及標頭型API金鑰。 生產前先向Epsilon確認。

| 欄位 | 價值 |
| --- | --- |
| **URL** | `https://{{your-instance}}.epsilon3.io/api/v1/planning/events` |
| **HTTP方法** | `GET` |
| **原則** | 視需要設定原則層級的詳細資訊。 |
| **回應承載** | 根據API回應，選取並設定要在編寫期間使用的回應欄位。 |

**路徑引數**

| Path引數 | 名稱 | 預設值 |
| --- | --- | --- |
| `your-instance` | `your-instance` | `<your_instance>` |

**標頭**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| Content-Type （預設） | Content-Type | 常數 | application/json | 是（開啟） |

**查詢引數**

| 參數 | 名稱 | 類型 | 值 | 強制 |
| --- | --- | --- | --- | --- |
| `start` | `start` | 變數 | 2019-08-24T14:15:22Z | 是（開啟） * |
| `end` | `end` | 變數 | 2019-08-24T14:15:22Z | 是（開啟） * |
| `eventType` | `eventType` | 變數 | 已排程/未排程 | 否（關閉） |
| `exclude_recurrences` | `exclude_recurrences` | 變數 | true / false | 否（關閉） |

\*選擇性： `eventType` = `unscheduled`，以及`exclude_recurrences` = `true`。

**驗證**

| 類型 | api金鑰名稱 | API金鑰值 | 位置 |
| --- | --- | --- | --- |
| API金鑰 | `<your_username>` | `<EPSILON3_API_KEY>` | Header |

+++

