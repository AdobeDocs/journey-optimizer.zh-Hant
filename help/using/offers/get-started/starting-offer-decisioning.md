---
title: 開始使用決策管理
description: 瞭解 Adobe Journey Optimizer 如何幫助您在適當的時間向客戶傳送適當的優惠
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: 2acb883b66e5da9c06ba1551f708bb8ab47ce343
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 100%

---

# 開始使用決策管理 {#about-decision-management}

使用 [!DNL Journey Optimizer] 可在適當的時間為所有接觸點的客戶提供最佳優惠和體驗。設計完成後，透過個人化優惠目標定位客群。

決策管理透過集中行銷優惠資料庫和決定引擎輕鬆實現個人化，該決策引擎將規則和限制套用於 Adobe Experience Platform 建立的豐富即時輪廓，以幫助您在適當的時間向客戶傳送合適的優惠。

「決定管理」功能由兩個主要元件組成：

* **集中式優惠資料庫**&#x200B;是您建立和管理不同元素的介面，這些元素會組成優惠，並定義其規則和限制。
* **優惠決定引擎**&#x200B;運用 Adobe Experience Platform 資料、即時客戶輪廓以及優惠資料庫，以選擇即將提供優惠的適當時間、客戶和管道。

![](../assets/architecture.png)

效益包括：

* 透過跨多管道提供個人化優惠，改善行銷活動績效；
* 改善工作流程：行銷團隊可以建立單一傳遞，並在範本的不同部分提供不同優惠方案，藉此改善工作流程，而無須建立多個傳遞或行銷活動；
* 控制在電子郵件行銷活動中和向客戶顯示優惠方案的次數。

➡️ [在這些影片中瞭解有關決策管理的更多資訊](#video)

>[!NOTE]
>
>如果您是 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hant){target="_blank"} 使用者且正在利用&#x200B;**優惠方案決策**&#x200B;應用程式，本節中介紹的所有決策管理功能也適用於您。

## 關於優惠和決定 {#about-offers-and-decisions}

**優惠方案**&#x200B;由內容、適用規則和限制組成，這些限制定義了向客戶展示優惠的條件。

它是使用&#x200B;**優惠資料庫**&#x200B;所建立，提供集中式的優惠目錄，讓您可利用適用規則和限制與多項內容連結，以建立和發佈優惠 (請參閱[優惠資料庫使用者介面](../get-started/user-interface.md))。

![](../assets/offer_structure.png)

一旦優惠資料庫已有足夠豐富的優惠，您可以將優惠整合至 **決定**&#x200B;中。

決定是優惠的容器，可運用優惠決定引擎，根據傳送的目標定位來挑選最佳優惠。

## 常見使用實例 {#common-use-cases}

配合 Adobe Experience Platform 的決定管理功能與整合可讓您涵蓋許多使用實例，協助您提高客戶參與度和轉化率。

* 在您網站首頁顯示的優惠方案，將會根據 Adobe Experience Platform 的資料以符合造訪客戶的興趣。

  ![](../assets/website.png)

* 如果客戶靠近某家商店，請傳送推播通知，可依其屬性 (忠誠度、性別、之前的購物內容……) 提醒他們可使用的優惠方案。

  ![](../assets/push_sample.png)

* 決定管理也可協助您在聯絡支援團隊時增強客戶體驗。 API 可讓您在呼叫中心代理的入口網站中顯示客戶的兌換資訊，以及下一個最佳優惠。

  ![](../../assets/do-not-localize/call-center.png)

## 授予決策管理的存取權限 {#granting-acess-to-decision-management}

使用 [Adobe Admin Console](https://helpx.adobe.com/tw/enterprise/managing/user-guide.html){target="_blank"} 管理存取及使用決策功能的權限。

要授予對決策管理功能的存取權限，您需要建立&#x200B;**[!UICONTROL 產品設定檔]**，並將對應權限指派給使用者。在[本節](../../administration/permissions.md)瞭解有關管理 [!DNL Journey Optimizer] 使用者及權限的更多資訊。

[本節](../../administration/high-low-permissions.md#decisions-permissions)列出了決策管理的特定權限。

## 字彙 {#glossary}

您可以在下方找到使用決定管理時，將使用的主要概念清單。

* **上限**&#x200B;或&#x200B;**頻率上限**：上限是用來作為限制，定義優惠方案的顯示次數。 共有兩種上限，分別是可在合併的目標客群間建議的優惠方案次數 (也稱為「限定總數」)，以及可向同一位一般使用者建議的優惠方案次數 (也稱為「輪廓上限」) 的次數。

* **集合**：集合是行銷人員根據優惠方案類別等預先定義的條件，定義的優惠方案子集。

* **決定**：決定包含通知選擇活動內容的邏輯。

* **決定規則**：決定規則是新增至個人化優惠方案的限制，並可套用至輪廓以判斷適用性。

* **符合資格優惠**：符合資格優惠方案符合上游定義的限制，並可持續地提供給輪廓。

* **決定管理**：可讓您使用商業邏輯和決定規則，跨頻道和應用程式建立並提供使用者個人化的優惠體驗。

* **遞補優惠**：當一般使用者不具集合中任何個人化優惠方案的資格時，遞補優惠方案會是顯示的預設優惠方案。

* **優惠方案**：優惠方案是行銷訊息，其內容可能包含與其相關聯的規則，指定誰有資格檢視優惠方案。

* **優惠資料庫**：優惠資料庫是一個中央資料庫，用來管理個人化和遞補優惠、決定規則和活動。

* **個人化優惠方案**：個人化優惠方案是根據適用性規則和限制的可自訂行銷訊息。

* **位置**：位置是為一般使用者所顯示優惠方案的所在位置和/或內容。

* **優先順序**：優先順序用於將符合所有限制的優惠方案排名，例如適用性、行事曆和上限。

* **表示方式**：表示方式是管道所使用的資訊，例如要顯示優惠方案的位置或語言。

## 作法影片{#video}

### 什麼是決定管理？ {#what-is-offer-decisioning}

下面的影片介紹了決定管理的重要功能、結構和使用案例：

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 定義和管理優惠 {#use-offer-decisioning}

以下影片說明如何使用決定管理來定義和管理您的優惠，並運用即時客戶資料。

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


