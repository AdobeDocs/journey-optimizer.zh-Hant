---
solution: Journey Optimizer
product: journey optimizer
title: 重要術語
description: Adobe Journey Optimizer中的基本術語和概念
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 14e72376-87ad-4fae-bf8c-f347109d7903
TQID: https://experienceleague.adobe.com/-aDvt4RUXyf0EnPfFTJkG1CvWgte-1Fr6YaWvgcNNu4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: b4ce14492d56e7121f827cf6a46abc5c222180e5
workflow-type: tm+mt
source-wordcount: 1760
ht-degree: 8%

---

# 重要術語 {#key-terminology}

本參考指南定義您在使用Adobe Journey Optimizer時會遇到的基本術語。 瞭解這些概念可協助您安心地瀏覽平台，並與團隊有效合作。

對於聽起來類似但經常令人困惑的辭彙組 — 例如&#x200B;**決策與決策管理**&#x200B;或&#x200B;**內容卡與應用程式內訊息** — 請參閱本頁底部的[當辭彙看起來類似時](#disambiguation)。

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
| **Campaign** | 協調的行銷動作，可跨一或多個管道將內容提供給特定對象。 與歷程不同，行銷活動會同時執行動作。 Journey Optimizer支援三種行銷活動型別： **動作行銷活動** （排程批次傳送）、**API觸發的行銷活動** （透過API的即時、事件導向的傳訊）和&#x200B;**協調的行銷活動** （具有視覺畫布的複雜多步驟工作流程）。 [了解更多](../campaigns/get-started-with-campaigns.md) |
| **活動** | 觸發或前進歷程的動作或發生次數。 事件可以是客戶動作（購買、放棄購物車）或系統事件（日期/時間、資料變更）。 [了解更多](../event/about-events.md) |
| **頻道** | 用來與客戶通訊的方法：電子郵件、簡訊、推播通知、應用程式內訊息、網頁或直接郵件。 每個管道都需要特定設定。 [了解更多](../configuration/get-started-configuration.md) |

## 客戶與受眾詞語 {#customer-audience-terms}

| 術語 | 定義 |
|------|------------|
| **客群** | 一組具有共同特徵或行為的客戶，例如「過去30天內購買的客戶」或「忠誠計畫會員」。 受眾是用來鎖定特定客戶區段。 [了解更多](../audience/about-audiences.md) |
| **對象資格** | 客戶加入或離開對象時發生的自動程式。 Journey Optimizer可在有人進入或離開對象時觸發動作，以確保及時且相關的通訊。 [了解更多](../building-journeys/audience-qualification-events.md) |
| **可參與的對象** | 您可以根據授權合約，透過Adobe Journey Optimizer主動聯絡的客戶設定檔數目。 這通常是指過去12個月內參與的設定檔。 |
| **測試設定檔** | 在傳送給真實客戶之前用於測試和預覽訊息的虛構設定檔。 測試設定檔有助於驗證個人化、內容和歷程邏輯。 [了解更多](../audience/creating-test-profiles.md) |

## 內容與個人化詞語 {#content-terms}

| 術語 | 定義 |
|------|------------|
| **個人化** | 使用個人資料資料、偏好設定和行為量身打造內容給個別客戶的程式。 例如，插入客戶名稱或根據瀏覽歷史記錄顯示產品推薦。 [了解更多](../personalization/personalize.md) |
| **內容範本** | 可重複使用的訊息設計，可用於多個行銷活動和歷程，以維持品牌一致性並加速內容建立。 [了解更多](../content-management/content-templates.md) |
| **片段** | 可重複使用的內容區塊（例如頁首、頁尾或促銷橫幅），可用於多則訊息，以確保一致性並啟用集中式更新。 [了解更多](../content-management/fragments.md) |
| **登陸頁面** | 獨立網頁，客戶可選擇加入或選擇退出通訊、訂閱服務，或透過線上表單提供資訊。 [了解更多](../landing-pages/get-started-lp.md) |
| **內容實驗** | A/B測試架構會將受眾分割為隨機群組，並向每個群組傳遞不同的訊息變體（內容、主旨行或選件），然後根據定義的成功量度識別績效最佳的變體。 [了解更多](../content-management/get-started-experiment.md) |
| **實驗中** | Journey Optimizer中用於測試和最佳化決策的更廣泛功能：內容實驗會測試行銷活動和歷程中的訊息變體，而決策實驗測試會提供選擇策略。 兩者都使用統計分析來識別成功方法。 [了解更多](../content-management/get-started-experiment.md) |

## 決定與優惠條款 {#decision-terms}

| 術語 | 定義 |
|------|------------|
| **決策** | Journey Optimizer中最新一代的決策架構，建議用於新實作。 提供結構描述型專案目錄管理、彈性的收集規則、可重複使用的決定元件和實驗功能。 可用於程式碼型體驗、推播、簡訊和電子郵件（可用性限制）。 [了解更多](../experience-decisioning/gs-experience-decisioning.md) |
| **決定管理** | Journey Optimizer中的舊版Offer Decisioning功能。 使用中央行銷優惠資料庫和規則型決定引擎，將限制套用至即時客戶設定檔。 現有實施仍支援，但新實施應改用Decisioning。 支援電子郵件、應用程式內、推播、簡訊和直接郵件。 [了解更多](../offers/get-started/starting-offer-decisioning.md) |
| **選件** | 可呈現給客戶的行銷訊息、折扣或促銷活動。 優惠方案包含適用性規則，可決定哪些客戶可接收優惠方案。 [了解更多](../offers/offer-library/creating-personalized-offers.md) |
| **決定原則** | 一組規則和策略，用來根據適用性、優先順序和上限規則等限制，決定要在何時向哪個客戶顯示哪個優惠方案。 [了解更多](../experience-decisioning/create-decision.md) |

## 資料與設定條款 {#data-config-terms}

| 術語 | 定義 |
|------|------------|
| **結構描述** | 定義資料在Adobe Experience Platform中如何組織的結構，包括欄位名稱、資料型別和關係。 結構描述可確保跨系統的資料一致性。 [了解更多](../data/get-started-schemas.md) |
| **資料集** | 遵循特定結構的資料集合（通常是表格）。 資料集能儲存客戶資料、互動事件，以及用於個人化的其他資訊。 [了解更多](../data/get-started-datasets.md) |
| **頻道設定** | 定義在特定通道傳遞訊息的方式的設定，包括寄件者詳細資訊、子網域、IP集區和訊息型別（行銷或異動）。 在舊版檔案中，以前稱為「表面」或「預設集」。 [了解更多](../configuration/channel-surfaces.md) |
| **禁止名單** | 由於硬退信、垃圾郵件投訴或手動新增，電子郵件地址和網域自動排除在郵件傳送之外的清單。 封鎖傳送至隱藏位址的作業，以保護傳遞能力及寄件者信譽。 [了解更多](../reports/suppression-list.md) |

## 衝突與優先順序術語 {#conflict-terms}

| 術語 | 定義 |
|------|------------|
| **規則集** | 套用至歷程和行銷活動的已命名商業規則群組，以控管訊息行為。 規則集可以將頻率限定、歷程進入限制和無訊息時間結合為單一可重複使用的原則。 [了解更多](../conflict-prioritization/rule-sets.md) |
| **頻率限定** | 規則集中的規則，可限制設定檔在指定時段內，針對每個頻道或通訊型別（銷售、促銷等）可接收多少訊息。 超出上限的設定檔會自動從傳送中排除。 [了解更多](../conflict-prioritization/channel-capping.md) |

>[!NOTE]
>
>如需Adobe Experience Platform術語的完整辭彙表，請參閱[Adobe Experience Platform辭彙表](https://experienceleague.adobe.com/docs/experience-platform/landing/glossary.html){target="_blank"}。

## 辭彙相似時：消除歧義指南 {#disambiguation}

Adobe Journey Optimizer經過數年成長發展，這表示有些功能區域有類似的名稱。 使用下表快速找出適合您需求的功能。

### 決策vs決策管理 {#decisioning-vs-dm}

這兩種功能都會選取並傳送優惠方案，但它們在產品生命週期的不同階段中運作。

| | 決策 | 決策管理 |
|---|---|---|
| **狀態** | 最新 — 建議用於所有新實作 | **舊版** — 仍受支援，但不再建議用於新實作 |
| **已匯入** | 2024 | 2021 |
| **專案目錄** | 以結構為基礎、靈活的中繼資料 | 集中式優惠資料庫 |
| **支援的管道** | 程式碼型體驗、推播、簡訊、電子郵件（可用性限制） | 電子郵件、應用程式內、推播、簡訊、直接郵件 |
| **金鑰區分符號** | 可重複使用的決策元件、實驗、更廣泛的管道藍圖 | 經驗證的限制引擎；移轉至新專案的決策 |
| **開始使用** | [決策](../experience-decisioning/gs-experience-decisioning.md) | [決定管理](../offers/get-started/starting-offer-decisioning.md) |

如果您目前正在使用決定管理且想要切換，請參閱[移轉指南](../experience-decisioning/migrate-to-decisioning.md)。

### 行銷活動類型 {#campaign-types-disambiguation}

Journey Optimizer提供三種以不同方式啟動的行銷活動型別，並處理不同的使用案例。

| | 動作行銷活動（排程的行銷活動） | API 觸發的行銷活動 | 協調的行銷活動 |
|---|---|---|---|
| **啟用** | 手動或排程 | 外部API呼叫 | 視覺工作流程畫布 |
| **最適合** | 一次性或重複批次傳送（電子報、促銷活動） | 即時事件導向訊息（訂單確認、密碼重設） | 複雜的多步驟跨頻道計畫 |
| **Personalization來源** | 輪廓屬性 | 設定檔屬性+ API裝載內容 | 設定檔屬性+關聯資料 |
| **開始使用** | [動作行銷活動](../campaigns/create-campaign.md) | [API觸發的行銷活動](../campaigns/api-triggered-campaigns.md) | [協調的行銷活動](../orchestrated/gs-orchestrated-campaigns.md) |

如需所有行銷活動型別的完整概觀，以及何時使用各型別，請參閱[開始使用行銷活動](../campaigns/get-started-with-campaigns.md)。

### 頻率限定與歷程仲裁 {#capping-vs-arbitration}

兩者都是衝突和優先順序工具集下的規則集機制，但它們可解決不同的問題。

| | 頻率上限 | 歷程仲裁 |
|---|---|---|
| **它解決的問題** | 設定檔會隨著時間接收太多訊息 | 設定檔同時符合多個歷程的資格 |
| **領域** | 每個管道和通訊型別（銷售、促銷等） | 歷程註冊 — 同時歷程的數量，或哪個歷程獲勝 |
| **機制** | 限制每個期間的訊息數；自動排除過度請求的設定檔 | 使用優先順序分數和上限規則來決定設定檔進入哪個歷程 |
| **設定於** | 規則集→頻率限定 | 歷程上限與仲裁→規則集 |
| **了解更多** | [依據頻道設定頻率上限](../conflict-prioritization/channel-capping.md) | [管理歷程上限與仲裁](../conflict-prioritization/journey-capping.md) |

### 內容卡片與應用程式內訊息 {#content-cards-vs-in-app}

這兩個管道都會在行動或網頁應用程式內傳送訊息，但它們有不同的轉譯模型和持續性行為。

| | 內容卡片 | 應用程式內訊息 |
|---|---|---|
| **顯示模型** | 內嵌於應用程式UI （摘要、收件匣或自訂表面）中的永續性卡片 | 應用程式上方顯示的暫時性覆蓋圖、橫幅或模式 |
| **持續性** | 在明確解除或過期之前保持可見 | 使用者互動或關閉後消失 |
| **觸發器** | SDK載入時轉譯；規則控制顯示和移除 | 歷程中的即時事件或行銷活動會觸發傳送 |
| **最適合** | 持續性促銷活動、忠誠度狀態、持續性警示 | 入門秘訣、限時優惠、暫時性通知 |
| **開始使用** | [內容卡](../content-card/create-content-card.md) | [應用程式內訊息](../in-app/get-started-in-app.md) |

>[!NOTE]
>
>**Adobe Journey Optimizer與Journey Optimizer B2B edition：**&#x200B;它們是相同品牌系列中兩個不同的產品。 Adobe Journey Optimizer （本檔案）目標為B2C客戶歷程。 Journey Optimizer B2B edition是專為帳戶式行銷而建置，可搭配購買群組和帳戶對象。 若您正在尋找B2B edition檔案，請瀏覽[Journey Optimizer B2B edition指南](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-b2b/user/guide-overview){target="_blank"}。

## 相關主題 {#related-topics}

* [瞭解Journey Optimizer的運作方式](understanding-ajo.md) — 瞭解歷程、行銷活動、設定檔和管道如何在產品架構中搭配使用。
* [開始使用決策功能](../experience-decisioning/gs-decision.md) — 並排比較決策與決策管理，並選擇適合您實作的方法。
* [開始使用歷程](../building-journeys/journey.md) — 瞭解如何逐步建置事件觸發的循序客戶體驗。
* [開始使用行銷活動](../campaigns/get-started-with-campaigns.md) — 瞭解三種行銷活動型別（動作、API觸發、協調）以及何時使用各型別。
* [衝突管理與優先順序](../conflict-prioritization/gs-conflict-prioritization.md) — 瞭解如何使用規則集、頻率限定、優先順序分數和無訊息時數，以避免過度傳訊。
* [開始使用通訊頻道](../channels/gs-channels.md) — 瀏覽所有可用的頻道、其先決條件以及如何設定它們。
