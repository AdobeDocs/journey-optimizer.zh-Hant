---
solution: Journey Optimizer
product: journey optimizer
title: 入門專案指南 |Adobe Journey Optimizer
description: 跨管理員、資料、開發人員和行銷人員角色規劃及管理Adobe Journey Optimizer入門專案。
feature: Get Started
topic: Content Management
role: Admin
level: Intermediate
keywords: journey optimizer，入門，入門專案，推出，實作計畫，管理員， csm，實作合作夥伴，分階段檢查清單
source-git-commit: 6a653e1dbb00f68ff689ea3e0dc0b15abda1e21e
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 4%

---

# 入門專案指南 {#onboarding-hub}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;透過跨越管理員、資料工程師、開發人員和行銷人員角色的分階段檢查清單，規劃並協調完整的Adobe Journey Optimizer轉出。

>[!ENDSHADEBOX]

此頁面適用於&#x200B;**系統管理員與實作合作夥伴**，負責協調完整的Journey Optimizer轉出。 它提供涵蓋所有角色的分階段檢查清單，並包含詳細角色特定指南的連結。

>[!NOTE]
>
>如果您是個人開始使用特定角色，請改為移至[開始使用Journey Optimizer](../../rp_landing_pages/get-started-landing-page.md)。

## 階段1 — 環境設定（管理員） {#phase-1}

請先完成這些基本工作，讓其他角色可以開始工作：

* [ ]布建沙箱（開發、測試、生產）
* [ ]在Adobe Admin Console中設定使用者角色和許可權
* [ ]設定產品設定檔和物件層級存取控制
* [ ]委派子網域並設定IP集區
* [ ]設定頻道設定（電子郵件、簡訊、推播、網頁、應用程式內、直接郵件）
* [ ]設定隱藏清單和同意原則

➡️檢視完整詳細資料： [管理員快速入門](path/administrator.md)

## 第2階段 — 資料基礎（資料工程師） {#phase-2}

建立可支援設定檔、對象和歷程觸發器的資料層：

* [ ]定義身分名稱空間
* [ ]建立XDM結構描述（設定檔、體驗事件、關聯式）
* [ ]設定並啟用即時客戶個人檔案的資料集
* [ ]設定資料擷取（批次和串流）
* [ ]建立計算屬性
* [ ]設定歷程事件和資料來源

➡️檢視完整詳細資料： [資料工程師快速入門](path/data-engineer.md)

## 階段3 — 技術整合（開發人員） {#phase-3}

連線您的應用程式，讓歷程可在即時資料上執行：

* [ ]整合Mobile SDK (iOS/Android)與推播設定
* [ ]實作適用於Web體驗和Web推播的Web SDK
* [ ]實作從應用程式傳送的事件
* [ ]外部系統整合的建置自訂動作端點
* [ 使用Adobe Experience Platform Assurance進行]驗證

➡️檢視完整詳細資料： [開發人員快速入門](path/developer.md)

## 第4階段 — 首次體驗（行銷人員） {#phase-4}

啟動您的第一個歷程和行銷活動，奠定良好的基礎：

* [ ]建置第一個對象（區段定義或CSV上傳）
* [ ]使用電子郵件動作建立測試歷程
* [ ]設定內容範本和片段
* [ ]發佈及監視行銷活動
* [ ]檢閱即時報告

➡️檢視完整詳細資料： [行銷人員快速入門](path/marketer.md)

## 入門檢查清單（可列印） {#checklist}

| 階段 | 所有者 | 狀態 |
|-------|-------|--------|
| 環境設定 | 管理員 | |
| 資料基礎 | 資料工程師 | |
| 技術整合 | Developer | |
| 第一個體驗 | 行銷人員 | |

## 相關資源 {#related-resources}

* [角色和責任](quick-start.md) — 這四個角色如何共同運作以及建議的實作順序。
* [Journey Optimizer教學課程](https://experienceleague.adobe.com/zh-hant/docs/journey-optimizer-learn/tutorials/overview){target="_blank"} — 每個角色的逐步影片和引導式逐步說明。
* [開始使用資料管理](../data/gs-data.md) — 如何擷取、統一及啟用資料。
