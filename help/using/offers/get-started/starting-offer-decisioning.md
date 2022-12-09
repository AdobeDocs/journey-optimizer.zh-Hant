---
title: 開始使用決策管理
description: 了解Adobe Journey Optimizer如何協助您在適當的時間為客戶提供合適的優惠方案
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# 關於決策管理 {#about-decision-management}

使用 [!DNL Journey Optimizer] 以在適當的時間跨所有接觸點為客戶提供最佳選件和體驗。 設計完成後，透過個人化優惠方案鎖定您的對象。

決策管理功能集中的行銷選件資料庫，以及將規則和限制套用至Adobe Experience Platform所建立的豐富即時設定檔的決策引擎，可協助您在正確的時間為客戶傳送合適的選件，讓您的個人化更加輕鬆。

「決策管理」功能包含兩個主要元件：

* 此 **集中優惠方案庫** 這是您建立和管理組成選件的不同元素，以及定義其規則和限制的介面。
* 此 **優惠方案決策引擎** 可運用Adobe Experience Platform資料和即時客戶設定檔，以及優惠方案庫，以選取將要提供優惠方案的正確時間、客戶和管道。

![](../assets/architecture.png)

優點包括：

* 透過跨多個管道提供個人化優惠方案，改善行銷活動效能，
* 改善的工作流程：行銷團隊可以透過建立單一傳送並在範本的不同部分變更優惠方案，來改善工作流程，而不需建立多個傳送或行銷活動，
* 控制促銷活動和客戶中顯示優惠方案的次數。

➡️ [透過這些影片深入了解決策管理](#video)


>[!NOTE]
>
>如果您是 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target=&quot;_blank&quot;}使用者運用 **Offer Decisioning** 應用程式服務，本節中描述的所有決策管理功能也適用於您。

## 關於選件與決策 {#about-offers-and-decisions}

安 **選件** 由內容、適用性規則和限制組成，定義向客戶呈現內容的條件。

會使用 **優惠方案庫**，此目錄提供集中優惠方案目錄，您可將適用性規則和限制與多個內容片段建立關聯，以建立和發佈優惠方案(請參閱 [選件程式庫使用者介面](../get-started/user-interface.md))。

![](../assets/offer_structure.png)

一旦優惠方案庫已擴充優惠方案，您就可以將優惠方案整合至 **決策**.

決策是您優惠方案的容器，可運用優惠方案決策引擎，以根據傳送目標挑選要傳送的最佳優惠方案。

## 常見使用案例 {#common-use-cases}

決策管理功能與Adobe Experience Platform整合可讓您涵蓋許多使用案例，協助您提高客戶參與度和轉換率。

* 根據Adobe Experience Platform的資料，顯示在網站首頁上符合訪客興趣點的優惠方案。

   ![](../assets/website.png)

* 如果客戶在您的某家商店附近走動，會傳送推播通知，提醒他們根據其屬性（忠誠度、性別、先前的購買……）提供優惠方案。

   ![](../assets/push_sample.png)

* 決策管理也可協助您在聯絡支援團隊時提升客戶體驗。 決策管理API可讓您在客服中心代理的入口網站中顯示有關客戶已贖回和下一個最佳優惠方案的資訊。

   ![](../../assets/do-not-localize/call-center.png)

## 授予Decision Management的存取權 {#granting-acess-to-decision-management}

存取和使用決策功能的權限是透過 [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}。

若要授與「決策管理」功能的存取權，您必須建立 **[!UICONTROL Product profile]** 並指派對應的權限給您的使用者。 深入了解管理 [!DNL Journey Optimizer] 使用者和權限 [本節](../../administration/permissions.md).

決策管理的特定權限列於 [本節](../../administration/high-low-permissions.md#decisions-permissions).

## 字彙表 {#glossary}

您可以在下方找到使用決策管理時要使用的主要概念清單。

* **限定** 或 **頻率限定**:限定作為定義呈現選件次數的限制。 有兩種大寫：可在合併的目標對象中建議某個優惠方案的次數，也稱為「大寫」，以及可向相同一般使用者建議某個優惠方案的次數，也稱為「設定檔大寫」。

* **集合**:集合是根據行銷人員定義的預先定義條件（例如優惠方案的類別）而提供的優惠方案子集。

* **決策**:決策包含通知選件選擇的邏輯。

* **決策規則**:決策規則是新增至個人化優惠方案的限制，並套用至設定檔以判斷資格。

* **合格優惠方案**:符合資格的優惠方案符合上游定義的限制，可一致地提供給設定檔。

* **決策管理**:可讓您使用業務邏輯和決策規則，跨管道和應用程式建立和提供使用者個人化優惠方案體驗。

* **回退優惠方案**:後援優惠方案是當使用者不符合集合中任何個人化優惠方案的資格時，所顯示的預設優惠方案。

* **選件**:優惠方案是行銷訊息，可能會有與其相關聯的規則，用以指定誰有資格看見優惠方案。

* **優惠方案庫**:優惠方案程式庫是集中的程式庫，用於管理個人化和備援優惠方案、決策規則和決策。

* **個人化優惠方案**:個人化優惠方案是根據適用性規則和限制而自訂的行銷訊息。

* **版位**:版位是一般使用者出現優惠方案的位置或內容。

* **優先順序**:優先順序可用來排名符合所有限制的選件，例如資格、日曆和上限。

* **表示**:表示法是管道使用的資訊，例如顯示選件的位置或語言。

## 作法影片{#video}

>[!NOTE]
>
>這些影片適用於以Adobe Experience Platform為基礎的Offer Decisioning應用程式服務，不是專屬於 [!DNL Adobe Journey Optimizer]. 但是，它們提供一般性指導，以在 [!DNL Journey Optimizer].

### 什麼是決策管理？ {#what-is-offer-decisioning}

以下影片簡介決策管理的主要功能、架構和使用案例：

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### 定義和管理優惠方案 {#use-offer-decisioning}

以下影片說明如何使用決策管理來定義和管理您的優惠方案，以及運用即時客戶資料。

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


