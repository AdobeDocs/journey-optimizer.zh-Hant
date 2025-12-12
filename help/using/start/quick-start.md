---
solution: Journey Optimizer
product: journey optimizer
title: 角色與職責
description: 了解 Adobe Journey Optimizer 中涉及的不同角色及其職責
feature: Get Started
role: Admin, Developer, User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
redpen-status: PASS_||_2025-04-28_15-13-07
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1177'
ht-degree: 20%

---


# 角色與職責

Adobe Journey Optimizer可讓品牌在整個客戶生命週期中提供連線且情境化的客戶歷程。 它可讓團隊大規模個人化互動，並使客戶期望與業務目標一致。本文件說明有效使用 Journey Optimizer 的主要角色、其職責以及如何開始使用。

**重要注意事項：** Adobe Journey Optimizer 定義具有特定職責的不同角色。視您的組織結構而定，個人可以執行多個角色或所有角色。

## 角色型快速入門手冊

為簡化實作，Adobe Journey Optimizer會根據專業知識將工作整理成特定角色。 每個角色都專注於提供順暢客戶體驗所需的基本工作。

| 角色 | 主要職責 | 關鍵技能 | 典型工作 |
|-------------------|----------------------------------|--------------------------------|-----------------------------------------------|
| **管理員** | 環境設定和存取管理 | 系統設定、使用者管理、安全性 | 設定沙箱、管理許可權、設定頻道設定 |
| **資料工程師** | 資料基礎與架構 | 資料模式， XDM結構描述，資料品質 | 建立方案和資料集、設定資料擷取、管理資料生命週期 |
| **Developer** | 技術實作與整合 | 行動/網頁SDK、API、事件導向架構 | 整合SDK、實作事件、建立自訂動作端點 |
| **行銷人員** | 客戶體驗設計與執行 | 歷程設計、內容建立、資料分析 | 建立歷程、建立個人化內容、最佳化行銷活動 |

每個角色都會處理Adobe Journey Optimizer實施的特定階段，並確保結構化且有效的部署流程。

## 實作順序和角色相依性

成功的 Journey Optimizer 實施通常會依照此順序進行，這會反映角色之間的相依性：

1. **管理員**：設定環境\
   管理員可設定沙箱、設定存取控制項及準備通道設定，奠定基礎作業。 必須先執行此動作，才能讓其他團隊正常運作。
   * 設定開發、測試和生產沙箱
   * 設定角色、許可權和物件層級存取控制(OLAC)
   * 設定頻道設定（電子郵件、簡訊、推播、應用程式內、網頁、內容卡）
   * 委派子網域並設定IP集區
   * 設定隱藏清單和同意原則

2. **資料工程師**：建立資料基礎\
   資料工程師會建置支援個人化的資料基礎架構，定義客戶資料如何傳入及流經系統。
   * 建立用於客戶識別的身分名稱空間
   * 設計XDM結構描述（設定檔、體驗事件、關聯式）
   * 設定資料集並為即時客戶個人檔案啟用它們
   * 設定資料擷取（批次和串流）
   * 建立複雜計算的計算屬性
   * 設定歷程的事件和資料來源

3. **開發人員**：實作技術整合\
   開發人員透過整合SDK、傳送事件及建立API端點，將應用程式連結至Journey Optimizer。 這些實施可讓歷程觸發和執行。
   * 整合Mobile SDK (iOS/Android)與推播通知設定
   * 為網站體驗實作Web SDK
   * 從應用程式傳送事件以觸發歷程
   * 建立外部系統整合的自訂動作端點
   * 使用Adobe Experience Platform Assurance測試實作

4. **行銷人員**：設計和執行客戶體驗\
   行銷人員運用所有基礎工作來建立歷程、建立內容，並跨所有管道最佳化客戶體驗。
   * 使用細分、CSV上傳或對象構成建立對象
   * 使用AI助理和範本設計個人化內容
   * 使用事件和受眾觸發程式建立多管道歷程
   * 啟動前使用核准工作流程進行測試
   * 根據報告深入分析監控效能並最佳化

**注意：**&#x200B;雖然此順序是典型的，但某些活動可以並行發生。例如，開發人員可在資料工程師設定結構時進行應用程式整合。

## 角色快速入門

每個角色都從根據其重點量身打造的特定任務開始。完成這些初始步驟可使引導更順利完成，確保與整體實施流程保持一致：

### 行銷人員適用的 {#for-marketers}

著重於跨所有管道建立個人化客戶體驗。

**您將使用的關鍵功能：**

* 使用多種方法（區段定義、CSV上傳、對象構成）建立對象和建立區段
* 使用AI Assistant設計內容以產生文字和影像
* 使用拖放設計工具建立多管道客戶歷程
* 運用傳送時間最佳化和衝突管理，以最大化參與程度
* 發佈前測試內容並使用核准工作流程
* 使用整合式報告儀表板監控效能

**開始於：**&#x200B;使用預先建立的範本，建立簡單的歡迎歷程或放棄的購物車復原行銷活動。

[行銷人員快速入→](path/marketer.md)

### 資料工程師專用 {#for-data-engineers}

建立可支援個人化體驗的資料基礎。

**主要職責：**

* 建立身分名稱空間並設定身分解析
* 為設定檔和事件資料（標準和關聯式）設計XDM結構描述
* 設定資料集並為即時客戶個人檔案啟用它們
* 設定批次和串流資料擷取的來源聯結器
* 建立計算屬性以簡化分段
* 設定歷程執行的事件和資料來源
* 管理資料品質、控管和生命週期

**開始於：**&#x200B;設定識別名稱空間，並使用必要的欄位群組建立您的第一個設定檔結構描述。

[資料工程師快速入→](path/data-engineer.md)

### 適用於管理員 {#for-administrators}

為貴組織設定和管理Journey Optimizer環境。

**主要職責：**

* 建立並管理用於開發、測試和生產的沙箱
* 使用現成可用或自訂角色設定角色和許可權
* 套用物件層級存取控制(OLAC)來保護資源
* 設定電子郵件、簡訊、推播、應用程式內、網頁和內容卡的頻道設定
* 委派子網域並建立電子郵件傳遞能力的IP集區
* 管理隱藏清單和允許清單
* 設定同意原則和資料控管（使用Healthcare/Privacy Shield）

**開始於：**&#x200B;設定沙箱、設定基本角色和許可權，然後與您的團隊合作進行頻道設定。

[管理員快速入→](path/administrator.md)

### 適用於開發人員 {#for-developers}

實作技術整合以將Journey Optimizer連線至您的應用程式。

**主要職責：**

* 整合Adobe Experience Platform Mobile SDK (iOS/Android)
* 實施適用於Web體驗和Web推播通知的Web SDK
* 設定推播通知憑證和憑證
* 從應用程式傳送事件以觸發歷程
* 建立Journey Optimizer透過自訂動作呼叫的API端點
* 針對Web、行動和其他介面實作程式碼型體驗
* 使用Adobe Experience Platform Assurance測試實作並除錯
* 使用Journey Optimizer API以程式設計方式存取

**開始於：**&#x200B;整合行動裝置或網頁SDK，然後實作您的第一個事件以觸發歷程。

[開發人員入門→](path/developer.md)

## 跨角色Collaboration

成功的Journey Optimizer實作需要跨所有角色共同作業：

* **管理員**&#x200B;可設定沙箱、許可權和通道設定，以啟用其他角色
* **資料工程師**&#x200B;提供開發人員和行銷人員賴以建立的資料基礎
* **開發人員**&#x200B;實作行銷人員用來觸發歷程的技術整合
* **行銷人員**&#x200B;針對資料品質、功能要求和使用者體驗，向所有團隊提供意見回饋

**最佳實務：**&#x200B;定期舉行跨職能會議，以調整優先順序、共用進度並處理跨團隊的封鎖程式。

## 作法影片 {#video}

若要進一步了解 Journey Optimizer 的主要功能和人物誌，請觀看簡介影片。影片會逐步介紹使用者介面，並根據角色專屬工作流程重點說明主要功能。

>[!VIDEO](https://video.tv.adobe.com/v/3424995?quality=12)

## 其他資源

如需更深入的學習和更新，請探索下列資源：

**學習與檔案：**

* [教學課程影片](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=zh-Hant){target="_blank"} — 所有角色的逐步教學課程影片
* [歷程使用案例庫](../building-journeys/jo-use-cases.md) — 實際範例和實施模式
* [AI與智慧型功能](ai-features.md) — 瞭解AI小幫手、傳送時間最佳化及內容產生
* [使用者介面指南](user-interface.md) — 有效瀏覽Journey Optimizer

**持續更新：**

* [發行說明](../rn/release-notes.md) — 最新功能、改良與修正
* [檔案更新](../rn/documentation-updates.md) — 追蹤近期檔案變更
* **產品通知** — 在您的[Adobe Experience Cloud設定檔](https://experience.adobe.com/preferences){target="_blank"}中啟用警示，以接收有關新版本、維護時段和重要公告的通知。 按一下您的設定檔圖示>偏好設定>通知以進行設定。

**社群與支援：**

* [Experience League社群](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} — 與其他使用者和專家交流
* [產品論壇](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"} — 詢問問題並分享知識
