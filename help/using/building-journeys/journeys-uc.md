---
solution: Journey Optimizer
product: journey optimizer
title: Journeys使用案例
description: Journeys使用案例
feature: Journeys, Use Cases, Email, Push
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: 使用案例，多頻道，訊息，歷程，頻道，事件，推播
exl-id: a1bbfcee-2235-4820-a391-d5d35f499cb0
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/o4-7bKdQzB3Yyz22khT4RHNpNvKL0sCg8YPPnaeav9I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: e57d1da4-32c2-4cc6-945c-9feb219156ffid: ebd64fe4-362a-4a1c-9476-b2573ed12a95id: fa683eda-48de-4558-af32-2673edcd44feid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1060
ht-degree: 1%

---

# 傳送多管道訊息 {#send-multi-channel-messages}

本節介紹結合讀取對象、事件、反應事件和電子郵件/推播訊息的使用案例。

![包含讀取對象、等待和電子郵件活動的簡單歷程流程](assets/jo-uc1.png)

## 使用案例的說明

在此使用案例中，目標是傳送第一封電子郵件訊息給屬於特定對象的所有客戶。

系統會根據使用者對第一條訊息的反應，傳送特定的後續訊息。

如果客戶開啟電子郵件，系統會等待購買，並傳送推播訊息以感謝客戶。

如果沒有回應，則會傳送後續電子郵件。

## 先決條件

為了讓此使用案例發揮作用，請設定下列專案：

* 適用於居住在亞特蘭大、舊金山或西雅圖且出生於1980年後之所有客戶的對象
* 購買事件

### 建立對象

在此歷程中，會運用特定的客戶對象。 屬於對象的所有個人都會進入歷程並遵循不同步驟。 在此範例中，受眾的目標是居住在亞特蘭大、舊金山或西雅圖並在1980年後出生的所有客戶。

如需對象的詳細資訊，[請參閱此頁面](../audience/about-audiences.md)。

1. 從「客戶」功能表區段中，選取&#x200B;**[!UICONTROL 對象]**。
1. 按一下位於對象清單右上角的&#x200B;**[!UICONTROL 建立對象]**&#x200B;按鈕。
1. 在&#x200B;**[!UICONTROL 對象屬性]**&#x200B;窗格中，輸入對象的名稱。
1. 將所需欄位從左窗格拖放至中央工作區，並根據您的需求進行設定。 在此範例中，使用&#x200B;**城市**&#x200B;和&#x200B;**出生年份**&#x200B;屬性欄位。
1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   ![用於選取擴充資料的其他屬性面板](assets/add-attributes.png)

對象現在已建立並準備好用於歷程中。 使用&#x200B;**讀取對象**&#x200B;活動，屬於該對象的所有個人都可以進入歷程。

### 設定事件

設定當客戶購買時傳送到歷程的事件。 歷程收到事件時會觸發「感謝您」訊息。

為此，請使用[規則型事件](../event/about-events.md)。

1. 在[管理]功能表區段中，選取&#x200B;**[!UICONTROL 組態]**，然後按一下&#x200B;**[!UICONTROL 事件]**。 按一下&#x200B;**[!UICONTROL 建立事件]**&#x200B;以建立新事件。

1. 輸入事件的名稱。

1. 在&#x200B;**[!UICONTROL 事件識別碼型別]**&#x200B;欄位中，選取&#x200B;**[!UICONTROL 以規則為基礎]**。

1. 定義&#x200B;**[!UICONTROL 結構描述]**&#x200B;和承載&#x200B;**[!UICONTROL 欄位]**。 使用數個欄位，例如購買的產品、購買日期和購買ID。

1. 在&#x200B;**[!UICONTROL 事件ID條件]**&#x200B;欄位中，定義系統用來識別觸發歷程之事件的條件。 例如，新增`purchaseMessage`欄位並定義下列規則： `purchaseMessage="thank you"`

1. 定義&#x200B;**[!UICONTROL 名稱空間]**&#x200B;和&#x200B;**[!UICONTROL 設定檔識別碼]**。

1. 按一下&#x200B;**[!UICONTROL 儲存]**。

   ![條件活動分支到Gold成員和其他路徑的歷程](assets/jo-uc2.png)

事件現在已設定完畢，且準備好用於歷程中。 使用相應的事件活動，即可在每次客戶購買時觸發動作。

## 設計歷程

1. 以&#x200B;**讀取對象**&#x200B;活動開始歷程。 選取先前建立的對象。 屬於對象的所有個人都會進入歷程。

   ![檢查溫度是否低於50度](assets/jo-uc4.png)的天氣狀況

1. 拖放&#x200B;**電子郵件**&#x200B;動作活動，並定義「第一封郵件」的內容。 此訊息會傳送給歷程中的所有個人。 請參閱此[區段](../email/create-email.md)，瞭解如何設定和設計電子郵件。

   ![完成天氣型歷程，包含溫度條件和電子郵件動作](assets/jo-uc5.png)

1. 新增&#x200B;**回應**&#x200B;事件並選取&#x200B;**電子郵件已開啟**。 當屬於閱聽眾的個人開啟電子郵件時，就會觸發事件。

1. 勾選&#x200B;**定義事件逾時**&#x200B;方塊、定義持續時間（在此範例中為1天），並勾選&#x200B;**設定逾時路徑**。 這會為未開啟推送或電子郵件第一則訊息的個人建立另一個路徑。

1. 在逾時路徑中，拖放&#x200B;**電子郵件**&#x200B;動作活動，並定義「後續追蹤」訊息的內容。 此訊息會傳送給隔天未開啟電子郵件或推播第一則訊息的個人。 [瞭解如何設定和設計電子郵件](../email/create-email.md)。

1. 在第一個路徑中，新增先前建立的購買事件。 當個人購買時會觸發事件。

1. 在事件之後，拖放&#x200B;**推播**&#x200B;動作活動，並定義「感謝您」訊息的內容。 請參閱此[區段](../push/create-push.md)，瞭解如何設定和設計推播。

## 測試並發佈歷程

1. 測試歷程之前，請先確認歷程有效且沒有錯誤。

1. 使用位於右上角的&#x200B;**測試**&#x200B;切換以啟動測試模式。 請參閱此[區段](testing-the-journey.md)以瞭解如何使用測試模式。

1. 歷程就緒時，請使用右上角的&#x200B;**發佈**&#x200B;按鈕發佈。

## 多階段忠誠度歷程 {#multi-phase-loyalty}

此範例說明關鍵歷程架構模式：將複雜的多階段歷程分解為與[**[!UICONTROL 跳轉]**](jump.md)活動連線的較小且集中的子歷程。 此情境中即包含熟客方案，但此模式適用於跨越多個里程碑或業務階段的任何歷程。

複雜的多階段歷程會快速產生大量不重複的客戶路徑。 每個階段將其分解為一個子歷程，讓每個歷程都能管理、測試及獨立維護。

### 藍本

考慮使用兩個行銷管道（[電子郵件](../email/create-email.md)和[推播](../push/create-push.md)），引導客戶完成三個里程碑的熟客方案：

1. **階段1 — 下載行動應用程式：**&#x200B;初始通訊鼓勵新忠誠會員下載應用程式。 若客戶在指定期間內未執行作業，系統會傳送後續提醒。
1. **階段2 — 進行第一筆交易：**&#x200B;下載應用程式後，目標訊息會引導客戶完成其第一筆忠誠度交易。
1. **階段3 — 進行第二筆交易：**&#x200B;在第一次交易之後，最後的通訊組會推動第二次交易，以深化忠誠度參與。

即使使用此直接的策略，此歷程仍會公開客戶可採取的20多個不重複路徑。 每個額外的接觸點或管道的複雜性都會以指數方式增加。

### 子歷程分解

將端對端歷程分成三個較小的連線子歷程：

| 子歷程 | 輸入條件 | 業務目標 |
|---|---|---|
| 階段1 — 應用程式下載 | 客戶加入忠誠計畫 | 推動行動應用程式下載 |
| 階段2 — 第一個交易 | 客戶下載應用程式 | 推動第一個熟客方案交易 |
| 階段3 — 第二個交易 | 客戶完成第一筆交易 | 推動第二筆熟客交易 |

使用[**[!UICONTROL 跳轉]**](jump.md)活動連線子歷程，讓設定檔順暢地從一個階段傳遞至下一個階段。 每個子歷程都維持簡單、可讀取和獨立維護的狀態。

<!--
>[!NOTE]
>
>If your goal is to build a gamified loyalty program with challenges, tasks, and built-in reward tracking, Journey Optimizer also offers a dedicated **Loyalty Challenges** capability.
-->

