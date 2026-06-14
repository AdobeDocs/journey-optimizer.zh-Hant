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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 548
ht-degree: 33%

---

# 在測試您的歷程之前疑難排解錯誤 {#troubleshooting}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何在測試或發佈之前找到並修正活動和歷程設定錯誤，讓您的歷程順利執行。

>[!ENDSHADEBOX]

在本節中，瞭解如何在測試或發佈之前疑難排解歷程。 下列所有檢查皆可在歷程處於測試模式或歷程為即時狀態時執行。 建議您在測試模式中進行下列所有檢查，然後繼續發佈。 在[此頁面](../building-journeys/testing-the-journey.md)上進一步瞭解測試模式。

瞭解如何疑難排解歷程事件、檢查設定檔是否進入您的歷程、如何瀏覽歷程，以及是否在此頁面](troubleshooting-execution.md)傳送[訊息。 如果儘管已擷取事件，但沒有設定檔進入您的事件型歷程，請確定[事件條件資料型別符合事件結構描述](troubleshooting-execution.md#verify-event-identity-and-rule-data-types)。

如果您使用輸入動作，請在此頁面](troubleshooting-inbound.md)瞭解如何疑難排解[。

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
