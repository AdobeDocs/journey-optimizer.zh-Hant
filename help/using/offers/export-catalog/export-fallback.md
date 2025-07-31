---
title: 遞補優惠資料集
description: 本節列出匯出的資料集中用於遞補優惠的所有欄位
badge: label="舊版" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Data Engineer
level: Intermediate
exl-id: 73bfdc24-28cf-4cfd-bac9-a4ff1ea543e3
source-git-commit: 2a5591617838e76e9cae99c0f97e8aff59311a69
workflow-type: tm+mt
source-wordcount: '1004'
ht-degree: 0%

---

# 遞補優惠資料集 {#fallback-dataset}

每次修改優惠時，自動產生的遞補優惠資料集都會更新。

資料集中最近成功的批次會顯示在右側。 資料集的結構描述階層檢視會顯示在左窗格中。

![](../assets/dataset-fallback.png)

>[!NOTE]
>
>已刪除的遞補優惠會在資料集中標示為已封存。

以下是可以在&#x200B;**[!UICONTROL 決定物件存放庫 — 遞補優惠]**&#x200B;資料集中使用的所有欄位清單。

+++ 識別碼

**欄位：** _id
**標題：**識別碼
**描述：**記錄的唯一識別碼。
**型別：**&#x200B;字串

+++

+++ 體驗(_E)

**欄位：**體驗(_E)
**型別：**&#x200B;物件

+++

+++ 體驗>決策(_E)

**欄位：**決策
**型別：**&#x200B;物件

+++

+++ 體驗>決策>特性(_E)

**欄位：**特性
**標題：**決定選項特性
**描述：**屬於此特定決定選項的其他特性或屬性。 不同的執行個體可以有不同的特性（地圖中的索引鍵）。 特性是名稱值配對，用來區分不同決定選項。 特性會用作內容中的值，代表此決定選項，並作為分析和最佳化選項效能的功能。 當每個執行個體都有相同的屬性或屬性時，該方面應該被模型化為衍生自決定選項詳細資訊的擴充功能結構描述。
**型別：**&#x200B;物件

+++

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

+++ 體驗>決策>內容(_E)

**欄位：**內容
**標題：**內容詳細資料
**描述：**要呈現不同內容中決定專案的內容專案。 單一決定選項可以有多個內容變體。 內容是導向對象以在（數位）體驗中消費的資訊。 內容會透過管道傳送到特定位置。
**型別：**&#x200B;陣列

+++

+++_體驗>決策>內容>元件

**欄位：**元件
**描述：**&#x200B;代表決定選項的內容元件，包括其所有語言變體。 特定元件是由&#39;dx:format&#39;、&#39;dc:subject&#39;和&#39;dc:language&#39;或它們的組合所找到。 此中繼資料用於尋找或表示與優惠方案相關聯的內容，並根據刊登版位合約加以整合。
**型別：**陣列
**必要：** &quot;_type&quot;， &quot;_dc&quot; <!--TBC?-->

* **_experience >決策>內容>元件>內容元件型別**

  **欄位：**型別(_T)
  **標題：**內容元件型別
  **描述：**列舉的URI集合，其中每個值對應到指定給內容元件的型別。 內容表示的某些消費者期望@type值是描述內容元件其他屬性的結構描述的參考。
  **型別：**&#x200B;字串

* **_experience >決策>內容>元件> _dc**

  **欄位：** _dc
  **型別：**物件
  **必要：** &quot;format&quot;

   * **格式**

     **欄位：**格式
     **標題：**格式
     **描述：**&#x200B;資源的實體或數位形式。 通常，格式應該包含資源的媒體型別。 格式可用於決定顯示或操作資源所需的軟體、硬體或其他裝置。 建議的最佳作法是從控制辭彙中選取值(例如，定義電腦媒體格式的[網際網路媒體型別]&#x200B;(https://www.iana.org/ assignments/media-types/)清單)。
     **型別：**字串
     **範例：** &quot;application/vnd.adobe.photoshop&quot;

   * **語言**

     **欄位：**語言
     **標題：**語言
     **描述：**&#x200B;資源的語言。 \n語言是以[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt) （屬於BCP 47，用於XDM的其他地方）中定義的語言代碼指定的。
     **型別：**陣列
     **範例：** &quot;\n&quot;， &quot;pt-BR&quot;， &quot;es-ES&quot;

* **_experience >決策>內容>元件> _repo**

  **欄位：** _repo
  **型別：**&#x200B;物件

   * **id**

     **欄位：** ID
     **描述：**&#x200B;參考內容存放庫中資產的選擇性唯一識別碼。 當使用Platform API擷取表示時，使用者端可能會期待額外的屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
     **型別：**字串
     **範例：** &quot;urn:aaid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

   * **名稱**

     **欄位：**名稱
     **描述：**&#x200B;關於要透過\&quot;repo:id\&quot;尋找儲存外部資產的存放庫位置的一些提示。
     **型別：**&#x200B;字串

   * **repositoryID**

     **欄位：**儲存庫識別碼
     **描述：**&#x200B;參考內容存放庫中資產的選擇性唯一識別碼。 當使用Platform API擷取表示時，使用者端可能會期待額外的屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
     **型別：**字串
     **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

   * **resolveURL**

     **欄位：** resolveURL
     **描述：**選用的唯一資源定位器，可讀取內容存放庫中的資產。 這將讓使用者端更容易取得資產，而無需瞭解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語意較簡單且目的性較強。
     **型別：**字串
     **範例：** &quot;https://plaftform.adobe.io/resolveByPath?path=&quot;/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3&quot;

* **_experience >決策>內容>元件>內容**

  **欄位：**內容
  **描述：**選擇性欄位，可直接保留內容。 元件可以直接儲存簡單的內容，而不是在資產存放庫中參照內容。 此欄位不適用於複合、複雜和二進位內容資產。
  **型別：**&#x200B;字串

* **_experience > decisioning >內容>元件> deliveryURL**

  **欄位：**傳遞URL
  **描述：**選用的唯一資源定位器，可從內容傳遞網路或服務端點取得資產。 使用者代理會使用此URL來公開存取資產。
  **型別：**字串
  **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

* **_experience >決策>內容>元件> linkURL**

  **欄位：** linkURL
  **描述：**使用者互動的選擇性唯一資源定位器。 此URL用於在使用者代理中將一般使用者引薦至，並且可被追蹤。
  **型別：**字串
  **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

+++

+++ _experience >決策>內容>版位

**欄位：**位置
**標題：**位置
**描述：**要遵守的位置。 該值是被參考之優惠方案位置的URI (@id)。 請參閱結構描述https://ns.adobe.com/experience/decisioning/placement 。
**型別：**&#x200B;字串

+++

+++ _experience >決策>生命週期狀態

**欄位：**生命週期狀態
**標題：**生命週期狀態
**描述：**生命週期狀態允許使用物件執行工作流程。 在物件可見或被視為相關的位置，狀態可能會受到影響。 狀態變更是由使用物件的使用者端或服務所驅動。
**型別：**字串
**可能的值：** 「草稿」（預設）、「已核准」、「即時」、「已完成」、「已封存」

+++

+++ _experience >決策>決策選項名稱

**欄位：**名稱
**標題：**決定選項名稱
**描述：**顯示在各種使用者介面中的選項名稱。
**型別：**&#x200B;字串

+++

+++ _experience >決策>標籤

**欄位：**標籤
**標題：**標籤
**描述：**與此實體相關聯的集合限定元集（先前稱為「標籤」）。 集合限定詞用於篩選運算式，以將整體詳細目錄限製為子集（類別）。
**型別：**&#x200B;陣列

+++

<!--Field without name under collection qualifiers: Description: An identifier of a collection qualifier object. The value is the @id of the collection qualifier that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

+++ 存放庫(_R)

**欄位：** _repo
**型別：**&#x200B;物件

+++

+++ _repo >決定選項ETag

**欄位：** etag
**標題：**決定選項ETag
**描述：**決定選項物件拍攝快照時的修訂版本。
**型別：**&#x200B;字串

+++
