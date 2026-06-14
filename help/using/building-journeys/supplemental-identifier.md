---
title: 在歷程中使用補充識別碼
description: 瞭解如何在歷程中使用補充識別碼。
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ABOlJ-ZF0a3xLNY-hH6jjFqu53ph4PynNalGkgQ6P8k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 2041
ht-degree: 2%

---

# 在歷程中使用補充識別碼 {#supplemental-id}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用補充識別碼（例如訂單或預訂ID之類的次要識別碼）來針對每個識別碼執行個別的歷程執行個體，並使用其屬性個人化訊息。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="使用補充識別碼"
>abstract="補充識別碼是次要識別碼，提供更多有關歷程執行方式的背景資訊。 若要定義它，請從對象或事件中選取任何非身分屬性（或非個人身分），以作為補充識別碼。"

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="vertical-align: top; padding-right: 20px; border: none;">
      <p>依預設，歷程會在<b>設定檔ID</b>的內容中執行。這表示，只要設定檔在指定歷程中處於作用中狀態，就無法將設定檔重新進入另一個歷程。為避免此問題，除了設定檔ID之外，Journey Optimizer可讓您擷取<b>補充識別碼</b>，例如訂單ID、訂閱ID、處方ID。  
      <p>在此範例中，我們已新增<b>預訂ID</b>作為補充識別碼。</p>
      <p>如此一來，歷程會在與補充識別碼（此處為預訂ID）相關聯的設定檔ID內容中執行。 每個補充識別碼的疊代都會執行一個歷程例項。 如果訪客已進行不同預約，這可在歷程中讓多個入口使用相同的設定檔ID。</p>
      <p>此外，Journey Optimizer可讓您運用補充識別碼的屬性來自訂訊息（例如預訂編號、處方續約日期、產品型別），確保高度相關的通訊。</p>
    </td>
    <td style="vertical-align: top; border: none; text-align: center; width: 40%;">
      <img src="assets/event-supplemental-id.png" alt="補充識別碼範例" style="max-width:100%;" />
    </td>
  </tr>
</table>

➡️ [在影片中探索此功能](#video)

## 護欄與限制 {#guardrails}

* **支援的歷程**： **事件觸發**&#x200B;和&#x200B;**讀取對象**&#x200B;歷程支援補充識別碼。 對象資格歷程（亦即以對象資格活動開始的歷程）中&#x200B;**不支援**。

* **傳入動作**：目前不支援傳入動作（例如應用程式內和Web動作）的補充識別碼。

* **並行執行個體限制**：設定檔不能有超過10個並行歷程執行個體。

* **資料型別和結構描述結構**：補充識別項必須是型別`string`。 它可以是獨立的字串屬性，也可以是物件陣列中的字串屬性。 獨立的字串屬性會產生單一歷程例項，而物件陣列中的字串屬性則會導致物件陣列的每個疊代產生唯一的歷程例項。 不支援字串陣列和地圖。

* **歷程重新進入**

  具有補充識別碼的歷程重新進入行為遵循現有的重新進入原則：

   * 如果歷程不可重新進入，則相同的設定檔ID +補充ID組合無法重新進入歷程。
   * 如果歷程透過時間視窗重新進入，則相同的設定檔ID +補充ID組合可在定義的時間視窗後重新進入。

* **資料使用標籤與實作(DULE)** — 未對補充ID執行DULE驗證檢查。 這表示當歷程尋找資料治理原則違規時，不會考慮此屬性。

* **下游事件設定**

  如果您在歷程下游使用另一個事件，該事件必須使用相同的補充ID並具有相同的ID名稱空間。

* **讀取對象歷程**

   * **商務事件**：如果您使用商務事件，則補充ID已停用。
   * **事件和內容欄位**：補充識別碼不得來自事件或歷程內容欄位。
   * **屬性選擇**：任何非身分屬性（或非個人身分）都可做為所有對象型別（統一設定檔服務、CSV匯入和同盟對象構成）的補充ID。 不允許以人員為基礎的身分屬性。 若為外部對象，請參閱[外部對象的補充識別碼](#external-audiences)以瞭解支援的資料模式和組態需求。
   * **讀取率**：對於使用陣列型別補充ID欄位的讀取對象歷程，讀取對象活動的讀取率限製為每秒500個設定檔。

## 具有補充ID的退出條件行為 {#exit-criteria}

先決條件：為補充ID啟用歷程（透過單一事件或讀取對象活動）

下表說明設定退出條件時，設定檔在啟用ID的補充歷程中的行為：

| 退出條件設定 | 符合退出准則時的行為 |
| ---------------------------- | ---------------------------------- |
| 根據非補充ID事件 | 將會退出該歷程中對應設定檔的所有執行個體。 |
| 根據補充ID事件&#x200B;<br/>*注意：補充ID名稱空間必須符合初始節點的名稱空間。* | 僅會退出相符的設定檔+補充ID例項。 |
| 根據對象 | 將會退出該歷程中對應設定檔的所有執行個體。 |

## 新增補充識別碼並在歷程中運用 {#add}

>[!BEGINTABS]

>[!TAB 事件觸發的歷程]

若要在事件觸發的歷程中使用補充識別碼，請遵循下列步驟：

1. **將補充ID新增至事件**

   1. 建立或編輯所需的事件。 [瞭解如何設定單一事件](../event/about-creating.md)

   1. 在事件組態畫面中，勾選&#x200B;**[!UICONTROL 使用補充識別碼]**&#x200B;選項。

      ![具有補充識別碼選項的事件組態](assets/supplemental-ID-event.png)

   1. 使用運算式編輯器來選取您要當作補充ID使用的欄位（例如，預訂ID、訂閱ID）。

      >[!NOTE]
      >
      >請確定您在&#x200B;**[!UICONTROL 進階模式]**&#x200B;中使用運算式編輯器來選取屬性。

1. **將事件新增至歷程**

   將已設定的事件拖曳至歷程畫布。 它會根據設定檔ID和補充ID來觸發歷程專案。

   ![使用事件觸發的補充識別碼的歷程](assets/supplemental-ID-journey.png)

>[!TAB 讀取對象歷程]

若要在讀取對象歷程中使用補充識別碼，請遵循下列步驟：

1. **在歷程中新增並設定讀取對象活動**

   1. 在您的歷程中拖曳&#x200B;**[!UICONTROL 讀取對象]**&#x200B;活動。

   1. 在活動屬性窗格中，開啟&#x200B;**[!UICONTROL 使用補充識別碼]**&#x200B;選項。

      ![使用補充識別碼設定讀取對象活動](assets/supplemental-ID-read-audience.png)

   1. 在&#x200B;**[!UICONTROL Supplemental identifier]**&#x200B;欄位中，使用運算式編輯器來選取補充識別碼屬性。

   針對從CSV檔案匯入的對象[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant#import-audience){target="_blank"}，如果您的CSV對象包含每個設定檔ID的多個列，請確定先啟用「快速啟用」 — 請參閱[外部對象的補充識別碼](#external-audiences)。

       >[！NOTE]
       >
       >請確定您在&#x200B;**[!UICONTROL 進階模式]**&#x200B;中使用運算式編輯器來選取屬性。
   
>[!ENDTABS]

## 善用補充ID屬性

使用運算式編輯器和個人化編輯器來參照個人化或條件邏輯的補充識別碼屬性。 可從&#x200B;**[!UICONTROL 內容屬性]**&#x200B;功能表存取屬性。

![Personalization編輯器顯示內容的補充識別碼欄位](assets/supplemental-ID-perso.png)

針對事件觸發的歷程，如果您使用陣列（例如，多個處方或原則），請使用公式來擷取特定元素。

+++ 檢視範例

在補充ID為`bookingNum`且屬性位於相同層級`bookingCountry`的物件陣列中，歷程將根據bookingNum逐一檢視陣列物件，並為每個物件建立歷程執行個體。

* 條件活動中的下列運算式將逐一檢視物件陣列，並檢查`bookingCountry`的值是否等於「FR」：

  ```
  @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
  ```

* 電子郵件個人化編輯器中的下列運算式將會逐一檢視物件陣列、提取適用於目前歷程執行個體的`bookingCountry`，並在內容中顯示它：

  ```
  {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
  
  {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
  
  {{/each}}
  ```

* 用來觸發歷程的事件範例：

  ```
  "bookingList": [
        {
            "bookingInfo": {
                "bookingNum": "x1",
                      "bookingCountry": "US"
            }
        },
        {
            "bookingInfo": {
                "bookingNum": "x2",
                "bookingCountry": "FR"
            }
        }
    ]
  ```

+++

## 補充ID和歷程仲裁 {#arbitration}

歷程仲裁（包括規則集中的並行上限和登入計數）在設定檔ID層級操作，而不是（設定檔ID、補充ID）配對層級。 這表示並行次數上限為1可能會封鎖相同設定檔的第二個歷程例項，即使其中包含不同的補充ID值亦然。

在依賴生產中的特定仲裁設定之前，請聯絡您的Adobe代表以取得仲裁行為的指引。

**相關檔案：**

* [歷程上限與仲裁](../conflict-prioritization/journey-capping.md)
* [使用規則集](../conflict-prioritization/rule-sets.md)
* [衝突管理與優先順序](../conflict-prioritization/gs-conflict-prioritization.md)

## 外部對象的補充識別碼 {#external-audiences}

外部對象支援補充ID，包括從CSV檔案[&#128279;](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=zh-Hant#import-audience){target="_blank"}匯入的對象以及使用[同盟對象構成](../audience/get-started-audience-orchestration.md)建立的對象。 設定從CSV或Federated對象構成對象讀取的歷程時，您可以指定該對象中的任何非身分屬性作為補充ID。 接著Journey Optimizer會為每個唯一設定檔+補充ID組合建立個別的歷程執行個體。

* 使用案例1：每個唯一設定檔一列+補充ID組

  這是CSV和同盟對象構成對象的主要使用案例。 對象包含多列，每一列代表設定檔（例如客戶）和補充ID （例如帳戶或訂單ID）的唯一組合。 每一列都會被視為獨立的啟用記錄。

  | profile_id | account_id *（補充識別碼）* | other_attributes |
  | --- | --- | --- |
  | customer_001 | ACC-1001 | ... |
  | customer_001 | ACC-1002 | ... |
  | customer_002 | ACC-2001 | ... |

  在此範例中，`customer_001`有兩個帳戶。 Journey Optimizer會為每個唯一設定檔+ `account_id`配對建立個別的歷程執行個體。

* 使用案例2：具有補充ID陣列的每個設定檔一列

  此使用案例適用於支援陣列的對象型別。 對象中的單一列包含設定檔，其陣列屬性保留多個補充ID值。 Journey Optimizer會在陣列中為每個值建立一個歷程例項。

  | profile_id | account_ids *（陣列，補充識別碼）* | other_attributes |
  | --- | --- | --- |
  | customer_001 | [ACC-1001、ACC-1002] | ... |
  | customer_002 | [ACC-2001] | ... |

  在此範例中，Journey Optimizer為`customer_001`產生兩個歷程執行個體（每個帳戶ID一個執行個體），並為`customer_002`產生一個執行個體。 此行為與補充ID對統一設定檔服務對象的運作方式一致。

### 如何設定 {#external-configuration}

針對使用案例1的CSV對象（對象有意包含相同設定檔ID的多列），您必須在設定歷程之前啟用「快速啟用」。 請參閱下列必要條件。 對於所有其他情況，請直接設定歷程。

+++ 先決條件：透過API在CSV對象上啟用快速啟用

>[!IMPORTANT]
>
>此先決條件僅適用於CSV對象，該對象有意包含相同設定檔ID的多個列（使用案例1）。 同盟對象構成對象預設會啟用「快速啟動」，不需要此步驟。 Audience Portal UI不支援設定`expressActivation` — 您必須使用外部對象API。

您必須在建立時啟用對象的`expressActivation`。 這會告訴Journey Optimizer要獨立啟用每筆記錄，而不需依設定檔ID重複資料刪除。 建立受眾後，就無法變更此標幟。

建立對象時，請使用下列API呼叫：

端點：

```http
POST https://platform.adobe.io/data/core/ais/external-audience
```

必要的標頭：

```http
Authorization: Bearer {ACCESS_TOKEN}
Content-Type: application/json
x-api-key: {API_KEY}
x-gw-ims-org-id: {IMS_ORG}
x-sandbox-name: {SANDBOX_NAME}
```

要求內文（設定`expressActivation: true`）：

```json
{
  "name": "my_audience_name",
  "fields": [ ... ],
  "sourceSpec": { ... },
  "audienceType": "people",
  "namespace": "CustomerAudienceUpload",
  "expressActivation": true
}
```

>[!NOTE]
>
>`expressActivation`預設為`false`。 它必須在建立對象時設定，並且無法在建立後變更。 所有同盟對象構成對象預設都會啟用「快速啟動」，不需要此標幟。

如需完整參考資訊，請參閱[建立外部對象API檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/segmentation/tutorials/create-external-audience#create){target="_blank"}。

+++

設定歷程：

1. 開啟或建立具有&#x200B;**[!UICONTROL 讀取對象]**&#x200B;節點的歷程。
1. 在&#x200B;**[!UICONTROL 讀取對象]**&#x200B;節點設定中，選取您的CSV或同盟對象構成對象。
1. 開啟&#x200B;**[!UICONTROL 使用增補識別碼]**&#x200B;選項，然後在&#x200B;**[!UICONTROL 增補識別碼]**&#x200B;欄位中，在&#x200B;**[!UICONTROL 進階模式]**&#x200B;中使用運算式編輯器，以選擇要用作次要識別碼的屬性（例如，`account_id`、`order_number`）。
1. 選取的屬性會視為歷程的補充ID — 不需要身分註冊。

### 重複資料刪除行為 {#external-dedup}

當對象啟用「快速啟用」（同盟對象構成一律為True — 必須為CSV明確設定）時，Journey Optimizer會根據歷程的設定方式處理重複資料刪除：

| 藍本 | 範例對象列 | 行為 |
| --- | --- | --- |
| **具有補充ID的歷程 — 沒有重複的（設定檔ID、補充ID）配對** | (P1、S1)、(P1、S2) | 預期使用案例。 Journey Optimizer會為每個唯一設定檔+補充ID組合建立個別的歷程執行個體。 允許所有列。 |
| **具有補充ID的歷程 — 存在重複的（設定檔識別碼、補充ID）配對** | (P1、S1)、(P1、S1)、(P1、S2) | 共用相同（設定檔ID、補充ID）組合的列會依一般歷程重新進入邏輯篩選掉。 僅允許每個唯一組合的第一個相符列。 |
| **未設定補充ID的歷程** | (P1、S1)、(P1、S2) | 若沒有補充ID，Journey Optimizer會將相同設定檔ID的所有列視為相同設定檔。 每個設定檔ID只允許一個歷程執行個體；會捨棄相同設定檔的其他列。 |

## 範例使用案例

這些範例顯示補充識別碼如何支援多個相關記錄。

### **原則更新通知**

* **案例**：保險公司針對客戶持有的每個有效保單傳送續約提醒。
* **執行**：
   * 設定檔： &quot;John&quot;。
   * 補充ID： `"AutoPolicy123", "HomePolicy456"`。
   * 歷程會針對每個原則個別執行，並提供個人化的續約日期、涵蓋範圍詳細資料和進階資訊。

### **訂閱管理**

* **案例**：當訂閱觸發事件時，訂閱服務會針對每個訂閱傳送量身打造的訊息。
* **執行**：
   * 設定檔： 「Jane」。
   * 補充ID： `"Luma Yoga Program ", "Luma Fitness Program"`。
   * 每個事件都包含訂閱ID和該訂閱的詳細資訊。 歷程會針對每個事件/訂閱個別執行，允許每個訂閱提供個人化的續約優惠。

### **產品推薦**

* **案例**：電子商務平台會根據客戶購買的特定產品傳送建議。
* **執行**：
   * 設定檔： 「Alex」。
   * 補充ID： `"productID1234", "productID5678"`。
   * 歷程會針對每個產品個別執行，並提供個人化的追加銷售機會。

## 作法影片 {#video}

瞭解如何在[!DNL Adobe Journey Optimizer]中啟用並套用補充識別碼。

>[!VIDEO](https://video.tv.adobe.com/v/3464803?captions=chi_hant&quality=12)
