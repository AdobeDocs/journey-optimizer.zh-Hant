---
solution: Journey Optimizer
product: journey optimizer
title: 使用自訂動作
description: 瞭解如何使用自訂動作
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 動作，自訂， API，歷程，設定，服務
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Sw-hR0cfAG8Lk8YbhJKj53UqG-er2bC3-7Ijih0PF44
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1024
ht-degree: 8%

---

# 使用自訂動作 {#use-custom-actions}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何使用自訂動作，透過REST API呼叫搭配JSON裝載將歷程連線至協力廠商系統，同時套用資料控管和同意原則。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="自訂動作"
>abstract="自訂動作可讓您設定第三方系統的連線，以傳送訊息或 API 呼叫。 您可以使用任何提供者提供的任何服務來設定動作，這些服務可經由 REST API，搭配 JSON 格式的承載進行呼叫。"

使用自訂動作來啟用與協力廠商系統的連線，以傳送訊息或API呼叫。 您可以使用任何提供者提供的任何服務來設定動作，這些服務可經由 REST API，搭配 JSON 格式的承載進行呼叫。

在[本節](../action/action.md)中進一步瞭解自訂動作。

瞭解如何在[此頁面](../action/about-custom-action-configuration.md)上建立和設定自訂動作。

瞭解如何在[此頁面](../action/action-response.md)上使用自訂動作的API呼叫回應進行個人化。

## 同意與資料控管 {#privacy}

在Journey Optimizer中，您可以將資料控管和同意原則套用至自訂動作，以防止特定欄位匯出至協力廠商系統，或排除尚未同意接收電子郵件、推播或簡訊通訊的客戶。 如需詳細資訊，請參閱下列頁面：

* [資料控管](../action/action-privacy.md)。
* [同意](../action/consent.md)。

## URL 組態

**自訂動作**&#x200B;活動的設定窗格會顯示URL設定引數，以及為自訂動作設定的驗證引數。 您無法在歷程中設定URL的靜態部分，但在自訂動作的全域設定中設定。 [了解更多](../action/about-custom-action-configuration.md)。

### 動態路徑

如果URL包含動態路徑，請在&#x200B;**[!UICONTROL 路徑]**&#x200B;欄位中指定路徑。

若要串連欄位和純文字字串，請使用字串函式或進階運算式編輯器中的加號(+)。 以單引號(&#39;)或雙引號(&#39;&#39;)括住純文字字串。 [了解更多](expression/expressionadvanced.md)。

此表格顯示組態範例：

| 欄位 | 價值 |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| 路徑 | `The _id + '/messages'` |

串連的URL具有以下形式：

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![具有動態引數對應的自訂動作URL組態](assets/journey-custom-action-url.png)

### 標頭和查詢引數 {#headers}

**[!UICONTROL URL組態]**&#x200B;區段會顯示動態標頭和查詢引數欄位，但不會顯示常數欄位。 動態標題和查詢引數欄位在動作設定畫面中定義為變數。 [了解更多](../action/about-custom-action-configuration.md#url-configuration)

若要指定動態標題和查詢引數欄位的值，請在欄位內或鉛筆圖示上按一下，然後選取所需欄位。

自訂動作中的![動態標頭欄位設定](assets/journey-dynamicheaderfield.png)

## 動作引數

在&#x200B;**[!UICONTROL 動作引數]**&#x200B;區段中，您會看到定義為&#x200B;_「變數」_&#x200B;的訊息引數。 對於這些引數，您可以定義從何處取得此資訊（例如：事件、資料來源）、手動傳遞值或使用進階運算式編輯器進行進階使用案例。 進階使用案例可以是資料操控和其他函式用途。 請參見此[頁面](expression/expressionadvanced.md)。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明如何在歷程中新增及設定自訂動作活動，以呼叫具有JSON裝載的第三方REST API，包括URL設定、標題/查詢引數對應、動作引數對應以及套用資料控管和同意原則。

**意圖：**

* 新增自訂動作活動至歷程，以透過REST API傳送資料至協力廠商系統
* 在運算式編輯器中串連欄位和靜態文字，設定動態URL路徑
* 從歷程事件或資料來源對應動態標題和查詢引數值
* 將動作引數（定義為變數）對應至事件欄位、資料來源欄位或靜態值
* 套用資料治理和同意原則，以控制透過自訂動作匯出的資料

**字彙表：**

* **自訂動作**：歷程動作活動，會呼叫具有JSON格式之裝載的外部REST API端點，以整合協力廠商系統&#x200B;*（產品專用）*
* **動態路徑**：自訂動作URL的變數部分，是使用歷程內容&#x200B;*（產品特定）*&#x200B;中的欄位針對每次執行所定義
* **動作引數**：在自訂動作設定中定義為「變數」的訊息裝載欄位，對應到歷程層級&#x200B;*（產品特定）*&#x200B;的歷程資料

**護欄：**

* URL的靜態部分無法在歷程中修改；它必須在全域自訂動作設定中設定。
* 動態標題和查詢引數欄位在動作設定畫面中定義為變數，而不是在歷程中。
* 可套用資料治理和同意原則，以防止匯出特定欄位或排除未同意的客戶。

**術語：**

* 正式名稱：自訂動作 — 縮寫：無 — 變體：自訂動作、協力廠商動作
* 同義字：&quot;action parameters&quot; = &quot;message parameters defined as Variable&quot;
* 請勿混淆：「靜態URL部分」（于全域動作設定中設定，在歷程中不可編輯）≠「動態路徑」（於每次執行的歷程中設定）

**常見問題集：**

* **問：我可以在歷程中變更自訂動作的基底URL嗎？**  — 否，歷程中只能設定動態路徑部分；URL的靜態部分是在全域自訂動作設定中設定。
* **問：如何建立包含設定檔ID的動態URL路徑？**  — 使用具有進階運算式編輯器的Path欄位來串連ID欄位與靜態字串，例如： `_id + '/messages'`。
* **問：如何將同意規則套用至自訂動作？**  — 在自訂動作上設定同意原則，以排除尚未同意接收相關通訊的客戶；如需詳細資訊，請參閱「同意」頁面。
* **問：我應該將動態標頭的值對應到哪裡？**  — 在活動窗格的「URL組態」區段中，按一下動態標頭欄位內部，或使用鉛筆圖示從事件或資料來源選取所需欄位。
* **問：我可以指派哪些型別的值給動作引數？**  — 您可以將引數對應到事件欄位、資料來源欄位、手動傳遞值，或使用進階運算式編輯器進行資料操作。

+++
