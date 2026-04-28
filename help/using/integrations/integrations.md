---
solution: Journey Optimizer
product: journey optimizer
title: 啟用外部整合
description: 將外部整合整合整合至管道製作程式，以個人化和動態資訊豐富內容
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: 整合
hide: true
exl-id: 104f283e-f6a5-431b-919a-d97b83d19632
source-git-commit: f40e030e7d14120cdbc118a8f93e2f752d713f6b
workflow-type: tm+mt
source-wordcount: '1227'
ht-degree: 7%

---

# 使用整合 {#external-sources}

>[!BEGINSHADEBOX]

目錄：

* **[使用整合](integrations.md)**
* [開始使用](vendor-integration-gs.md)
* [可用的廠商](vendor-integration.md)
* [常見問題集](vendor-integration-faq.md)

>[!ENDSHADEBOX]

## 概觀

**整合**&#x200B;功能將Adobe Journey Optimizer連結至您已在其他地方管理其資料和可撰寫內容的協力廠商系統。 您可以在編寫期間和傳送時間顯示這些資料，這可跨您在Journey Optimizer中使用的各個管道支援回應速度更快、個人化的體驗。

您可以使用此功能來存取外部資料，以及從第三方工具提取內容，例如：

* **獎勵積分**&#x200B;來自忠誠度系統。
* 產品的&#x200B;**價格資訊**。
* 來自建議引擎的&#x200B;**產品建議**。
* **物流更新**&#x200B;為傳遞狀態。

若要開始使用整合，使用者必須獲授&#x200B;**[!UICONTROL 管理AJO整合設定]**&#x200B;和&#x200B;**[!UICONTROL 檢視AJO整合]**&#x200B;許可權。 [進一步瞭解許可權](../administration/permissions.md)

+++ 瞭解如何指派整合的相關許可權

1. 在&#x200B;**[!UICONTROL 權限]**&#x200B;產品中，前往&#x200B;**[!UICONTROL 角色]**&#x200B;標籤，然後選取所需的&#x200B;**[!UICONTROL 角色]**。

1. 按一下&#x200B;**[!UICONTROL 編輯]**&#x200B;以修改權限。

1. 新增&#x200B;**[!UICONTROL AJO整合設定]**&#x200B;資源，然後從下拉式功能表中選取適當的整合許可權。

   ![](assets/external-integration-config-9.png)

1. 按一下&#x200B;**[!UICONTROL 儲存]**，以套用所做的變更。

   任何已指派給此角色的使用者都會自動更新其權限。

1. 若要將此角色指派給新使用者，請瀏覽至&#x200B;**[!UICONTROL 角色]**&#x200B;儀表板中的&#x200B;**[!UICONTROL 使用者]**&#x200B;標籤，然後按一下&#x200B;**[!UICONTROL 新增使用者]**。

1. 輸入使用者的名稱、電子郵件地址，或從清單當中選擇，然後按一下&#x200B;**[!UICONTROL 儲存]**。

如果使用者先前未建立，請參閱[此檔案](https://experienceleague.adobe.com/zh-hant/docs/experience-platform/access-control/abac/permissions-ui/users)。

+++

## 設定您的整合 {#configure}

>[!AVAILABILITY]
>
> 此整合功能僅限傳出頻道（電子郵件、簡訊和推播）並提供JSON或HTML格式的資料。 請注意，API是唯讀的，僅支援擷取操作。

身為管理員，您可以依照下列步驟設定外部整合：

1. 導覽至左側功能表中的&#x200B;**[!UICONTROL 組態]**&#x200B;區段，然後從&#x200B;**[!UICONTROL 整合]**&#x200B;卡片按一下&#x200B;**[!UICONTROL 管理]**。

   然後，按一下[建立整合] ****&#x200B;以開始新的組態。

   ![](assets/external-integration-config-1.png)

1. 選擇性地貼上&#x200B;**cURL**&#x200B;命令以自動填入URL、HTTP方法、標頭和查詢引數。

1. 提供整合的&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

   >[!NOTE]
   >
   >這些欄位不可包含空格。

1. 輸入API端點&#x200B;**[!UICONTROL URL]**，其中可能包含路徑引數，以及可使用標籤和預設值定義的變數。

1. 使用&#x200B;**[!UICONTROL 名稱]**&#x200B;和&#x200B;**[!UICONTROL 預設值]**&#x200B;設定&#x200B;**[!UICONTROL 路徑範本]**。

   ![](assets/external-integration-config-2.png)

1. 選取GET與POST之間的&#x200B;**[!UICONTROL HTTP方法]**。

1. 視整合需要，按一下&#x200B;**[!UICONTROL 新增標題]**&#x200B;和/或&#x200B;**[!UICONTROL 新增查詢引數]**。 針對每個引數，提供下列詳細資訊：

   * **[!UICONTROL 引數]**：：內部用來參考引數的唯一識別碼。

   * **[!UICONTROL 名稱]**： API預期的引數實際名稱。

   * **[!UICONTROL 型別]**：選擇固定值的&#x200B;**常數**&#x200B;或動態輸入的&#x200B;**變數**。

   * **[!UICONTROL 值]**：直接輸入常數值，或選取變數對應。

   * **[!UICONTROL 必要]**：指定是否需要此引數。

   ![](assets/external-integration-config-3.png)

1. 選擇&#x200B;**[!UICONTROL 驗證型別]**：

   * **[!UICONTROL 無驗證]**：適用於不需要任何認證的開放API。

   * **[!UICONTROL API金鑰]**：使用靜態API金鑰驗證請求。 輸入您的&#x200B;**[!UICONTROL API金鑰名稱{1&#x200B;}、**[!UICONTROL  API金鑰值{3&#x200B;}並指定您的&#x200B;**[!UICONTROL 位置]**。]**]**

   * **[!UICONTROL 基本驗證]**：使用標準HTTP基本驗證。 輸入&#x200B;**[!UICONTROL 使用者名稱]**&#x200B;和&#x200B;**[!UICONTROL 密碼]**。

   * **[!UICONTROL OAuth 2.0]**：使用OAuth 2.0通訊協定進行驗證。 按一下![編輯](assets/do-not-localize/Smock_Edit_18_N.svg)圖示以設定或更新&#x200B;**[!UICONTROL 裝載]**。

   ![](assets/external-integration-config-4.png)

1. 設定API要求的&#x200B;**[!UICONTROL 原則組態]** （例如&#x200B;**[!UICONTROL 逾時]**&#x200B;期間），並選擇啟用節流、快取和/或重試。

   啟用節流時，支援的速率範圍從&#x200B;**50** TPS （最小）到&#x200B;**5000** TPS （最大）。
啟用重試時，其他失敗依預設會跟隨**三次**&#x200B;次重試，在連續嘗試之間有&#x200B;**200毫秒**、**400毫秒**&#x200B;和&#x200B;**800毫秒**。

1. 透過&#x200B;**[!UICONTROL 回應承載]**&#x200B;欄位，您可以決定樣例輸出的哪些欄位需要用於訊息個人化。

   按一下![編輯](assets/do-not-localize/Smock_Edit_18_N.svg)圖示並貼上範例JSON回應裝載以自動偵測資料型別。

1. 選擇要公開以進行個人化的欄位，並指定其對應的資料型別。

   ![](assets/external-integration-config-5.png)

   >[!NOTE]
   >
   >**[!UICONTROL 回應承載]**&#x200B;設定定義了編寫的預期回應，包括該步驟中套用的任何結構描述。 行銷人員只能參考公開的欄位，其他路徑的Token無法在編輯器中驗證。

1. 使用&#x200B;**[!UICONTROL 傳送測試連線]**&#x200B;來驗證整合。

   驗證後，按一下&#x200B;**[!UICONTROL 啟動]**。

### 傳送時間限制和行為 {#configure-send-time}

在傳送時，來自外部API的回應預設為最多&#x200B;**4 MB**。 任何大於此值的專案都會被視為整合錯誤，當失敗是由回應大小所導致時，將不會嘗試&#x200B;**次重試**。

呼叫會遵循您設定的&#x200B;**節流**&#x200B;速率：即使外部系統關機或傳回錯誤，Journey Optimizer排程也會嘗試達到該限制。 如果已啟用&#x200B;**快取**，則只會儲存並重複使用&#x200B;**個成功的**&#x200B;回應，直到您定義的快取&#x200B;**TTL**&#x200B;過期為止；絕不會快取失敗的回應。

每個佇列的訊息也包含有效視窗(TTL)。 如果處理延遲，且訊息位於該視窗之後，系統&#x200B;**會捨棄該視窗**&#x200B;並發出&#x200B;**`MessageValidityExclusion`**&#x200B;事件，讓過時的工作從佇列中清除，而資源仍可繼續使用。


## 使用外部整合進行個人化 {#personalization}

在使用外部整合進行個人化之前，請注意，整合呼叫的排程和隔離取決於執行上下文：

* **批次執行** （批次行銷活動、協調的行銷活動以及API觸發的行銷活動）：每次批次執行都會在專用的隔離環境中運作。 因此，呼叫外部系統的同時批次執行不會相互競爭或互相阻礙。

* **單一執行** （單一歷程、批次歷程及API觸發的交易式行銷活動）：每個品牌沙箱會隔離整合流量，因此一個品牌的緩慢外部API不會延遲另一個品牌。 在您的沙箱中，同時整合可能會短暫延遲其他整合支援的訊息；每則訊息最多會在到期前12小時嘗試。

身為行銷人員，您可以使用已設定的整合來個人化您的內容。 請依照下列步驟操作：

1. 存取您的行銷活動內容，然後按一下[文字]或[HTML **[!UICONTROL 元件]**]中的[新增個人化&#x200B;]**]。**[!UICONTROL 

   [進一步瞭解元件](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. 瀏覽至&#x200B;**[!UICONTROL 整合]**&#x200B;區段，然後按一下&#x200B;**[!UICONTROL 開啟整合]**&#x200B;以檢視所有使用中的整合。

   請注意，內容片段可與整合搭配使用，但僅支援傳出頻道，傳入發佈將不會成功。 片段發佈後，會停用新增和儲存新的整合，以避免對現有歷程和行銷活動造成影響。

   ![](assets/external-integration-content-2.png)

1. 選取整合併按一下&#x200B;**[!UICONTROL 儲存]**。

   ![](assets/external-integration-content-3.png)

1. 啟用&#x200B;**[!UICONTROL Pills]**&#x200B;模式以解除鎖定進階整合功能表。

   ![](assets/external-integration-content-4.png)

1. 當您編寫整合個人化時，整合協助程式會包含&#x200B;**`required`**&#x200B;欄位，以定義失敗或遺失資料如何與預設內容互動：

   * **`required=true`** （預設）：該訊息的轉譯停止。 此傳送已與&#x200B;**`ExternalDataLookupExclusion`**&#x200B;一起排除，而且此排除記錄在&#x200B;**訊息意見資料集**&#x200B;中。
   * **`required=false`**：結果變數已設為&#x200B;**`null`**，且轉譯作業會繼續進行。 在範本中使用預設文字、後援或條件式邏輯，這樣在整合未傳回資料時，設定檔就不會接收空白內容。

     ![](assets/external-integration-content-8.png)

1. 若要完成整合設定，請定義先前在[組態](#configure)期間指定的整合屬性。

   您可以使用靜態值（保持常數）或設定檔屬性（動態地從使用者設定檔中提取資訊）來指派值給這些屬性。

   ![](assets/external-integration-content-5.png)

1. 定義整合屬性後，您現在可以按一下![新增](assets/do-not-localize/Smock_Add_18_N.svg)圖示，將內容中的整合欄位用於個人化傳訊。

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >範本中的權杖只能使用管理員在整合設定中公開的欄位。 例如，`{{weatherResponse.temperature}}`在`temperature`公開時有效；如果`humidity`未公開，編輯器中會拒絕`{{weatherResponse.humidity}}`。

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

您的整合個人化現在已成功套用至您的內容，確保每位收件者都能根據您設定的屬性獲得量身打造的相關體驗。

![](assets/external-integration-content-7.png)

