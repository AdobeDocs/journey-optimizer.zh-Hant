---
solution: Journey Optimizer
product: journey optimizer
title: 模擬您的歷程
description: 瞭解如何模擬您的歷程
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: 測試，歷程，檢查，錯誤，疑難排解
version: Journey Orchestration
hide: true
feature_v2: []
subfeature_v2: []
source-git-commit: e9a1f2da50585204a4d793ad11ec3e08c0b9fe48
workflow-type: tm+mt
source-wordcount: 1319
ht-degree: 0%

---

# 模擬您的歷程{#simulate-journey}

使用&#x200B;**[!UICONTROL 模擬]**，在您發佈之前先與&#x200B;**模擬使用者**&#x200B;驗證您的歷程。 此頁面會逐步引導您完成&#x200B;**[!UICONTROL 快速模擬]**&#x200B;和&#x200B;**[!UICONTROL 手動模擬]**、建立和傳送模擬的使用者、在您的歷程需要這些使用者時觸發單一事件，以及檢閱&#x200B;**[!UICONTROL 結果]**&#x200B;記錄。

如需依歷程型別的概觀，請參閱[開始使用歷程模擬](simulate-journey-gs.md)。

## 模擬型別 {#simulation-types}

啟用後，包含讀取對象專案的批次歷程提供兩種執行模擬的方式：

* **[!UICONTROL 快速模擬]**&#x200B;會以產生的使用者和預設值執行端對端作業。 請注意，快速模擬不適用於單一歷程。

* **[!UICONTROL 手動模擬]**&#x200B;可讓您逐步選擇使用者、傳送順序、事件裝載，以及等待覆寫。

![模擬面板中的快速模擬和手動模擬](assets/quick-simulation-1.png)

### 快速模擬 {#quick-simulation}

在&#x200B;**[!UICONTROL 模擬]**&#x200B;中的批次歷程中，**[!UICONTROL 快速模擬]**&#x200B;會使用產生的使用者與預先填入的設定來執行歷程。

1. 選取&#x200B;**[!UICONTROL 快速模擬]**。

1. 檢閱Adobe Journey Optimizer為執行收集的欄位。 按一下「**[!UICONTROL 更新值]**」以變更校訂或頻道設定，或繼續而不變更。

   ![快速模擬檢閱步驟](assets/quick-simulation-2.png)

1. 如果您開啟&#x200B;**[!UICONTROL 更新值]**，請編輯設定，例如用於訊息校訂的地址，然後確認開始模擬。

   ![快速模擬更新值](assets/quick-simulation-3.png)

1. Adobe Journey Optimizer會從歷程定義產生模擬使用者，並觸發每個使用者進入歷程。

1. 執行完成時，按一下&#x200B;**[!UICONTROL 檢視結果]**&#x200B;以檢視路徑、錯誤和未涵蓋的分支。 檢視[檢視結果](#viewing-results)。

   ![快速模擬已完成回合](assets/quick-simulation-4.png)

### 手動模擬 {#manual-simulation}

當您需要挑選每個模擬使用者、控制傳送順序、設定事件裝載，以及覆寫執行中的&#x200B;**[!UICONTROL 等待]**&#x200B;期間時，請選擇&#x200B;**[!UICONTROL 手動模擬]**。 此流程適用於批次和單一歷程。

繼續[建立和管理模擬的使用者](#test-users)、[觸發您的事件](#firing_events)和[檢視結果](#viewing-results)。

## 建立和管理模擬使用者 {#test-users}

>[!IMPORTANT]
>
>您至少需要下列其中一個許可權才能存取&#x200B;**[!UICONTROL 模擬]**&#x200B;功能： **模擬歷程**、**發佈歷程**&#x200B;或&#x200B;**核准並發佈歷程**。 [了解更多](../administration/permissions.md)

模擬使用者是您在&#x200B;**[!UICONTROL 模擬設定]**&#x200B;中定義的臨時設定檔實體。 本節說明如何建立範本、儲存範本以供重複使用、從清單中調整或移除範本，以及將範本傳送至歷程。

1. 從填入&#x200B;**[!UICONTROL 測試使用者]**&#x200B;清單開始：

   +++ 使用AI產生使用者

   Adobe Journey Optimizer會從歷程定義產生一組模擬使用者。

   對於具有電子郵件或簡訊節點的歷程，AI會提示您確認要使用的電子郵件地址或電話號碼。 完成後，按一下&#x200B;**[!UICONTROL 產生]**。

   ![模擬的使用者選擇面板](assets/simulate-generate.png)

   +++

   +++ 瀏覽詳細目錄

   選擇&#x200B;**[!UICONTROL 瀏覽詳細目錄]**&#x200B;以新增您已儲存的模擬使用者，例如您從表單或JSON建立的使用者，或您在AI產生執行後保留的使用者。

   ![模擬的使用者選擇面板](assets/simulate-inventory.png)

   +++

   +++ 從表單建立

   1. 輸入&#x200B;**[!UICONTROL 顯示名稱]**&#x200B;和&#x200B;**[!UICONTROL 描述]**&#x200B;以識別此模擬使用者。

      ![模擬的使用者選擇面板](assets/simulate-form.png)

   1. 然後，從聯合綱要中選取要為此使用者填入的屬性。

   1. 按一下&#x200B;**[!UICONTROL 新增對象成員資格]**&#x200B;以模擬區段成員資格。

   1. 按一下&#x200B;**[!UICONTROL 新增設定檔]**，在單一工作階段中建立多個模擬使用者。

   1. 從功能表，使用&#x200B;**[!UICONTROL 複製]**&#x200B;來複製使用者，**[!UICONTROL 套用至全部]**&#x200B;以將一個使用者的屬性複製到工作階段中的每個其他使用者，或使用&#x200B;**[!UICONTROL 刪除]**&#x200B;來移除使用者。

      ![模擬的使用者選擇面板](assets/simulate-form-2.png)

   1. 當您完成此工作階段中的使用者設定時，請按一下[儲存]。****

   +++

   +++ 從JSON建立

   使用您的模擬使用者資料更新對應欄位，以定義新的模擬使用者。

   ![模擬的使用者選擇面板](assets/simulate-json.png)

   +++

1. 您建立的模擬使用者會顯示在&#x200B;**[!UICONTROL 測試使用者]**&#x200B;清單中。 針對每個專案，選取下列其中一項：

   * ![編輯圖示](assets/do-not-localize/Smock_Edit_18_N.svg)：更新模擬使用者的詳細資料。
   * ![傳送圖示](assets/do-not-localize/Smock_Send_18_N.svg)：僅針對這個模擬的使用者執行模擬。
   * ![清除圖示](assets/do-not-localize/Smock_Close_18_N.svg)：從此清單移除使用者。 系統不會刪除模擬使用者，而會保留在「模擬使用者」選項中。

   ![模擬的使用者選擇面板](assets/simulate-4-2.png)

1. 若要在選取後變更清單，請按一下[管理使用者]，從詳細目錄或建立新使用者新增更多模擬使用者。 ****&#x200B;若要從此回合的&#x200B;**[!UICONTROL 測試使用者]**&#x200B;清單中移除所有使用者，請選擇&#x200B;**[!UICONTROL 清除所有使用者]**。

   ![模擬的使用者選擇面板](assets/simulate-manage.png)

1. 如果您的歷程包含&#x200B;**[!UICONTROL 等待]**&#x200B;活動，請開啟&#x200B;**[!UICONTROL 測試設定]**&#x200B;索引標籤以微調模擬期間等待的時間長度。 例如，如果即時&#x200B;**[!UICONTROL 等待]**&#x200B;活動設定了數天，您可以將其覆寫為10秒，以便模擬使用者在移至下一個活動之前只在節點上花費那段時間。

1. 按一下&#x200B;**[!UICONTROL 全部傳送]**&#x200B;以將清單中的每個模擬使用者傳送至歷程，或按一下資料列上的![傳送圖示](assets/do-not-localize/Smock_Send_18_N.svg)以僅傳送該使用者。 當模擬的使用者成功進入歷程時，會出現`Simulated users have entered the journey successfully.`確認訊息。

   ![模擬的使用者選擇面板](assets/simulate-5-2.png)

1. 如果歷程包含單一事件，您必須選取要觸發的事件。 請參閱[觸發您的事件](#firing_events)。

1. 存取&#x200B;**[!UICONTROL 結果]**&#x200B;標籤以開啟執行記錄檔並檢閱每個步驟的執行方式。 如需詳細資訊，請參閱[檢視結果](#viewing-results)。

在&#x200B;**[!UICONTROL 模擬]**&#x200B;中驗證歷程後，請檢閱&#x200B;**[!UICONTROL 結果]**&#x200B;記錄。 如果發生錯誤，請保留&#x200B;**[!UICONTROL 模擬]**，將必要的變更套用至歷程，然後再次執行&#x200B;**[!UICONTROL 模擬]**，直到執行看起來正確為止。 接著，您就可以發佈歷程。 檢視[發佈您的歷程](../building-journeys/publish-journey.md)。

## 觸發您的事件 {#firing_events}

如果您的歷程包含一或多個單一事件，您會在模擬作用中時觸發這些事件。

1. 在&#x200B;**[!UICONTROL 選取事件型別]**&#x200B;中，選取要為此模擬引發的事件。

   ![事件設定介面，其中包含事件選取範圍的欄位和下拉式清單](assets/simulate-10-2.png)

1. 若要將相同的變更套用至清單中的每個使用者，請使用&#x200B;**[!UICONTROL 管理事件]**&#x200B;選項來：

   * **[!UICONTROL 產生事件值]**&#x200B;以讓Adobe Journey Optimizer使用AI產生裝載。 產生值時，使用者會標籤為&#x200B;**[!UICONTROL 準備傳送]**。
   * **[!UICONTROL 編輯事件日期]**&#x200B;以僅變更該模擬使用者的裝載。

   ![事件設定介面，其中包含事件選取範圍的欄位和下拉式清單](assets/simulate-9-2.png)

1. 按一下使用者旁的![編輯事件](assets/do-not-localize/Smock_Edit_18_N.svg)，設定每個使用者的事件裝載，以：

   * **[!UICONTROL 產生事件值]**&#x200B;以讓Adobe Journey Optimizer使用AI產生裝載。 產生值時，使用者會標籤為&#x200B;**[!UICONTROL 準備傳送]**。
   * **[!UICONTROL 編輯事件日期]**&#x200B;以僅變更該模擬使用者的裝載。

   ![事件設定介面，其中包含事件選取範圍的欄位和下拉式清單](assets/simulate-8-2.png)

1. 在&#x200B;**[!UICONTROL 測試事件]**&#x200B;中，選取&#x200B;**[!UICONTROL 全部傳送]**，將列在&#x200B;**[!UICONTROL 測試使用者]**&#x200B;下的每個模擬使用者傳送至歷程，或選取![傳送圖示](assets/do-not-localize/Smock_Send_18_N.svg)，讓單一使用者只為該使用者執行模擬。

   ![事件設定介面，其中包含事件選取範圍的欄位和下拉式清單](assets/simulate-11-2.png)

1. 觸發事件後，畫布會更新以反映每個使用者的進度。 按一下&#x200B;**[!UICONTROL 測試使用者]**&#x200B;清單中的任一列，以檢視使用者在歷程中採用的新路徑。

1. 存取&#x200B;**[!UICONTROL 結果]**&#x200B;標籤以開啟執行記錄檔並檢閱每個步驟的執行方式。 如需詳細資訊，請參閱[檢視結果](#viewing-results)。

## 檢視結果 {#viewing-results}

**[!UICONTROL 結果]**&#x200B;索引標籤可讓您檢視測試結果。 在&#x200B;**[!UICONTROL 測試使用者]**&#x200B;下拉式清單中，選取您要檢查其執行的模擬使用者。

選取「全部&#x200B;**[!UICONTROL 個]**」，檢視執行中每個模擬使用者彙總的結果。 此檢視可協助您掃描完整模擬的一覽、活動、結果和錯誤，而不需先挑選單一模擬使用者。

測試使用者的![記錄](assets/simulate-6-2.png)

對於每個活動，記錄可以顯示模擬的使用者是否進入或退出步驟，以及在模擬期間發生的錯誤。

對於&#x200B;**等待**&#x200B;活動，記錄檔包含兩個持續時間相關的值：

* **定義的持續時間**：在已發佈歷程的&#x200B;**等待**&#x200B;活動上指定的持續時間，並在歷程上線後套用。 記錄會記錄模擬是否從測試設定套用覆寫（例如10秒），而非僅依賴歷程上定義的值。
* **實際持續時間**：模擬使用者留在&#x200B;**等待**&#x200B;活動上的經過時間。 此值是從&#x200B;**[!UICONTROL 測試設定]**&#x200B;索引標籤設定的。

當記錄中出現錯誤時，保留&#x200B;**模擬**，將必要的變更套用至歷程，然後再次執行&#x200B;**模擬**。 驗證成功後，發佈歷程。 檢視[發佈您的歷程](../building-journeys/publish-journey.md)。
