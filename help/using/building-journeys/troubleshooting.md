---
solution: Journey Optimizer
product: journey optimizer
title: 在測試或發佈您的歷程之前疑難排解錯誤
description: 瞭解如何在測試或發佈歷程之前進行錯誤疑難排解
feature: Journeys, Monitoring
topic: Content Management
role: User
level: Intermediate
keywords: 疑難排解，疑難排解，歷程，檢查，錯誤
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DorhpVm3trSxHG-l77-DpwbLTNQQxET1SIMYX-8ClQc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 995
ht-degree: 18%

---

# 在測試您的歷程之前疑難排解錯誤 {#troubleshooting}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在測試或發佈之前找到並修正活動和歷程設定錯誤，讓您的歷程順利執行。

>[!ENDSHADEBOX]

在本節中，瞭解如何在測試或發佈之前疑難排解歷程。 下列所有檢查皆可在歷程處於測試模式或歷程為即時狀態時執行。 建議您在測試模式中進行下列所有檢查，然後繼續發佈。 在[此頁面](../building-journeys/testing-the-journey.md)上進一步瞭解測試模式。

瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何瀏覽歷程，以及是否在此頁面[&#128279;](troubleshooting-execution.md)傳送訊息。 如果儘管已擷取事件，但沒有設定檔進入您的事件型歷程，請確定[事件條件資料型別符合事件結構描述](troubleshooting-execution.md#verify-event-identity-and-rule-data-types)。

如果您使用輸入動作，請在此頁面[&#128279;](troubleshooting-inbound.md)瞭解如何疑難排解。

## 活動中的錯誤 {#activity-errors}

在測試和發佈您的歷程之前，請先確認所有活動皆已正確設定。 如果系統仍偵測到錯誤，則無法進行測試或發佈。

發生錯誤，而且畫布上的活動本身會顯示警告符號。 將游標放在驚嘆號上，即可顯示錯誤訊息。 如果您選取活動，應該會看到錯誤的行並會顯示警告。 例如:

* 如果必填欄位為空，則會顯示錯誤

  ![畫布中顯示歷程驗證錯誤，錯誤指標為](assets/journey63.png)

* 在畫布中，當兩個活動中斷連線時，會顯示警告

  ![警告圖示在歷程畫布中顯示已中斷連線的活動](assets/canvas-disconnected.png)

## 歷程中的錯誤 {#canvas-errors}

畫布上方的&#x200B;**[!UICONTROL 警示]**&#x200B;按鈕也會顯示錯誤。 此按鈕可讓您檢視系統偵測到的錯誤，這些錯誤會阻止測試模式啟動或歷程發佈。

系統偵測到兩種問題： **錯誤**&#x200B;和&#x200B;**警告**。 錯誤會封鎖發佈及測試啟動。 警告指出未封鎖測試啟動或發佈的潛在問題。 您會看到問題的說明，以及類型 ERR_XXX_XXX 的問題日誌 ID。 這可協助識別問題。

![歷程中的錯誤和警告指示器，包含說明工具提示](assets/journey-error-and-warning.png)

<!--Most of the time, errors detected by the system are linked to errors visible on the activities but they can also relate to other issues. In all cases, check alerts and resolve the issue using to the error description. If you cannot identify the issue, use the **[!UICONTROL Copy details]** button to store the alerts, and send them to your administrator.-->

與歷程相關的全域錯誤和警告會先出現在清單中。 會依活動順序或外觀，由左至右地列出與特定活動相關的錯誤及警告。 在警示清單底部，**[!UICONTROL 複製詳細資料]**&#x200B;按鈕可讓您複製有助於疑難排解問題的歷程相關技術資訊。 如需已複製欄位的清單（包括暫停和繼續資訊），請參閱歷程屬性中的[複製技術詳細資訊](journey-properties.md#access-properties)。

## 新增替代路徑 {#canvas-add-path}

您可以為下列歷程活動定義發生錯誤時的遞補動作： **[!UICONTROL 最佳化]**&#x200B;和&#x200B;**[!UICONTROL 動作]**。

當動作或條件發生錯誤時，個人的歷程就會停止。 唯一能讓它繼續的方法是解決這個問題。 為避免中斷歷程，您還可以核取選項&#x200B;**[!UICONTROL 在逾時或活動屬性中的錯誤]**&#x200B;的情況下新增替代路徑。 若要了解更多資訊，請參閱[此區段](../building-journeys/using-the-journey-designer.md#paths)。

+++ AI知識參考

本節包含結構化知識，用於支援與本主題相關的解譯、擷取和問答。

如需完整瞭解，此資訊應結合本頁的檔案。 兩者皆非獨立來源；頁面說明功能，本節提供額外內容，以協助去除術語、意圖、適用性和限制條件的歧義。

* **TL；DR：**&#x200B;此頁面說明在進入測試模式或發佈之前，如何識別並解決歷程中的設定錯誤和警告。

**意圖：**

* 在測試或發佈歷程之前識別活動層級設定錯誤
* 在「警示」面板中區分封鎖錯誤與非封鎖警告
* 使用錯誤記錄ID （ERR_XXX_XXX格式）來診斷歷程問題
* 複製技術歷程詳細資料與管理員共用，以進行疑難排解
* 新增替代路徑以防止個別歷程在錯誤或逾時時時停止

**字彙表：**

* **警示按鈕**：顯示所有系統偵測到的錯誤和警告的畫布控制項，封鎖發佈或測試啟動&#x200B;*（產品特定）*
* **ERR_XXX_XXX**：指派給每個偵測到問題的問題記錄檔ID格式，用於識別及傳達錯誤&#x200B;*（產品特定）*
* **替代路徑**：在錯誤或逾時發生時，在動作或條件活動中新增了遞補分支&#x200B;*（產品特定）*，繼續歷程

**護欄：**

* 如果封鎖錯誤仍未解決，則您無法啟用測試模式或發佈歷程。
* 警告不會阻止發佈或測試啟動，但會指出潛在問題。
* 只有「最佳化」和「動作」活動可使用替代路徑。

**術語：**

* 正式名稱：警示 — 縮寫：無 — 變體：警示面板，警示按鈕
* 同義字： &quot;errors&quot; = &quot;blocking issues&quot;；&quot;warnings&quot; = &quot;non-blocking issues&quot;
* 請勿混淆：「錯誤」（封鎖發佈）≠「警告」（不要封鎖發佈）

**常見問題集：**

* **問：Journey Optimizer中的錯誤和警告有何不同？**  — 錯誤會封鎖測試模式啟用和歷程發佈；警告會指出潛在問題，但不會阻止測試或發佈。
* **問：我可以在哪裡看到影響我歷程的所有錯誤？**  — 按一下畫布上方的「警示」按鈕，檢視所有系統偵測到的錯誤和警告的整合清單。
* **問：如果無法從錯誤說明中找出問題，怎麼辦？**  — 使用「警示」清單底部的「複製詳細資訊」按鈕來擷取技術資訊，並將其傳送給您的管理員。
* **問：即使動作發生錯誤，我是否可以為個人維持歷程執行？**  — 是，在活動屬性中啟用「在逾時或錯誤的情況下新增替代路徑」選項以定義遞補路徑。
* **問：何時應該執行這些疑難排解檢查？**  — 所有檢查都可以在測試模式或歷程為即時狀態時執行；建議先在測試模式下解決所有問題，然後再發佈。

+++
