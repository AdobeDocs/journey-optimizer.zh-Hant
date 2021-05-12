---
title: 備援選件資料集
description: 本節列出匯出資料集中用於備援選件的所有欄位。
translation-type: tm+mt
source-git-commit: 70c172e19d5900c898d4850801468a2e186e682d
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 3%

---

# 備援選件資料集{#fallback-dataset}

每次修改選件時，會更新自動產生的備援選件資料集。

![](../../assets/dataset-fallback.png)

資料集中最近成功的批次會顯示在右側。 資料集的架構階層檢視會顯示在左窗格上。

>[!NOTE]
>
>瞭解如何在[本節](../export-catalog/access-dataset.md)中存取選件程式庫每個物件的匯出資料集。

以下是&#x200B;**[!UICONTROL Decision Object Repository - Fallback Offers]**&#x200B;資料集中可使用的所有欄位清單。

## 識別碼

**欄位：** _id標
**題：識** 別碼
**說明：記** 錄的唯一識別碼。**類型:**&#x200B;字串

## _體驗

**欄位：** _experience 
**Type：物** 件

### 決策

**欄位：決** 策類
**型：物** 件

#### 特徵

**欄位：特** 性
**標題：決策選** 項特性說明：屬
**** 於此特定決策選項的附加屬性或屬性。不同的例項可以有不同的特性（地圖中的鍵）。 這些特徵是用於區分一個決策選項和其他決策選項的名稱值對。 特徵用作代表此決策選項的內容值，以及用於分析和最佳化選項效能的功能。 當每個實例具有相同的屬性或屬性時，應將該方面建模為擴展方案，該擴展方案源自決策選項詳細資訊。
**類型：對** 像

<!--Field under Characteristics without title = additionalProperties? Desc = Value of the property. Type: string-->

#### 內容

**欄位：內** 容
**標題：內容詳細** 資訊說明：
**** 內容項目，可在不同的上下文中呈現決策項目。單一決策選項可包含多個內容變體。 內容是指針對受眾的資訊，以便在（數位）體驗中消費。 內容透過通道傳遞至特定位置。
**類型：陣** 列

* **元件**

   **欄位：元** 件
   **說明：** 代表決策選項的內容元件，包括其所有語言變體。特定元件由「dx:format」、「dc:subject」和「dc:language」或其組合找到。 此中繼資料可用來尋找或表示與選件相關的內容，並根據位置合約加以整合。
   **類型：陣** 列
   **必要：** &quot;_type&quot;, &quot;_dc&quot;  <!--TBC?-->

   * **內容元件類型**

      **欄位：** _type
      **標題：內** 容元件類型
      **說明：** 一組列舉的URI，其中每個值對應至指定給內容元件的類型。內容表示法的某些使用者預期@type值會是描述內容元件其他屬性之架構的參考。
      **類型:**&#x200B;字串

   * **_dc**

      **欄位：** _dc
      **類型：對** 像
      **必要：** 「格式」

      * **格式**

         **欄位：格** 式
         **標題：格** 式
         **說明：** 資源的物理或數位表現。通常，格式應包括資源的媒體類型。 該格式可用於確定顯示或操作該資源所需的軟體、硬體或其它設備。 建議的最佳實務是從受控辭彙中選取值(例如，定義電腦媒體格式的[網際網路媒體類型](http://www.iana.org/工作／媒體類型/)清單)。
         **類型:**字串
         **範例：** 「application/vnd.adobe.photoshop」

      * **語言**

         **欄位：語** 言
         **標題：語** 言
         **說明：** 資源的語言或語言。\n語言在[IETF RFC 3066](https://www.ietf.org/rfc/rfc3066.txt)中定義的語言代碼中指定，該代碼是BCP 47的一部分，BCP 47在XDM中的其他位置使用。
         **類型：陣** 列
         **範例：** &quot;\n&quot;、&quot;pt-BR&quot;、&quot;es-ES&quot;
   * **_repo**

      **欄位：** _repo
      **類型：對** 像

      * **id**

         **欄位：** id
         **說明：可** 選的唯一識別碼，可參考內容儲存庫中的資產。當使用平台API來擷取表示法時，用戶端可能會預期有其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
         **類型:**字串
         **範例：** &quot;urn:aid:sc:US:6dc33479-13ca-4b19-b25d-c805eff8a69e&quot;

      * **名稱**

         **欄位：名** 稱
         **說明：** 有關使用\&quot;repo:id\&quot;查找儲存外部資產的儲存庫的位置的提示。
         **類型:**&#x200B;字串

      * **repositoryID**

         **欄位：** repositoryID
         **說明：可** 選的唯一識別碼，可參考內容儲存庫中的資產。當使用平台API來擷取表示法時，用戶端可能會預期有其他屬性\&quot;repo:resolveUrl\&quot;來擷取資產。
         **類型:**字串
         **範例：** &quot;C87932A55B06F7070A49412D@AdobeOrg&quot;

      * **resolveURL**

         **欄位：** resolveURL
         **說明：用** 於讀取內容儲存庫中資產的可選唯一資源定位器。這可讓用戶端更輕鬆地取得資產，而不需瞭解資產的管理位置以及要呼叫的API。 這類似於HAL連結，但語義更簡單、更有針對性。
         **類型:**字串
         **範例：** 「https://plaftform.adobe.io/resolveByPath?path=」「/mycorp/content/projectx/fragment/prod/herobanners/banner14.html3」
   * **content**

      **欄位：內** 容
      **說明：** 可直接保留內容的選用欄位。該元件可以直接保存簡單內容，而不是引用資產儲存庫中的內容。 此欄位不用於複合、複雜和二進位內容資產。
      **類型:**&#x200B;字串

   * **deliveryURL**

      **欄位：** deliveryURL
      **說明：可** 選的唯一資源定位器，可從內容傳送網路或服務端點取得資產。此URL可供使用者代理公開存取資產。
      **類型:**字串
      **範例：** &quot;https://cdn.adobe.io/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;

   * **linkURL**

      **欄位：** linkURL
      **說明：用** 戶交互的可選唯一資源定位器。此URL用於將使用者引薦至使用者代理中，並可加以追蹤。
      **類型:**字串
      **範例：** &quot;https://cdn.adobe.io/tracker?code=23432&amp;redirect=/content/projectx/fragment/prod/static/1232324wd32.jpeg&quot;



* **版位**

   **欄位：位** 置
   **標題：位** 置
   **說明：** 要符合的位置。此值是參考之選件位置的URI(@id)。 請參閱架構https://ns.adobe.com/experience/decisioning/placement。
   **類型:**&#x200B;字串

#### 生命週期狀態

**Field:** lifecycleStatus 
**Title:** Lifecycle Status 
**Description:** Lifecycle status允許使用對象執行工作流。狀態可能會影響對象可見或被認為相關的位置。 狀態更改由使用對象的客戶端或服務驅動。
**類型：字** 串
**可能的值：** &quot;Draft&quot;、&quot;Approved&quot;、&quot;Live&quot;、&quot;Completed&quot;、&quot;Archived&quot;預設值：
**** &quot;Draft&quot;

#### 決策選項名稱

**欄位：** 名稱
**標題：決** 策選項名稱說
**明：** 顯示於各種使用者介面中的選項名稱。**類型:**&#x200B;字串

#### 標記

**Field:** tags 
**Title:** Tags 
**Description:** 與此實體關聯的標籤集。這些標籤用於篩選運算式中，以將整體庫存限制為子集（類別）。
**類型：陣** 列

<!--Field without name under tags: Description: An identifier of a tag object. The value is the @id of the tag that is referenced. See tag schema: https://ns.adobe.com/experience/decisioning/tag. Type: string-->

## _repo

### 決策選項ETag

**欄位：** etag 
**Title:** Decision Option ETag 
**Description:** 拍攝快照時決策選項對象所在的修訂版。**類型:**&#x200B;字串
