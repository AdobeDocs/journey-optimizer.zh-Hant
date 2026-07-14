---
solution: Journey Optimizer
product: journey optimizer
title: 路徑目標定位
description: 瞭解如何在歷程中使用路徑鎖定目標
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 鎖定目標，規則，歷程，路徑，最佳化，個人化
exl-id: b30ce5c9-a0e2-4601-97a3-5bec648368e4
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1327
ht-degree: 4%

---

# 利用路徑目標鎖定 {#targeting}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在「最佳化」活動中使用目標定位規則，以使用選用的遞補路徑，決定性地將特定對象路由到正確的歷程路徑。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="什麼是後備路徑？"
>abstract="透過後備路徑，在沒有任何目標選擇規則符合要求時，會讓您的客群進入替代路徑。 </br>如果未選取此選項，則任何不符合定向規則的客群都不會進入後備路徑，並會退出歷程。"

目標規則可讓您根據特定受眾區段<!-- depending on profile attributes or contextual attributes-->，決定客戶必須符合哪些特定規則或資格，才能符合進入其中一個歷程路徑的資格。

實驗是指定路徑的隨機指派，而目標定位則是確定性的，可確保正確的對象或設定檔進入指定的路徑。

<!--
With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.
-->

若要在歷程中設定鎖定目標，請遵循下列步驟。

1. 從&#x200B;**[!UICONTROL 協調流程]**&#x200B;區段，將&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動拖放至歷程畫布。

1. 新增選用標籤，這對於在報告和測試模式記錄中識別活動很有用。

1. 從&#x200B;**[!UICONTROL 方法]**&#x200B;下拉式清單中選取&#x200B;**[!UICONTROL 目標規則]**。

   在最佳化活動中選取![目標規則](assets/journey-optimize-targeting.png){width=60%}

1. 按一下&#x200B;**[!UICONTROL 建立目標規則]**。

1. 按一下「**[!UICONTROL 建立規則]**」>「**[!UICONTROL 新建]**」，然後使用規則產生器來定義您的條件。

   ![用於建立目標定位條件的規則產生器介面](assets/journey-targeting-create-rule.png){width=100%}

   例如，定義忠誠度計畫的金會員規則(`loyalty.status.equals("Gold", false)`)，以及其他會員規則(`loyalty.status.notEqualTo("Gold", false)`)。

   金級與非金級會員的![忠誠度狀態目標規則](assets/journey-targeting-rule.png)

1. 您也可以按一下「建立規則&#x200B;]**>**[!UICONTROL &#x200B;選取規則&#x200B;]**」，選取從**[!UICONTROL &#x200B;規則&#x200B;]**功能表建立的現有目標規則。**[!UICONTROL [了解更多](../experience-decisioning/rules.md)

   ![從[規則]功能表選取現有的鎖定目標規則](assets/journey-targeting-select-rule.png){width=70%}

   在此情況下，組成規則的公式只會複製到歷程活動中。 從&#x200B;**[!UICONTROL 規則]**&#x200B;選單對該規則所做的任何後續變更將不會影響歷程的副本。

   >[!AVAILABILITY]
   >
   >[使用專用的[!DNL Journey Optimizer]功能表建立鎖定目標規則](../experience-decisioning/rules.md#create)，目前可供已購買決策附加元件產品的組織使用，其他組織也可依需求使用（可用性限制）。
   >
   >此容量將逐步向所有客戶推出。 與此同時，請聯絡您的Adobe代表以取得存取權。

1. 新增規則後，您仍可加以修改。 選擇&#x200B;**[!UICONTROL 編輯內嵌]**，以使用規則產生器即時更新它，或選擇&#x200B;**[!UICONTROL 選取規則]**&#x200B;以挑選另一個現有的規則。

   ![編輯內嵌或選取用於修改定位規則的規則選項](assets/journey-targeting-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >編輯規則內嵌不會影響其源自的現有規則。

1. 視需要選取&#x200B;**[!UICONTROL 啟用遞補路徑]**&#x200B;選項。 此動作會針對不符合上述任何鎖定目標規則的對象建立遞補路徑。

   >[!NOTE]
   >
   >如果您未選取此選項，則任何不符合鎖定目標規則的對象都不會進入後援路徑並退出歷程。

1. 按一下&#x200B;**[!UICONTROL 建立]**&#x200B;以儲存您的目標規則設定。

1. 回到歷程中，拖放特定動作以自訂每個路徑。 例如，建立包含金級忠誠度會員個人化優惠方案的電子郵件，以及所有其他會員的簡訊提醒。

   ![含金級會員電子郵件和其他人簡訊的歷程路徑](assets/journey-targeting-paths.png)

1. 如果您在定義規則設定時選取了&#x200B;**[!UICONTROL 啟用遞補內容]**&#x200B;選項，請為自動新增的遞補路徑定義一或多個動作。

   不合格設定檔的![遞補路徑設定](assets/journey-targeting-fallback.png){width=70%}

1. 或者，在逾時或錯誤的情況下使用&#x200B;**[!UICONTROL 新增替代路徑]**&#x200B;以定義發生問題時的替代動作。 [了解更多](using-the-journey-designer.md#paths)

1. 針對目標規則設定所定義的每個群組，為每個動作設計適當的內容。

   在此範例中，設計包含金會員特殊優惠方案的電子郵件，以及其他會員的SMS提醒。<!--You can seamlessly navigate between the different contents for each action. ![Content design panel for targeting rule actions](assets/journey-targeting-design.png)-->

1. [發佈](publish-journey.md)您的歷程。

一旦歷程上線，系統就會處理為每個區段指定的路徑，以便Gold成員輸入有電子郵件選件的路徑，而其他成員輸入有簡訊提醒的路徑。

使用歷程報告追蹤您的歷程成功。 [了解更多](../reports/journey-global-report-cja.md#targeting)

## 鎖定目標規則使用案例 {#uc-targeting}

下列範例顯示如何搭配使用&#x200B;**[!UICONTROL 最佳化]**&#x200B;活動與&#x200B;**[!UICONTROL 鎖定目標規則]**&#x200B;方法來個人化不同子對象的路徑。

+++區段專用管道

金級狀態忠誠會員可以透過電子郵件接收個人化優惠，而所有其他會員則會導向簡訊提醒。

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![以電子郵件和其他簡訊的Gold會員為目標的區段特定管道](assets/journey-optimize-targeting-uc-segment.png)

+++

+++行為型目標定位

已開啟電子郵件但未點按的客戶會收到推播通知，而完全未開啟的客戶則會收到簡訊。

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![使用推播或簡訊遞補進行電子郵件參與的行為型目標定位](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++購買記錄目標定位

最近購買過的客戶可以進入簡短的「感謝您+交叉銷售」路徑，而沒有購買記錄的客戶則會進入更長的培育歷程。

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![購買者交叉銷售路徑與非購買者培養路徑的購買歷程記錄](assets/journey-optimize-targeting-uc-purchase.png)

+++

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

- **TL；DR：**&#x200B;本頁說明如何在Adobe Journey Optimizer歷程中使用路徑鎖定目標，以根據定義的規則決定性地將特定受眾區段路由到指定的歷程路徑。

**意圖：**
- 使用最佳化活動搭配鎖定目標規則方法來設定確定性路徑鎖定目標
- 從「規則」選單中建立新目標規則或重複使用現有規則
- 為不符合任何定位規則的設定檔定義遞補路徑
- 針對不同的受眾區段（例如忠誠度等級、行為、購買記錄）個人化歷程路徑
- 修改內嵌鎖定目標規則，而不影響原始規則定義

**字彙表：**
- **最佳化活動**：歷程畫布活動，用來透過實驗（隨機）或目標（確定性） *（產品特定）*&#x200B;將設定檔分割為不同的路徑
- **目標規則**：根據設定檔或對象屬性&#x200B;*（產品特定）*，決定設定檔進入哪個歷程路徑的確定性資格條件
- **遞補路徑**：設定檔的替代歷程路徑未滿足任何已定義的鎖定目標規則&#x200B;*（產品特定）*

**護欄：**
- 路徑鎖定目標目前處於「有限可用性」；請聯絡您的Adobe代表以請求存取權。
- 從專用的Journey Optimizer「規則」選單建立鎖定目標規則需要決策附加元件或可依需求使用（可用性限制）。
- 從「規則」選單中選取規則並複製到歷程時，對原始規則的後續變更不會影響歷程的副本。
- 編輯內嵌規則不會修改其來源的原始規則。
- 如果未啟用遞補路徑選項，則不符合任何定位規則的設定檔將完全退出歷程。

**術語：**
- 正式名稱：路徑鎖定目標 — 縮寫：none — 變體：確定性路徑路由、規則型路徑分割
- 同義字： &quot;Targeting rule&quot; = &quot;qualification rule&quot; = &quot;path condition&quot;
- 請勿混淆：「鎖定目標」≠「實驗」（鎖定目標是確定性的；實驗是隨機指派）

**常見問題集：**
- **問：路徑鎖定目標與路徑實驗之間有何差異？**  — 鎖定目標是確定性的：設定檔會根據定義的規則輸入路徑。 實驗是隨機的：設定檔會偶然指派給路徑，以比較效能。
- **問：不符合任何定位規則的設定檔會發生什麼事？**  — 如果已啟用遞補路徑選項，他們會輸入遞補路徑。 如果未啟用，他們會完全退出歷程。
- **問：我可以重複使用[規則]功能表中的現有規則嗎？**  — 是，但規則公式會複製到歷程活動中；後續變更「規則」選單中的原始規則時，不會影響歷程的副本。
- **問：編輯目標規則內嵌是否會變更原始規則？**  — 否，編輯內聯只會更新歷程活動中的規則，不會影響來源規則。
- **問：誰可以存取路徑鎖定目標？**  — 目前處於「有限可用性」；請聯絡您的Adobe代表以請求存取權。

+++
