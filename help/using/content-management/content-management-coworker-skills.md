---
solution: Journey Optimizer
product: journey optimizer
title: 內容管理的同事
description: 探索可用於探索、建立和管理CX Enterprise Coworker內容資產的Journey Optimizer內容管理工具，其中包含深入指引和範例提示。
feature: Overview
topic: Artificial Intelligence
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 9f23a6f5-7221-4f87-95cd-047955ca33d5
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
subfeature_v2:
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
    internal-label: Templates
source-git-commit: 85784fbe98b5347f86899ce7811017cd368745ff
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 2%
---

# 內容管理的同事 {#content-management-coworker-skills}

>[!BEGINSHADEBOX]

**在此頁面上：**&#x200B;探索Adobe Journey Optimizer中可用的CX Enterprise Coworker內容管理工具 — 以瀏覽、建立、更新、複製和發佈內容範本、片段、登陸頁面，以及歷程/行銷活動內嵌內容 — 提供詳細指引、範例提示和最佳實務。

了解更多：

* [Journey Optimizer的同事技能](../start/ai-features.md#cx-coworker-skills) — Journey Optimizer中跨歷程、忠誠度和內容管理之同事技能的概觀。
* [同事檔案](https://experienceleague.adobe.com/zh-hant/docs/cx-enterprise-ai/experience-cloud-ai/coworker/overview){target="_blank"} — 同事的行銷活動、聊天和專案功能概觀。
* [同事聊天UI指南](https://experienceleague.adobe.com/en/docs/cx-enterprise-ai/experience-cloud-ai/coworker/chat/ui-guide){target="_blank"} — 如何存取和瀏覽同事聊天。

>[!ENDSHADEBOX]

## 內容管理工具 {#content-management}

>[!AVAILABILITY]
>
>所有有權存取Co-worker的客戶皆可使用內容管理。

Journey Optimizer使用者可以使用自然語言提示，直接從同事探索和管理內容資產，包括內容範本、片段、登陸頁面，以及歷程/行銷活動內嵌訊息內容。 它可讓您從「告訴我我的內容」到「建立、更新和發佈」，而不需離開交談。 這項功能由15種可讀取和寫入的MCP工具提供支援，適用於Journey Optimizer內容。

### 主要使用案例

1. **瀏覽並檢查內容**

   * 列出可用的內容範本、片段或登入頁面，並擷取其結構、中繼資料和狀態。
   * 擷取在歷程或行銷活動動作節點上設定的內嵌訊息內容。

   範例提示：
   * 「列出我的電子郵件內容範本。」
   * 「顯示可用於夏季行銷活動的片段。」
   * 「取得登陸頁面123的詳細資料。」
   * 「促銷活動camp-789中動作節點的電子郵件變體設定了哪些內容？」

1. **建立內容範本**

   * 為任何管道建立新的內容範本。

   範例提示：
   * 「使用此HTML內容建立名為Summer Sale的電子郵件範本。」
   * 「建立新的SMS範本，稱為Flash Alert。」

1. **更新內容範本**

   * 完全取代現有範本的內容。

   範例提示：
   * 「使用這個新HTML內文更新範本abc-123。」

1. **建立、更新、複製和發佈片段**

   * 建立新的HTML或運算式片段。
   * 更新現有片段的內容或中繼資料。
   * 以新名稱原地複製現有片段。
   * 提交草稿片段以供發佈。

   範例提示：
   * 「使用此標籤建立名為「促銷橫幅」的HTML片段。」
   * 「更新片段frag-456以將其名稱變更為促銷橫幅V2。」
   * 「以Promo Banner - Summer （變體B）形式復製片段abc-123。」
   * 「發佈片段frag-456。」

1. **更新內嵌訊息內容**

   * 取代行銷活動或歷程動作節點內嵌訊息上的一個管道變體。
   * 列出歷程或行銷活動動作節點上定義的管道變體。

   範例提示：
   * &quot;使用此新內容更新行銷活動camp-789中動作節點的電子郵件變體。&quot;
   * 「在此動作節點上定義了哪些管道變體？」

### 在範圍中

內容管理支援下列功能：

* **列出並取得內容範本**：瀏覽內容範本並擷取其結構和中繼資料。
* **列出並取得片段**：瀏覽內容與運算式片段，並擷取其詳細資料。
* **列出並取得登入頁面**：瀏覽登入頁面，並擷取其中繼資料和頁面內容。
* **取得行銷活動/歷程內嵌內容**：擷取行銷活動或歷程動作節點上設定的內嵌訊息內容，包括多語言變體。
* **建立內容範本**：為任何頻道建立新範本。
* **更新內容範本**：完全取代現有範本的內容。
* **建立、更新、複製和發佈片段**：建立新片段、更新現有片段、以新名稱復製片段，並提交草稿片段以供發佈。
* **更新內嵌訊息內容**：取代行銷活動/歷程動作節點內嵌訊息上的頻道變體（包括多語言變體），並列出動作節點上定義的頻道變體。

### 超出範圍

目前不支援以下功能：

* **跨範本或片段的全文檢索搜尋**
* **範本或片段驗證** （孤立的參考、中斷的連結、已棄用的元件）
* **建立或發佈登入頁面**
* **正在刪除內容範本、片段或登入頁面**

### 提示最佳實務

1. **已知時的參考ID**：要求取得、更新、複製或發佈特定資產時，請提供範本、片段、登陸頁面或行銷活動/歷程ID。
1. **明確關於頻道**：建立範本或片段時，請指定頻道或內容型別（電子郵件、HTML片段、運算式片段）。
1. **發佈前確認**：在建立或更新片段內容後，要求同事發佈之前，請先檢閱片段的內容。
1. **提供完整的取代內容**：更新作業會完整取代內容，因此在您的提示中包含完整的HTML內文或變體內容。

{{$include /help/_includes/do-not-localize/start/ai-augmented-content-management-coworker-skills.md}}
