---
solution: Journey Optimizer
product: journey optimizer
title: 重要術語
description: Adobe Journey Optimizer中的基本術語和概念
feature: Get Started
role: Admin, Developer, User
level: Beginner
source-git-commit: 4ae9e908d259dbd266417242cf9e65d693227061
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 9%

---

# 重要術語 {#key-terminology}

本參考指南定義您在使用Adobe Journey Optimizer時會遇到的基本術語。 瞭解這些概念可協助您安心地瀏覽平台，並與團隊有效合作。

>[!TIP]
>
>如需功能和工作流程的詳細說明，請參閱本指南中連結的特定檔案區段。

## 核心平台術語 {#core-terms}

| 術語 | 定義 |
|------|------------|
| **Adobe Journey Optimizer** | 跨管道（電子郵件、簡訊、推播通知、網頁）建立及傳遞個人化訊息給客戶的應用程式。 它可讓您設計回應即時客戶動作的客戶歷程。 |
| **Adobe Experience Platform** | Adobe Journey Optimizer的基礎，可在一個地方收集並整理所有客戶資料。 它會建立Journey Optimizer用於個人化的統一客戶設定檔。 [了解更多](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=zh-Hant){target="_blank"} |
| **即時客戶輪廓** | 每個客戶的統一即時檢視，結合來自多個管道的資料，包括線上、離線、CRM和第三方資料。 每個設定檔會隨著客戶與您的品牌互動而動態更新。 [了解更多](../audience/get-started-profiles.md) |
| **沙箱** | 提供獨立的工作區以供測試和實驗，而不會影響即時客戶通訊。 Adobe Journey Optimizer為開發、測試和生產環境提供多個沙箱。 [了解更多](../administration/sandboxes.md) |

## 歷程與行銷活動條款 {#journey-campaign-terms}

| 術語 | 定義 |
|------|------------|
| **歷程** | 一系列連線的步驟，可引導客戶逐步使用您的品牌體驗。 每個步驟都是根據客戶動作或時間觸發器進行，這會啟用循序的個人化互動。 [了解更多](../building-journeys/journey.md) |
| **Campaign** | 傳送給特定對象的單一通訊或一組通訊。 不同於隨時間展開的歷程，行銷活動會依排程或觸發器立即或於特定時間傳送訊息。 [了解更多](../campaigns/get-started-with-campaigns.md) |
| **活動** | 觸發或前進歷程的動作或發生次數。 事件可以是客戶動作（購買、放棄購物車）或系統事件（日期/時間、資料變更）。 [了解更多](../event/about-events.md) |
| **頻道** | 用來與客戶通訊的方法：電子郵件、簡訊、推播通知、應用程式內訊息、網頁或直接郵件。 每個管道都需要特定設定。 [了解更多](../configuration/get-started-configuration.md) |

## 客戶與受眾詞語 {#customer-audience-terms}

| 術語 | 定義 |
|------|------------|
| **客群** | 一組具有共同特徵或行為的客戶，例如「過去30天內購買的客戶」或「忠誠計畫會員」。 受眾是用來鎖定特定客戶區段。 [了解更多](../audience/about-audiences.md) |
| **對象資格** | 客戶加入或離開對象時發生的自動程式。 Journey Optimizer可在有人進入或離開對象時觸發動作，以確保及時且相關的通訊。 [了解更多](../building-journeys/audience-qualification-events.md) |
| **可參與的對象** | 您可以根據授權合約，透過Adobe Journey Optimizer主動聯絡的客戶設定檔數目。 這通常是指過去12個月內參與的設定檔。 |
| **測試設定檔** | 在傳送給真實客戶之前用於測試和預覽訊息的虛構設定檔。 測試設定檔有助於驗證個人化、內容和歷程邏輯。 [了解更多](../audience/creating-test-profiles.md) |

## 內容與Personalization術語 {#content-terms}

| 術語 | 定義 |
|------|------------|
| **個人化** | 使用個人資料資料、偏好設定和行為量身打造內容給個別客戶的程式。 例如，插入客戶名稱或根據瀏覽歷史記錄顯示產品推薦。 [了解更多](../personalization/personalize.md) |
| **內容範本** | 可重複使用的訊息設計，可用於多個行銷活動和歷程，以維持品牌一致性並加速內容建立。 [了解更多](../content-management/content-templates.md) |
| **片段** | 可重複使用的內容區塊（例如頁首、頁尾或促銷橫幅），可用於多則訊息，以確保一致性並啟用集中式更新。 [了解更多](../content-management/fragments.md) |
| **登陸頁面** | 獨立網頁，客戶可選擇加入或選擇退出通訊、訂閱服務，或透過線上表單提供資訊。 [了解更多](../landing-pages/get-started-lp.md) |

## 決定與優惠條款 {#decision-terms}

| 術語 | 定義 |
|------|------------|
| **決策管理** | 可根據即時設定檔資料、內容和商業規則，自動為每個客戶選取最佳內容或優惠方案的功能。 [了解更多](../offers/get-started/starting-offer-decisioning.md) |
| **選件** | 可呈現給客戶的行銷訊息、折扣或促銷活動。 優惠方案包含適用性規則，可決定哪些客戶可接收優惠方案。 [了解更多](../offers/offer-library/creating-personalized-offers.md) |
| **決定原則** | 一組規則和策略，用來根據適用性、優先順序和上限規則等限制，決定要在何時向哪個客戶顯示哪個優惠方案。 [了解更多](../experience-decisioning/create-decision.md) |

## 資料與設定條款 {#data-config-terms}

| 術語 | 定義 |
|------|------------|
| **結構描述** | 定義資料在Adobe Experience Platform中如何組織的結構，包括欄位名稱、資料型別和關係。 結構描述可確保跨系統的資料一致性。 [了解更多](../data/get-started-schemas.md) |
| **資料集** | 遵循特定結構的資料集合（通常是表格）。 資料集能儲存客戶資料、互動事件，以及用於個人化的其他資訊。 [了解更多](../data/get-started-datasets.md) |

>[!NOTE]
>
>如需Adobe Experience Platform術語的完整辭彙表，請參閱[Adobe Experience Platform辭彙表](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html?lang=zh-Hant){target="_blank"}。

## 相關主題 {#related-topics}

* [瞭解Journey Optimizer的運作方式](understanding-ajo.md)
* [開始使用使用者介面](user-interface.md)
* [選擇您的角色和學習路徑](quick-start.md)

