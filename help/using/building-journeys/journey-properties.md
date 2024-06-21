---
solution: Journey Optimizer
product: journey optimizer
title: 定義歷程的屬性
description: 瞭解如何使用Adobe Journey Optimizer設定您歷程的屬性
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: 歷程，設定，屬性
exl-id: 6c21371c-6cbc-4d39-8fe6-39f1b8b13280
source-git-commit: 87fa5875dfdbae091b36129812948362324f2516
workflow-type: tm+mt
source-wordcount: '1722'
ht-degree: 8%

---

# 設定您的歷程屬性 {#jo-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="歷程屬性"
>abstract="本區段會顯示歷程屬性。預設情況下，會隱藏唯讀參數。可用設定會依據歷程的狀態、您的權限和產品設定而定。"

>[!CONTEXTUALHELP]
>id="ajo_journey_exit_criterias"
>title="歷程結束條件"
>abstract="本區段顯示結束條件選項。您可以為您的歷程建立一個或多個結束條件規則。"

歷程屬性會集中在歷程的右側邊欄中。 建立新歷程時，預設會顯示此區段。 對於現有歷程，按一下歷程名稱旁的鉛筆圖示以存取其屬性。


使用此區段來設定歷程的名稱、新增說明，以及：

* 管理 [進入與重新進入](#entrance)，
* 選擇開始和結束 [日期](#dates)，
* 管理 [存取資料](#manage-access)，
* 定義 [逾時期間](#timeout) 在歷程活動中（僅供管理員使用者使用），
* 選取歷程和設定檔 [時區](#timezone)
* 將Adobe Experience Platform統一標籤指派給您的歷程，以輕鬆分類並改善行銷活動清單中的搜尋。 [了解如何使用標籤](../start/search-filter-categorize.md#tags)

![](assets/journey32.png)

>[!NOTE]
>
>若為即時歷程，此畫面只會顯示發佈日期和發佈歷程的使用者名稱。

此 **複製技術細節** 可讓您複製支援團隊可用於疑難排解的歷程相關技術資訊。 下列資訊已複製： `JourneyVersion UID`， `OrgID`， `orgName`， `sandboxName`， `lastDeployedBy`， `lastDeployedAt`.


## 進入和重新進入 {#entrance}

### 允許重新進入  {#allow-re-entrance}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_entrance"
>title="允許重新進入"
>abstract="依預設，新歷程允許重新進入。 您可以取消勾選 **允許重新進入** 選項，例如，如果要在人員進入商店時提供一次性贈品。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="設定檔入口管理"

依預設，新歷程允許重新進入。 您可以取消勾選 **允許重新進入** 「單次」歷程的選項，例如，如果您想在某人進入商店時提供一次性禮物。

### 重新進入等待期  {#re-entrance-wait}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_re-entrance_wait"
>title="重新進入等待期"
>abstract=" 設定允許設定檔在單一歷程中再次進入歷程之前的等待時間。 這可防止使用者在選定的期間內重新進入歷程。 持續時間上限：29天。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/manage-journey/entry-management" text="設定檔入口管理"

當 **允許重新進入** 選項已啟用， **重新進入等待期** 欄位。 此欄位可讓您定義在允許設定檔在單一歷程中再次進入歷程 (從事件或對象資格開始) 之前等待的時間。 這可防止同一事件多次錯誤觸發歷程。預設情況下，欄位會設為 5 分鐘。 持續時間上限為29天。

在中進一步瞭解設定檔進入和重入管理 [本節](entry-management.md).

## 管理存取權 {#manage-access}

若要指派自訂或核心資料使用標籤給歷程，請按一下 **[!UICONTROL 管理存取權]** 按鈕。 [深入瞭解物件層級存取控制(OLAC)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

## 歷程和設定檔時區 {#timezone}

時區是在歷程層級定義。 您可以輸入固定時區，或使用Adobe Experience Platform設定檔來定義歷程時區。 如果在Adobe Experience Platform設定檔中定義了時區，則可在歷程中擷取該時區。

如需時區管理的詳細資訊，請參閱 [此頁面](../building-journeys/timezone-management.md).

## 開始和結束日期 {#dates}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_start_date"
>title="開始日期"
>abstract="選擇專案可以開始進入歷程的日期。 如果未指定開始日期，則會在發佈時自動設定。"


>[!CONTEXTUALHELP]
>id="ajo_journey_properties_end_date"
>title="結束日期"
>abstract="選擇歷程的結束日期。 達到該日期時，該歷程中的設定檔會自動退出，且新的設定檔無法再進入。"

您可以定義 **開始日期**. 如果您尚未指定，則會在發佈時自動定義。

您也可以新增 **結束日期**. 這可讓設定檔在達到日期時自動退出。 如果未指定結束日期，則設定檔可保留至 [全域歷程逾時](#global_timeout) （通常為91天，若使用Healthcare Shield附加產品，縮短為7天）。 唯一的例外是循環讀取受眾歷程，具有 **在重複時強制重新進入** 已啟用，在下一次事件的開始日期結束。

## 逾時 {#timeout}

### 歷程活動逾時或錯誤 {#timeout_and_error}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_timeout"
>title="逾時"
>abstract="定義歷程嘗試執行動作或驗證條件的時間長度，之後視為逾時。"


編輯動作或條件活動時，您可以定義替代路徑，以防錯誤或逾時。 如果處理詢問協力廠商系統的活動超過中定義的逾時期間。 **[!UICONTROL 逾時或錯誤]** 歷程屬性的欄位中，將選擇第二個路徑來執行潛在的遞補動作。

授權值介於1到30秒之間。

建議您最好定義一個非常簡短的 **[!UICONTROL 逾時或錯誤]** 值（如果您的歷程有時效性，例如：對個人的即時位置有所反應），因為您的動作無法延遲超過幾秒鐘。 如果您的歷程較不有時效性，您可以使用較長的值，讓系統有更多時間呼叫，以傳送有效回應。

歷程也會使用全域逾時，如下所述。

### 全域歷程逾時 {#global_timeout}

除了 [逾時](#timeout_and_error) 在歷程活動中使用，會套用全域歷程逾時。 它不會顯示在介面中，且無法變更。

此全域逾時會停止歷程中個人的進度 **91天** 在他們進入之後。 此逾時已減少為 **7天** 搭配Healthcare Shield附加產品。 這表示個人的歷程不能持續超過91天（或7天）。 在此逾時期間後，個人的資料會被刪除。 在逾時期間結束時仍在歷程中流動的個人將會停止，且將不會在報表中將其列入考量。 因此，您可能會看到更多人進入歷程而不是退出。

>[!NOTE]
>
>歷程不會直接回應隱私權選擇退出、存取或刪除請求。 不過，全域逾時可確保個人在任何歷程中的逗留時間不會超過91天。

由於91天歷程逾時，當歷程不允許重新進入時，我們無法確保重新進入封鎖將超過91天。 事實上，當我們移除在進入歷程91天後進入歷程之人員的所有相關資訊時，我們無法得知此人之前已進入（超過91天前）。

個人只有在歷程剩餘的時間夠在91天歷程逾時前的等待期間完成時，才能進入等待活動。 請參閱[此頁面](../building-journeys/wait-activity.md)。


#### 存留時間(TTL)與資料保留常見問題集 {#timeout-faq}

自2024年6月Adobe Journey Optimizer發行版本開始，歷程全域逾時已從30天移動至91天。 影響會列於以下的常見問題集中：

**針對單一歷程**
<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>TTL擴充功能推出後發佈的歷程會如何？</p>
    </td>
    <td>
      <p>進入新歷程的設定檔會自動具有91天的TTL。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>進入TTL擴充功能啟動前所發佈之歷程的個人資料會發生什麼事？</p>
    </td>
    <td>
      <p>個人資料的TTL為91天（HIPAA為7天），與歷程的初始發佈時間一致。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>啟動TTL擴充功能時，已進入歷程的個人資料會發生什麼事？</p>
    </td>
    <td>
      <p>根據歷程的原始發佈時間，設定檔將保留91天的TTL （HIPAA為7天）。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能啟動後重新發佈的舊版歷程中的設定檔會有什麼改變？</p>
    </td>
    <td>
      <p>設定檔將保留91天（HIPAA為7天）的TTL，與原始歷程版本的發佈時間一致。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能啟動後，新設定檔進入重新發佈的歷程版本會發生什麼事？</p>
    </td>
    <td>
      <p>設定檔的TTL為91天，符合新重新發佈的歷程版本的TTL。</p>
    </td>
  </tr>
</table>

**針對區段觸發歷程**

<table style="table-layout:auto">
  <tr style="border: 1;">
    <td>
      <p>TTL擴充功能之後發佈的新一次性歷程有什麼改變？</p>
    </td>
    <td>
      <p>進入新歷程的設定檔會自動擁有91天的TTL。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能之後發佈的新週期性歷程沒有強制重新進入會怎樣？</p>
    </td>
    <td>
      <p>進入新歷程的設定檔會自動擁有91天的TTL。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能之後發佈的新循環歷程會如何處理，因為會強制重新進入？</p>
    </td>
    <td>
      <p>進入新歷程的設定檔的TTL將等於週期期間。 例如，如果歷程每日執行，則TTL將為1天。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>進入TTL擴充功能啟動前所發佈之歷程的個人資料會發生什麼事？</p>
    </td>
    <td>
      <p>設定檔的TTL為91天（HIPAA為7天），與原始發佈時間一致。 對於具有強制重新進入的週期性歷程，TTL將符合週期性期間。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>啟動TTL擴充功能時，透過歷程執行的設定檔會發生什麼事？</p>
    </td>
    <td>
      <p>根據歷程的原始發佈時間，設定檔將保留91天的TTL （HIPAA為7天）。 對於具有強制重新進入的週期性歷程，TTL將符合週期性期間。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能啟動後重新發佈的先前歷程版本中，執行中的設定檔有何改變？</p>
    </td>
    <td>
      <p>設定檔將保留91天（HIPPA為7天）的TTL，與原始歷程版本的發佈時間一致。 對於具有強制重新進入的週期性歷程，TTL將符合週期性期間。</p>
    </td>
  </tr>
  <tr style="border: 1;">
    <td>
      <p>在TTL擴充功能啟動後，新設定檔進入重新發佈的歷程版本會發生什麼事？</p>
    </td>
    <td>
      <p>設定檔的TTL為91天，符合新重新發佈的歷程版本的TTL。 對於具有強制重新進入的週期性歷程，TTL將符合週期性期間。</p>
    </td>
  </tr>
</table>

## 合併政策 {#merge-policies}

Journey在從Adobe Experience Platform擷取設定檔資料時使用合併原則。 根據歷程型別，會使用不同的合併原則：

* 在讀取對象或對象資格歷程中：使用來自對象的合併原則
* 在單一事件歷程中：使用預設合併原則
* 在業務事件歷程中：使用以下讀取對象活動中來自目標對象的合併原則

歷程將遵循在整個歷程中使用的合併原則。 因此，如果歷程中使用多個對象（例如：「inAudience」函式中），導致歷程使用的合併原則不一致，則會引發錯誤並封鎖發佈。 不過，如果在訊息個人化中使用不一致的對象，則儘管不一致，仍不會引發警報。 因此，強烈建議您在訊息個人化使用此對象時，檢查與對象相關聯的合併原則。

若要深入瞭解合併原則，請參閱 [Adobe Experience Platform檔案](https://experienceleague.adobe.com/en/docs/experience-platform/profile/merge-policies/overview){target="_blank"}.
