---
title: 回退優惠方案資料集
description: 本區段列出匯出資料集中用於後援優惠方案的所有欄位。
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 3%

---

# 回退優惠方案資料集 {#fallback-dataset}

每次修改優惠方案時，都會更新後援優惠方案的自動產生資料集。

![](../../assets/dataset-fallback.png)

資料集中最新成功的批次資料會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>了解如何在 [本節](../export-catalog/access-dataset.md).

以下是可在 **[!UICONTROL Decision Object Repository - Fallback Offers]** 資料集。

## 識別碼

**欄位：** _id
**標題：** 識別碼
**說明：** 記錄的唯一標識符。
**類型:**&#x200B;字串

## _體驗

**欄位：** _體驗
**類型：** 物件

### _experience > decisioning

**欄位：** 決策
**類型：** 物件

#### 「體驗>決策>特性」

**欄位：** 特徵
**標題：** 決策選項特徵
**說明：** 屬於此特定決策選項的其他屬性或屬性。 不同的例項可能具有不同的特性（地圖中的索引鍵）。 特徵是用於區分一個決策選項與其他決策選項的名稱值組。 特徵用作表示此決策選項的內容中的值，以及用於分析和優化選項效能的功能。 當每個例項都有相同的屬性或屬性時，該方面應該建模為衍生自決策選項詳細資料的擴充架構。
**類型：** 物件

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### 「體驗>決策>內容」

**欄位：** 內容
**標題：** 內容詳細資料
**說明：** 內容項目，以在不同內容中呈現決策項目。 單一決策選項可以有多種內容變體。 內容是指針對受眾以在（數位）體驗中消費的資訊。 內容會透過管道傳遞至特定版位。
**類型：** 陣列

**「體驗>決策>內容>元件」**

**欄位：** 元件
**說明：** 代表決策選項的內容元件，包括其所有語言變體。 特定元件由「dx:format」、「dc:subject」和「dc:language」或其組合找到。 此中繼資料可用來尋找或呈現與優惠方案相關聯的內容，並根據版位合約加以整合。
**類型：** 陣列
**必要：** &quot;_type&quot;, &quot;_dc&quot; <!--TBC?-->

* **_experience > decisioning > contents > components >內容元件類型**

   **欄位：** _type
   **標題：** 內容元件類型
   **說明：** 枚舉的URI集，其中每個值映射到為內容元件指定的類型。 內容表示的某些使用者希望@type值能作為描述內容元件其他屬性的架構的參考。
   **類型:**&#x200B;字串

* **「體驗>決策>內容>元件> _dc」**

   **欄位：** _dc
   **類型：** 物件
   **必要：** &quot;format&quot;

   * **格式**

      **欄位：** 格式
      **標題：** 格式
      **說明：** 資源的物理或數字表現。 通常，格式應包含資源的媒體類型。 可使用格式來確定顯示或操作資源所需的軟體、硬體或其它設備。 建議的最佳實務是從受控辭匯中選取值(例如 [Internet媒體類型](http://www.iana.org/工作總攬/media-types/)定義電腦媒體格式)。
      **類型:**字串
      **範例：** &quot;application/vnd.adobe.photoshop&quot;

   * **語言**

      **欄位：** 語言
      **標題：** 語言
      **說明：** 資源的語言或語言。 \n語言是在語言代碼中指定的，如 [IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)，此為BCP47的一部分，而BCP47會用於XDM的其他位置。
      **類型：** 陣列
      **範例：** &quot;\n&quot;, &quot;pt-BR&quot;, &quot;es-ES&quot;

* **「體驗>決策>內容>元件>_repo」**

   **欄位：** _repo
   **類型：** 物件

   * **id**

      **欄位：** id
      **說明：** 可選的唯一識別碼，用於參考內容存放庫中的資產。 當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：** &quot;urn&quot;:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e」

   * **名稱**

      **欄位：** 名稱
      **說明：** 透過\&quot;repo:id\&quot;提供存放外部資產的存放庫位置相關提示。
      **類型:**&#x200B;字串

   * **repositoryID**

      **欄位：** repositoryID
      **說明：** 可選的唯一識別碼，用於參考內容存放庫中的資產。 當使用Platform API擷取表示法時，用戶端可能會預期其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
      **類型:**字串
      **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

      **欄位：** resolveURL
      **說明：** 可選的唯一資源定位器，用於讀取內容存放庫中的資產。 如此一來，若客戶不了解資產的管理位置以及要呼叫的API，就能更輕鬆取得資產。 這類似於HAL連結，但語義更簡單、更有針對性。
      **類型:**字串
      **範例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;&quot;

* **「體驗>決策>內容>元件」**

   **欄位：** 內容
   **說明：** 直接保留內容的選用欄位。 元件可直接保留簡單內容，而非參考資產存放庫中的內容。 此欄位不適用於複合、複雜和二進位內容資產。
   **類型:**&#x200B;字串

* **_experience > decisioning > contents > components > deliveryURL**

   **欄位：** deliveryURL
   **說明：** 可選的唯一資源定位器，用於從內容傳送網路或服務端點取得資產。 此URL可供使用者代理公開存取資產。
   **類型:**字串
   **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience > decisioning > contents > components > linkURL**

   **欄位：** linkURL
   **說明：** 用戶交互的可選唯一資源定位器。 此URL用於將使用者引用至使用者代理中，且可加以追蹤。
   **類型:**字串
   **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

**_experience > decisioning >內容>位置**

**欄位：** 刊登
**標題：** 版位
**說明：** 符合的位置。 值是所參考之優惠方案版位的URI(@id)。 請參閱結構https://ns.adobe.com/experience/decisioning/placement。
**類型:**&#x200B;字串

#### _experience > decisioning >生命週期狀態

**欄位：** lifecycleStatus
**標題：** 生命週期狀態
**說明：** 生命週期狀態可讓工作流程與物件一起執行。 狀態可能會影響對象可見或被認為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：** 字串
**可能的值：** 「草稿」（預設）、「已核准」、「已上線」、「已完成」、「已封存」

#### _experience > decisioning >決策選項名稱

**欄位：** 名稱
**標題：** 決策選項名稱
**說明：** 顯示在各種用戶介面中的選項名稱。
**類型:**&#x200B;字串

#### _experience > decisioning >標籤

**欄位：** 標籤
**標題：** 標籤
**說明：** 與此實體相關聯的標籤集。 標籤用於篩選運算式，以將整體清單限制為子集（類別）。
**類型：** 陣列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

**欄位：** _repo
**類型：** 物件

### _repo >決策選項ETag

**欄位：** etag
**標題：** 決策選項ETag
**說明：** 建立快照時決策選項對象所在的修訂。
**類型:**&#x200B;字串
