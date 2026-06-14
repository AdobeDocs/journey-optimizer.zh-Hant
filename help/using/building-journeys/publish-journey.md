---
solution: Journey Optimizer
product: journey optimizer
title: 發佈歷程
description: 瞭解如何在Adobe Journey Optimizer中發佈歷程、建立新版本、管理歷程狀態，並瞭解重新發佈的要求。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 發佈，歷程，即時，有效性，檢查
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Hhvwpfq0phAjvzIGgv-NMnnhWhYJ-PpLOL0F4Q-CnqA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 1295
ht-degree: 20%

---

# 發佈您的歷程 {#publishing-the-journey}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;瞭解如何發佈歷程以將其設定為上線，包括先決條件、發佈程式、版本管理和重新發佈需求。

>[!ENDSHADEBOX]

發佈歷程會將其啟用：它會移至&#x200B;**[!UICONTROL 即時]**&#x200B;狀態、可供新設定檔進入，並切換至唯讀模式。 您無法發佈包含錯誤的歷程。

>[!NOTE]
>
>當您儲存或發佈歷程時，Journey Optimizer會驗證歷程裝載總大小，如果您接近或超過限制，可能會警告或封鎖發佈。 深入瞭解[歷程裝載大小驗證](../start/guardrails.md#journey-payload-size)。

➡️ [在影片中探索此功能](#video)

## 發佈之前 {#before-you-publish}

發佈之前，請確認您的歷程符合下列先決條件：

* **沒有驗證錯誤** — 您無法發佈包含錯誤的歷程。 [請先測試您的歷程](testing-the-journey.md)，然後[疑難排解任何活動錯誤](../building-journeys/troubleshooting.md#activity-errors)。
* **發佈許可權** — 發佈需要&#x200B;**[!DNL Publish journeys]**&#x200B;高階許可權。 深入瞭解[管理存取許可權](../administration/permissions-overview.md)。
* **有效負載在限制內** — 歷程有效負載必須在設定的限制內（預設為4 MB）。 請參閱[歷程裝載大小驗證](../start/guardrails.md#journey-payload-size)。
* **已取得核准** — 如果您的歷程受限於核准原則，請在發佈前要求並取得核准。 [了解更多](../test-approve/gs-approval.md)。

>[!TIP]
>
>發佈之前，請使用其中一個可用的測試選項來驗證您的歷程：
>
>* [模擬](simulate-journey-gs.md) — 使用模擬使用者進行測試，而不使用Adobe Experience Platform中的持續性測試設定檔。
>* [測試模式](testing-the-journey.md) — 使用在Adobe Experience Platform中標籤為測試設定檔的持續設定檔進行測試。
>* [試用](journey-dry-run.md) — 以真實的生產資料進行測試，無需連絡設定檔。

## 發佈程式 {#journey-publication}

發佈歷程的步驟詳述如下：

1. 確認歷程有效且沒有錯誤，並且符合上述[必要條件](#before-you-publish)。

1. 若要發佈歷程，請按一下右上角下拉式功能表中的&#x200B;**[!UICONTROL 發佈]**&#x200B;選項。

   >[!NOTE]
   >
   > 如果您的歷程受核准政策的約束，您必須請求核准才能發佈您的歷程。 [了解更多](../test-approve/gs-approval.md)

   歷程工具列中的![發佈按鈕以啟動歷程](assets/journeyuc1_18.png)

發佈歷程時，它處於&#x200B;**唯讀**&#x200B;模式。 在唯讀模式中，您只能修改活動標籤和說明、歷程名稱和歷程說明。 如果您需要對已發佈的歷程進行額外的修改，請建立歷程的[新版本](journey-ui.md#journey-filter)。

### 歷程狀態 {#journey-statuses}

發佈後，歷程會經歷幾種狀態：

* **[!UICONTROL 即時]** — 已發佈歷程且設定檔可以進入歷程。
* **[!UICONTROL 已關閉]** — 發佈新版本時自動結束的先前版本。 無法進入。
* **[!UICONTROL 已完成]** — 歷程已根據其結束條件完成。 如需歷程被視為完成時間的確切定義，請參閱[歷程如何結束](end-journey.md#journey-finished-definition)。

### 停止歷程 {#stop-journey}

當您停止歷程時，歷程會永久停止。 流經歷程的所有個人會永久停止，且歷程會停止允許新登入。 如果您需要再次執行歷程，請複製歷程並發佈新歷程。 如需歷程如何結束的詳細資訊，請參閱[歷程如何結束](end-journey.md)。

### 重新發佈需求 {#republishing}

在某些情況下，您必須重新發佈歷程才能讓變更或資產保持有效：

>[!IMPORTANT]
>
>* 如果對歷程訊息中使用的優惠決定進行變更，您需要取消發佈歷程並重新發佈。 這可確保將變更納入歷程的訊息中，且訊息與最新更新一致。
>
>* Assets/影像在任何片段/內嵌訊息中的首次發佈後，最多可在2年（730天）的傳遞內容中存取。 在此到期日後（730天後的任何時間）必須重新發佈，才能在隨後2年內可供存取。 在首次發佈後730天內完成的任何重新發佈，都不會將資產/影像的到期日延長至接下來的730天。

## 歷程版本 {#journey-versions}

在歷程清單中，所有歷程版本都會連同版本號碼一起顯示。 當您搜尋歷程時，最新版本會在應用程式首次開啟時出現在清單頂端。 然後，您可以定義所需的排序，應用程式會將其保留為使用者偏好設定。 歷程的版本也會顯示在畫布上方的歷程版本介面頂端。

![歷程版本清單顯示已發佈和草稿版本](assets/journeyversions1.png)

>[!NOTE]
>
>通常，對於歷程的所有作用中版本，設定檔無法在同一歷程中同時出現多次。 如果啟用重新進入，輪廓可以重新進入歷程，但必須完全退出歷程的上一個執行個體，才能執行此動作。 [閱讀全文](entry-management.md)。

### 建立歷程的新版本 {#journey-create-new-version}

如果您需要修改為即時歷程，請建立歷程的新版本。 若要建立現有歷程的新版本，請遵循下列步驟：

1. 開啟最新版本的即時歷程，按一下&#x200B;**[!UICONTROL 建立新版本]**&#x200B;並確認。

   ![建立新版本對話方塊以複製歷程](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能從歷程的最新版本建立新版本。

1. 進行修改，按一下&#x200B;**[!UICONTROL 發佈]**&#x200B;並確認。

從發佈歷程的那一刻起，個人就會開始進入歷程的最新版本。 已進入舊版本的人會保留在舊版本中，直到歷程結束。 如果他們稍後重新進入相同的歷程，則會進入最新版本。

歷程版本可個別停止。 所有版本的歷程都有相同的名稱。

當您發佈歷程的新版本時，舊版本會自動結束並切換到&#x200B;**已關閉**&#x200B;狀態。 歷程無法進入。 即使您停止最新版本，先前版本仍會保持關閉狀態。


>[!NOTE]
>
>特定護欄和限制適用於歷程的版本設定。 請在[此頁面](../start/guardrails.md#journey-versions-g)了解更多。


## 常見問題 {#faq}

**為什麼我無法發佈我的歷程？**

最常見的原因是歷程包含驗證錯誤 — 您無法發佈有錯誤的歷程。 其他封鎖程式包括超過[承載大小限制](../start/guardrails.md#journey-payload-size)、缺少&#x200B;**[!DNL Publish journeys]**&#x200B;許可權或擱置中的[核准](../test-approve/gs-approval.md)。 請參閱[發佈之前](#before-you-publish)和[疑難排解活動錯誤](../building-journeys/troubleshooting.md#activity-errors)。

**我可以在歷程發佈後編輯歷程嗎？**

已發佈歷程處於唯讀模式。 您只能變更活動標籤和說明、歷程名稱和歷程說明。 針對任何其他變更，[建立歷程的新版本](#journey-create-new-version)。

**當我發佈新版本時，歷程中已有的設定檔會發生什麼事？**

新的設定檔會流入最新版本。 在先前版本中已存在的設定檔會保留在那裡，直到完成為止；如果設定檔稍後重新輸入，則會進入最新版本。 舊版會自動切換為&#x200B;**[!UICONTROL 已關閉]**，不接受任何新專案。 檢視[歷程版本](#journey-versions)。

**如何重新執行已停止的歷程？**

停止歷程是永久性的。 若要再次執行，請複製它並發佈新歷程。 請參閱[停止歷程](#stop-journey)。

**變更優惠決定或更新資產後，是否需要重新發佈？**

有。 如果您變更歷程訊息中使用的優惠決定，請取消發佈並重新發佈歷程，以套用變更。 Assets和影像會在首次發佈後730天到期，然後重新發佈以方便存取。 請參閱[重新發佈需求](#republishing)。

**我可以發佈需要核准的歷程嗎？**

如果您的歷程受限於核准政策，您必須在發佈前要求核准。 [進一步瞭解核准](../test-approve/gs-approval.md)。

## 相關主題 {#related-topics}

* [測試您的歷程](testing-the-journey.md) — 在發佈之前使用測試設定檔驗證您的歷程
* [歷程模擬](simulate-journey-gs.md) — 在發佈之前透過模擬的使用者驗證您的歷程
* [歷程練習](journey-dry-run.md) — 測試真實的生產資料，但不連絡設定檔
* [疑難排解](../building-journeys/troubleshooting.md#activity-errors) — 解決活動和發佈錯誤
* [歷程結束的方式](end-journey.md#journey-finished-definition) — 瞭解歷程完成和狀態
* [設定檔入口管理](entry-management.md) — 設定設定檔如何進入及重新進入歷程
* [歷程護欄和限制](../start/guardrails.md#journeys-guardrails-journeys) — 檢閱出版物和版本設定護欄

## 作法影片 {#video}

透過此影片瞭解如何發佈歷程：

>[!VIDEO](https://video.tv.adobe.com/v/3427942?captions=chi_hant&quality=12)
